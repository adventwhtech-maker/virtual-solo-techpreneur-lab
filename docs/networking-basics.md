# Networking Basics for Virtual Labs

This document explains the fundamental networking concepts
used in this project, with a focus on virtual machines
and local lab environments.

The goal is understanding, not memorization.

---

## Why Networking Matters Early

Every system component depends on networking:

- SSH requires reachable IP addresses
- APIs rely on ports and routing
- IoT devices communicate over networks
- Cloud services are remote networks by design

Without understanding networking, debugging becomes guesswork.

---

## Local Network Overview

In a typical home or lab setup:

- The router acts as the gateway (e.g. `192.168.1.1`)
- Devices receive private IP addresses
- Traffic is routed, not broadcast globally

Virtual machines must integrate into this environment
using specific networking modes.

---

## Common VM Networking Modes

### 1. NAT (Network Address Translation)

**How it works:**
- The VM lives in a private virtual network
- The host acts as a gateway
- Outbound traffic works by default

**Characteristics:**
- VM IP is not directly reachable from the LAN
- Safe and simple
- Common in local labs

**Typical use cases:**
- Learning Linux
- Package installation
- SSH access from host to VM
- Development environments

---

### 2. Bridged Networking

**How it works:**
- The VM appears as a separate device on the LAN
- Receives an IP from the same router as the host

**Characteristics:**
- VM behaves like a physical machine
- Other devices can reach the VM directly

**Limitations:**
- Often not supported on Wi-Fi interfaces
- Depends on driver and hardware capabilities

**Typical use cases:**
- Wired Ethernet environments
- Server simulations
- Advanced networking labs

---

### 3. Macvtap (Advanced)

**How it works:**
- VM attaches directly to the physical interface
- Bypasses traditional Linux bridges

**Characteristics:**
- Better compatibility with Wi-Fi than bridges
- Host-to-VM communication may be limited

**Typical use cases:**
- Advanced labs
- Workarounds for Wi-Fi bridge limitations

---

## Why Bridged Networking Failed in Phase 01

In this lab:

- The host uses a Wi-Fi interface
- Most Wi-Fi drivers do not support Layer 2 bridging
- This is a technical limitation, not a misconfiguration

Understanding this prevents wasted debugging time.

---

## Practical Learning Strategy

For Phase 01:

- NAT is sufficient and realistic
- Focus is placed on:
  - Linux fundamentals
  - SSH connectivity
  - Service deployment
- Bridged networking will be revisited later using:
  - Wired Ethernet
  - Cloud environments

---

## Key Takeaways

- Networking mode defines visibility and reachability
- NAT is common, safe, and widely used
- Bridged networking is not always available
- Understanding limitations is part of system design

A working system with known limitations is better
than a broken system chasing ideal assumptions.
