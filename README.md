# 🦉 ORadiusX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **ORadiusX** — Offline AAA / RADIUS Server Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

ORadiusX is an offline, read-only auditor for FreeRADIUS/radiusd AAA configurations. It parses raddb trees, clients.conf and EAP modules to flag weak secrets, the BlastRADIUS vulnerability (CVE-2024-3596), EAP/TLS issues and insecure proxy, LDAP and SQL settings. Secrets are masked and findings map to CWE and MITRE.

---

## ✨ Features

- Stdlib FreeRADIUS parser handling sections, unlang words and ${var} expansion
- clients.conf checks for default/short/reused secrets and BlastRADIUS (CVE-2024-3596)
- radiusd.conf review of run-as user, core dumps, password logging and listeners
- EAP/TLS analysis of protocol versions, ciphers, CRL, MSCHAPv2 and inner tunnels
- ldap/sql/proxy.conf and users-file checks plus world-readable secret/key detection
- TXT/Markdown/JSON/CSV/SARIF export, --root discovery and CI gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORadiusX --home /etc/freeradius/3.0
./ORadiusX --clients clients.conf --sarif -o report.sarif
./ORadiusX --scan --root /mnt/collected --fail-on high
./ORadiusX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
