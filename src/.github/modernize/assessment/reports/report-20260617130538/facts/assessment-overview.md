# Assessment Overview

This directory contains supplementary architecture and design documents generated as part of the application assessment. Each document provides a focused view of a different aspect of the Jackett codebase.

## Supplementary Documents

| Document | Description |
|---|---|
| [Architecture Diagram](./architecture-diagram.md) | Two-layer architecture visualization: high-level application architecture (layers, external services, OS integration) and detailed component relationships (controllers, services, indexer engine, data access) |
| [Dependency Map](./dependency-map.md) | Visual map of all external NuGet dependencies grouped by functional category (web frameworks, HTML parsing, HTTP/networking, serialization, logging, DI, utilities), plus test dependencies |
| [API & Service Contracts](./api-service-contracts.md) | Complete inventory of all REST API endpoints across 8 controllers, communication patterns (Torznab, TorrentPotato, JSON), authentication model, and service communication sequence diagram |
| [Data Architecture](./data-architecture.md) | Data persistence layer documentation: file-based JSON configuration, in-memory cache strategy (TTL, eviction, threading), entity model ER diagram, and data classification/sensitivity analysis |
| [Configuration Inventory](./configuration-inventory.md) | Comprehensive inventory of all configuration sources, CLI options, runtime settings, ServerConfig properties, build profiles, secrets handling, and framework/runtime versions |
| [Business Workflows](./business-workflows.md) | Core business process documentation: torrent search aggregation, indexer configuration, health/error recovery, automatic updates, and startup initialization workflows with sequence diagrams |
