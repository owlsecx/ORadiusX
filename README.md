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

Offline AAA / RADIUS (FreeRADIUS) server configuration auditor

---

## ✨ Features

- Stdlib FreeRADIUS config parser (sections, pairs, unlang words, quoted strings, ${var} expansion)
- clients.conf — default 'testing123', short / guessable / reused secrets, 0.0.0.0/0 clients, Message-Authenticator (BlastRADIUS CVE-2024-3596), limit_proxy_state
- radiusd.conf — run-as user, core dumps, password logging, vulnerable OpenSSL, status_server, wildcard listeners, control-socket rw without uid restriction
- EAP — tls_min_version, cipher_list, private_key_password, check_crl, auto_chain, MD5 / LEAP, MSCHAPv2 preference, PEAP / TTLS inner virtual server, bootstrap test certs
- ldap / sql / proxy.conf / detail / linelog / users file
- World-readable secrets & private keys, inner-tunnel copy
- Secrets masked everywhere; --root discovery; CWE + MITRE
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORadiusX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
