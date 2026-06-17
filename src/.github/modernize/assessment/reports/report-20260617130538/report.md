# DateTimeRoutines

## Summary

| Metric | Value |
|--------|-------|
| Total Issues | 16 |
| Mandatory Blockers | 8 |
| Potential Issues | 6 |

## Component Information

| Property | Value |
|----------|-------|
| Language | C# |
| Frameworks | netstandard2.0, net9.0 |
| Build tools | MSBuild |

## Cloud Readiness Issues

| Issue Name | Criticality | Story Points | Occurrences |
|------------|-------------|--------------|-------------|
| Service control manager API calls detected | Mandatory | 3 | [4](#Service_control_manager_API_calls_detected) |
| COM usage detected | Mandatory | 5 | [2](#COM_usage_detected) |
| Local or network IO operations detected | Potential | 3 | [2](#Local_or_network_IO_operations_detected) |
| Hardcoded URLs detected | Potential | 1 | [1](#Hardcoded_URLs_detected) |
| Local OS environment access detected | Potential | 1 | [1](#Local_OS_environment_access_detected) |
| Local process start detected | Optional | 5 | [15](#Local_process_start_detected) |
| Static content detected | Optional | 3 | [4](#Static_content_detected) |

### Issue Details

<details id="Service_control_manager_API_calls_detected">
<summary><b>Service control manager API calls detected</b> — affected files</summary>

- `Jackett.Service\Program.cs (line 16)`
- `Jackett.Service\Program.cs (line 11)`
- `Jackett.Service\Program.cs (line 12)`
- `Jackett.Service\Service.cs (line 12)`

</details>

<details id="COM_usage_detected">
<summary><b>COM usage detected</b> — affected files</summary>

- `Jackett.Tray\Main.cs (line 293)`
- `Jackett.Tray\Main.cs (line 299)`

</details>

<details id="Local_or_network_IO_operations_detected">
<summary><b>Local or network IO operations detected</b> — affected files</summary>

- `Jackett.Tray\Main.cs (line 136)`
- `Jackett.Tray\Main.cs (line 145)`

</details>

<details id="Hardcoded_URLs_detected">
<summary><b>Hardcoded URLs detected</b> — affected files</summary>

- `Jackett.Tray\Main.cs (line 121)`

</details>

<details id="Local_OS_environment_access_detected">
<summary><b>Local OS environment access detected</b> — affected files</summary>

- `Jackett.Tray\Main.cs (line 150)`

</details>

<details id="Local_process_start_detected">
<summary><b>Local process start detected</b> — affected files</summary>

- `Jackett.Service\Service.cs (line 63)`
- `Jackett.Service\Service.cs (line 15)`
- `Jackett.Service\Service.cs (line 54)`
- `Jackett.Tray\Main.cs (line 275)`
- `Jackett.Tray\Main.cs (line 26)`
- `Jackett.Tray\Main.cs (line 125)`
- `Jackett.Tray\Main.cs (line 111)`
- `Jackett.Tray\Main.cs (line 156)`
- `Jackett.Tray\Main.cs (line 157)`
- `Jackett.Tray\Main.cs (line 119)`
- `Jackett.Tray\Main.cs (line 101)`
- `Jackett.Tray\Main.cs (line 266)`
- `Jackett.Tray\Program.cs (line 18)`
- `Jackett.Tray\Program.cs (line 16)`
- `Jackett.Tray\Program.cs (line 17)`

</details>

<details id="Static_content_detected">
<summary><b>Static content detected</b> — affected files</summary>

- `Jackett.Common\Jackett.Common.csproj`
- `Jackett.Service\Jackett.Service.csproj`
- `Jackett.Test\Jackett.Test.csproj`
- `Jackett.Tray\Jackett.Tray.csproj`

</details>

## DotNET Upgrade Issues [View Details](scenarios/dotnet-version-upgrade/assessment.md)

| Issue Category | Criticality | Story Points | Occurrences |
|----------------|-------------|--------------|-------------|
| Binary incompatible for selected .NET version | Mandatory | 1 | [281](#Binary_incompatible_for_selected_NET_version) |
| Project's target framework(s) needs to be changed | Mandatory | 1 | [8](#Project_s_target_framework_s_needs_to_be_changed) |
| NuGet package functionality is included with framework reference | Mandatory | 1 | [1](#NuGet_package_functionality_is_included_with_framework_reference) |
| Windows Forms Legacy Controls | Mandatory | 3 | 0 |
| GDI+ / System.Drawing | Mandatory | 1 | 0 |
| Windows Forms | Mandatory | 1 | 0 |
| Behavioral change in selected .NET version | Potential | 1 | [984](#Behavioral_change_in_selected_NET_version) |
| Source incompatible for selected .NET version | Potential | 1 | [116](#Source_incompatible_for_selected_NET_version) |
| NuGet package upgrade is recommended | Potential | 1 | [8](#NuGet_package_upgrade_is_recommended) |

### Issue Details

<details id="Binary_incompatible_for_selected_NET_version">
<summary><b>Binary incompatible for selected .NET version</b> — affected files</summary>

- `Jackett.Tray\Program.cs (line 48, col 16)`
- `Jackett.Tray\Program.cs (line 47, col 16)`
- `Jackett.Tray\Program.cs (line 46, col 16)`
- `Jackett.Tray\Program.cs (line 23, col 16)`
- `Jackett.Tray\Main.Designer.cs (line 136, col 56)`
- `Jackett.Tray\Main.Designer.cs (line 135, col 55)`
- `Jackett.Tray\Main.Designer.cs (line 134, col 55)`
- `Jackett.Tray\Main.Designer.cs (line 133, col 56)`
- `Jackett.Tray\Main.Designer.cs (line 132, col 55)`
- `Jackett.Tray\Main.Designer.cs (line 131, col 55)`
- `Jackett.Tray\Main.Designer.cs (line 130, col 55)`
- `Jackett.Tray\Main.Designer.cs (line 129, col 54)`
- `Jackett.Tray\Main.Designer.cs (line 128, col 48)`
- `Jackett.Tray\Main.Designer.cs (line 122, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 121, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 120, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 119, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 118, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 117, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 116, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 115, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 114, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 113, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 109, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 108, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 107, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 103, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 102, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 101, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 100, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 99, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 95, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 94, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 90, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 89, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 88, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 87, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 83, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 82, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 81, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 80, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 76, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 75, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 71, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 70, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 69, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 65, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 64, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 63, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 55, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 51, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 50, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 49, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 48, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 44, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 43, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 42, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 41, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 40, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 39, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 38, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 37, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 36, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 35, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 34, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 21, col 12)`
- `Jackett.Tray\Main.cs (line 259, col 12)`
- `Jackett.Tray\Main.cs (line 247, col 12)`
- `Jackett.Tray\Main.cs (line 246, col 12)`
- `Jackett.Tray\Main.cs (line 245, col 12)`
- `Jackett.Tray\Main.cs (line 232, col 24)`
- `Jackett.Tray\Main.cs (line 214, col 24)`
- `Jackett.Tray\Main.cs (line 198, col 12)`
- `Jackett.Tray\Main.cs (line 192, col 16)`
- `Jackett.Tray\Main.cs (line 191, col 16)`
- `Jackett.Tray\Main.cs (line 190, col 16)`
- `Jackett.Tray\Main.cs (line 189, col 16)`
- `Jackett.Tray\Main.cs (line 188, col 16)`
- `Jackett.Tray\Main.cs (line 184, col 16)`
- `Jackett.Tray\Main.cs (line 181, col 20)`
- `Jackett.Tray\Main.cs (line 180, col 20)`
- `Jackett.Tray\Main.cs (line 179, col 20)`
- `Jackett.Tray\Main.cs (line 175, col 20)`
- `Jackett.Tray\Main.cs (line 174, col 20)`
- `Jackett.Tray\Main.cs (line 173, col 20)`
- `Jackett.Tray\Main.cs (line 169, col 16)`
- `Jackett.Tray\Main.cs (line 168, col 16)`
- `Jackett.Tray\Main.cs (line 167, col 16)`
- `Jackett.Tray\Main.cs (line 166, col 16)`
- `Jackett.Tray\Main.cs (line 130, col 106)`
- `Jackett.Tray\Main.cs (line 100, col 16)`
- `Jackett.Tray\Main.cs (line 83, col 16)`
- `Jackett.Tray\Main.cs (line 82, col 16)`
- `Jackett.Tray\Main.cs (line 81, col 16)`
- `Jackett.Tray\Main.cs (line 80, col 16)`
- `Jackett.Tray\Main.cs (line 66, col 16)`
- `Jackett.Tray\Main.cs (line 62, col 12)`
- `Jackett.Tray\Main.cs (line 61, col 12)`
- `Jackett.Tray\Main.cs (line 60, col 12)`
- `Jackett.Tray\Main.cs (line 58, col 12)`
- `Jackett.Tray\Main.cs (line 57, col 12)`
- `Jackett.Tray\Main.cs (line 38, col 12)`
- `Jackett.Tray\Main.cs (line 37, col 12)`
- `Jackett.Tray\Main.cs (line 36, col 12)`
- `Jackett.Tray\Main.cs (line 35, col 12)`
- `Jackett.Tray\Main.cs (line 32, col 12)`
- `Jackett.Tray\Main.cs (line 30, col 8)`
- `Jackett.Tray\Main.cs (line 18, col 32)`

</details>

<details id="Project_s_target_framework_s_needs_to_be_changed">
<summary><b>Project's target framework(s) needs to be changed</b> — affected files</summary>

- `DateTimeRoutines\DateTimeRoutines.csproj`
- `Jackett.Common\Jackett.Common.csproj`
- `Jackett.IntegrationTests\Jackett.IntegrationTests.csproj`
- `Jackett.Server\Jackett.Server.csproj`
- `Jackett.Service\Jackett.Service.csproj`
- `Jackett.Test\Jackett.Test.csproj`
- `Jackett.Tray\Jackett.Tray.csproj`
- `Jackett.Updater\Jackett.Updater.csproj`

</details>

<details id="NuGet_package_functionality_is_included_with_framework_reference">
<summary><b>NuGet package functionality is included with framework reference</b> — affected files</summary>

- `Jackett.Common\Jackett.Common.csproj`

</details>

<details id="Behavioral_change_in_selected_NET_version">
<summary><b>Behavioral change in selected .NET version</b> — affected files</summary>

- `Jackett.Common\Utils\Clients\WebClient.cs (line 265, col 8)`
- `Jackett.Common\Utils\Clients\WebClient.cs (line 290, col 12)`
- `Jackett.Common\Utils\Clients\WebClient.cs (line 284, col 20)`
- `Jackett.Common\Utils\Clients\WebClient.cs (line 267, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 232, col 20)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 230, col 20)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 218, col 16)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 214, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 182, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 175, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 165, col 20)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 159, col 20)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 156, col 20)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 146, col 16)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 119, col 16)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 110, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 51, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 210, col 40)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 208, col 40)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 196, col 36)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 192, col 32)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 160, col 32)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 153, col 32)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 142, col 36)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 136, col 36)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 133, col 36)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 123, col 32)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 100, col 28)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 68, col 16)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 67, col 16)`
- `Jackett.Common\Utils\Variants.cs (line 53, col 16)`
- `Jackett.Common\Utils\ServerUtil.cs (line 110, col 20)`
- `Jackett.Common\Utils\ServerUtil.cs (line 109, col 20)`
- `Jackett.Common\Utils\MagnetUtil.cs (line 34, col 8)`
- `Jackett.Common\Utils\MagnetUtil.cs (line 27, col 8)`
- `Jackett.Common\Utils\MagnetUtil.cs (line 31, col 12)`
- `Jackett.Common\Utils\EnvironmentUtil.cs (line 27, col 40)`
- `Jackett.Common\Utils\CookieUtil.cs (line 84, col 16)`
- `Jackett.Common\Utils\CookieUtil.cs (line 79, col 16)`
- `Jackett.Common\Utils\CookieUtil.cs (line 73, col 20)`
- `Jackett.Common\Utils\CookieUtil.cs (line 68, col 20)`
- `Jackett.Common\Utils\BrowserUtil.cs (line 8, col 48)`
- `Jackett.Common\Services\Interfaces\IServerService.cs (line 12, col 8)`
- `Jackett.Common\Services\TrayLockService.cs (line 24, col 12)`
- `Jackett.Common\Services\TrayLockService.cs (line 15, col 12)`
- `Jackett.Common\Services\ImdbResolver.cs (line 42, col 12)`
- `Jackett.Common\Services\ImdbResolver.cs (line 39, col 16)`
- `Jackett.Common\Services\ImdbResolver.cs (line 37, col 12)`
- `Jackett.Common\Services\ConfigurationService.cs (line 217, col 12)`
- `Jackett.Common\Services\ConfigurationService.cs (line 103, col 12)`
- `Jackett.Common\Services\ConfigurationService.cs (line 68, col 12)`
- `Jackett.Common\Services\CacheService.cs (line 122, col 16)`
- `Jackett.Common\Models\Config\ServerConfig.cs (line 18, col 12)`
- `Jackett.Common\Models\Config\RuntimeSettings.cs (line 37, col 16)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 46, col 12)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 44, col 12)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 19, col 12)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 18, col 12)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 17, col 12)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 12, col 40)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 12, col 35)`
- `Jackett.Common\Models\TrackerCacheResult.cs (line 12, col 8)`
- `Jackett.Common\Models\ResultPage.cs (line 54, col 8)`
- `Jackett.Common\Models\ResultPage.cs (line 58, col 12)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 105, col 443)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 105, col 402)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 105, col 111)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 105, col 95)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 105, col 82)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 95, col 12)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 93, col 12)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 66, col 12)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 65, col 12)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 64, col 12)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 42, col 36)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 42, col 31)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 42, col 8)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 40, col 33)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 40, col 28)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 40, col 8)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 13, col 34)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 13, col 29)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 13, col 8)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 12, col 31)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 12, col 26)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 12, col 8)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 11, col 31)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 11, col 26)`
- `Jackett.Common\Models\ReleaseInfo.cs (line 11, col 8)`
- `Jackett.Common\Models\ChannelInfo.cs (line 8, col 31)`
- `Jackett.Common\Models\ChannelInfo.cs (line 8, col 26)`
- `Jackett.Common\Models\ChannelInfo.cs (line 8, col 8)`
- `Jackett.Common\Indexers\Feeds\BaseNewznabIndexer.cs (line 98, col 16)`
- `Jackett.Common\Indexers\Feeds\BaseNewznabIndexer.cs (line 75, col 12)`
- `Jackett.Common\Indexers\Feeds\BaseNewznabIndexer.cs (line 60, col 12)`
- `Jackett.Common\Indexers\Feeds\BaseFeedIndexer.cs (line 43, col 12)`
- `Jackett.Common\Indexers\Feeds\BaseFeedIndexer.cs (line 16, col 41)`
- `Jackett.Common\Indexers\Feeds\BaseFeedIndexer.cs (line 16, col 8)`
- `Jackett.Common\Indexers\Definitions\Feeds\MoreThanTVAPI.cs (line 149, col 39)`
- `Jackett.Common\Indexers\Definitions\Feeds\MoreThanTVAPI.cs (line 149, col 42)`
- `Jackett.Common\Indexers\Definitions\Feeds\MoreThanTVAPI.cs (line 149, col 8)`
- `Jackett.Common\Indexers\Definitions\Feeds\MoreThanTVAPI.cs (line 139, col 16)`
- `Jackett.Common\Indexers\Definitions\Feeds\MoreThanTVAPI.cs (line 86, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\SpeedAppTracker.cs (line 210, col 8)`
- `Jackett.Common\Indexers\Definitions\Abstract\SpeedAppTracker.cs (line 177, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\SpeedAppTracker.cs (line 168, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\SpeedAppTracker.cs (line 152, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\SpeedAppTracker.cs (line 150, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\PublicBrazilianIndexerBase.cs (line 131, col 8)`
- `Jackett.Common\Indexers\Definitions\Abstract\PublicBrazilianIndexerBase.cs (line 134, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 579, col 8)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 581, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 574, col 8)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 576, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 545, col 8)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 567, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 509, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 508, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 507, col 12)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 321, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\GazelleTracker.cs (line 318, col 24)`
- `Jackett.Common\Indexers\Definitions\Abstract\CouchPotatoTracker.cs (line 99, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\CouchPotatoTracker.cs (line 93, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\AvistazTracker.cs (line 283, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\AvistazTracker.cs (line 268, col 20)`
- `Jackett.Common\Indexers\Definitions\Abstract\AvistazTracker.cs (line 267, col 20)`
- `Jackett.Common\Indexers\Definitions\XSpeeds.cs (line 329, col 20)`
- `Jackett.Common\Indexers\Definitions\XSpeeds.cs (line 319, col 24)`
- `Jackett.Common\Indexers\Definitions\XSpeeds.cs (line 305, col 20)`
- `Jackett.Common\Indexers\Definitions\XSpeeds.cs (line 304, col 20)`
- `Jackett.Common\Indexers\Definitions\XSpeeds.cs (line 303, col 20)`
- `Jackett.Common\Indexers\Definitions\Wolfmax4K.cs (line 288, col 16)`
- `Jackett.Common\Indexers\Definitions\Wolfmax4K.cs (line 272, col 12)`
- `Jackett.Common\Indexers\Definitions\Wolfmax4K.cs (line 267, col 12)`
- `Jackett.Common\Indexers\Definitions\Wolfmax4K.cs (line 158, col 8)`
- `Jackett.Common\Indexers\Definitions\Wolfmax4K.cs (line 43, col 16)`
- `Jackett.Common\Indexers\Definitions\Uniotaku.cs (line 189, col 8)`
- `Jackett.Common\Indexers\Definitions\Uniotaku.cs (line 200, col 12)`
- `Jackett.Common\Indexers\Definitions\Uniotaku.cs (line 159, col 20)`
- `Jackett.Common\Indexers\Definitions\Uniotaku.cs (line 146, col 20)`
- `Jackett.Common\Indexers\Definitions\TVStore.cs (line 207, col 20)`
- `Jackett.Common\Indexers\Definitions\TVStore.cs (line 169, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentSyndikat.cs (line 282, col 8)`
- `Jackett.Common\Indexers\Definitions\TorrentSyndikat.cs (line 225, col 24)`
- `Jackett.Common\Indexers\Definitions\TorrentSyndikat.cs (line 200, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentSyndikat.cs (line 197, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentsCSV.cs (line 141, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentsCSV.cs (line 89, col 16)`
- `Jackett.Common\Indexers\Definitions\TorrentNetwork.cs (line 266, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentNetwork.cs (line 264, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentNetwork.cs (line 252, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentDay.cs (line 236, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentDay.cs (line 232, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentDay.cs (line 228, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentBytes.cs (line 189, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentBytes.cs (line 168, col 20)`
- `Jackett.Common\Indexers\Definitions\TorrentBytes.cs (line 167, col 20)`
- `Jackett.Common\Indexers\Definitions\Toloka.cs (line 325, col 24)`
- `Jackett.Common\Indexers\Definitions\Toloka.cs (line 317, col 24)`
- `Jackett.Common\Indexers\Definitions\Toloka.cs (line 315, col 24)`
- `Jackett.Common\Indexers\Definitions\SubsPlease.cs (line 234, col 20)`
- `Jackett.Common\Indexers\Definitions\SubsPlease.cs (line 233, col 20)`
- `Jackett.Common\Indexers\Definitions\SubsPlease.cs (line 232, col 20)`
- `Jackett.Common\Indexers\Definitions\SubsPlease.cs (line 222, col 24)`
- `Jackett.Common\Indexers\Definitions\SubsPlease.cs (line 206, col 20)`
- `Jackett.Common\Indexers\Definitions\SpeedCD.cs (line 264, col 20)`
- `Jackett.Common\Indexers\Definitions\SpeedCD.cs (line 257, col 20)`
- `Jackett.Common\Indexers\Definitions\SpeedCD.cs (line 256, col 20)`
- `Jackett.Common\Indexers\Definitions\Shazbat.cs (line 256, col 20)`
- `Jackett.Common\Indexers\Definitions\Shazbat.cs (line 234, col 16)`
- `Jackett.Common\Indexers\Definitions\Shazbat.cs (line 221, col 16)`
- `Jackett.Common\Indexers\Definitions\Shazbat.cs (line 220, col 16)`
- `Jackett.Common\Indexers\Definitions\SceneHD.cs (line 142, col 20)`
- `Jackett.Common\Indexers\Definitions\SceneHD.cs (line 138, col 20)`
- `Jackett.Common\Indexers\Definitions\SceneHD.cs (line 137, col 20)`
- `Jackett.Common\Indexers\Definitions\SceneHD.cs (line 85, col 12)`
- `Jackett.Common\Indexers\Definitions\RuTracker.cs (line 1622, col 16)`
- `Jackett.Common\Indexers\Definitions\RuTracker.cs (line 1605, col 16)`
- `Jackett.Common\Indexers\Definitions\RuTracker.cs (line 1602, col 16)`
- `Jackett.Common\Indexers\Definitions\RuTracker.cs (line 1513, col 8)`
- `Jackett.Common\Indexers\Definitions\RuTracker.cs (line 1526, col 16)`
- `Jackett.Common\Indexers\Definitions\RuTracker.cs (line 1515, col 12)`
- `Jackett.Common\Indexers\Definitions\RevolutionTT.cs (line 198, col 20)`
- `Jackett.Common\Indexers\Definitions\RevolutionTT.cs (line 181, col 20)`
- `Jackett.Common\Indexers\Definitions\RevolutionTT.cs (line 171, col 20)`
- `Jackett.Common\Indexers\Definitions\RedeTorrent.cs (line 128, col 20)`
- `Jackett.Common\Indexers\Definitions\RedeTorrent.cs (line 108, col 16)`
- `Jackett.Common\Indexers\Definitions\RedeTorrent.cs (line 104, col 16)`
- `Jackett.Common\Indexers\Definitions\Redacted.cs (line 103, col 8)`
- `Jackett.Common\Indexers\Definitions\Redacted.cs (line 105, col 12)`
- `Jackett.Common\Indexers\Definitions\PreToMe.cs (line 283, col 20)`
- `Jackett.Common\Indexers\Definitions\PreToMe.cs (line 273, col 20)`
- `Jackett.Common\Indexers\Definitions\PreToMe.cs (line 272, col 20)`
- `Jackett.Common\Indexers\Definitions\PixelHD.cs (line 197, col 24)`
- `Jackett.Common\Indexers\Definitions\PixelHD.cs (line 191, col 24)`
- `Jackett.Common\Indexers\Definitions\PixelHD.cs (line 189, col 24)`
- `Jackett.Common\Indexers\Definitions\PixelHD.cs (line 168, col 20)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 355, col 8)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 357, col 12)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 340, col 8)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 348, col 12)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 325, col 8)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 333, col 12)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 313, col 8)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 215, col 24)`
- `Jackett.Common\Indexers\Definitions\PassThePopcorn.cs (line 207, col 24)`
- `Jackett.Common\Indexers\Definitions\Orpheus.cs (line 73, col 8)`
- `Jackett.Common\Indexers\Definitions\Orpheus.cs (line 75, col 12)`
- `Jackett.Common\Indexers\Definitions\NorBits.cs (line 450, col 8)`
- `Jackett.Common\Indexers\Definitions\NorBits.cs (line 453, col 12)`
- `Jackett.Common\Indexers\Definitions\NorBits.cs (line 297, col 24)`
- `Jackett.Common\Indexers\Definitions\NorBits.cs (line 286, col 24)`
- `Jackett.Common\Indexers\Definitions\NorBits.cs (line 282, col 24)`
- `Jackett.Common\Indexers\Definitions\NebulanceAPI.cs (line 371, col 16)`
- `Jackett.Common\Indexers\Definitions\NebulanceAPI.cs (line 351, col 16)`
- `Jackett.Common\Indexers\Definitions\MyAnonamouse.cs (line 373, col 8)`
- `Jackett.Common\Indexers\Definitions\MyAnonamouse.cs (line 375, col 12)`
- `Jackett.Common\Indexers\Definitions\MyAnonamouse.cs (line 297, col 20)`
- `Jackett.Common\Indexers\Definitions\MyAnonamouse.cs (line 293, col 20)`
- `Jackett.Common\Indexers\Definitions\MyAnonamouse.cs (line 275, col 16)`
- `Jackett.Common\Indexers\Definitions\MTeamTp.cs (line 255, col 16)`
- `Jackett.Common\Indexers\Definitions\MTeamTp.cs (line 253, col 16)`
- `Jackett.Common\Indexers\Definitions\MTeamTp.cs (line 252, col 16)`
- `Jackett.Common\Indexers\Definitions\MTeamTp.cs (line 137, col 8)`
- `Jackett.Common\Indexers\Definitions\MTeamTp.cs (line 158, col 12)`
- `Jackett.Common\Indexers\Definitions\MejorTorrent.cs (line 424, col 12)`
- `Jackett.Common\Indexers\Definitions\MejorTorrent.cs (line 423, col 12)`
- `Jackett.Common\Indexers\Definitions\MejorTorrent.cs (line 422, col 12)`
- `Jackett.Common\Indexers\Definitions\MejorTorrent.cs (line 137, col 8)`
- `Jackett.Common\Indexers\Definitions\MejorTorrent.cs (line 140, col 12)`
- `Jackett.Common\Indexers\Definitions\Magnetico.cs (line 129, col 20)`
- `Jackett.Common\Indexers\Definitions\Magnetico.cs (line 126, col 20)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 785, col 28)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 782, col 28)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 640, col 32)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 633, col 28)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 574, col 28)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 567, col 24)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 505, col 24)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 482, col 20)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 155, col 12)`
- `Jackett.Common\Indexers\Definitions\LostFilm.cs (line 154, col 12)`
- `Jackett.Common\Indexers\Definitions\Libble.cs (line 273, col 24)`
- `Jackett.Common\Indexers\Definitions\Libble.cs (line 255, col 24)`
- `Jackett.Common\Indexers\Definitions\Libble.cs (line 254, col 24)`
- `Jackett.Common\Indexers\Definitions\Libble.cs (line 253, col 24)`
- `Jackett.Common\Indexers\Definitions\Libble.cs (line 230, col 24)`
- `Jackett.Common\Indexers\Definitions\Knaben.cs (line 284, col 16)`
- `Jackett.Common\Indexers\Definitions\Knaben.cs (line 277, col 16)`
- `Jackett.Common\Indexers\Definitions\Knaben.cs (line 271, col 16)`
- `Jackett.Common\Indexers\Definitions\IPTorrents.cs (line 404, col 20)`
- `Jackett.Common\Indexers\Definitions\IPTorrents.cs (line 364, col 20)`
- `Jackett.Common\Indexers\Definitions\IPTorrents.cs (line 361, col 20)`
- `Jackett.Common\Indexers\Definitions\ImmortalSeed.cs (line 277, col 20)`
- `Jackett.Common\Indexers\Definitions\ImmortalSeed.cs (line 250, col 20)`
- `Jackett.Common\Indexers\Definitions\ImmortalSeed.cs (line 249, col 20)`
- `Jackett.Common\Indexers\Definitions\ImmortalSeed.cs (line 248, col 20)`
- `Jackett.Common\Indexers\Definitions\HDRTorrent.cs (line 149, col 20)`
- `Jackett.Common\Indexers\Definitions\HDRTorrent.cs (line 117, col 16)`
- `Jackett.Common\Indexers\Definitions\HDRTorrent.cs (line 115, col 16)`
- `Jackett.Common\Indexers\Definitions\HDBitsApi.cs (line 195, col 16)`
- `Jackett.Common\Indexers\Definitions\HDBitsApi.cs (line 194, col 16)`
- `Jackett.Common\Indexers\Definitions\HDBitsApi.cs (line 189, col 16)`
- `Jackett.Common\Indexers\Definitions\GazelleGamesAPI.cs (line 374, col 24)`
- `Jackett.Common\Indexers\Definitions\GazelleGamesAPI.cs (line 322, col 24)`
- `Jackett.Common\Indexers\Definitions\GazelleGamesAPI.cs (line 321, col 24)`
- `Jackett.Common\Indexers\Definitions\FunFile.cs (line 222, col 20)`
- `Jackett.Common\Indexers\Definitions\FunFile.cs (line 214, col 20)`
- `Jackett.Common\Indexers\Definitions\FunFile.cs (line 210, col 20)`
- `Jackett.Common\Indexers\Definitions\FilmesHdTorrent.cs (line 117, col 20)`
- `Jackett.Common\Indexers\Definitions\FilmesHdTorrent.cs (line 108, col 20)`
- `Jackett.Common\Indexers\Definitions\FilmesHdTorrent.cs (line 91, col 16)`
- `Jackett.Common\Indexers\Definitions\FilmesHdTorrent.cs (line 90, col 16)`
- `Jackett.Common\Indexers\Definitions\FileList.cs (line 180, col 20)`
- `Jackett.Common\Indexers\Definitions\FileList.cs (line 177, col 20)`
- `Jackett.Common\Indexers\Definitions\FileList.cs (line 176, col 20)`
- `Jackett.Common\Indexers\Definitions\EraiRaws.cs (line 299, col 16)`
- `Jackett.Common\Indexers\Definitions\EraiRaws.cs (line 291, col 20)`
- `Jackett.Common\Indexers\Definitions\EraiRaws.cs (line 285, col 20)`
- `Jackett.Common\Indexers\Definitions\EraiRaws.cs (line 281, col 16)`
- `Jackett.Common\Indexers\Definitions\EraiRaws.cs (line 250, col 16)`
- `Jackett.Common\Indexers\Definitions\EpubLibre.cs (line 174, col 8)`
- `Jackett.Common\Indexers\Definitions\EpubLibre.cs (line 176, col 12)`
- `Jackett.Common\Indexers\Definitions\EpubLibre.cs (line 143, col 24)`
- `Jackett.Common\Indexers\Definitions\EpubLibre.cs (line 132, col 24)`
- `Jackett.Common\Indexers\Definitions\EpubLibre.cs (line 130, col 24)`
- `Jackett.Common\Indexers\Definitions\EpubLibre.cs (line 106, col 16)`
- `Jackett.Common\Indexers\Definitions\DonTorrent.cs (line 562, col 12)`
- `Jackett.Common\Indexers\Definitions\DonTorrent.cs (line 561, col 12)`
- `Jackett.Common\Indexers\Definitions\DonTorrent.cs (line 560, col 12)`
- `Jackett.Common\Indexers\Definitions\DonTorrent.cs (line 161, col 8)`
- `Jackett.Common\Indexers\Definitions\DonTorrent.cs (line 185, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2185, col 8)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2401, col 20)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2399, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2398, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2217, col 20)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2216, col 20)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2209, col 20)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2208, col 20)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2204, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2203, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2199, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2198, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2193, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2058, col 8)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2133, col 28)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2105, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2104, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2005, col 8)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2012, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2008, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 2007, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1948, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1559, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1508, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1403, col 8)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1403, col 95)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1403, col 73)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1025, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1024, col 24)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1007, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 1002, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 996, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 875, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 859, col 12)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 835, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 825, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 728, col 20)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 722, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 598, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 585, col 16)`
- `Jackett.Common\Indexers\Definitions\CardigannIndexer.cs (line 246, col 20)`
- `Jackett.Common\Indexers\Definitions\BroadcasTheNet.cs (line 341, col 20)`
- `Jackett.Common\Indexers\Definitions\BroadcasTheNet.cs (line 309, col 16)`
- `Jackett.Common\Indexers\Definitions\BroadcasTheNet.cs (line 306, col 16)`
- `Jackett.Common\Indexers\Definitions\BroadcasTheNet.cs (line 305, col 16)`
- `Jackett.Common\Indexers\Definitions\BrasilTracker.cs (line 335, col 24)`
- `Jackett.Common\Indexers\Definitions\BrasilTracker.cs (line 334, col 24)`
- `Jackett.Common\Indexers\Definitions\BrasilTracker.cs (line 333, col 24)`
- `Jackett.Common\Indexers\Definitions\BrasilTracker.cs (line 281, col 24)`
- `Jackett.Common\Indexers\Definitions\BrasilTracker.cs (line 243, col 28)`
- `Jackett.Common\Indexers\Definitions\BitHDTV.cs (line 191, col 24)`
- `Jackett.Common\Indexers\Definitions\BitHDTV.cs (line 190, col 24)`
- `Jackett.Common\Indexers\Definitions\BitHDTV.cs (line 189, col 24)`
- `Jackett.Common\Indexers\Definitions\BitHDTV.cs (line 188, col 24)`
- `Jackett.Common\Indexers\Definitions\BitHDTV.cs (line 173, col 24)`
- `Jackett.Common\Indexers\Definitions\BitHDTV.cs (line 171, col 24)`
- `Jackett.Common\Indexers\Definitions\BeyondHDAPI.cs (line 286, col 16)`
- `Jackett.Common\Indexers\Definitions\BakaBT.cs (line 316, col 8)`
- `Jackett.Common\Indexers\Definitions\BakaBT.cs (line 233, col 24)`
- `Jackett.Common\Indexers\Definitions\BakaBT.cs (line 231, col 24)`
- `Jackett.Common\Indexers\Definitions\BakaBT.cs (line 230, col 24)`
- `Jackett.Common\Indexers\Definitions\AudioBookBay.cs (line 279, col 8)`
- `Jackett.Common\Indexers\Definitions\AudioBookBay.cs (line 281, col 12)`
- `Jackett.Common\Indexers\Definitions\AudioBookBay.cs (line 241, col 16)`
- `Jackett.Common\Indexers\Definitions\AudioBookBay.cs (line 213, col 16)`
- `Jackett.Common\Indexers\Definitions\AudioBookBay.cs (line 107, col 8)`
- `Jackett.Common\Indexers\Definitions\AudioBookBay.cs (line 128, col 12)`
- `Jackett.Common\Indexers\Definitions\ApacheTorrent.cs (line 127, col 20)`
- `Jackett.Common\Indexers\Definitions\ApacheTorrent.cs (line 107, col 16)`
- `Jackett.Common\Indexers\Definitions\ApacheTorrent.cs (line 104, col 16)`
- `Jackett.Common\Indexers\Definitions\AnimeZ.cs (line 73, col 8)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 737, col 31)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 737, col 26)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 736, col 8)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 594, col 28)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 592, col 28)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 551, col 28)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 549, col 28)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 330, col 24)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 328, col 24)`
- `Jackett.Common\Indexers\Definitions\AnimeBytes.cs (line 284, col 20)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 207, col 8)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 207, col 52)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 205, col 8)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 205, col 55)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 203, col 8)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 203, col 52)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 201, col 8)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 201, col 62)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 168, col 12)`
- `Jackett.Common\Indexers\Definitions\Anilibria.cs (line 124, col 12)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 539, col 8)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 543, col 12)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 379, col 8)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 384, col 12)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 327, col 8)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 328, col 12)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 254, col 20)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 253, col 20)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 236, col 16)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 216, col 12)`
- `Jackett.Common\Indexers\Definitions\AniDUB.cs (line 157, col 8)`
- `Jackett.Common\Indexers\IIndexer.cs (line 76, col 8)`
- `Jackett.Common\Indexers\IIndexer.cs (line 74, col 8)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 820, col 8)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 832, col 12)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 806, col 20)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 804, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 696, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 574, col 8)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 576, col 12)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 536, col 8)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 556, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 530, col 8)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 532, col 12)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 385, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 266, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 259, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 246, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 232, col 24)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 230, col 25)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 228, col 24)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 226, col 25)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 224, col 24)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 222, col 20)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 220, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 216, col 20)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 214, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 210, col 20)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 208, col 16)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 137, col 12)`
- `Jackett.Common\Extensions\UriExtensions.cs (line 7, col 8)`
- `Jackett.Common\Extensions\UriExtensions.cs (line 14, col 12)`
- `Jackett.Server\Services\ServerService.cs (line 82, col 16)`
- `Jackett.Server\Services\ServerService.cs (line 79, col 16)`
- `Jackett.Server\Services\ServerService.cs (line 50, col 8)`
- `Jackett.Server\Services\ServerService.cs (line 60, col 12)`
- `Jackett.Server\Controllers\ServerConfigurationController.cs (line 220, col 16)`
- `Jackett.Server\Controllers\ServerConfigurationController.cs (line 145, col 21)`
- `Jackett.Server\Controllers\ServerConfigurationController.cs (line 107, col 21)`
- `Jackett.Server\Controllers\ResultsController.cs (line 618, col 24)`
- `Jackett.Server\Controllers\ResultsController.cs (line 617, col 25)`
- `Jackett.Server\Controllers\ResultsController.cs (line 616, col 24)`
- `Jackett.Server\Controllers\ResultsController.cs (line 615, col 20)`
- `Jackett.Server\Controllers\ResultsController.cs (line 612, col 16)`
- `Jackett.Server\Controllers\ResultsController.cs (line 611, col 16)`
- `Jackett.Server\Controllers\ResultsController.cs (line 609, col 16)`
- `Jackett.Server\Controllers\ResultsController.cs (line 578, col 16)`
- `Jackett.Server\Controllers\ResultsController.cs (line 572, col 16)`
- `Jackett.Server\Controllers\ResultsController.cs (line 570, col 12)`
- `Jackett.Server\Controllers\ResultsController.cs (line 467, col 16)`
- `Jackett.Server\Controllers\ResultsController.cs (line 451, col 24)`
- `Jackett.Server\Controllers\ResultsController.cs (line 450, col 24)`
- `Jackett.Server\Controllers\ResultsController.cs (line 439, col 16)`
- `Jackett.Server\Controllers\IndexerApiController.cs (line 174, col 20)`
- `Jackett.Server\Controllers\IndexerApiController.cs (line 173, col 16)`
- `Jackett.Server\Controllers\IndexerApiController.cs (line 172, col 16)`
- `Jackett.Server\Controllers\IndexerApiController.cs (line 171, col 16)`
- `Jackett.Server\Controllers\IndexerApiController.cs (line 169, col 16)`
- `Jackett.Server\Controllers\ImageController.cs (line 51, col 16)`
- `Jackett.Server\Controllers\DownloadController.cs (line 54, col 16)`
- `Jackett.Server\Controllers\BlackholeController.cs (line 51, col 16)`
- `Jackett.Server\Startup.cs (line 181, col 12)`
- `Jackett.Server\Program.cs (line 81, col 16)`
- `Jackett.Server\Program.cs (line 28, col 12)`
- `Jackett.Test\Server\Services\RuntimeSettingsTests.cs (line 17, col 12)`
- `Jackett.Test\Common\Utils\UriFixture.cs (line 32, col 12)`
- `Jackett.Test\Common\Utils\UriFixture.cs (line 31, col 12)`
- `Jackett.Test\Common\Utils\UriFixture.cs (line 16, col 12)`
- `Jackett.Test\Common\Utils\UriFixture.cs (line 15, col 12)`
- `Jackett.Test\Common\Utils\MagnetUtilTests.cs (line 39, col 12)`
- `Jackett.Test\Common\Utils\MagnetUtilTests.cs (line 34, col 12)`
- `Jackett.Test\Common\Utils\MagnetUtilTests.cs (line 26, col 12)`
- `Jackett.Test\Common\Utils\MagnetUtilTests.cs (line 22, col 12)`
- `Jackett.Test\Common\Utils\MagnetUtilTests.cs (line 18, col 12)`
- `Jackett.Test\Common\Utils\CookieUtilTests.cs (line 126, col 12)`
- `Jackett.Test\Common\Utils\CookieUtilTests.cs (line 125, col 12)`
- `Jackett.Test\Common\Utils\CookieUtilTests.cs (line 110, col 12)`
- `Jackett.Test\Common\Utils\CookieUtilTests.cs (line 108, col 12)`
- `Jackett.Test\Common\Models\ResultPageTests.cs (line 50, col 12)`
- `Jackett.Test\Common\Models\ResultPageTests.cs (line 47, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerJsonTests.cs (line 54, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerJsonTests.cs (line 52, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerJsonTests.cs (line 51, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerJsonTests.cs (line 50, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerJsonTests.cs (line 49, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerHtmlTests.cs (line 53, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerHtmlTests.cs (line 52, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerHtmlTests.cs (line 51, col 12)`
- `Jackett.Test\Common\Indexers\CardigannIndexerHtmlTests.cs (line 50, col 12)`
- `Jackett.Test\Common\Indexers\BaseWebIndexerTests.cs (line 207, col 12)`
- `Jackett.Test\Common\Indexers\BaseWebIndexerTests.cs (line 205, col 12)`
- `Jackett.Test\Common\Indexers\BaseWebIndexerTests.cs (line 201, col 12)`
- `Jackett.Test\Common\Indexers\BaseWebIndexerTests.cs (line 199, col 12)`
- `Jackett.Test\Common\Indexers\BaseWebIndexerTests.cs (line 178, col 12)`
- `Jackett.Tray\Main.cs (line 64, col 12)`
- `Jackett.Updater\Program.cs (line 86, col 20)`

</details>

<details id="Source_incompatible_for_selected_NET_version">
<summary><b>Source incompatible for selected .NET version</b> — affected files</summary>

- `Jackett.Common\Utils\Clients\WebClient.cs (line 95, col 42)`
- `Jackett.Common\Utils\Clients\HttpWebClient2.cs (line 103, col 12)`
- `Jackett.Common\Utils\Clients\HttpWebClient.cs (line 96, col 24)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 166, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 155, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 81, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 79, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 77, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 75, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 73, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 71, col 20)`
- `Jackett.Common\Utils\DateTimeUtil.cs (line 69, col 20)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 95, col 16)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 94, col 16)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 92, col 16)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 91, col 16)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 89, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 83, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 47, col 8)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 47, col 133)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 47, col 67)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 44, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 43, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 38, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 37, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 33, col 40)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 33, col 29)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 33, col 12)`
- `Jackett.Common\Services\WindowsServiceConfigService.cs (line 30, col 39)`
- `Jackett.Common\Services\UpdateService.cs (line 69, col 16)`
- `Jackett.Common\Services\CacheService.cs (line 175, col 36)`
- `Jackett.Common\Indexers\Meta\BaseMetaIndexer.cs (line 92, col 12)`
- `Jackett.Common\Indexers\BaseIndexer.cs (line 471, col 16)`
- `Jackett.Common\Exceptions\TooManyRequestsException.cs (line 23, col 20)`
- `Jackett.IntegrationTests\DashboardTests.cs (line 84, col 12)`
- `Jackett.IntegrationTests\DashboardTests.cs (line 78, col 12)`
- `Jackett.IntegrationTests\DashboardTests.cs (line 65, col 12)`
- `Jackett.IntegrationTests\DashboardTests.cs (line 64, col 12)`
- `Jackett.IntegrationTests\DashboardTests.cs (line 63, col 12)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 89, col 16)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 88, col 16)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 86, col 16)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 85, col 16)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 83, col 12)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 77, col 12)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 38, col 8)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 41, col 51)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 39, col 12)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 36, col 30)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 34, col 31)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 32, col 40)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 32, col 29)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 32, col 12)`
- `Jackett.Server\Services\ServiceConfigService.cs (line 29, col 39)`
- `Jackett.Server\Controllers\ResultsController.cs (line 478, col 20)`
- `Jackett.Server\Startup.cs (line 70, col 16)`
- `Jackett.Server\Startup.cs (line 69, col 16)`
- `Jackett.Server\Startup.cs (line 68, col 16)`
- `Jackett.Server\Startup.cs (line 67, col 16)`
- `Jackett.Server\Startup.cs (line 66, col 16)`
- `Jackett.Server\Program.cs (line 169, col 12)`
- `Jackett.Server\Program.cs (line 124, col 20)`
- `Jackett.Service\Service.Designer.cs (line 31, col 12)`
- `Jackett.Service\Service.Designer.cs (line 19, col 12)`
- `Jackett.Service\Service.cs (line 78, col 16)`
- `Jackett.Service\Service.cs (line 19, col 8)`
- `Jackett.Service\Service.cs (line 12, col 35)`
- `Jackett.Service\Program.cs (line 16, col 12)`
- `Jackett.Test\TestHelpers\TestCacheService.cs (line 26, col 36)`
- `Jackett.Tray\Main.Designer.cs (line 116, col 12)`
- `Jackett.Tray\Main.Designer.cs (line 49, col 12)`
- `Jackett.Tray\Main.cs (line 245, col 12)`

</details>

<details id="NuGet_package_upgrade_is_recommended">
<summary><b>NuGet package upgrade is recommended</b> — affected files</summary>

- `Jackett.Common\Jackett.Common.csproj`
- `Jackett.Server\Jackett.Server.csproj`
- `Jackett.Test\Jackett.Test.csproj`

</details>

---

## Codebase Insights

> **Note:** These documents are generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

1. **[Architecture Diagram](facts/architecture-diagram.md)** — Understand the big picture: system layers and component relationships
2. **[Dependency Map](facts/dependency-map.md)** — Know what the project depends on and where the risks are
3. **[API & Service Contracts](facts/api-service-contracts.md)** — See how services communicate and what contracts they expose
4. **[Data Architecture](facts/data-architecture.md)** — Explore data models, storage, and data flow patterns
5. **[Configuration Inventory](facts/configuration-inventory.md)** — Review how the application is configured across environments
6. **[Business Workflows](facts/business-workflows.md)** — Trace end-to-end business processes and domain logic

[Share feedback](https://aka.ms/ghcp-appmod/feedback)
