# SSH Notes – Phase 01

This document explains Secure Shell (SSH) as used in this
project, focusing on safe and practical remote access
to Linux servers and virtual machines.

---

## What SSH Is

SSH (Secure Shell) is a protocol for securely accessing
a remote machine over an untrusted network.

It provides:
- Encrypted communication
- Strong authentication
- Integrity of transmitted data

SSH is the default access method for Linux servers.

---

## Why SSH Is Central to This Lab

All servers in this project are managed without a graphical
interface.

SSH enables:
- Headless server administration
- Automation and scripting
- Remote debugging and maintenance

If SSH works correctly, the system is manageable.

---

## Basic SSH Usage

ssh user@server_ip


This command:
- Authenticates the user
- Establishes an encrypted session
- Provides a remote shell

---

## Authentication Methods

### Password-Based Authentication

- Simple to use
- Higher risk if exposed publicly
- Vulnerable to brute-force attacks

Used only for initial lab setup.

---

### Key-Based Authentication (Preferred)

- Uses cryptographic key pairs
- No password transmitted over the network
- Resistant to brute-force attacks

This is the recommended method for all long-term access.

---

## SSH Keys (Conceptual Overview)

- A key pair consists of:
  - Private key (kept secret)
  - Public key (shared with the server)

The server verifies possession of the private key
without ever receiving it.

---

## Common SSH Files

- `~/.ssh/authorized_keys`  
  Controls which public keys are allowed to log in

- `~/.ssh/known_hosts`  
  Tracks previously connected hosts to prevent impersonation

---

## Security Considerations

- Avoid logging in as root directly
- Disable password authentication when possible
- Use strong, unique keys per environment
- Treat SSH access as privileged access

---

## Learning Perspective

SSH is not just a tool, but a trust relationship
between machines.

Understanding how SSH works helps prevent accidental
exposure and improves system confidence.

---

## Key Takeaways

- SSH is the primary access method for servers
- Key-based authentication is more secure than passwords
- Security is about design choices, not complexity
- Safe defaults enable long-term scalability
