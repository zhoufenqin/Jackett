# Configuration & Externalized Settings Inventory

Jackett uses two configuration layers: a runtime `appsettings.json` written to the OS-specific application data folder (not in source control), and command-line arguments parsed at startup. There are no Spring-style profile files, no cloud config servers, and no secret manager integrations.

## Configuration Sources

| Source | Type | Path/Location | Notes |
|---|---|---|---|
| Command-line arguments | CLI flags | N/A (parsed at startup) | Primary runtime configuration source; parsed via `CommandLineParser` into `ConsoleOptions` → `RuntimeSettings` |
| appsettings.json | JSON file | `{AppDataFolder}/appsettings.json` | Optional; generated at runtime in OS-specific data folder; not committed to source control |
| ServerConfig.json | JSON file | `{AppDataFolder}/ServerConfig.json` | Persistent server configuration (port, auth, proxy, cache settings); created on first run |
| Indexer config files | JSON files | `{AppDataFolder}/Indexers/{indexerId}.json` | Per-indexer configuration; passwords/cookies encrypted via IProtectionService |
| In-memory config (RuntimeSettings) | IConfiguration | Process memory | Built from CLI args; injected into IConfiguration as in-memory collection |
| Directory.Build.props | MSBuild props | `src/Directory.Build.props` | Build-time: version (`0.0.0`), PathMap for debugging, common project properties |
| NLog config | XML/code | Embedded in Program.cs via NLog.Web.AspNetCore | Logging configuration; can be overridden by custom log file name via `--LogFileName` |

## Build Profiles

| Profile | Activation | Purpose | Key Properties |
|---|---|---|---|
| Debug | `dotnet build` default | Development build; full debug symbols | `<Optimize>false</Optimize>`, debug symbols included |
| Release | `dotnet build -c Release` | Production packaging; optimized | `<Optimize>true</Optimize>`, no debug symbols |
| net9.0 | Target framework moniker | Primary modern .NET target | Full ASP.NET Core SDK; Microsoft.AspNetCore.Mvc.NewtonsoftJson 9.0.16 |
| net471 | Target framework moniker | Legacy .NET Framework 4.7.1 target | References Microsoft.AspNetCore 2.3.x, Microsoft.NETFramework.ReferenceAssemblies |
| net9.0-windows | Target framework moniker | Windows-specific services | Jackett.Service and Jackett.Tray targets; Windows Service APIs available |

> Version is set to `0.0.0` by default in `Directory.Build.props` and overridden at release build time via CI/CD (azure-pipelines.yml).

## Runtime Profiles

| Profile | Activation Method | Config Files | Key Overrides |
|---|---|---|---|
| Default (all environments) | Automatic | `{AppDataFolder}/ServerConfig.json`, `{AppDataFolder}/appsettings.json` (optional) | Port (default 9117), bind address (default 127.0.0.1), auth, proxy |
| Public-listen mode | `--ListenPublic` CLI flag | Same as default | Overrides `AllowExternal=true`, binds to `0.0.0.0` |
| Private-listen mode | `--ListenPrivate` CLI flag | Same as default | Overrides `AllowExternal=false`, binds to `127.0.0.1` |
| Custom data folder | `--DataFolder <path>` CLI flag | Reads from specified path | Overrides all config file locations |
| Tracing mode | `--Tracing` CLI flag | Same as default | Enables verbose tracing via `RuntimeSettings.TracingEnabled` |
| No-update mode | `--NoUpdates` CLI flag | Same as default | Disables automatic update checks |

> There are no `ASPNETCORE_ENVIRONMENT`-specific `appsettings.{Environment}.json` files in the source tree.

## Properties Inventory

### ServerConfig (persisted in `{AppDataFolder}/ServerConfig.json`)

| Property Key | Default Value | Type | Source |
|---|---|---|---|
| Port | 9117 | int | ServerConfig.json / `--Port` CLI |
| LocalBindAddress | "127.0.0.1" | string | ServerConfig.json / `--ListenPublic`/`--ListenPrivate` CLI |
| AllowExternal | true (Unix), false (Windows) | bool | ServerConfig.json |
| AllowCORS | false | bool | ServerConfig.json |
| APIKey | auto-generated GUID | string | ServerConfig.json |
| AdminPassword | "" (no password) | string (hashed) | ServerConfig.json |
| InstanceId | auto-generated GUID | string | ServerConfig.json |
| BlackholeDir | "" | string | ServerConfig.json |
| UpdateDisabled | false | bool | ServerConfig.json |
| UpdatePrerelease | false | bool | ServerConfig.json |
| BasePathOverride | "" | string | ServerConfig.json |
| BaseUrlOverride | "" | string | ServerConfig.json |
| CacheEnabled | true | bool | ServerConfig.json |
| CacheTtl | 2100 (seconds) | long | ServerConfig.json |
| CacheMaxResultsPerIndexer | 1000 | long | ServerConfig.json |
| FlareSolverrUrl | "" | string | ServerConfig.json |
| FlareSolverrMaxTimeout | 55000 (ms) | int | ServerConfig.json |
| OmdbApiKey | "" | string | ServerConfig.json |
| OmdbApiUrl | "https://www.omdbapi.com" | string | ServerConfig.json |
| ProxyType | 0 (None) | ProxyType enum | ServerConfig.json |
| ProxyUrl | "" | string | ServerConfig.json |
| ProxyPort | null | int? | ServerConfig.json |
| ProxyUsername | "" | string | ServerConfig.json |
| ProxyPassword | "" | string | ServerConfig.json |

