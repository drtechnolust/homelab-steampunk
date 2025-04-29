![SteamPunk Homelab](assets/cover.png)

# 🚀 SteamPunk Homelab

Welcome to my cyberpunk-themed homelab — a playground where learning, automation, and entertainment collide.  
Powered by Unraid, Docker, and secured through Traefik and Cloudflare Tunnels, this environment balances serious production reliability with a spirit of experimentation.

> "It's not just a homelab — it's a lifestyle."

---

## 🛡️ Principles

- **Containerization First**: All services are deployed in isolated containers to ensure modularity, resilience, and effortless scalability.
- **Secure Ingress and Traffic Control**: All inbound and internal traffic is dynamically routed with SSL encryption, strict routing policies, and minimal attack surface exposure.
- **Identity and Access Governance**: Centralized authentication and fine-grained access controls are enforced across all services, ensuring that only trusted identities gain appropriate access to protected resources.
- **Zero-Trust External Access**: External connectivity operates under a zero-trust model, leveraging encrypted tunnels and forward authentication to prevent unauthorized entry.
- **Resilient Storage Architecture**: Storage combines fast NVMe caching with a robust hard drive array to balance performance, redundancy, and expansion without compromising data integrity.
- **Holistic System Monitoring and Automation**: System health, automation, and backup processes are fully integrated across storage and service layers to ensure uptime, efficiency, and rapid recovery capabilities.
- **Open-Source Ethos**: The environment is designed around open-source solutions, prioritizing transparency, adaptability, and community-driven innovation.
- **Continuous Optimization and Fortification**: All systems undergo continuous evaluation and refinement to improve performance, bolster security, and integrate the latest technological advancements.
- **Purpose-Driven Design**: Every deployed component is selected based on long-term reliability, operational excellence, and alignment with the homelab’s evolving mission.


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
| <img src="assets/jellyfin.png" width="24"> | **Jellyfin** | Open-source personal media server. |
| <img src="assets/emby.png" width="24"> | **EmbyServer** | Media server with advanced metadata support. |
| <img src="assets/tautulli.png" width="24"> | **Tautulli** | Monitoring for Plex/Emby activity. |
| <img src="assets/radarr.png" width="24"> | **Radarr** | Automated movie collection management. |
| <img src="assets/sonarr.png" width="24"> | **Sonarr** | Automated TV show downloading and organization. |
| <img src="assets/overseerr.png" width="24"> | **Overseerr** | Request management system for media libraries. |
| <img src="assets/recyclarr.png" width="24"> | **Recyclarr** | Syncs Radarr/Sonarr quality profiles automatically. |

---

### 📊 Monitoring Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="assets/netdata.png" width="24"> | **Netdata** | Real-time system monitoring and alerts. |
| <img src="assets/glances.png" width="24"> | **Glances** | Cross-platform system monitor. |
| <img src="assets/homepage.png" width="24"> | **Homepage** | Dashboard for organizing self-hosted services. |
| <img src="assets/dashy.png" width="24"> | **Dashy** | Dashboard focused on app links and widgets. |
| <img src="assets/speedtest.png" width="24"> | **Speedtest Tracker** | Internet connection monitoring. |

---

### 🧰 Utilities Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="assets/code-server.png" width="24"> | **Code-Server** | Web-based VSCode IDE. |
| <img src="assets/rustdesk.png" width="24"> | **RustDesk Server** | Self-hosted remote desktop solution. |
| <img src="assets/docker.png" width="24"> | **Docker Socket Proxy** | Secure docker.sock access. |

---

### ☁️ Cloud / Storage Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="assets/nextcloud.png" width="24"> | **Nextcloud AIO** | Personal cloud platform for storage, collaboration, and backup. |
| <img src="assets/immich.png" width="24"> | **Immich** | High-speed AI-powered photo backup service. |
| <img src="assets/photoprism.png" width="24"> | **PhotoPrism** | Private photo management platform. |
| <img src="assets/syncthing.png" width="24"> | **Syncthing** | Decentralized peer-to-peer file sync. |

---

### 🔒 Security Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="assets/traefik.svg" width="24"> | **Traefik** | Dynamic reverse proxy with SSL support. |
| <img src="assets/authentik.png" width="24"> | **Authentik** | SSO and Identity provider. |
| <img src="assets/crowdsec.png" width="24"> | **CrowdSec** | Collaborative IPS security tool. |
| <img src="assets/pihole.png" width="24"> | **Pi-hole** | DNS-level ad-blocker for the entire network. |
| <img src="assets/unbound.png" width="24"> | **Unbound** | Local DNS resolver. |
| <img src="assets/cloudflare.png" width="24"> | **Cloudflare Tunnel** | Securely connects homelab services to the public internet. |

---

### 🗄️ Database Stack

| Logo | Application | Description |
|:----:|:------------|:------------|
| <img src="assets/postgresql.png" width="24"> | **PostgreSQL** | Database for Authentik and Immich. |
| <img src="assets/mariadb.png" width="24"> | **MariaDB** | Database for Nextcloud. |
| <img src="assets/redis.png" width="24"> | **Redis** | In-memory database and cache. |

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
