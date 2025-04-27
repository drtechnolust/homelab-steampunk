![SteamPunk Homelab](assets/cover.png)

# 🚀 SteamPunk Homelab

Welcome to my cyberpunk-themed homelab — a playground where learning, automation, and entertainment collide.  
Powered by Unraid, Docker, and secured through Traefik and Cloudflare Tunnels, this environment balances serious production reliability with a spirit of experimentation.

> "It's not just a homelab — it's a lifestyle."

---

## 🛡️ Principles

- All services run in **Docker containers**.
- **Traefik** is used as the ingress controller and reverse proxy.
- **Cloudflare Tunnel** securely exposes select apps without open ports.
- **Unraid** provides simple, flexible storage management.
- Monitoring, automation, and backup services run across **NVMe cache pools** and a robust **array** of HDDs.
- Preference for **open-source** solutions wherever possible.
- Secrets and sensitive configs are separated and minimized for security.

---

## 🛠️ Setup Overview

- **Server:** AMD Ryzen 7 5800X - 8 cores / 16 threads
- **Memory:** 96GB DDR4
- **Storage:**
  - 2 × 4TB NVMe Cache Drives
  - Mixed 16TB, 8TB, and 4TB HDD Array
- **Virtualization:** AMD-V Enabled
- **OS:** Unraid 6.6.78

---

# 📦 Application Stack

### 🎬 Media Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Jellyfin](assets/jellyfin.png) | **Jellyfin** | Open-source personal media server. |
| ![Emby](assets/emby.png) | **EmbyServer** | Media server with advanced metadata support. |
| ![Tautulli](assets/tautulli.png) | **Tautulli** | Monitoring for Plex/Emby activity. |
| ![Radarr](assets/radarr.png) | **Radarr** | Automated movie collection management. |
| ![Sonarr](assets/sonarr.png) | **Sonarr** | Automated TV show downloading and organization. |
| ![Overseerr](assets/overseerr.png) | **Overseerr** | Request management system for media libraries. |
| ![Recyclarr](assets/recyclarr.png) | **Recyclarr** | Syncs Radarr/Sonarr quality profiles automatically. |

---

### 📊 Monitoring Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Netdata](assets/netdata.png) | **Netdata** | Real-time system monitoring and alerts. |
| ![Glances](assets/glances.png) | **Glances** | Cross-platform system monitor. |
| ![Homepage](assets/homepage.png) | **Homepage** | Dashboard for organizing self-hosted services. |
| ![Dashy](assets/dashy.png) | **Dashy** | Dashboard focused on app links and widgets. |
| ![Speedtest Tracker](assets/speedtest.png) | **Speedtest Tracker** | Internet connection monitoring. |

---

### 🧰 Utilities Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Code-Server](assets/code-server.png) | **Code-Server** | Web-based VSCode IDE. |
| ![RustDesk](assets/rustdesk.png) | **RustDesk Server** | Self-hosted remote desktop solution. |
| ![Docker Socket Proxy](assets/docker.png) | **Docker Socket Proxy** | Secure docker.sock access. |

---

### ☁️ Cloud / Storage Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Nextcloud](assets/nextcloud.png) | **Nextcloud AIO** | Personal cloud platform for storage, collaboration, and backup. |
| ![Immich](assets/immich.png) | **Immich** | High-speed AI-powered photo backup service. |
| ![PhotoPrism](assets/photoprism.png) | **PhotoPrism** | Private photo management platform. |
| ![Syncthing](assets/syncthing.png) | **Syncthing** | Decentralized peer-to-peer file sync. |

---

### 🔒 Security Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Traefik](assets/traefik.svg) | **Traefik** | Dynamic reverse proxy with SSL support. |
| ![Authentik](assets/authentik.png) | **Authentik** | SSO and Identity provider. |
| ![CrowdSec](assets/crowdsec.png) | **CrowdSec** | Collaborative IPS security tool. |
| ![Pi-hole](assets/pihole.png) | **Pi-hole** | DNS-level ad-blocker for the entire network. |
| ![Unbound](assets/unbound.png) | **Unbound** | Local DNS resolver. |
| ![Cloudflare Tunnel](assets/cloudflare.png) | **Cloudflare Tunnel** | Securely connects homelab services to the public internet. |

---

### 🗄️ Database Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![PostgreSQL](assets/postgresql.png) | **PostgreSQL** | Database for Authentik and Immich. |
| ![MariaDB](assets/mariadb.png) | **MariaDB** | Database for Nextcloud. |
| ![Redis](assets/redis.png) | **Redis** | In-memory database and cache. |

---

# 📈 Storage Architecture

![Storage Map](assets/storage-map.png)

---

# 🛡️ Docker Application Architecture

![Docker Flow](assets/docker-flow.png)

---

# 🏅 Badges

![Docker Pulls](https://img.shields.io/docker/pulls/linuxserver/plex)  
![Uptime Robot](https://img.shields.io/uptimerobot/ratio/m788597361-XXXXXXXXXXXXX)  
![GitHub Last Commit](https://img.shields.io/github/last-commit/drtechnolust/homelab)  
![GitHub Stars](https://img.shields.io/github/stars/drtechnolust/homelab?style=social)

---

# 📝 Notes

This homelab is an evolving ecosystem — balancing real-world production practices with a passion for learning, self-hosting, and automation at home.

---
