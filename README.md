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
| ![Jellyfin](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/jellyfin.svg) | **Jellyfin** | Open-source personal media server. |
| ![Emby](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/emby.svg) | **EmbyServer** | Media server with advanced metadata support. |
| ![Tautulli](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/plex.svg) | **Tautulli** | Monitoring for Plex/Emby activity. |
| ![Radarr](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/radarr.svg) | **Radarr** | Automated movie collection management. |
| ![Sonarr](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/sonarr.svg) | **Sonarr** | Automated TV show downloading and organization. |
| ![Overseerr](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/plex.svg) | **Overseerr** | Request management system for media libraries. |
| ![Recyclarr](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/plex.svg) | **Recyclarr** | Syncs Radarr/Sonarr quality profiles automatically. |

> 📌 **Why I chose Jellyfin:** Fully open-source, customizable clients, no license fees.

---

### 📊 Monitoring Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Netdata](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/netdata.svg) | **Netdata** | Real-time system monitoring and alerts. |
| ![Glances](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/glances.svg) | **Glances** | Cross-platform system monitor. |
| ![Homepage](https://raw.githubusercontent.com/gethomepage/homepage/main/public/logo.png) | **Homepage** | Dashboard for organizing self-hosted services. |
| ![Dashy](https://raw.githubusercontent.com/Lissy93/dashy/main/public/icon.png) | **Dashy** | Dashboard focused on app links and widgets. |
| ![Speedtest Tracker](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/speedtest.svg) | **Speedtest Tracker** | Internet connection monitoring. |

---

### 🧰 Utilities Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Code-Server](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/visualstudiocode.svg) | **Code-Server** | Web-based VSCode IDE. |
| ![RustDesk](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/rustdesk.svg) | **RustDesk Server** | Self-hosted remote desktop solution. |
| ![Docker Socket Proxy](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/docker.svg) | **Docker Socket Proxy** | Secure docker.sock access. |

---

### ☁️ Cloud / Storage Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Nextcloud](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/nextcloud.svg) | **Nextcloud AIO** | Personal cloud platform for storage, collaboration, and backup. |
| ![Immich](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/immich.svg) | **Immich** | High-speed AI-powered photo backup service. |
| ![PhotoPrism](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/photoprism.svg) | **PhotoPrism** | Private photo management platform. |
| ![Syncthing](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/syncthing.svg) | **Syncthing** | Decentralized peer-to-peer file sync. |

---

### 🔒 Security Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![Traefik](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/traefik.svg) | **Traefik** | Dynamic reverse proxy with SSL support. |
| ![Authentik](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/authentik.svg) | **Authentik** | SSO and Identity provider. |
| ![CrowdSec](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/crowdsec.svg) | **CrowdSec** | Collaborative IPS security tool. |
| ![Pi-hole](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/pihole.svg) | **Pi-hole** | DNS-level ad-blocker for the entire network. |
| ![Unbound](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/unbound.svg) | **Unbound** | Local DNS resolver. |
| ![Cloudflare Tunnel](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/cloudflare.svg) | **Cloudflare Tunnel** | Securely connects homelab services to the public internet. |

> 📌 **Why I chose Traefik:** Automatic SSL, seamless Docker integration, flexibility.

---

### 🗄️ Database Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| ![PostgreSQL](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/postgresql.svg) | **PostgreSQL** | Database for Authentik and Immich. |
| ![MariaDB](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/mariadb.svg) | **MariaDB** | Database for Nextcloud. |
| ![Redis](https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/redis.svg) | **Redis** | In-memory database and cache. |

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
