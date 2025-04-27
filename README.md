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

### 🎬 Media Stack

| Logo                                                                                                | Application   | Description                                    |
| :-------------------------------------------------------------------------------------------------- | :------------ | :--------------------------------------------- |
| <img src="https://cdn.worldvectorlogo.com/logos/jellyfin.svg" width="24" alt="Jellyfin logo">        | **Jellyfin** | Open-source personal media server.             |
| <img src="https://raw.githubusercontent.com/Jackett/Jackett/master/src/Jackett.Server/Content/Images/favicon.ico" width="24" alt="Emby logo"> | **EmbyServer** | Media server with advanced metadata support. (Note: Using Jackett Icon as placeholder, official Emby icon hard to find small/free) |
| <img src="https://raw.githubusercontent.com/Tautulli/Tautulli/master/data/interfaces/default/images/logo-plex-lg.png" width="24" alt="Tautulli logo"> | **Tautulli** | Monitoring for Plex/Emby activity. |
| <img src="https://raw.githubusercontent.com/Radarr/Radarr/develop/Logo/48.png" width="24" alt="Radarr logo"> | **Radarr** | Automated movie collection management.         |
| <img src="https://raw.githubusercontent.com/Sonarr/Sonarr/develop/Logo/48.png" width="24" alt="Sonarr logo"> | **Sonarr** | Automated TV show downloading & organization. |
| <img src="https://raw.githubusercontent.com/sct/overseerr/develop/public/logo.svg" width="24" alt="Overseerr logo"> | **Overseerr** | Request management system for media libraries. |
| <img src="https://raw.githubusercontent.com/recyclarr/recyclarr/master/images/recyclarr.png" width="24" alt="Recyclarr logo"> | **Recyclarr** | Syncs Radarr/Sonarr quality profiles.       |

> 📌 **Why I chose Jellyfin:** Fully open-source, customizable clients, no license fees.

---

### 📊 Monitoring Stack

| Logo                                                                                                   | Application          | Description                                    |
| :----------------------------------------------------------------------------------------------------- | :------------------- | :--------------------------------------------- |
| <img src="https://cdn.worldvectorlogo.com/logos/netdata.svg" width="24" alt="Netdata logo">             | **Netdata** | Real-time system monitoring and alerts.        |
| <img src="https://raw.githubusercontent.com/nicolargo/glances/master/docs/images/glances-logo-docs.png" width="24" alt="Glances logo"> | **Glances** | Cross-platform system monitor.                 |
| <img src="https://raw.githubusercontent.com/gethomepage/homepage/main/public/logo.png" width="24" alt="Homepage logo"> | **Homepage** | Dashboard for organizing self-hosted services. |
| <img src="https://raw.githubusercontent.com/Lissy93/dashy/master/public/favicon.ico" width="24" alt="Dashy logo"> | **Dashy** | Dashboard focused on app links and widgets.    |
| <img src="https://raw.githubusercontent.com/alexjustesen/speedtest-tracker/main/public/img/logo.svg" width="24" alt="Speedtest Tracker logo"> | **Speedtest Tracker** | Internet connection monitoring.             |

---

### 🧰 Utilities Stack

| Logo                                                                                                              | Application           | Description                           |
| :---------------------------------------------------------------------------------------------------------------- | :-------------------- | :------------------------------------ |
| <img src="https://raw.githubusercontent.com/coder/code-server/main/docs/assets/logo-128.png" width="24" alt="Code-Server logo"> | **Code-Server** | Web-based VSCode IDE.                 |
| <img src="https://rustdesk.com/images/rustdesk_logo.png" width="24" alt="RustDesk logo">                           | **RustDesk Server** | Self-hosted remote desktop solution.  |
| <img src="https://raw.githubusercontent.com/Tecnativa/docker-socket-proxy/develop/logo/docker-socket-proxy.png" width="24" alt="Docker Socket Proxy logo"> | **Docker Socket Proxy** | Secure docker.sock access.            |

---

### ☁️ Cloud / Storage Stack

| Logo                                                                                                     | Application   | Description                                         |
| :------------------------------------------------------------------------------------------------------- | :------------ | :-------------------------------------------------- |
| <img src="https://cdn.worldvectorlogo.com/logos/nextcloud-2.svg" width="24" alt="Nextcloud logo">          | **Nextcloud AIO** | Personal cloud platform (storage, collaboration). |
| <img src="https://immich.app/img/logo.svg" width="24" alt="Immich logo">                                  | **Immich** | High-speed AI-powered photo backup service.         |
| <img src="https://docs.photoprism.app/assets/images/logo.svg" width="24" alt="PhotoPrism logo">            | **PhotoPrism** | Private photo management platform.                  |
| <img src="https://syncthing.net/images/logo-horizontal.svg" width="24" alt="Syncthing logo">               | **Syncthing** | Decentralized peer-to-peer file sync.             |

---

### 🔒 Security Stack

| Logo                                                                                                     | Application         | Description                                     |
| :------------------------------------------------------------------------------------------------------- | :------------------ | :---------------------------------------------- |
| <img src="https://cdn.worldvectorlogo.com/logos/traefik-proxy.svg" width="24" alt="Traefik logo">          | **Traefik** | Dynamic reverse proxy with SSL support.         |
| <img src="https://goauthentik.io/img/icon.svg" width="24" alt="Authentik logo">                           | **Authentik** | SSO and Identity provider.                      |
| <img src="https://www.crowdsec.net/images/crowdsec_logo.svg" width="24" alt="CrowdSec logo">               | **CrowdSec** | Collaborative IPS security tool.                |
| <img src="https://pi-hole.net/wp-content/uploads/2016/12/pihole-logo-horizontal-150x50.png" width="24" alt="Pi-hole logo"> | **Pi-hole** | DNS-level ad-blocker for the entire network.  |
| <img src="https://nlnetlabs.nl/static/logos/Unbound/unbound-logo.svg" width="24" alt="Unbound logo">       | **Unbound** | Local DNS resolver.                             |
| <img src="https://cdn.worldvectorlogo.com/logos/cloudflare-1.svg" width="24" alt="Cloudflare logo">       | **Cloudflare Tunnel** | Securely connects homelab to the public internet. |

> 📌 **Why I chose Traefik:** Automatic SSL, seamless Docker integration, flexibility.

---

### 🗄️ Database Stack

| Logo                                                                                                     | Application   | Description                             |
| :------------------------------------------------------------------------------------------------------- | :------------ | :-------------------------------------- |
| <img src="https://cdn.worldvectorlogo.com/logos/postgresql.svg" width="24" alt="PostgreSQL logo">         | **PostgreSQL** | Database for Authentik and Immich.      |
| <img src="https://cdn.worldvectorlogo.com/logos/mariadb.svg" width="24" alt="MariaDB logo">               | **MariaDB** | Database for Nextcloud.                 |
| <img src="https://cdn.worldvectorlogo.com/logos/redis.svg" width="24" alt="Redis logo">                   | **Redis** | In-memory database and cache.           |

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
