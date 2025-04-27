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
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/jellyfin.svg" alt="Jellyfin" width="24" /> | **Jellyfin** | Open-source personal media server. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/emby.svg" alt="Emby" width="24" /> | **EmbyServer** | Media server with advanced metadata support. |
| <img src="https://raw.githubusercontent.com/Tautulli/Tautulli/master/data/interfaces/default/images/logo.png" alt="Tautulli" width="24" /> | **Tautulli** | Monitoring for Plex/Emby activity. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/radarr.svg" alt="Radarr" width="24" /> | **Radarr** | Automated movie collection management. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/sonarr.svg" alt="Sonarr" width="24" /> | **Sonarr** | Automated TV show downloading and organization. |
| <img src="https://raw.githubusercontent.com/sct/overseerr/develop/public/logo_full.svg" alt="Overseerr" width="24" /> | **Overseerr** | Request management system for media libraries. |
| <img src="https://raw.githubusercontent.com/Recyclarr/recyclarr/develop/src/assets/logo/recyclarr.svg" alt="Recyclarr" width="24" /> | **Recyclarr** | Syncs Radarr/Sonarr quality profiles automatically. |

> 📌 **Why I chose Jellyfin:** Fully open-source, customizable clients, no license fees.

---

### 📊 Monitoring Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/netdata.svg" alt="Netdata" width="24" /> | **Netdata** | Real-time system monitoring and alerts. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/glances.svg" alt="Glances" width="24" /> | **Glances** | Cross-platform system monitor. |
| <img src="https://raw.githubusercontent.com/gethomepage/homepage/main/public/logo.png" alt="Homepage" width="24" /> | **Homepage** | Dashboard for organizing self-hosted services. |
| <img src="https://raw.githubusercontent.com/Lissy93/dashy/main/public/icon.png" alt="Dashy" width="24" /> | **Dashy** | Dashboard focused on app links and widgets. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/speedtest.svg" alt="Speedtest Tracker" width="24" /> | **Speedtest Tracker** | Internet connection monitoring. |

---

### 🧰 Utilities Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/visualstudiocode.svg" alt="Code-Server" width="24" /> | **Code-Server** | Web-based VSCode IDE. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/rustdesk.svg" alt="RustDesk Server" width="24" /> | **RustDesk Server** | Self-hosted remote desktop solution. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/docker.svg" alt="Docker Socket Proxy" width="24" /> | **Docker Socket Proxy** | Secure docker.sock access. |

---

### ☁️ Cloud / Storage Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/nextcloud.svg" alt="Nextcloud" width="24" /> | **Nextcloud AIO** | Personal cloud platform for storage, collaboration, and backup. |
| <img src="https://raw.githubusercontent.com/immich-app/immich/main/apps/website/public/logo-color.png" alt="Immich" width="24" /> | **Immich** | High-speed AI-powered photo backup service. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/photoprism.svg" alt="PhotoPrism" width="24" /> | **PhotoPrism** | Private photo management platform. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/syncthing.svg" alt="Syncthing" width="24" /> | **Syncthing** | Decentralized peer-to-peer file sync. |

---

### 🔒 Security Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/traefik.svg" alt="Traefik" width="24" /> | **Traefik** | Dynamic reverse proxy with SSL support. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/authentik.svg" alt="Authentik" width="24" /> | **Authentik** | SSO and Identity provider. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/crowdsec.svg" alt="CrowdSec" width="24" /> | **CrowdSec** | Collaborative IPS security tool. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/pihole.svg" alt="Pi-hole" width="24" /> | **Pi-hole** | DNS-level ad-blocker for the entire network. |
| <img src="https://www.nlnetlabs.nl/logo/nlnetlabs_logo_color.svg" alt="Unbound" width="24" /> | **Unbound** | Local DNS resolver. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/cloudflare.svg" alt="Cloudflare Tunnel" width="24" /> | **Cloudflare Tunnel** | Securely connects homelab services to the public internet. |

> 📌 **Why I chose Traefik:** Automatic SSL, seamless Docker integration, flexibility.

---

### 🗄️ Database Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/postgresql.svg" alt="PostgreSQL" width="24" /> | **PostgreSQL** | Database for Authentik and Immich. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/mariadb.svg" alt="MariaDB" width="24" /> | **MariaDB** | Database for Nextcloud. |
| <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/redis.svg" alt="Redis" width="24" /> | **Redis** | In-memory database and cache. |

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
