# Storage Architecture

Homelab Steampunk uses a workload-based storage model rather than treating all storage the same. Different classes of data are placed according to performance, persistence, growth behavior, and operational importance.

The result is a storage design that supports always-on applications, large media libraries, document workflows, photo management, and virtual machines within the same platform.

---

# Storage Philosophy

The storage model is built around a few core ideas:

- Place high-churn application data where performance matters
- Keep large long-term datasets organized by function
- Separate application state from user content where practical
- Use structured paths for document and media workflows
- Support both containerized services and VM-based workloads
- Keep the layout understandable enough to maintain over time

---

# Primary Storage Tiers

## Cache Layer

The cache layer is used for performance-sensitive workloads and fast-access application data.

Typical use cases include:
- appdata
- active service configuration
- selected working data
- temporary or staging workflows
- cache-backed shares for faster reads and writes

This layer is important for responsiveness across the homelab and helps reduce unnecessary pressure on slower long-term storage.

## Array Layer

The Unraid array acts as the large-capacity persistent storage layer.

Typical use cases include:
- media libraries
- long-term document storage
- bulk data
- archival content
- general share-based storage

This layer provides the scale needed for a multi-role homelab with large media, document, and personal data footprints.

## NVMe / High-Performance Paths

Some workloads benefit from dedicated higher-performance storage outside the general array pattern.

Typical use cases include:
- virtual machine storage
- selected application data
- Nextcloud-related data placement
- other workloads that benefit from lower latency and better throughput

This tier supports the hybrid nature of the homelab by giving selected services faster storage when needed.

---

# Major Storage Areas

## Appdata

Application configuration and persistent container state are primarily stored under:

`/mnt/user/appdata`

This area is one of the most important parts of the environment because it contains:
- service configs
- database persistence
- dashboard settings
- reverse proxy configuration
- identity platform state
- AI service config
- media automation settings

Appdata is effectively the operational heart of the container stack.

## General Data

Shared service data is heavily organized around:

`/mnt/user/data`

This area supports:
- media automation
- downloads
- organized library paths
- content consumed by multiple services

It acts as a shared operational content layer for much of the media stack.

## Document Management Storage

Document workflows use structured storage rather than a single undifferentiated folder.

This includes paths dedicated to:
- document ingestion
- archive storage
- export workflows
- long-term document organization

This structure is especially important for services such as:
- Paperless-NGX
- Paperless-AI
- Nextcloud
- Seafile
- PDF processing tools

## Photo and Image Storage

Photo and image workflows are separated to support different platforms and organizational needs.

This helps support:
- Immich
- PhotoPrism
- family photo storage
- image import workflows
- broader media preservation

Because photo platforms can have different strengths, separating these paths helps keep the environment flexible.

## VM and Specialty Storage

Virtual machines and certain performance-sensitive services use their own storage strategy.

This supports:
- VM disks
- boot images
- specialized guest workloads
- services that benefit from faster dedicated storage

This tier is a key part of the hybrid VM + container design.

---

# Workload-Based Storage Patterns

## Media Workloads

Media services benefit from:
- large-capacity storage
- organized share structure
- separation between downloads and final libraries
- shared access across automation and streaming services

This is why the media stack is closely tied to structured content paths rather than isolated single-service storage.

## Document Workloads

Document services benefit from:
- structured intake paths
- archive destinations
- export locations
- clear separation between application logic and content storage

This is especially useful for OCR, AI-assisted enrichment, and long-term archival workflows.

## Photo Workloads

Photo platforms benefit from:
- dedicated import paths
- persistent library storage
- separation from generic downloads and bulk media
- room for long-term growth

## Application State Workloads

Core service state benefits from:
- faster storage
- predictable backup scope
- clean separation from user-generated content
- easier maintenance and restore operations

---

# Practical Design Benefits

This storage model provides several advantages:

- better performance for active services
- clearer separation between config and content
- easier mental model for troubleshooting
- better support for multiple service domains
- flexibility for both containers and VMs
- cleaner future documentation and inventory tracking

---

# Current Considerations

The environment is large enough that storage planning matters.

Areas that deserve ongoing attention include:
- overall array utilization
- growth of appdata over time
- document archive expansion
- media library growth
- photo library growth
- deciding which workloads belong on cache, array, or higher-performance paths

As the homelab evolves, storage placement should continue to be reviewed based on growth, performance, and operational simplicity.

---

# Documentation Direction

This page is intended to describe the storage model at a high level.

More detailed documentation can later be added for:
- backup strategy
- appdata backup scope
- VM storage layout
- media share organization
- document management paths
- photo library structure
- restore priorities

The goal is to document storage clearly enough to understand the platform without exposing unnecessary operational detail publicly.
