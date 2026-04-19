# Architecture

Homelab Steampunk is a multi-role self-hosted platform built on Unraid, combining containerized services, virtual machines, structured storage, identity-aware access, reverse proxying, and selective external publishing.

The environment is designed to support real daily-use services while still leaving room for experimentation, testing, and platform evolution.

---

## Core Platform

### Unraid Host
The homelab runs on Unraid as the primary infrastructure platform. Unraid provides the foundation for:
- Docker container hosting
- KVM/QEMU virtualization
- array and cache-based storage management
- share-based application and data organization
- operational access through the Unraid management layer

### Container Layer
Most services run as Docker containers. This allows:
- modular deployment
- easier maintenance and rollback
- flexible networking models
- workload separation by function
- simpler service expansion over time

### Virtualization Layer
In addition to containers, the platform uses VMs for workloads that benefit from full operating system isolation, specialty applications, testing, or desktop-like behavior.

Running and offline virtual machines are part of the broader architecture, making this a hybrid container-and-VM homelab rather than a Docker-only system.

---

## Architectural Domains

The platform is organized into several major service domains.

### Media & Automation
This domain handles acquisition, organization, requests, subtitles, playback, and watch-state synchronization.

The media stack is intentionally segmented across multiple Sonarr and Radarr instances to separate general, anime, and kids-focused workflows. This keeps libraries cleaner, supports more specialized automation behavior, and allows safer content boundaries across different media types.

Key services include:
- Jellyfin
- Emby
- Sonarr
- Sonarr Anime
- Sonarr Kids
- Radarr
- Radarr Anime
- Radarr Kids
- Lidarr
- Bazarr
- Prowlarr
- Overseerr
- SABnzbd
- qBittorrentVPN
- Unpackerr
- Autoscan
- Watchstate

### Documents & Content
This domain supports cloud-style file access, document ingestion, search, PDF workflows, and long-term archive management.

Key services include:
- Nextcloud AIO
- Collabora
- Talk
- Whiteboard
- Full Text Search
- Paperless-NGX
- Paperless-AI
- Apache Tika
- Gotenberg
- Seafile
- Stirling-PDF

### AI & Voice
This domain supports local inference, AI-assisted workflows, and voice-related services.

Key services include:
- Ollama
- Open WebUI
- faster-whisper
- Piper
- openWakeWord

### Security & Access
This domain is responsible for routing, identity, filtering, and selective service protection.

Key services include:
- Traefik
- Authentik
- CrowdSec
- CrowdSec Traefik Bouncer
- Pi-hole
- Unbound
- Cloudflare Tunnel

### Monitoring & Operations
This domain provides visibility into service state, uptime, resource usage, and administration.

Key services include:
- Homepage
- Dashy
- Netdata
- Glances
- Uptime Kuma
- Unraid API
- GoAccess

### Photos, Cameras & Smart Home
This domain handles photo management, NVR workflows, and smart home automation.

Key services include:
- Immich
- PhotoPrism
- Frigate
- Home Assistant
- HomeAssistant_inabox

---

## Network Architecture

The homelab uses multiple network models instead of placing everything into one flat network.

### `steampunknet`
This is the primary custom Docker network and hosts most of the main service stack.  
It acts as the central application network for inter-service communication and reverse proxy relationships.

### `nextcloud-aio`
A dedicated application network used by the Nextcloud AIO stack to keep its components grouped and isolated.

### `seafile-net`
A dedicated service network used for Seafile and its supporting database layer.

### `br0`
Used for services that benefit from direct LAN presence, including DNS-related workloads such as Pi-hole and Unbound.

### `host`
Used for select services that require host-level visibility or tighter host integration.

### `bridge`
Used selectively for containers where the default Docker bridge remains sufficient.

---

## Ingress & Access Flow

Access to services is intentionally mixed based on function, exposure level, and operational need.

### Internal Access
Many services are accessible internally through direct ports for administrative convenience, testing, or local-only usage.

### Reverse Proxy Access
Traefik acts as the primary reverse proxy for selected services, handling routing, HTTPS entrypoints, and middleware integration.

### Identity-Aware Protection
Authentik is used to support centralized authentication and protected access flows for selected applications.

### Selective External Publishing
Cloudflare Tunnel is used to expose chosen services without broadly opening inbound ports in a traditional way.

### DNS & Filtering
Pi-hole and Unbound provide local DNS filtering and recursive resolution support as part of the internal network control model.

---

## Storage Architecture Overview

Storage is organized by workload rather than treated as one generic pool.

### Appdata
Container configs and persistent application state are primarily stored under:
- `/mnt/user/appdata`

### General Data
Shared content for media automation and related services is primarily organized under:
- `/mnt/user/data`

### Document Workflows
Structured document-management paths are used for ingestion, archive, and export workflows.

### Photo / Media Libraries
Photo and image libraries are maintained separately to support platforms like Immich and PhotoPrism.

### VM / High-Performance Paths
Some workloads use dedicated NVMe-backed or performance-sensitive paths, including VM-related storage and selected application data.

---

## Hybrid Platform Model

A defining characteristic of this homelab is that it is not purely a media server, not purely a document server, and not purely a lab sandbox.

It is instead a hybrid platform that combines:
- always-on infrastructure services
- media automation and streaming
- personal cloud and document systems
- AI experimentation
- smart home and camera services
- VM-based testing and specialty workflows

That hybrid approach is what makes the environment flexible, but also what makes documentation important.

---

## Current Design Direction

The platform is being continuously refined with a focus on:
- clearer separation between live and legacy workloads
- tighter documentation of what is actually running
- better visibility into access paths and dependencies
- improved consistency between README presentation and real infrastructure state

As the repo evolves, this page serves as the architectural overview that connects all other documentation.
