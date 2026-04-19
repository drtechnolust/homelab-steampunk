# Virtual Machine Inventory

This inventory documents the VM layer of Homelab Steampunk, including active and offline guests that support smart home, desktop, testing, gaming, and platform experimentation workflows.

---

# Status Key

- **🟢 Live Now** — currently running
- **🕘 Offline** — retained but not currently running

---

# Active Virtual Machines

| VM | Status | Role | Notes |
|:--|:--:|:--|:--|
| Windows 11 Ghost 25H2 | 🟢 | Windows workstation / utility VM | Active Windows VM used for platform-specific workflows inside the Unraid virtualization layer |
| Home Assistant | 🟢 | Smart home platform | Primary VM for home automation workloads |
| Fedora | 🟢 | Linux workstation / lab VM | Retained for Linux experimentation and workstation-style workflows |
---

# Offline Virtual Machines

| VM | Status | Role | Notes |
|:--|:--:|:--|:--|
| Kali | 🕘 | Security testing VM | Used for isolated security-oriented lab activities |
| macOS Ventura | 🕘 | macOS experimentation VM | Retained for Apple-platform testing and compatibility experimentation |
| Windows 11 - Hyperspin 23H2 | 🕘 | Specialty / gaming VM | Used for gaming and frontend experimentation |
| Windows 11 Ghost 2025 | 🕘 | Alternate Windows VM | Retained as part of the broader Windows lab environment |

---

# VM Role in the Homelab

The VM layer complements the container stack rather than replacing it.

Virtual machines are used where full guest isolation, desktop operating systems, specialty software, or platform-specific testing make more sense than a containerized approach.

This hybrid model allows the homelab to support:
- always-on containerized services
- smart home workloads
- desktop-like utility environments
- operating system experimentation
- specialty and gaming-related use cases

---

# Notes

The VM inventory should be updated whenever:
- a new VM is created
- a guest is retired
- a VM changes role significantly
- an offline guest becomes part of the active platform again
