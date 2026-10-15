# 🦉 OCockpitX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OCockpitX** — Cockpit Web Console Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline Cockpit web console configuration hardening auditor

---

## ✨ Features

- Offline, read-only audit of a Cockpit installation (live host or mounted image via --root) — never runs commands, never opens network connections
- cockpit.conf — AllowUnencrypted, Origins, LoginTo, AllowMultiHost, ProtocolHeader, ForwardedForHeader, MaxStartups, IdleTimeout, Banner, auth schemes, typos
- ws-certs.d — stdlib DER parser: expiry, key size, signature algorithm, self-signed, key permissions
- cockpit.socket / cockpit.service drop-ins — effective ListenStream resolution, --no-tls, --local-session
- PAM stack, disallowed-users, polkit .rules / .pkla, sudoers escalation path, machines.d, firewalld zones
- 80+ rules with severity, CWE, MITRE ATT&CK, remediation
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCockpitX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
