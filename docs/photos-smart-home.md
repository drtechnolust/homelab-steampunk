# Photos, Cameras, and Smart Home

A combined platform for photo preservation, camera monitoring, and home automation built around self-hosted services that prioritize control, local access, and long-term flexibility.

> Primary photo platform: Immich  
> Secondary photo platform: PhotoPrism  
> Camera platform: Frigate  
> Home automation platform: Home Assistant

---

# At a Glance

| Area | Design |
|:--|:--|
| Primary photo system | Immich |
| Secondary photo system | PhotoPrism |
| Camera and NVR layer | Frigate |
| Home automation | Home Assistant |
| Main migration goal | Move away from Google Photos, Dropbox, Google Drive, and the Google Nest ecosystem |
| Broader role | Photos, surveillance, and smart environment workflows |
| Design focus | Local control, organization, and long-term flexibility |

---

# Stack Layout

| Component | Role | Notes |
|:--|:--|:--|
| Immich | Primary photo platform | Main system for photo and video management |
| PostgreSQL_Immich | Database backend | Supports Immich data and indexing workflows |
| PhotoPrism | Secondary photo platform | Alternate photo browsing and organization platform |
| Frigate | Camera / NVR platform | Handles surveillance, event detection, and camera workflows |
| Home Assistant | Smart home platform | Primary automation and smart-device orchestration layer |
| HomeAssistant_inabox | Support utility | Containerized support component tied to the broader Home Assistant workflow |

---

# Why This Stack Exists

This part of the homelab is not just about adding more services.

It exists to support a move away from:

- Google Photos
- Dropbox
- Google Drive
- the Google Nest ecosystem

The goal is to replace dependence on consumer cloud platforms with a more self-hosted, local-first environment that provides better control over storage, automation, access, and long-term ownership.

---

# Design Intent

This part of the homelab is built to support more than one kind of media workflow.

It is designed to handle:

- photo and video preservation
- personal and family media organization
- alternate photo-management platforms
- camera monitoring and event workflows
- home automation and device orchestration
- local-first control over important household systems

This makes the stack one of the most practical day-to-day parts of the homelab.

---

# Photo Platforms

| Platform | Role | Notes |
|:--|:--|:--|
| Immich | Primary | Main photo and video platform for ongoing library use |
| PhotoPrism | Secondary | Alternate interface and organization model for image libraries |

Using more than one photo platform creates flexibility.

This allows:
- different browsing experiences
- different strengths in organization and discovery
- side-by-side evaluation of photo platforms
- more freedom to evolve the photo workflow over time

This part of the stack is especially important because it supports the move away from Google Photos, Dropbox, and Google Drive toward a more self-hosted photo and media library model.

---

# Camera and Surveillance Layer

Frigate is the camera and NVR-focused part of the stack.

Its role includes:

- camera event handling
- surveillance workflows
- video-related monitoring
- integration potential with the broader smart-home environment

This gives the homelab a security- and awareness-oriented camera layer rather than treating cameras as isolated devices.

---

# Smart Home Layer

Home Assistant is the central smart-home platform.

Its role includes:

- device orchestration
- automation workflows
- dashboards and household visibility
- tying sensors, devices, and services into one environment
- acting as the operational core of the smart-home side of the homelab

HomeAssistant_inabox complements this by supporting related management and integration workflows inside the broader Unraid environment.

This part of the stack is also a move away from the Google Nest ecosystem and toward a more flexible self-hosted automation model.

---

# Workflow View

```text
Photos / Videos / Camera Events / Smart Devices
                    ↓
   Immich / PhotoPrism / Frigate / Home Assistant
                    ↓
   Organization / Monitoring / Automation / Retrieval
                    ↓
        Daily Use, Visibility, and Long-Term Control
