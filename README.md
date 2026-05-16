<div align="center">

<img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 256 256'%3E%3Crect width='256' height='256' rx='44' fill='%230a0a0f'/%3E%3Crect x='70' y='80' width='116' height='96' rx='12' fill='%23161b22' stroke='%2330363d' stroke-width='2'/%3E%3Crect x='82' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='160' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='82' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='160' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='82' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='95' y='152' width='70' height='14' rx='3' fill='%2358a6ff' opacity='0.6'/%3E%3Ccircle cx='210' cy='46' r='12' fill='%233fb950'/%3E%3C/svg%3E" width="100" alt="ENI Typewriter Logo" />

# ⌨️ ENI Typewriter

### Phone-to-Laptop Code Typing — Wireless. Instant. Built for Productivity.

[![Version](https://img.shields.io/badge/version-5.1-blue?style=for-the-badge&logo=github)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-brightgreen?style=for-the-badge&logo=windows)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Size](https://img.shields.io/badge/size-~30MB-orange?style=for-the-badge&logo=files)](https://github.com/SATVIK202004/enitypewriter/releases)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge&logo=opensourceinitiative)](LICENSE)
[![Status](https://img.shields.io/badge/status-stable-success?style=for-the-badge)](https://github.com/SATVIK202004/enitypewriter/releases)

<br/>

> **Wirelessly stream text from your phone into any laptop editor — via QR code pairing, LAN-only communication, and native `SendInput()` keystroke simulation. No Bluetooth. No cables. No installs. Supports 15,000+ characters per send. Designed for developers, researchers, and legitimate productivity workflows.**

<br/>

[⬇️ Download .exe](https://github.com/SATVIK202004/enitypewriter/releases) · [🌐 Web App](https://enitypewriter.netlify.app/) · [📖 Quick Start](#-quick-start) · [❓ FAQ](#-faq)

</div>

---

> [!WARNING]
> **ETHICAL USE REQUIRED — READ CAREFULLY**
>
> This tool is built for **learning, research, accessibility, and personal productivity**. It is a keystroke automation utility — similar in principle to text expanders, macro tools, and assistive input devices that have existed for decades.
>
> **This software is NOT intended to:**
> - Facilitate academic dishonesty, exam fraud, or cheating of any kind
> - Violate institutional policies, honor codes, or terms of service
> - Bypass proctoring systems in academic or certification environments
> - Enable impersonation or misrepresentation of your work
>
> **The developer assumes ZERO liability for misuse.** By downloading or using this software, you agree that you are solely responsible for ensuring your use complies with all applicable policies, laws, and ethical standards. If you are unsure whether your intended use is permitted, consult your institution or do not use this tool.
>
> **Use responsibly. Use ethically. Use with care.**

---

## 📌 What Is ENI Typewriter?

ENI Typewriter is a **local-network keystroke injection tool** — it runs a lightweight server on your Windows laptop, exposes a Progressive Web App (PWA) interface on your phone (via QR code), and when triggered, streams text from phone to laptop using the Windows `SendInput()` API — the same low-level API used by physical keyboard drivers.

It is designed for legitimate scenarios where you need to **input large amounts of pre-written text** (code snippets, templates, boilerplate, accessibility scripts, repetitive documentation) into a desktop application from your phone, without relying on copy-paste, email, cloud sync, or any internet service.

**Legitimate use cases include:**
- Developers testing text-input interfaces across devices
- Accessibility tool for users with mobility impairments
- Productivity automation for repetitive text entry tasks
- Educational research on input APIs and network protocols
- Personal knowledge-base snippet injection into local IDEs

**This is not a cheating tool.** If you use it as one, you are misusing the software and violating its intended purpose.

---

## ✨ Feature Breakdown

| # | Feature | Detail |
|---|---------|--------|
| 📱 | **Phone PWA** | Add to home screen. Opens full-screen like a native app. Auto-pastes clipboard on tap. Haptic feedback on send. |
| 🔤 | **Perfect Character Accuracy** | Every character — uppercase, lowercase, symbol — resolved via `VkKeyScanW(ord(c))`. Zero case errors regardless of keyboard layout. |
| ⏹ | **Instant STOP** | Red abort button halts typing within **0.5 seconds**, even mid-stream or during the 2.5s grace window. |
| 📷 | **QR Code Pairing** | Auto-generates QR on launch. Scan once → instantly connected. No manual IP entry needed. |
| 🛡 | **Native Keystroke API** | Uses Windows `SendInput()` — byte-identical to physical keyboard events. No clipboard events. No paste logs. No synthetic input flags. |
| ⚡ | **Speed Control** | Variable speed slider (Slow → Fast) on the phone UI. Live character progress bar. |
| 🔄 | **Zero Internet** | All communication is LAN-only (`192.168.x.x`). No data touches external servers. |
| 💾 | **Ultra Lightweight** | Under 30MB. Portable `.exe` — no Python runtime, no VC++ redistributables, no installer. |
| 🔢 | **High Capacity** | Up to **15,000 characters** per send. Counter turns orange above 9,000 as a visual warning. |

> ℹ️ These features exist for productivity and accessibility. Misuse in academic or certification environments violates the spirit of this project.

---

## 🚀 Quick Start

### Step 1 — Download

Head to **[Releases](https://github.com/SATVIK202004/enitypewriter/releases)** and download `ENI_Typewriter.exe` (latest: v5.1).

No installation required. It's fully portable.

---

### Step 2 — Launch on Laptop

Double-click the `.exe`. A window will appear showing:
