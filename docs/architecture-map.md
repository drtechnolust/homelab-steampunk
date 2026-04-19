```mermaid
flowchart TB

    subgraph Access["Access Layer"]
        TS["Tailscale<br/>Private Remote Access"]
        CF["Cloudflare Tunnel<br/>Selective External Access"]
        TR["Traefik<br/>Ingress / Routing"]
        AK["Authentik<br/>Identity / Protected Access"]
    end

    subgraph Ops["Monitoring and Operations"]
        HP["Homepage"]
        UK["Uptime Kuma"]
        ND["Netdata"]
        GL["Glances"]
        UA["Unraid API"]
        GA["GoAccess"]
    end

    subgraph Media["Media Stack"]
        OV["Overseerr"]
        PR["Prowlarr"]
        SO["Sonarr"]
        SA["Sonarr Anime"]
        SK["Sonarr Kids"]
        RA["Radarr"]
        RAA["Radarr Anime"]
        RK["Radarr Kids"]
        LI["Lidarr"]
        BA["Bazarr"]
        QB["qBittorrentVPN"]
        SAB["SABnzbd"]
        UN["Unpackerr"]
        AU["Autoscan"]
        EM["Emby<br/>Primary"]
        JF["Jellyfin<br/>Secondary"]
        WS["Watchstate"]
    end

    subgraph Docs["Document and Cloud Stack"]
        NC["Nextcloud AIO"]
        COL["Collabora"]
        TAL["Talk"]
        WB["Whiteboard"]
        FTS["Full Text Search"]
        PL["Paperless-NGX"]
        PAI["Paperless-AI"]
        TIKA["Apache Tika"]
        GOT["Gotenberg"]
        SEA["Seafile"]
        STP["Stirling-PDF"]
    end

    subgraph AI["AI and Voice Stack"]
        OL["Ollama"]
        OW["Open WebUI"]
        FW["faster-whisper"]
        PI["Piper"]
        OWW["openWakeWord"]
    end

    subgraph Photos["Photos, Cameras, and Smart Home"]
        IM["Immich"]
        PP["PhotoPrism"]
        FR["Frigate"]
        HA["Home Assistant"]
        HAI["HomeAssistant_inabox"]
    end

    subgraph Infra["Infrastructure and Security Services"]
        CS["CrowdSec"]
        CB["CrowdSec Traefik Bouncer"]
        PH["Pi-hole"]
        UB["Unbound"]
        DSP["Docker Socket Proxy"]
    end

    subgraph Data["Storage and Platform Layer"]
        APP["appdata"]
        DAT["data"]
        STO["storage"]
        PIC["pictures / photos"]
        BAK["backups"]
        DOM["domains / VM storage"]
        UNR["Unraid Host"]
        VM["KVM / QEMU VMs"]
    end

    CF --> TR
    TS --> TR
    TR --> AK

    TR --> HP
    TR --> NC
    TR --> IM
    TR --> OW

    AK --> NC
    AK --> HP

    HP --> UK
    HP --> ND
    HP --> GL
    HP --> UA
    HP --> GA

    OV --> JF
    PR --> SO
    PR --> SA
    PR --> SK
    PR --> RA
    PR --> RAA
    PR --> RK
    SO --> QB
    SA --> QB
    SK --> QB
    RA --> SAB
    RAA --> SAB
    RK --> SAB
    LI --> SAB
    QB --> UN
    SAB --> UN
    UN --> AU
    AU --> EM
    AU --> JF
    EM --> WS
    JF --> WS
    BA --> EM
    BA --> JF

    PAI --> PL
    TIKA --> PL
    GOT --> PL
    STP --> PL
    NC --> COL
    NC --> TAL
    NC --> WB
    NC --> FTS

    OW --> OL
    FW --> OW
    PI --> OW
    OWW --> OW

    IM --> PIC
    PP --> PIC
    FR --> STO
    HA --> HAI

    CS --> CB
    CB --> TR
    PH --> UB

    EM --> DAT
    JF --> DAT
    SO --> DAT
    SA --> DAT
    SK --> DAT
    RA --> DAT
    RAA --> DAT
    RK --> DAT
    LI --> DAT
    PL --> STO
    NC --> STO
    SEA --> STO
    OL --> APP
    OW --> APP
    HP --> APP
    TR --> APP
    AK --> APP
    IM --> APP
    PP --> APP
    FR --> APP

    UNR --> APP
    UNR --> DAT
    UNR --> STO
    UNR --> BAK
    UNR --> DOM
    UNR --> VM
    VM --> HA

    style TS fill:#dbeafe,stroke:#1d4ed8,stroke-width:2px,color:#111827
    style CF fill:#dbeafe,stroke:#1d4ed8,stroke-width:2px,color:#111827
    style TR fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#111827
    style AK fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#111827

    style HP fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style UK fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style ND fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style GL fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style UA fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style GA fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827

    style OV fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style PR fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style SO fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style SA fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style SK fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style RA fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style RAA fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style RK fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style LI fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style BA fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style QB fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style SAB fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style UN fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style AU fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style EM fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style JF fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style WS fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827

    style NC fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style COL fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style TAL fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style WB fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style FTS fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style PL fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style PAI fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style TIKA fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style GOT fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style SEA fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style STP fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827

    style OL fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style OW fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style FW fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style PI fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style OWW fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827

    style IM fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style PP fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style FR fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style HA fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style HAI fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827

    style CS fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827
    style CB fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827
    style PH fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827
    style UB fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827
    style DSP fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827

    style APP fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style DAT fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style STO fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style PIC fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style BAK fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style DOM fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style UNR fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
    style VM fill:#ecfccb,stroke:#65a30d,stroke-width:2px,color:#111827
