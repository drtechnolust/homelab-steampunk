# Paperless Document Stack

A document-ingestion and archival workflow built around structured intake, OCR, AI-assisted enrichment, searchable storage, and long-term document organization.

> Primary document platform: Paperless-NGX  
> AI enrichment layer: Paperless-AI  
> Supporting processors: Apache Tika, Gotenberg, Stirling-PDF  
> Broader ecosystem: Nextcloud, Seafile, structured document storage

---

# At a Glance

| Area | Design |
|:--|:--|
| Core archive platform | Paperless-NGX |
| AI-assisted enrichment | Paperless-AI |
| OCR / text extraction support | Apache Tika |
| PDF conversion support | Gotenberg |
| PDF utility tooling | Stirling-PDF |
| Intake model | Structured consume paths |
| Archive model | Dedicated archive and export paths |
| Goal | Searchable long-term document management |

---

# Stack Layout

| Component | Role | Notes |
|:--|:--|:--|
| Paperless-NGX | Primary document archive | Main system for ingestion, OCR, tagging, metadata, and retrieval |
| Paperless-AI | AI enrichment layer | Adds automated document analysis and metadata assistance |
| Apache Tika | Content extraction | Supports document parsing and text extraction workflows |
| Gotenberg | PDF conversion | Supports document-to-PDF conversion processes |
| Stirling-PDF | PDF utility layer | Additional PDF handling and transformation tooling |
| PostgreSQL / Redis support | Platform backend services | Supports persistence and application responsiveness |

---

# Design Intent

This part of the homelab is built to do more than store files.

The document stack is designed to support:

- structured intake
- OCR and text extraction
- archive-friendly storage
- metadata enrichment
- searchable retrieval
- cleaner long-term digital organization
- future-friendly automation

The goal is to reduce document chaos and move toward a more organized personal document platform.

---

# Intake and Processing Model

Documents are not treated as a flat pile of files.

The workflow is built around distinct stages:

- intake
- processing
- enrichment
- archive
- export
- retrieval

That separation makes the system easier to understand and maintain over time.

---

# Processing Flow

```text
Document Intake
      ↓
 Paperless Consume Path
      ↓
 OCR / Extraction / Parsing
      ↓
 Metadata / Tagging / AI Review
      ↓
 Archived Document Store
      ↓
 Search / Retrieval / Export