### RuntimeSettings (from command-line arguments, never persisted)

| CLI Option | RuntimeSettings Property | Default | Description |
|---|---|---|---|
| `--Port <n>` | Port override | From ServerConfig | Overrides listen port |
| `--ListenPublic` | AllowExternal=true | Platform default | Bind to all interfaces |
| `--ListenPrivate` | AllowExternal=false | Platform default | Bind to localhost only |
| `--DataFolder <path>` | CustomDataFolder | Platform-specific AppData | Override config storage location |
| `--Client <name>` | ClientOverride | Default HttpWebClient | Override HTTP client implementation |
| `--IgnoreSslErrors` | IgnoreSslErrors=true | false | Disable SSL certificate validation |
| `--Tracing` | TracingEnabled=true | false | Enable verbose tracing |
| `--Logging` | N/A | false | Enable request logging |
| `--NoRestart` | NoRestart=true | false | Prevent restart after update |
| `--NoUpdates` | NoUpdates=true | false | Disable update checks |
| `--PIDFile <path>` | PIDFile | null | Write PID to specified file |
| `--LogFileName <name>` | CustomLogFileName | null | Override log file name |
| `--BasePath <path>` | BasePath | "" | URL base path prefix |
| `--Install` | N/A | N/A | Install Windows Service |
| `--Uninstall` | N/A | N/A | Uninstall Windows Service |
| `--Start` | N/A | N/A | Start Windows Service |
| `--Stop` | N/A | N/A | Stop Windows Service |
| `--ReserveUrls` | N/A | N/A | Reserve HTTP URLs (Windows) |

### Default AppData Folder Locations

| Platform | Default Path |
|---|---|
| Unix/macOS | `~/.config/Jackett` (ApplicationData) |
| Windows | `C:\ProgramData\Jackett` (CommonApplicationData) |
| Custom | `{--DataFolder value}` |

## Startup Parameters & Resource Requirements

| Service | Runtime | CLI Options | Memory | Notes |
|---|---|---|---|---|
| Jackett.Server | .NET 9 / net471 | See RuntimeSettings table above | Not specified | Self-contained; no fixed heap settings |
| Jackett.Service | .NET 9 (Windows) | Inherits Jackett.Server args | Not specified | Windows Service wrapper |
| Jackett.Tray | .NET 9 (Windows) | `--Port`, `--DataFolder` | Not specified | WinForms tray UI |
| Jackett.Updater | .NET 9 / net471 | Update-specific args | Not specified | Short-lived; spawned by Jackett.Server |

> No Docker images, Kubernetes manifests, or container memory/CPU limits are defined in this repository. No JVM-style heap settings apply (managed .NET runtime handles memory automatically).

## Startup Dependency Chain

Jackett is a **single-process application** with no inter-service startup dependencies. All components start within the same process:

1. **Program.cs** — Parses CLI args, creates RuntimeSettings
2. **ConfigurationService** — Initializes AppData folder, migrates legacy configs
3. **JackettModule (Autofac)** — Registers all services (singleton pattern)
4. **IndexerManagerService** — Loads YAML definitions and instantiates indexer instances
5. **Kestrel/ASP.NET Core** — Binds to configured port and begins accepting requests

> No `dockerize` wait-for-TCP, Kubernetes readiness probes, or inter-service health checks are required. The `/health` endpoint becomes available once Kestrel starts (step 5).

## Secrets & Sensitive Configuration

| Secret Reference | Type | Storage |
|---|---|---|
| ServerConfig.APIKey | Random GUID API key | `{AppDataFolder}/ServerConfig.json` — **plaintext** |
| ServerConfig.AdminPassword | Admin password | `{AppDataFolder}/ServerConfig.json` — bcrypt hash |
| ServerConfig.ProxyUsername | Proxy credential | `{AppDataFolder}/ServerConfig.json` — **plaintext** |
| ServerConfig.ProxyPassword | Proxy credential | `{AppDataFolder}/ServerConfig.json` — **plaintext** |
| ServerConfig.OmdbApiKey | OMDB API key | `{AppDataFolder}/ServerConfig.json` — **plaintext** |
| IndexerConfig.CookieHeader | Session cookies per tracker | `{AppDataFolder}/Indexers/{id}.json` — encrypted (DPAPI) |
| IndexerConfig.Password | Tracker login password | `{AppDataFolder}/Indexers/{id}.json` — encrypted (DPAPI) |
| IndexerConfig.ApiKey | Tracker API key | `{AppDataFolder}/Indexers/{id}.json` — encrypted (DPAPI) |
| sonarr_api.json | Sonarr API key | `{AppDataFolder}/sonarr_api.json` — **plaintext** |
| DataProtection keys | ASP.NET Core data protection | `{AppDataFolder}/DataProtection/` — filesystem keys |

