# Nextcloud Stack

A self-hosted cloud and collaboration platform built around file access, synchronized storage, document collaboration, search, and integrated app services.

> Core platform: Nextcloud AIO  
> Collaboration layer: Collabora, Talk, Whiteboard  
> Search layer: Full Text Search  
> Role in homelab: primary personal cloud and file collaboration platform

---

# At a Glance

| Area | Design |
|:--|:--|
| Core platform | Nextcloud AIO |
| Main purpose | Personal cloud, sync, collaboration, document access |
| Web layer | AIO Apache |
| Office editing | Collabora |
| Communication | Talk |
| Whiteboarding | Whiteboard |
| Search | Full Text Search |
| Storage model | Dedicated Nextcloud-related data paths |
| Broader role | Central file and collaboration service |

---

# Stack Layout

| Component | Role | Notes |
|:--|:--|:--|
| Nextcloud AIO Master | Stack management | Controls and orchestrates the AIO deployment |
| Nextcloud AIO Apache | Web entry layer | Front-end access point for the stack |
| Nextcloud AIO Nextcloud | Core application | Main file, sync, and app platform |
| Nextcloud Talk | Communication | Real-time chat and collaboration layer |
| Nextcloud Collabora | Office editing | Browser-based document editing |
| Nextcloud Whiteboard | Visual collaboration | Shared whiteboarding workflows |
| Nextcloud Full Text Search | Search enhancement | Improves document and content retrieval |
| Nextcloud Redis | Cache / support service | Supports responsiveness and session-related behavior |
| Nextcloud Database | Persistence | Database backend for the stack |

---

# Design Intent

This stack exists to provide more than just file storage.

It is designed to support:

- personal cloud workflows
- synchronized file access
- browser-based collaboration
- document editing
- communication features
- searchable content
- broader integration with the rest of the homelab

The goal is to make file access and collaboration feel like a cohesive platform rather than a loose collection of shares.

---

# Core Platform Role

Nextcloud is one of the central user-facing platforms in the homelab.

Its role includes:

- file access across devices
- personal cloud-style storage
- collaboration support
- structured document access
- acting as part of the broader document ecosystem
- complementing Paperless and Seafile rather than fully replacing them

This gives the homelab a true cloud-and-collaboration layer.

---

# Collaboration Features

| Feature | Purpose |
|:--|:--|
| Collabora | In-browser office document editing |
| Talk | Communication and collaboration workflows |
| Whiteboard | Shared visual planning and collaboration |
| Full Text Search | Better retrieval across stored content |

These features move the stack beyond basic sync and storage into a more complete collaboration environment.

---

# Relationship to Other Document Services

The Nextcloud stack is part of a broader document and file ecosystem.

| Service | Relationship |
|:--|:--|
| Paperless-NGX | More archive and document-management focused |
| Paperless-AI | Adds enrichment to document workflows |
| Seafile | Alternate file collaboration and sync platform |
| Stirling-PDF / Gotenberg / Tika | Utility and processing support for broader document workflows |

This means Nextcloud is not the only document-related platform in the homelab, but it is one of the most central ones.

---

# Storage and Data Role

The Nextcloud stack uses a more deliberate storage strategy than a simple generic app deployment.

Its role in storage includes:

- managing user-facing file access
- supporting dedicated data placement
- separating core app state from broader stored content
- integrating into the homelab’s structured storage model

That makes it one of the more important storage-connected services in the environment.

---

# Access Model

Nextcloud is designed as a core platform service, not just an internal utility.

Its access model is built around:

- stable browser access
- controlled publishing through the broader access layer
- integration with reverse proxy and security controls
- positioning as a primary cloud platform inside the homelab

This makes it more central than many of the purely internal tools.

---

# Workflow View

```text
User Files / Synced Content
            ↓
       Nextcloud Core
            ↓
 Collabora / Talk / Whiteboard
            ↓
   Search / Retrieval / Sharing
            ↓
 Broader Document and Cloud Workflows
