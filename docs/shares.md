# Share Inventory

A practical overview of the main storage shares and major data areas used across Homelab Steampunk.

> Primary app state area: `appdata`  
> Primary shared content area: `data`  
> Document-focused area: structured document management storage  
> Media, photos, backups, and VM-related paths are separated by role

---

# At a Glance

| Share / Area | Primary Role | Notes |
|:--|:--|:--|
| `appdata` | Container configs and persistent app state | Core operational data for most services |
| `data` | Shared service content | Main shared content area for media-related workflows |
| `storage` | Structured long-term content area | Supports broader organized storage workflows |
| `pictures` / `photos` | Photo and image storage | Supports Immich, PhotoPrism, and related media preservation |
| `Media` | Media-oriented content area | Used by media services and related workflows |
| `backups` | Backup storage | Supports operational backups and retained copies |
| `domains` | VM-related storage | Supports virtualization-related workflows |
| `nextcloud` | Nextcloud-related data area | Tied to the broader personal cloud platform |
| `seafile` | Seafile data | Alternate file collaboration and sync platform storage |
| `documents` | General document area | Supports broader document organization needs |
| `downloads` | Intake / download staging | Supports acquisition and temporary content movement |

---

# Core Share Roles

| Share / Area | Role | Why It Matters |
|:--|:--|:--|
| `appdata` | Application state | One of the most important storage areas in the homelab because it holds service configuration and persistent runtime state |
| `data` | Shared content layer | Connects automation, downloads, and library-style media workflows |
| `storage` | Structured long-term storage | Helps support cleaner organization outside a flat generic data model |
| `pictures` / `photos` | Photo preservation | Supports photo platforms and long-term personal media organization |
| `Media` | Media-focused storage | Supports the broader playback and acquisition ecosystem |
| `backups` | Recovery support | Important for resilience and retained copies of critical data |
| `domains` | Virtualization support | Part of the VM layer and guest storage model |

---

# Application State

`appdata` is the operational heart of the container stack.

It supports:

- service configuration
- dashboard settings
- reverse proxy state
- identity platform data
- AI service configuration
- media automation settings
- database persistence for multiple services

This area is one of the most important parts of the homelab to understand and protect.

---

# Shared Content

`data` acts as a major shared content layer across the homelab.

It is especially important for:

- media automation workflows
- downloads
- organized content movement
- shared access between acquisition and playback services

This is one of the key areas that turns the platform from isolated apps into a connected ecosystem.

---

# Document-Oriented Storage

The homelab uses more than one document-oriented area instead of treating all files as one undifferentiated pool.

Document-related storage supports:

- intake
- archive
- export
- long-term organization
- cloud-style file access
- alternate collaboration platforms

This is important for services such as:

- Paperless-NGX
- Paperless-AI
- Nextcloud
- Seafile
- PDF utility workflows

---

# Photo and Personal Media Storage

Photo-oriented areas support the move away from consumer cloud storage and into self-hosted preservation.

These areas matter for:

- Immich
- PhotoPrism
- personal media organization
- long-term preservation of photos and videos
- library growth over time

This is one of the more personal and high-value parts of the storage model.

---

# Backup and Recovery Areas

Backup-oriented areas support operational resilience.

These areas are important for:

- retained copies of important data
- recovery workflows
- safer maintenance
- platform continuity

As the homelab grows, backup-related organization becomes more important rather than less.

---

# VM and Platform Support Areas

Some shares support the virtualization and platform layer more directly.

These areas are useful for:

- VM disks
- guest-related assets
- platform-level workloads
- service areas tied to the broader Unraid host model

This reflects the fact that the homelab is hybrid, not container-only.

---

# Why This Matters

This share model provides:

- clearer functional separation
- easier troubleshooting
- a better mental model for storage
- better alignment between service role and data location
- cleaner long-term organization
- more understandable documentation

It helps make the homelab feel structured rather than improvised.

---

# Notes

Future additions could include:

- backup priority classification
- restore order notes
- appdata backup scope
- media share mapping
- document path mapping
- photo-library path mapping