### Secrets Provisioning Workflow

Jackett does not integrate with any external secret manager (no HashiCorp Vault, Azure Key Vault, AWS Secrets Manager, or Kubernetes Secrets). All secrets are managed locally on the host filesystem:

1. **First run**: `ConfigurationService.BuildServerConfig()` generates a random `APIKey` (GUID) and `InstanceId` and writes them to `ServerConfig.json`.
2. **Admin password**: Set by the user via the web UI (`POST /api/v2.0/server/AdminPassword`); stored as a bcrypt hash.
3. **Indexer credentials**: Entered by the user through the web UI; encrypted using `IProtectionService` (DPAPI on Windows, custom AES on Linux/macOS) before writing to the indexer's JSON config file.
4. **Proxy credentials and OMDB key**: Entered via web UI; stored in **plaintext** in `ServerConfig.json`.
5. **No rotation mechanism** exists — secrets are static until manually changed through the UI.

**Risk**: The `ServerConfig.json` file contains plaintext proxy credentials and API keys. Filesystem read access to the AppData folder is sufficient to expose these values. No secrets rotation, audit logging, or access controls are applied beyond OS-level filesystem permissions.

## Feature Flags

| Flag / Setting | Default | Controlled By | Notes |
|---|---|---|---|
| CacheEnabled | true | `ServerConfig.CacheEnabled` (UI toggle) | Enables/disables in-memory search result cache |
| AllowCORS | false | `ServerConfig.AllowCORS` (UI toggle) | Enables/disables CORS `AllowAnyOrigin` policy |
| UpdateDisabled | false | `ServerConfig.UpdateDisabled` or `--NoUpdates` CLI | Disables GitHub update checks |
| UpdatePrerelease | false | `ServerConfig.UpdatePrerelease` (UI toggle) | Opt-in to pre-release versions |
| AllowExternal | platform default | `--ListenPublic`/`--ListenPrivate` CLI or UI | Bind to all interfaces vs localhost only |
| TracingEnabled | false | `--Tracing` CLI | Verbose tracing output |
| IgnoreSslErrors | false | `--IgnoreSslErrors` CLI | Disable SSL certificate validation for outbound requests |
| NoRestart | false | `--NoRestart` CLI | Prevent server restart after updates |

> No feature flag framework (LaunchDarkly, Unleash, .NET FeatureManagement) is used. All flags are simple boolean fields in `ServerConfig` or `RuntimeSettings`.

## Framework & Runtime Versions

| Component | Version | Source |
|---|---|---|
| .NET SDK | 10.0.300 (installed) | `dotnet --version` |
| Target framework (primary) | net9.0 | `Jackett.Server.csproj`, `Jackett.Common.csproj` |
| Target framework (legacy) | net471 (.NET Framework 4.7.1) | `Jackett.Server.csproj`, `Jackett.Common.csproj` (conditional) |
| Target framework (Windows services) | net9.0-windows | `Jackett.Service.csproj`, `Jackett.Tray.csproj` |
| ASP.NET Core | 9.0.16 (net9.0) / 2.3.10 (net471) | `Jackett.Server.csproj` |
| Autofac | 8.0.0 | `Jackett.Common.csproj`, `Jackett.Server.csproj` |
| Autofac.Extensions.DependencyInjection | 9.0.0 | `Jackett.Server.csproj` |
| NLog | 5.5.1 | `Jackett.Common.csproj` |
| NLog.Web.AspNetCore | 5.5.0 | `Jackett.Server.csproj` |
| Newtonsoft.Json | 13.0.4 | `Jackett.Common.csproj` |
| YamlDotNet | 16.3.0 | `Jackett.Common.csproj` |
| AngleSharp | 1.4.0 | `Jackett.Common.csproj` |
| Polly | 8.6.6 | `Jackett.Common.csproj` |
| CommandLineParser | 2.9.1 | `Jackett.Common.csproj`, `Jackett.Server.csproj` |
| FlareSolverrSharp | 3.0.7 | `Jackett.Common.csproj` |
| Build version | 0.0.0 (source default) | `src/Directory.Build.props` |
| Build tool | MSBuild / dotnet CLI | Standard .NET SDK |
