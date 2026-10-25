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

OCockpitX is an offline, read-only auditor for the Cockpit web console configuration that never runs commands or opens network connections. It reviews cockpit.conf, ws-certs.d certificates (via a stdlib DER parser), the cockpit.socket/service units, the PAM stack, polkit rules and firewalld exposure. More than 80 rules carry severity, CWE and MITRE ATT&CK tags with remediation, and it can audit a live host or a mounted image via --root.

---

## ✨ Features

- cockpit.conf checks: AllowUnencrypted, Origins, LoginTo, AllowMultiHost, IdleTimeout
- ws-certs.d stdlib DER parser: expiry, key size, signature algorithm, self-signed, perms
- cockpit.socket/service drop-in analysis with effective ListenStream resolution
- PAM stack, disallowed-users, polkit rules and sudoers escalation review
- 80+ rules with severity, CWE and MITRE ATT&CK plus remediation
- Hardened templates and export TXT/MD/JSON/CSV/SARIF 2.1.0

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCockpitX --scan
./OCockpitX --conf /etc/cockpit/cockpit.conf --format json -o report.json --fail-on high
./OCockpitX --root /mnt/image --scan
./OCockpitX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
