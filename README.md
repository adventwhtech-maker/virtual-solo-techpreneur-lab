# virtual-solo-techpreneur-lab

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
