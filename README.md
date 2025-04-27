![SteamPunk Homelab](assets/cover.png)

# 🚀 SteamPunk Homelab

Welcome to my cyberpunk-themed homelab — a personal playground where learning, automation, and entertainment collide. This repository serves as documentation for the setup and the services running within it. Powered by Unraid, Docker, and secured through Traefik and Cloudflare Tunnels, this environment balances reliability with a spirit of experimentation.

> "It's not just a homelab — it's a lifestyle."

---

## 🛡️ Principles

-   All services run in **Docker containers**.
-   **Traefik** is used as the ingress controller and reverse proxy.
-   **Cloudflare Tunnel** securely exposes select apps without open ports.
-   **Unraid** provides simple, flexible storage management.
-   Monitoring, automation, and backup services run across **NVMe cache pools** and a robust **array** of HDDs.
-   Preference for **open-source** solutions wherever possible.
-   Secrets and sensitive configs are separated and minimized for security.

---

## 🛠️ Setup Overview

-   **Server:** AMD Ryzen 7 5800X - 8 cores / 16 threads
-   **Memory:** 96GB DDR4
-   **Storage:**
    -   2 × 4TB NVMe Cache Drives
    -   Mixed 16TB, 8TB, and 4TB HDD Array
-   **Virtualization:** AMD-V Enabled
-   **OS:** Unraid 6.12.x *(Please update with your current version)*

---

# 📦 Application Stack

**Note:** Please ensure you have downloaded the corresponding logos and placed them in the `assets` folder with matching filenames (e.g., `jellyfin.svg`, `emby.png`, `radarr.svg`).

### 🎬 Media Stack

| Logo                                              | Application   | Description                                    |
| :------------------------------------------------ | :------------ | :--------------------------------------------- |
| <img src="assets/jellyfin.svg" width="24" alt="Jellyfin logo"> | **Jellyfin** | Open-source personal media server.             |
| <img src="assets/emby.png" width="24" alt="Emby logo"> | **EmbyServer** | Media server with advanced metadata support. |
| <img src="assets/tautulli.png" width="24" alt="Tautulli logo"> | **Tautulli** | Monitoring for Plex/Emby activity.             |
| <img src="assets/radarr.svg" width="24" alt="Radarr logo"> | **Radarr** | Automated movie collection management.         |
| <img src="assets/sonarr.svg" width="24" alt="Sonarr logo"> | **Sonarr** | Automated TV show downloading & organization. |
| <img src="assets/overseerr.svg" width="24" alt="Overseerr logo"> | **Overseerr** | Request management system for media libraries. |
| <img src="assets/recyclarr.png" width="24" alt="Recyclarr logo"> | **Recyclarr** | Syncs Radarr/Sonarr quality profiles.       |

> 📌 **Why I chose Jellyfin:** Fully open-source, customizable clients, no license fees.

---

### 📊 Monitoring Stack

| Logo                                                | Application          | Description                                    |
| :-------------------------------------------------- | :------------------- | :--------------------------------------------- |
| <img src="assets/netdata.svg" width="24" alt="Netdata logo"> | **Netdata** | Real-time system monitoring and alerts.        |
| <img src="assets/glances.png" width="24" alt="Glances logo"> | **Glances** | Cross-platform system monitor.                 |
| <img src="assets/homepage.png" width="24" alt="Homepage logo"> | **Homepage** | Dashboard for organizing self-hosted services. |
| <img src="assets/dashy.png" width="24" alt="Dashy logo"> | **Dashy** | Dashboard focused on app links and widgets.    |
| <img src="assets/speedtest-tracker.svg" width="24" alt="Speedtest Tracker logo"> | **Speedtest Tracker** | Internet connection monitoring.             |

---

### 🧰 Utilities Stack

| Logo                                                        | Application           | Description                           |
| :---------------------------------------------------------- | :-------------------- | :------------------------------------ |
| <img src="assets/code-server.svg" width="24" alt="Code-Server logo"> | **Code-Server** | Web-based VSCode IDE.                 |
| <img src="assets/rustdesk.png" width="24" alt="RustDesk logo"> | **RustDesk Server** | Self-hosted remote desktop solution.  |
| <img src="assets/docker-socket-proxy.png" width="24" alt="Docker Socket Proxy logo"> | **Docker Socket Proxy** | Secure docker.sock access.            |

---

### ☁️ Cloud / Storage Stack

| Logo                                                | Application     | Description                                         |
| :-------------------------------------------------- | :-------------- | :-------------------------------------------------- |
| <img src="assets/nextcloud.svg" width="24" alt="Nextcloud logo"> | **Nextcloud AIO** | Personal cloud platform (storage, collaboration). |
| <img src="assets/immich.svg" width="24" alt="Immich logo"> | **Immich** | High-speed AI-powered photo backup service.         |
| <img src="assets/photoprism.svg" width="24" alt="PhotoPrism logo"> | **PhotoPrism** | Private photo management platform.                  |
| <img src="assets/syncthing.svg" width="24" alt="Syncthing logo"> | **Syncthing** | Decentralized peer-to-peer file sync.             |

---

### 🔒 Security Stack

| Logo                                                   | Application         | Description                                     |
| :----------------------------------------------------- | :------------------ | :---------------------------------------------- |
| <img src="assets/traefik.svg" width="24" alt="Traefik logo"> | **Traefik** | Dynamic reverse proxy with SSL support.         |
| <img src="assets/authentik.svg" width="24" alt="Authentik logo"> | **Authentik** | SSO and Identity provider.                      |
| <img src="assets/crowdsec.svg" width="24" alt="CrowdSec logo"> | **CrowdSec** | Collaborative IPS security tool.                |
| <img src="assets/pi-hole.svg" width="24" alt="Pi-hole logo"> | **Pi-hole** | DNS-level ad-blocker for the entire network.  |
| <img src="assets/unbound.svg" width="24" alt="Unbound logo"> | **Unbound** | Local DNS resolver.                             |
| <img src="assets/cloudflare.svg" width="24" alt="Cloudflare logo"> | **Cloudflare Tunnel** | Securely connects homelab to the public internet. |

> 📌 **Why I chose Traefik:** Automatic SSL, seamless Docker integration, flexibility.

---

### 🗄️ Database Stack

| Logo                                                  | Application   | Description                             |
| :---------------------------------------------------- | :------------ | :-------------------------------------- |
| <img src="assets/postgresql.svg" width="24" alt="PostgreSQL logo"> | **PostgreSQL** | Database for Authentik and Immich.      |
| <img src="assets/mariadb.svg" width="24" alt="MariaDB logo"> | **MariaDB** | Database for Nextcloud.                 |
| <img src="assets/redis.svg" width="24" alt="Redis logo"> | **Redis** | In-memory database and cache.           |

---

## 📈 Storage Architecture

*(Ensure assets/storage-map.png path is correct)*
![Storage Map](assets/storage-map.png)

---

## 🛡️ Docker Application Architecture

*(Ensure assets/docker-flow.png path is correct)*
![Docker Flow](assets/docker-flow.png)

---

## 🏅 Badges

![Docker Pulls](https://img.shields.io/docker/pulls/linuxserver/jellyfin) ![Uptime Robot Status](https://img.shields.io/uptimerobot/status/YOUR_MONITOR_ID) ![GitHub Last Commit](https://img.shields.io/github/last-commit/drtechnolust/homelab)
![GitHub Stars](https://img.shields.io/github/stars/drtechnolust/homelab?style=social)

---

## 📜 License

*(Consider adding a LICENSE file to your repository)*

This project's documentation (README, diagrams) is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Any included configuration examples or code snippets are licensed under the [MIT License](https://opensource.org/licenses/MIT) unless otherwise specified.

---

## 📝 Notes

This homelab is an evolving ecosystem — balancing real-world production practices with a passion for learning, self-hosting, and automation at home.

---
