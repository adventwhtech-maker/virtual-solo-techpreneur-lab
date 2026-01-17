# Security Notes

This document defines the security boundaries for this public repository.

The purpose of these notes is not to expose a production-ready security
implementation, but to clarify what information is safe to share and what
must remain private during this learning journey.

---

## What This Repository IS

- A public learning lab focused on:
  - Linux server fundamentals
  - Virtualization and networking
  - SSH access and system administration basics
- An experimental environment running on virtual machines
- A documentation-first approach to learning through errors and fixes

---

## What This Repository IS NOT

- A production environment
- A penetration testing lab
- A place to publish real credentials, secrets, or internal infrastructure
- A complete security hardening guide

---

## Information That Will NEVER Be Published

- SSH private keys or access tokens
- Real usernames and passwords
- Public IP addresses of active servers
- Exact hostnames tied to real infrastructure
- Privilege escalation paths or exploit-ready configurations

All examples will use sanitized placeholders such as:

- `VM_HOST`
- `SERVER_IP`
- `SSH_USER`
- `NETWORK_INTERFACE`

---

## SSH & Access Policy

- SSH access is used only for local or lab-based virtual machines
- Key-based authentication is preferred over password login
- Root login over SSH is disabled when applicable
- Any SSH configuration shared is simplified and non-production

---

## Network Exposure

- Public exposure (e.g., tunnels or reverse proxies) is documented at a
  conceptual level only
- No direct inbound access to a real home network is documented
- Firewall rules are discussed without exposing live configurations

---

## Philosophy

Security is treated as a discipline, not a checklist.

Mistakes and misconfigurations may be discussed, but always with context,
sanitization, and an emphasis on learning rather than exploitation.

If a detail feels unsafe to publish, it will not be published.

---

_Last updated: Phase 01 – Virtual Lab Infrastructure_
