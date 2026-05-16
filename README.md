<div align="center">

<img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 256 256'%3E%3Crect width='256' height='256' rx='44' fill='%230a0a0f'/%3E%3Crect x='70' y='80' width='116' height='96' rx='12' fill='%23161b22' stroke='%2330363d' stroke-width='2'/%3E%3Crect x='82' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='160' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='82' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='160' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='82' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='95' y='152' width='70' height='14' rx='3' fill='%2358a6ff' opacity='0.6'/%3E%3Ccircle cx='210' cy='46' r='12' fill='%233fb950'/%3E%3C/svg%3E" width="100" alt="ENI Typewriter Logo" />

# ⌨️ ENI Typewriter

### Phone-to-Laptop Code Typing — Wireless. Instant. Built for Developers.

[![Version](https://img.shields.io/badge/version-5.1-blue?style=for-the-badge&logo=github)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-brightgreen?style=for-the-badge&logo=windows)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Size](https://img.shields.io/badge/size-~30MB-orange?style=for-the-badge&logo=files)](https://github.com/SATVIK202004/enitypewriter/releases)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge&logo=opensourceinitiative)](LICENSE)
[![Status](https://img.shields.io/badge/status-stable-success?style=for-the-badge)](https://github.com/SATVIK202004/enitypewriter/releases)

<br/>

> **Wirelessly transmit text from your phone into any laptop editor — via QR code pairing, LAN-only communication, and native `SendInput()` keystroke simulation. No Bluetooth. No cables. No installs. Supports 15,000+ characters per send. Designed for legitimate developer productivity, learning, and accessibility workflows.**

<br/>

[⬇️ Download .exe](https://github.com/SATVIK202004/enitypewriter/releases) · [🌐 Web App](https://enitypewriter.netlify.app/) · [📖 Quick Start](#-quick-start) · [❓ FAQ](#-faq)

</div>

---

> [!CAUTION]
> ## ⚠️ IMPORTANT — PLEASE READ BEFORE USE
> **This tool is designed for legitimate educational, research, personal productivity, and accessibility purposes only.**
>
> It is **NOT intended** to:
> - Facilitate academic dishonesty, exam fraud, or cheating of any kind
> - Violate institutional policies, honor codes, or proctoring guidelines
> - Circumvent assessment integrity measures imposed by universities, certification bodies, or employers
>
> **The developer explicitly condemns misuse and assumes zero liability for any unauthorized or unethical use.**
> By downloading or using this software, you accept full and sole responsibility for ensuring your use complies with all applicable rules, policies, and laws. If you are unsure whether your intended use is permitted, **do not use this tool.** Always seek clarification from your institution or organization first.
>
> **This is a tool. Tools are neutral. How you use it defines you.**

---

## 📌 What Is ENI Typewriter?

ENI Typewriter is a **local-network keystroke injection tool** — it runs a lightweight server on your Windows laptop, exposes a PWA interface on your phone (via QR code), and when triggered, streams text from phone to laptop using the Windows `SendInput()` API — the same low-level API used by physical keyboard drivers.

### ✅ Legitimate Use Cases

- **Developers** transferring code snippets, configuration blocks, or boilerplate between devices without cloud sync
- **Students** practicing coding problems in a local IDE with solutions referenced from a phone
- **Accessibility** — users who find phone typing easier and need to input text into desktop applications
- **Productivity** — pasting pre-written templates, email drafts, or documentation into desktop tools
- **Research & Learning** — studying keystroke simulation, local networking, PWA architecture, and Win32 API behavior

### ❌ Prohibited Use Cases

- Any activity that violates your institution's academic integrity policy
- Circumventing online exam proctoring systems or remote assessment tools
- Any form of dishonesty, fraud, or misrepresentation
- Any use that breaks local laws or institutional rules

> **When in doubt, don't use it. Your integrity is worth more than any shortcut.**

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
| ⚠️ | **Use Responsibly** | This tool is a powerful utility. Its capabilities demand responsible use. Always ensure your usage aligns with applicable policies. |

---

## 🚀 Quick Start

> [!IMPORTANT]
> **Before using this tool, confirm that your intended use is permitted by your institution, organization, or the platform you are interacting with. This tool is designed for legitimate productivity — using it to bypass assessment integrity measures is prohibited.**

### Step 1 — Download

Head to **[Releases](https://github.com/SATVIK202004/enitypewriter/releases)** and download `ENI_Typewriter.exe` (latest: v5.1).

No installation required. It's fully portable.

---

### Step 2 — Launch on Laptop

Double-click the `.exe`. A window will appear showing:
