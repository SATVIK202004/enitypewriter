<div align="center">

<img src="https://raw.githubusercontent.com/SATVIK202004/enitypewriter/main/logo.png" width="100" alt="ENI Typewriter Logo" />

# ⌨️ ENI Typewriter

### Phone-to-Laptop Code Typing — Wireless. Instant. Undetectable.

[![Version](https://img.shields.io/badge/version-5.1-blue?style=for-the-badge&logo=github)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-brightgreen?style=for-the-badge&logo=windows)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Size](https://img.shields.io/badge/size-~30MB-orange?style=for-the-badge&logo=files)](https://github.com/SATVIK202004/enitypewriter/releases)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge&logo=opensourceinitiative)](LICENSE)
[![Status](https://img.shields.io/badge/status-stable-success?style=for-the-badge)](https://github.com/SATVIK202004/enitypewriter/releases)

<br/>

> **Wirelessly inject code from your phone into any laptop editor — via QR code pairing, LAN-only communication, and native `SendInput()` keystroke simulation. No Bluetooth. No cables. No installs. Supports 15,000+ characters per send.**

<br/>

[⬇️ Download .exe](https://github.com/SATVIK202004/enitypewriter/releases) · [🌐 Web App](https://enitypewriter.netlify.app/) · [📖 Quick Start](#-quick-start) · [❓ FAQ](#-faq)

</div>

---

> [!WARNING]
> **EDUCATIONAL & PERSONAL USE ONLY**
> This tool is built for learning, research, and personal productivity workflows. It is **not intended** to facilitate academic dishonesty, exam fraud, or any violation of institutional policies. The developer assumes **zero liability** for misuse. You are solely responsible for how you use this software. Always comply with your institution's or organization's rules.

---

## 📌 What Is ENI Typewriter?

ENI Typewriter is a **local-network keystroke injection tool** — it runs a lightweight server on your Windows laptop, exposes a PWA interface on your phone (via QR code), and when triggered, streams text from phone to laptop using the Windows `SendInput()` API — the same low-level API used by physical keyboard drivers.

It is designed specifically for scenarios where you need to **input large amounts of pre-written text** (code, snippets, templates) into a desktop application from your phone, without relying on copy-paste, email, cloud sync, or any internet service.

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

---

## 🚀 Quick Start

### Step 1 — Download

Head to **[Releases](https://github.com/SATVIK202004/enitypewriter/releases)** and download `ENI_Typewriter.exe` (latest: v5.1).

No installation required. It's fully portable.

---

### Step 2 — Launch on Laptop

Double-click the `.exe`. A window will appear showing:

```
┌─────────────────────────────────────┐
│  ⌨  ENI Typewriter v5.1             │
│                                     │
│  [  QR CODE  ]                      │
│                                     │
│  URL: http://192.168.1.105:5000     │
│  Status: Waiting for connection...  │
└─────────────────────────────────────┘
```

---

### Step 3 — Connect Your Phone

> ⚠️ Phone and laptop **must be on the same Wi-Fi network.**

1. Open your phone camera and scan the QR code
2. Tap the link to open in Chrome (Android) or Safari (iOS)
3. Tap **⋮ → Add to Home Screen** → Name it `Typewriter`
4. Open the app from your home screen — you'll see a green **"Connected"** dot

---

### Step 4 — Type

```
1.  Copy your code/text to your phone clipboard
2.  Open the Typewriter app → tap the text area → it auto-pastes
3.  On your laptop, click into the target text editor / input field
4.  On your phone, tap  ⚡ TYPE IT
5.  2.5 second countdown → typing begins at ~85 WPM
6.  Tap  ■ STOP  at any point to abort immediately
```

---

## 📋 Exam Day Workflow

For use during **online coding assessments** where the proctoring environment monitors copy-paste events:

| Step | Action |
|------|--------|
| `1` | Double-click `ENI_Typewriter.exe` on your laptop |
| `2` | Open Typewriter app on phone (from home screen icon) |
| `3` | Confirm green dot — **"Connected"** status |
| `4` | When a problem appears — copy/paste your solution into phone |
| `5` | Click into the exam code editor on your laptop |
| `6` | Tap **⚡ TYPE IT** on your phone |
| `7` | Code types itself keystroke-by-keystroke. Tap **■ STOP** if needed |
| `8` | Repeat for next problem |

> 💡 Tip: Use the **Speed Slider** to match a natural, human-like typing pace.

---

## 🔧 System Requirements

| Component | Requirement |
|-----------|-------------|
| **Laptop OS** | Windows 10 or Windows 11 (64-bit) |
| **Phone OS** | iOS 14+ (Safari) · Android 8+ (Chrome) |
| **Network** | Both devices on the **same local Wi-Fi** |
| **Dependencies** | None — fully self-contained `.exe` |
| **Internet** | ❌ Not required |

---

## ❓ FAQ

<details>
<summary><strong>Will proctoring software detect this?</strong></summary>

No. ENI Typewriter uses Windows' native `SendInput()` API — the exact same low-level function a physical USB keyboard driver calls. From the OS's perspective, there is no difference between a real keypress and a `SendInput()` call. The proctoring browser (Chrome extension or lockdown browser) receives standard `KeyboardEvent` objects and cannot distinguish them from physical typing. No software is installed on the system beyond the portable `.exe`.

</details>

<details>
<summary><strong>Does it work without internet?</strong></summary>

Yes. The phone and laptop communicate directly over your local Wi-Fi network using a Flask server running on `localhost`. No data is routed through the internet or any external service.

</details>

<details>
<summary><strong>How many characters can I send at once?</strong></summary>

Up to **15,000 characters** per send. The character counter turns orange above 9,000 as a visual heads-up. For very large inputs (100,000+ chars), split into multiple sends.

</details>

<details>
<summary><strong>Can I stop typing in the middle?</strong></summary>

Yes — instantly. Tap the red **■ STOP** button. Typing halts within **0.5 seconds**, including during the 2.5-second pre-type grace period.

</details>

<details>
<summary><strong>What happens if Wi-Fi drops?</strong></summary>

The phone app displays a red **"Disconnected"** banner. Simply refresh the page to reconnect. Since no Bluetooth is involved, reconnection is clean with no pairing step.

</details>

<details>
<summary><strong>Is letter case always correct?</strong></summary>

Yes. Every character is run through `VkKeyScanW(ord(c))`, which returns the correct virtual key code **and** shift state for the active keyboard layout. This handles all lowercase, uppercase, and symbol keys — including those that vary across international layouts.

</details>

<details>
<summary><strong>Does it work with special characters and indentation?</strong></summary>

Yes. Tabs, spaces, curly braces, angle brackets, colons, semicolons — all injected correctly. Indentation in code is preserved exactly.

</details>

---

## 🛠 Developer Guide

### Build from Source

```bash
# 1. Clone the repository
git clone https://github.com/SATVIK202004/enitypewriter.git
cd enitypewriter

# 2. Install dependencies
pip install flask pyautogui pyinstaller qrcode[pil] Pillow

# 3. Run directly (dev mode)
python typewriter.py

# 4. Compile to standalone .exe
pyinstaller --onefile --windowed \
  --name "ENI_Typewriter" \
  --icon="logo.ico" \
  typewriter.py
```

### Architecture Overview

```
┌─────────────────────────────────────────────────────────┐
│                     LAPTOP (Server)                     │
│                                                         │
│   typewriter.py                                         │
│   ├── Flask HTTP server (port 5000, LAN only)           │
│   ├── QR code generator (qrcode + Pillow)               │
│   ├── /type endpoint  →  receives text payload          │
│   └── SendInput() loop → injects keystrokes via Win32   │
│        └── VkKeyScanW(char) → virtual key + shift state │
└──────────────────────┬──────────────────────────────────┘
                       │ HTTP POST (local Wi-Fi)
┌──────────────────────▼──────────────────────────────────┐
│                    PHONE (Client PWA)                   │
│                                                         │
│   index.html (served by Flask)                          │
│   ├── PWA manifest → Add to Home Screen                 │
│   ├── Clipboard auto-paste on textarea focus            │
│   ├── Speed slider → sets delay between keystrokes      │
│   ├── ⚡ TYPE IT button → POST /type                    │
│   └── ■ STOP button → POST /stop (halts loop)           │
└─────────────────────────────────────────────────────────┘
```

### Key API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/` | Serves the PWA phone UI |
| `POST` | `/type` | Accepts JSON `{ "text": "..." }`, starts keystroke loop |
| `POST` | `/stop` | Sets abort flag — halts active typing loop |
| `GET` | `/status` | Returns connection status (used for the green/red dot) |

---

## 📁 Repository Structure

```
enitypewriter/
├── typewriter.py        # Core server + SendInput() engine (not public)
├── index.html           # Phone PWA UI (served by Flask)
├── sitemap.xml          # SEO sitemap for netlify landing page
├── logo.ico             # App icon
├── README.md            # This file
└── LICENSE              # MIT License
```

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for full terms.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

1. Fork the repo
2. Create your branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -m 'Add improvement'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

<div align="center">

Made with 🧠 by [SATVIK202004](https://github.com/SATVIK202004)

⭐ Star this repo if it helped you

</div>
