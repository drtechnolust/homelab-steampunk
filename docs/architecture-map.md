# Platform Map

This high-level map shows how the main service domains in Homelab Steampunk relate to access, operations, storage, and the Unraid platform.

```mermaid
flowchart TB

    A["Access Layer<br/>Tailscale / Traefik / Authentik / Cloudflare Tunnel"]
    B["Monitoring and Operations<br/>Homepage / Uptime Kuma / Netdata / Glances / Unraid API"]
    C["Media Stack<br/>Automation / Downloads / Playback"]
    D["Document and Cloud Stack<br/>Nextcloud / Paperless / Seafile / PDF Tools"]
    E["AI and Voice Stack<br/>Ollama / Open WebUI / Voice Services"]
    F["Photos, Cameras, and Smart Home<br/>Immich / PhotoPrism / Frigate / Home Assistant"]
    G["Infrastructure and Security Services<br/>CrowdSec / Pi-hole / Unbound / Support Services"]
    H["Storage and Platform Layer<br/>appdata / data / storage / photos / backups / VMs"]
    I["Unraid Host<br/>Docker + KVM/QEMU"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F

    G --> A
    B --> H
    C --> H
    D --> H
    E --> H
    F --> H

    I --> H
    I --> B
    I --> C
    I --> D
    I --> E
    I --> F
    I --> G

    style A fill:#dbeafe,stroke:#1d4ed8,stroke-width:2px,color:#111827
    style B fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style C fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style D fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style E fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style F fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style G fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827
    style H fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style I fill:#fde68a,stroke:#b45309,stroke-width:2px,color:#111827
