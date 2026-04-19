# Virtualization

A hybrid virtualization layer that complements the Docker stack by supporting full guest operating systems, smart-home workloads, testing environments, and specialty platform use cases.

> Hypervisor model: Unraid with KVM/QEMU  
> Role in homelab: guest operating systems, lab experimentation, and workloads better suited to VMs than containers  
> Active VM focus: Windows and Home Assistant

---

# At a Glance

| Area | Design |
|:--|:--|
| Virtualization platform | Unraid |
| Hypervisor model | KVM/QEMU |
| Active VMs | Windows 11 Ghost 25H2, Home Assistant |
| Offline lab VMs | Fedora, Kali, Ventura, Windows 11 - Hyperspin 23H2, Windows 11 Ghost 2025 |
| Main value | OS-level isolation, specialty workloads, and experimentation |
| Broader role | Complements the container stack rather than replacing it |

---

# VM Inventory Snapshot

| VM | Status | Role | Notes |
|:--|:--:|:--|:--|
| Windows 11 Ghost 25H2 | Live Now | Windows workstation / utility VM | Active Windows environment inside the Unraid platform |
| Home Assistant | Live Now | Smart-home platform | Primary VM for home automation workloads |
| Fedora | Offline | Linux workstation / lab VM | Retained for Linux experimentation |
| Kali | Offline | Security testing VM | Used for isolated lab activities |
| Ventura | Offline | macOS experimentation VM | Retained for Apple-platform testing |
| Windows 11 - Hyperspin 23H2 | Offline | Specialty / gaming VM | Used for gaming and frontend experimentation |
| Windows 11 Ghost 2025 | Offline | Alternate Windows VM | Retained as part of the broader Windows lab environment |

---

# Why the VM Layer Exists

The homelab is not container-only.

Virtual machines are used where full guest operating systems make more sense than containerized services.

This includes:

- smart-home workloads
- Windows-based workflows
- OS-specific experimentation
- security testing
- specialty and gaming-related use cases
- workloads that benefit from stronger isolation or a desktop-style environment

This makes the homelab more flexible than a pure Docker deployment.

---

# Relationship to the Docker Stack

The VM layer is designed to complement the container layer rather than compete with it.

| Layer | Best Fit |
|:--|:--|
| Containers | Always-on services, dashboards, automation, media, AI, documents |
| Virtual Machines | Full operating systems, desktop-style workflows, specialty testing, smart-home VM workloads |

This hybrid model allows the homelab to use the right tool for the right type of workload.

---

# Active VM Roles

## Windows 11 Ghost 25H2

This VM acts as an active Windows-based environment inside the homelab.

Its value includes:

- Windows-specific workflows
- general utility use
- platform flexibility inside the lab
- support for cases where a full Windows guest is more practical than a container or Linux VM

## Home Assistant

This VM is the primary smart-home platform.

Its value includes:

- home automation logic
- device coordination
- dashboards
- sensor and smart-device integration
- acting as one of the most practically useful VMs in the homelab

This makes the virtualization layer directly relevant to day-to-day life, not just experimentation.

---

# Offline and Specialty VMs

The offline VM set reflects the broader experimental nature of the homelab.

These VMs support:

- Linux experimentation
- security testing
- Apple-platform testing
- frontend and gaming experimentation
- alternate Windows environments

Keeping these guests available, even when not running, supports a more flexible and reusable lab model over time.

---

# Design Benefits

This virtualization layer provides:

- OS-level isolation
- support for desktop-class workloads
- greater flexibility than containers alone
- cleaner separation for specialty environments
- a place for experiments that do not belong in always-on service containers
- better support for mixed personal, technical, and hobby use cases

It is one of the reasons the homelab feels like a platform instead of only a service host.

---

# Workflow View

```text
Unraid Host
    ↓
KVM / QEMU Virtualization Layer
    ↓
Windows / Home Assistant / Linux / Specialty Guests
    ↓
Testing, Automation, Utility, and Platform Workflows
