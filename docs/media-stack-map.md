```mermaid
flowchart TB
    A["Import Lists and Requests"]
    B["Sonarr / Sonarr Anime / Sonarr Kids"]
    C["Radarr / Radarr Anime / Radarr Kids"]
    D["Lidarr"]
    E["Prowlarr"]
    F["qBittorrentVPN / SABnzbd"]
    G["Unpackerr / Autoscan"]
    H["Shared Media Libraries"]
    I["Emby<br/>Primary"]
    J["Jellyfin<br/>Secondary"]
    K["Watchstate"]
    L["Tailscale<br/>Private Remote Access"]

    E --> B
    E --> C
    A --> B
    A --> C
    A --> D
    B --> F
    C --> F
    D --> F
    F --> G
    G --> H
    H --> I
    H --> J
    I --> K
    J --> K
    L --> I
    L --> J

    style A fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style B fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style C fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style D fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style E fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style F fill:#fde68a,stroke:#b45309,stroke-width:2px,color:#111827
    style G fill:#fde68a,stroke:#b45309,stroke-width:2px,color:#111827
    style H fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style I fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style J fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style K fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style L fill:#dbeafe,stroke:#1d4ed8,stroke-width:2px,color:#111827
