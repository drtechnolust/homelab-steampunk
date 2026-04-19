# 🎬 Media Stack

A segmented media automation and delivery platform built around shared libraries, separate acquisition workflows, controlled remote access, and dual playback platforms.

> **Primary platform:** Emby  
> **Secondary platform:** Jellyfin  
> **Remote access:** Tailscale only  
> **Public exposure:** None

---

# 🧭 Media Stack Snapshot

| Area | Current Design |
|:--|:--|
| Primary playback platform | Emby |
| Secondary playback platform | Jellyfin |
| Shared libraries | Yes |
| Public media exposure | None |
| Remote access outside home | Tailscale only |
| Automation model | Segmented Sonarr/Radarr instances |
| Discovery model | Import lists + requests |
| Standards influence | Trash Guides |
| Retired platform | Plex |

---

# 🏗️ Platform Layout

| Platform | Role | Notes |
|:--|:--|:--|
| Emby | Primary playback platform | Main day-to-day media experience |
| Jellyfin | Secondary playback platform | Alternate FOSS-first interface using the same libraries |
| Plex | Retired | No longer used due to platform direction, ads, and preference for more self-hosted-first options |

Emby and Jellyfin point to the same underlying media libraries, allowing both platforms to operate against the same content base without maintaining separate collections.

---

# 🧩 Segmented Automation Design

The automation layer is intentionally split to keep workflows cleaner, more targeted, and easier to maintain.

| Service Group | Purpose |
|:--|:--|
| Sonarr | General TV workflows |
| Sonarr Anime | Anime-focused TV workflows |
| Sonarr Kids | Kids-focused TV workflows |
| Radarr | General movie workflows |
| Radarr Anime | Anime movie workflows |
| Radarr Kids | Kids movie workflows |
| Lidarr | Music workflows |

This separation improves:

- cleaner library hygiene
- safer content boundaries
- more specialized anime handling
- simpler long-term maintenance
- less clutter in automation logic

---

# 📥 Import Lists & Automated Discovery

Import lists are a meaningful part of the media workflow and help reduce manual adds.

They are used for things like:

- streaming TV discovery
- Trakt-based imports
- anime-focused lists
- curated movie-user lists
- specialty collection lists
- themed imports such as Studio Ghibli

Trash Guides is also an important influence here, especially for keeping media automation more standardized, maintainable, and aligned with cleaner long-term practices.

---

# ⚙️ Supporting Services

| Service | Function |
|:--|:--|
| Prowlarr | Indexer aggregation and management |
| Bazarr | Subtitle workflows |
| Overseerr | Request workflow feeding Jellyfin |
| qBittorrentVPN | Torrent-based downloads |
| SABnzbd | Usenet downloads |
| Unpackerr | Archive extraction |
| Autoscan | Faster library refresh |
| Watchstate | Playback-state continuity |

---

# 🔐 Access Model

> Nothing in the media stack is exposed directly to the internet.

Media access is designed around:

- internal home access
- private remote access through Tailscale
- no public-facing media endpoints

This keeps the stack aligned with the broader self-hosted security model while still making remote use practical.

---

# 🔄 Workflow Overview

```text
Import Lists / Requests
          ↓
 Sonarr / Radarr / Lidarr
          ↓
 qBittorrentVPN / SABnzbd
          ↓
  Unpackerr / Autoscan
          ↓
   Shared Media Libraries
          ↓
 Emby (Primary) / Jellyfin (Secondary)
