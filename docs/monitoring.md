# Monitoring and Operations

A visibility layer built around dashboards, uptime tracking, host telemetry, service health checks, and operational access across the homelab.

> Primary dashboard: Homepage  
> Telemetry tools: Netdata and Glances  
> Availability monitoring: Uptime Kuma  
> Operational visibility: Unraid API and log tooling

---

# At a Glance

# Alerting and Notifications

The monitoring layer is not limited to passive dashboards.

It also includes active alerting and notification workflows so issues can be surfaced quickly instead of only being noticed during manual checks.

Current alerting methods include:

- email-based alerting
- phone notifications
- active service and availability alerts

This helps the homelab move beyond visibility alone and into a more operational model where failures, interruptions, or degraded service states can be noticed sooner.

| Area | Design |
|:--|:--|
| Primary dashboard | Homepage |
| Secondary dashboard concept | Dashy |
| Host telemetry | Netdata |
| Lightweight system view | Glances |
| Uptime monitoring | Uptime Kuma |
| Operational data source | Unraid API |
| Log visibility | GoAccess |
| Main goal | Know what is running, what is healthy, and what needs attention |

---

# Stack Layout

| Component | Role | Notes |
|:--|:--|:--|
| Homepage | Main dashboard | Primary service landing page and operational overview |
| Dashy | Secondary dashboard | Alternate dashboard platform retained for layout and presentation flexibility |
| Netdata | Host telemetry | Real-time infrastructure monitoring and resource visibility |
| Glances | Lightweight monitoring | Fast view into resource usage and container-related health |
| Uptime Kuma | Availability monitoring | Endpoint and service health checks |
| Unraid API | Platform operations | Access to host and platform-aware data |
| GoAccess | Log visibility | Request and access-log analysis |

---

# Design Intent

This layer exists to make the homelab understandable at a glance.

It is designed to support:

- quick service access
- visibility into system health
- uptime awareness
- host-level monitoring
- lightweight troubleshooting
- clearer operational awareness across a large service stack

The goal is not just to know that services exist, but to know when they are healthy, reachable, and behaving the way they should.

---

# Dashboard Layer

| Tool | Purpose |
|:--|:--|
| Homepage | Main front door for the homelab service ecosystem |
| Dashy | Alternate dashboard and layout platform |

Homepage serves as the main operational landing page and gives the stack a cleaner day-to-day control surface.

Dashy is retained as an alternate dashboard platform and design option rather than the primary operational surface.

---

# Telemetry Layer

| Tool | Purpose |
|:--|:--|
| Netdata | High-visibility host and infrastructure telemetry |
| Glances | Fast system overview and quick diagnostics |

These tools provide different kinds of visibility.

Netdata is stronger for broader real-time infrastructure awareness, while Glances is useful for quick checks and lightweight monitoring.

Together, they make the platform easier to inspect without jumping directly into raw host troubleshooting every time.

---

# Availability Monitoring

Uptime Kuma provides endpoint and service monitoring across the environment.

Its role includes:

- confirming service reachability
- surfacing outages or interruptions
- supporting a more operational view of service health
- helping identify which parts of the platform need attention first
- feeding active alerting workflows when monitored services fail or become unavailable

This is important in a homelab with many services because “installed” and “healthy” are not the same thing.

---

# Operations and Platform Awareness

The Unraid API adds a more platform-aware operational layer.

Its role includes:

- surfacing host-related data
- supporting dashboard integrations
- helping bridge the gap between service-level visibility and platform-level visibility

This is especially useful in a stack where containers, storage, and virtualization all coexist on the same host platform.

---

# Log Visibility

GoAccess adds a log-oriented view into request activity.

Its role includes:

- access log analysis
- visibility into traffic patterns
- easier review of request activity
- support for understanding how services are being reached

This complements dashboards and uptime monitoring by giving a more traffic-oriented operational perspective.

---

# Workflow View

```text
Host and Service Activity
          ↓
 Netdata / Glances / Uptime Kuma
          ↓
 Homepage / Unraid API / GoAccess
          ↓
 Operational Awareness and Troubleshooting
