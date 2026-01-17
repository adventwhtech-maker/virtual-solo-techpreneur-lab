# Virtual Solo Techpreneur Lab

> A long-term experimental lab for learning systems, networking, and software engineering — built slowly, transparently, and intentionally.

---

## Why This Repository Exists

This repository is **not** a startup pitch, not a portfolio flex, and not a product showcase.

It is a **learning laboratory**.

I believe that in a world where AI can generate code instantly, the real advantage is not *writing code faster*, but **understanding systems deeply**, making good technical decisions, and documenting the thinking process behind them.

This repo captures:

* Experiments
* Errors
* Fixes
* Mental models
* Infrastructure decisions

Everything starts from zero.

---

## Core Principles

* **Build first, understand by breaking**
* **Errors are assets, not failures**
* **Small, reproducible steps beat big promises**
* **Documentation is part of the product**

This lab follows an *engineering mindset*, not a tutorial mindset.

---

## Learning Focus (Technical Scope)

This repository focuses on foundational technical skills:

* Linux systems & CLI
* Virtualization (KVM / libvirt)
* Networking fundamentals
* SSH & remote access
* Infrastructure thinking

Future layers (not fully exposed here):

* Backend systems (Python, Django, APIs)
* IoT-oriented architecture
* Selective use of Machine Learning where it is **technically justified**

This repo intentionally avoids:

* Business logic
* Monetization details
* Proprietary implementations

---

## Roadmap Structure

The lab is organized into **phases**, each representing a real technical milestone.

### Phase 01 — Virtual Lab Infrastructure

**Goal:**
Build a Linux server inside a virtual machine that behaves like a real physical server.

**Key skills:**

* VM setup using KVM / virt-manager
* Linux installation (Ubuntu Server LTS)
* Network configuration
* SSH remote access

**Outcome:**
The server can be accessed remotely from the host machine **without interacting with the VM UI**.

Detailed notes are documented in:

* `PHASE-01-NOTES.md`
* `docs/`

---

## Repository Structure

```
virtual-solo-techpreneur-lab/
├── README.md              # This document
├── SECURITY.md            # Security boundaries & publishing rules
├── PHASE-01-NOTES.md      # Phase 01 technical journey
├── docs/
│   ├── networking-basics.md
│   ├── linux-cli-notes.md
│   └── ssh-notes.md
```

---

## Security & Responsibility

This repository is designed with **security awareness**:

* No real credentials
* No private keys
* No internal IP exposure beyond lab context
* No privileged system dumps

See `SECURITY.md` for details.

---

## About the Builder

This lab is built by a solo technical builder experimenting at the intersection of:

* Systems engineering
* Software infrastructure
* Automation
* Hardware–software integration

The goal is not speed.

The goal is **clarity, depth, and long-term leverage**.

---

## Final Note

This repository will evolve.

Not linearly.

But honestly.

If you are reading this and building your own lab:

> Start messy. Document clearly. Improve continuously.

That is the only sustainable path.

---

## ✅ PHASE 01 – FORMAL CLOSING & CHECKLIST

### Phase Objective Recap

**Phase 01** focuses on building a *realistic virtual lab* using industry-grade tools to understand:

* Virtualization fundamentals
* Linux server operations
* Basic networking
* Secure remote access (SSH)
* Technical documentation & version control

This phase intentionally prioritizes **learning by doing and breaking things**, not speed.

---

### ✔️ Technical Checklist

#### 1. Virtualization (Host Level)

* [x] Fedora Linux as primary host OS
* [x] Hardware virtualization enabled (VT-x)
* [x] KVM + libvirt stack installed and running
* [x] virt-manager used as VM controller

#### 2. Virtual Machine (Guest Level)

* [x] Ubuntu Server LTS installed (CLI-only)
* [x] VM created using default NAT networking (libvirt `virbr0`)
* [x] VM boots reliably and survives restart

> **Note:** Bridged networking over Wi-Fi was attempted and failed due to kernel/driver limitations. This is expected behavior and documented as part of learning.

#### 3. Linux CLI Fundamentals

* [x] User-based login (non-root)
* [x] `sudo` privilege escalation understood
* [x] Core commands practiced: `ip`, `ss`, `apt`, `systemctl`, `journalctl`
* [x] System update workflow executed safely

#### 4. Networking Basics

* [x] Host routing table analyzed
* [x] libvirt NAT network (`192.168.122.0/24`) understood
* [x] Difference between NAT vs Bridged networking documented
* [x] DHCP lease inspection attempted and explained

#### 5. SSH & Remote Access

* [x] SSH keypair (ed25519) generated
* [x] SSH agent configured and understood
* [x] Passwordless SSH login verified
* [x] SSH trust model (known_hosts) documented

#### 6. Git & GitHub Workflow

* [x] Git installed and verified
* [x] Repository cloned securely
* [x] HTTPS authentication issues understood
* [x] SSH-based GitHub authentication configured
* [x] `pull --rebase` workflow learned and applied

#### 7. Documentation & Security Mindset

* [x] README.md written as technical journey, not marketing
* [x] SECURITY.md added to clarify boundaries and threat model
* [x] Phase notes separated from public-facing docs
* [x] No credentials, secrets, or sensitive metadata exposed

---

### 🧠 Key Lessons Learned

* Errors are not failures; they are **data**
* Virtualization on laptops has real-world constraints
* Networking behaves differently on Wi-Fi vs Ethernet
* Git is a distributed history system, not file sync
* Security is about **intentional exposure**, not silence

---

### 🔒 Security Position Statement

This repository intentionally documents **process, reasoning, and troubleshooting**, while excluding:

* Private keys
* Passwords or tokens
* Public IPs or production endpoints

This ensures learning transparency **without increasing attack surface**.

---
## Phase-01 Closure

This phase focused on building a solid foundation:
- VM provisioning using KVM/libvirt
- Basic Linux server setup
- SSH remote access from host machine
- Understanding modern SSH behavior (systemd socket activation)
- Interpreting authentication failures and logs

Outcome:
The VM can be managed entirely from the host via SSH without relying on GUI access.
This environment will be reused for Python automation and system-level experiments in Phase-02.

Status: ✅ Completed

---

➡️ **Next Phase Preview:**
Phase 02 will focus on *service-level networking and server hardening*, preparing the lab for real workloads (APIs, dashboards, automation).

