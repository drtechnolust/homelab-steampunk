# 🔐 Security & Access Model

A layered access model built around private networking, reverse proxy control, identity-aware protection, DNS filtering, and selective service exposure.

> **Primary ingress layer:** Traefik  
> **Identity platform:** Authentik  
> **DNS filtering:** Pi-hole + Unbound  
> **Remote/private access:** Tailscale  
> **Public exposure philosophy:** selective and minimized

---

# ✨ At a Glance

| Area | Design |
|:--|:--|
| Reverse proxy | Traefik |
| Identity and access control | Authentik |
| DNS filtering | Pi-hole |
| Recursive DNS | Unbound |
| Threat-response layer | CrowdSec + Traefik Bouncer |
| Remote private access | Tailscale |
| External publishing approach | Limited and intentional |
| Default philosophy | Minimize unnecessary exposure |

---

# 🧱 Core Security Layers

| Layer | Primary Tooling | Purpose |
|:--|:--|:--|
| Ingress control | Traefik | Centralized routing, HTTPS entrypoints, middleware-based request handling |
| Identity and protected access | Authentik | Authentication and access workflows for selected services |
| DNS control | Pi-hole + Unbound | Filtering, recursive resolution, and local DNS control |
| Threat response | CrowdSec + Traefik Bouncer | Behavioral analysis and ingress-side enforcement |
| Private remote connectivity | Tailscale | Secure remote access without broadly exposing internal services |
| Selective external access | Cloudflare Tunnel | Used where limited external publishing is needed |

---

# 🚪 Access Philosophy

The homelab does not treat every service the same way.

Instead, access is intentionally split into a few practical models:

| Access Type | Use Case |
|:--|:--|
| Internal direct access | Admin tools, utility services, local-only apps |
| Reverse-proxied access | Cleaner routed access for selected services |
| Identity-protected access | Services that benefit from sign-in and access control |
| LAN-facing infrastructure | DNS and network services that belong on the local network |
| Private remote access | Tailscale access when services need to be reached away from home |

The goal is practical security, not maximum public exposure.

---

# 🌐 Core Components

### Traefik

Traefik is the primary reverse proxy and central ingress layer.

It is used for:
- routed access to selected services
- HTTPS entrypoints
- middleware-based request control
- cleaner service exposure patterns
- avoiding a flat unmanaged port-access model

### Authentik

Authentik is the identity and access platform.

It is used for:
- centralized authentication
- protected application access
- cleaner sign-in workflows
- identity-aware access patterns for selected services

### Pi-hole

Pi-hole provides LAN-level DNS filtering and local DNS visibility.

It is used for:
- blocking unwanted domains
- improving DNS awareness
- supporting cleaner local network behavior

### Unbound

Unbound complements Pi-hole by acting as the recursive resolver.

It is used for:
- recursive lookups
- DNSSEC-aware validation
- more controlled local DNS resolution

### CrowdSec

CrowdSec is part of the threat-response layer.

It is used for:
- identifying suspicious behavior
- analyzing traffic and events
- contributing decisions used by the enforcement layer

### CrowdSec Traefik Bouncer

The Traefik bouncer applies CrowdSec decisions at the ingress layer.

It is used for:
- request enforcement
- adding a response layer between analysis and inbound traffic handling

### Tailscale

Tailscale is the preferred private remote access method.

It is used for:
- reaching services away from home
- avoiding unnecessary public exposure
- keeping remote access aligned with a private-network-first approach

### Cloudflare Tunnel

Cloudflare Tunnel is part of the external access toolkit where selective publishing is needed.

Its use is intended to stay limited and deliberate rather than becoming the default path for everything.

---

# 🕸️ Network Placement

| Network | Role | Security Value |
|:--|:--|:--|
| `steampunknet` | Primary application network | Cleaner service grouping and app-to-app communication |
| `nextcloud-aio` | Dedicated Nextcloud network | Keeps the Nextcloud stack grouped and more isolated |
| `seafile-net` | Dedicated Seafile network | Separate boundary for Seafile and related services |
| `br0` | LAN-facing services | Appropriate for network services such as DNS |
| `host` | Host-integrated services | Used intentionally where host-level visibility or integration is needed |
| `bridge` | Default Docker bridge | Used selectively where it remains sufficient |

This keeps the environment from becoming one flat network with every service mixed together.

---

# 🛡️ Practical Security Boundaries

The environment can be thought of in a few layers:

| Layer | Examples |
|:--|:--|
| Ingress and protection layer | Traefik, Authentik, CrowdSec, Cloudflare Tunnel |
| Application layer | Reverse-proxied or locally accessed services |
| Internal service layer | Databases, workers, indexing services, support containers |
| LAN infrastructure layer | Pi-hole, Unbound, local network-facing utilities |
| Private remote layer | Tailscale access for off-site connectivity |

---

# 🔄 Security Direction

The current direction of the homelab is toward:

- less unnecessary direct exposure
- clearer distinction between internal and externally reachable services
- stronger consistency around private remote access
- better use of identity-aware access where appropriate
- cleaner alignment between architecture and actual deployment behavior

---

# 🧠 Design Notes

This is a practical self-hosting security model, not a claim of perfect hardening.

The security approach balances:
- usability
- private access
- layered controls
- selective exposure
- ongoing refinement as the homelab evolves
