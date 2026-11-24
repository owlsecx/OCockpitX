# 🦉 OCockpitX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OCockpitX --help   # watch every network call
firejail --net=none ./OCockpitX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
