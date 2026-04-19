# Document Management System Map

This map shows how the main document-management components in Homelab Steampunk relate to intake, processing, enrichment, archival storage, retrieval, and broader file-platform access.

```mermaid
flowchart TB
    A["Document Intake"]
    B["Consume Path"]
    C["Paperless-NGX"]
    D["Apache Tika"]
    E["Gotenberg"]
    F["Paperless-AI"]
    G["Archive Storage"]
    H["Export Path"]
    I["Search and Retrieval"]
    J["Nextcloud"]
    K["Seafile"]
    L["Stirling-PDF"]

    A --> B
    B --> C
    D --> C
    E --> C
    F --> C
    C --> G
    C --> H
    C --> I
    L --> C
    G --> J
    G --> K
    I --> J
    I --> K

    style A fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style B fill:#e0f2fe,stroke:#0284c7,stroke-width:2px,color:#111827
    style C fill:#ede9fe,stroke:#7c3aed,stroke-width:2px,color:#111827
    style D fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style E fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
    style F fill:#dbeafe,stroke:#1d4ed8,stroke-width:2px,color:#111827
    style G fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style H fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#111827
    style I fill:#f3f4f6,stroke:#4b5563,stroke-width:2px,color:#111827
    style J fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style K fill:#fce7f3,stroke:#db2777,stroke-width:2px,color:#111827
    style L fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#111827
