# Phase 01 Notes – Virtual Lab Infrastructure

This document records the technical journey of Phase 01:
building a local virtual lab using a Linux host and
Ubuntu Server virtual machines.

The focus of this phase is not speed, but understanding.

---

## Host Environment

- Host OS: Fedora Linux (Workstation)
- Virtualization stack:
  - KVM / QEMU
  - libvirt
  - virt-manager
- Network interface (host): Wi-Fi (wireless)

This setup represents a realistic personal lab environment,
not a datacenter or cloud infrastructure.

---

## Initial Goal

- Install Ubuntu Server inside a virtual machine
- Enable network connectivity
- Allow remote access via SSH
- Simulate a real server with its own IP address

---

## Virtualization Validation

Hardware virtualization support was verified on the host:

- CPU virtualization extensions available (VT-x / AMD-V)
- KVM modules available and loaded
- libvirtd service running correctly

This confirms the host is capable of running
hardware-accelerated virtual machines.

---

## Networking Attempt: Bridged Mode

### Objective

Use bridged networking so the VM appears as a separate
device on the local network with its own IP address
(e.g. `192.168.x.x`).

This simulates a real physical server connected to the LAN.

---

### Encountered Issue

When attempting to start the VM with a bridged network
attached directly to the Wi-Fi interface, the VM failed
to start with an error similar to:

- Unable to add bridge port to wireless interface
- Operation not supported

---

### Root Cause (Important Learning)

Most Linux Wi-Fi drivers do **not support true Layer 2
bridging** due to limitations in the 802.11 standard
and driver implementations.

Unlike Ethernet interfaces, Wi-Fi interfaces generally
cannot act as a bridge port in a traditional Linux bridge.

This is a **technical limitation**, not a misconfiguration.

---

## Temporary Solution: NAT Networking

To continue the learning process without blocking progress:

- libvirt default NAT network was used
- VM received a private IP (e.g. `192.168.122.x`)
- Outbound internet access worked correctly
- SSH access from the host to the VM was possible

While this does not fully simulate a physical server,
it is sufficient for learning Linux, SSH, and services.

---

## Key Takeaways

- Virtualization works independently of networking mode
- Bridged networking over Wi-Fi is not always feasible
- NAT is a valid and common solution for local labs
- Errors are part of understanding infrastructure reality

This limitation will be revisited in later phases using:
- Wired Ethernet
- Macvtap
- Or cloud-based environments

---

## Phase 01 Status

- Ubuntu Server installed successfully
- VM accessible via SSH
- Networking functional (NAT)
- Learning objectives achieved

This phase prioritizes understanding system behavior
over forcing an ideal but unrealistic configuration.
