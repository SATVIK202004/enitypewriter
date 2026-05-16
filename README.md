<div align="center">

<img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 256 256'%3E%3Crect width='256' height='256' rx='44' fill='%230a0a0f'/%3E%3Crect x='70' y='80' width='116' height='96' rx='12' fill='%23161b22' stroke='%2330363d' stroke-width='2'/%3E%3Crect x='82' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='160' y='92' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='82' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='160' y='112' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='82' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='108' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='134' y='132' width='20' height='14' rx='3' fill='%2358a6ff'/%3E%3Crect x='95' y='152' width='70' height='14' rx='3' fill='%2358a6ff' opacity='0.6'/%3E%3Ccircle cx='210' cy='46' r='12' fill='%233fb950'/%3E%3C/svg%3E" width="100" alt="ENI Typewriter Logo" />

<img src="https://raw.githubusercontent.com/SATVIK202004/enitypewriter/main/logo.png" width="100" alt="ENI Typewriter Logo" />

# ⌨️ ENI Typewriter

### Phone-to-Laptop Code Typing — Wireless. Instant. Built for Developers.

[![Version](https://img.shields.io/badge/version-5.1-blue?style=for-the-badge&logo=github)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-brightgreen?style=for-the-badge&logo=windows)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Size](https://img.shields.io/badge/size-~30MB-orange?style=for-the-badge&logo=files)](https://github.com/SATVIK202004/enitypewriter/releases)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge&logo=opensourceinitiative)](LICENSE)
[![Status](https://img.shields.io/badge/status-stable-success?style=for-the-badge)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Ethics](https://img.shields.io/badge/use-ethically%20only-red?style=for-the-badge)](README.md)

<br/>

> **Wirelessly inject code from your phone into any laptop editor — via QR code pairing, LAN-only communication, and native `SendInput()` keystroke simulation. No Bluetooth. No cables. No installs. Supports 15,000+ characters per send.**

<br/>

[⬇️ Download .exe](https://github.com/SATVIK202004/enitypewriter/releases) · [🌐 Web App](https://enitypewriter.netlify.app/) · [📖 Quick Start](#-quick-start) · [❓ FAQ](#-faq)

</div>

---

> [!CAUTION]
> ## 🚫 NOT FOR ACADEMIC CHEATING — READ BEFORE USE
>
> This tool **must not** be used to cheat in exams, bypass proctoring systems, commit academic dishonesty, or violate any institutional, organizational, or professional policy.
>
> **Using this tool to cheat:**
> - Violates your institution's academic integrity code
> - Can result in permanent expulsion, degree revocation, or legal consequences
> - Undermines your own learning and skill development
> - Is unfair to every student who prepares honestly
>
> The developer **explicitly condemns** any use of this tool for academic fraud. The MIT License grants technical freedom — not ethical permission. **You are solely and fully responsible for how you use this software.** If you are unsure whether your intended use is permitted, assume it is not and do not proceed.

---

> [!WARNING]
> ## ⚠️ EDUCATIONAL & PERSONAL USE ONLY
> This tool is built for **personal productivity, developer workflows, legitimate learning environments, and research**. It is **not intended** to facilitate academic dishonesty, exam fraud, or any violation of institutional policies. The developer assumes **zero liability** for misuse. Always comply with your institution's or organization's rules before using any tool in a professional or academic setting.

---

## 📌 What Is ENI Typewriter?

ENI Typewriter is a **local-network keystroke injection tool** — it runs a lightweight server on your Windows laptop, exposes a PWA interface on your phone (via QR code), and when triggered, streams text from phone to laptop using the Windows `SendInput()` API — the same low-level API used by physical keyboard drivers.

It is designed specifically for **legitimate scenarios** where you need to **input large amounts of pre-written text** (code snippets, templates, personal notes, practice problems) into a desktop application from your phone, without relying on copy-paste, email, cloud sync, or any internet service.

**Legitimate use cases include:**
- 🧑‍💻 Developers transferring code snippets from phone notes to a desktop IDE
- 📋 Professionals who draft content on mobile and want to inject it hands-free into desktop tools
- ♿ Accessibility workflows where physical keyboard use is limited
- 🎓 Personal practice sessions where you review solutions on your phone and want to type them out for muscle memory
- 🛠 Live demos or presentations where pre-written content needs to be "typed" naturally

> [!IMPORTANT]
> **If your use case involves an exam, assessment, or any form of evaluation — stop. Do not use this tool. There is no legitimate reason to run ENI Typewriter during a proctored test.**

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

> [!NOTE]
> This workflow is intended for **your own text, in your own environment**. Use it in personal projects, practice environments, local development setups, or any context where you have full permission to operate freely.

---

## 📋 Personal Practice Workflow

A great use case: reviewing your own solutions on your phone and practicing typing them out on your laptop — excellent for learning, muscle memory, and building genuine coding speed.

> [!CAUTION]
> **This workflow is for personal practice only — NOT for live exams, assessments, or any evaluated environment.** If you are in an exam right now, close this tool immediately.

| Step | Action |
|------|--------|
| `1` | Double-click `ENI_Typewriter.exe` on your laptop |
| `2` | Open Typewriter app on phone (from home screen icon) |
| `3` | Confirm green dot — **"Connected"** status |
| `4` | Copy your practice snippet or solution into the phone |
| `5` | Click into your local code editor on your laptop |
| `6` | Tap **⚡ TYPE IT** on your phone |
| `7` | Code types itself keystroke-by-keystroke. Tap **■ STOP** if needed |
| `8` | Repeat for the next snippet |

> 💡 Tip: Use the **Speed Slider** to match a natural, comfortable typing pace while practicing.

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
<summary><strong>Who is this tool actually built for?</strong></summary>

ENI Typewriter is built for developers, students doing personal practice, and productivity-focused users who want a seamless way to move text from their phone into a desktop editor — without copy-paste, cloud sync, or cables. It is a **developer productivity tool**, not a cheating aid.

</details>

<details>
<summary><strong>Can I use this in an exam?</strong></summary>

**No. Absolutely not.** Using ENI Typewriter — or any similar tool — in a proctored exam, online assessment, or any evaluated context is academic dishonesty. It violates institutional integrity policies and can result in serious consequences including expulsion. This tool is not designed for, marketed toward, or supportive of that use case. Do not do it.

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
| `POST` | `/type` | Accepts JSON `{ "text": "..." }` , starts keystroke loop |
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

## ⚖️ Ethical Use Policy

This software is released under the MIT License, which grants broad technical freedoms. However, **technical freedom is not ethical permission.**

The following uses are explicitly **prohibited and condemned** by the developer:

- ❌ Using ENI Typewriter during any exam, quiz, test, or assessment
- ❌ Bypassing proctoring or monitoring systems of any kind
- ❌ Facilitating academic dishonesty on behalf of yourself or others
- ❌ Using the tool in any context that violates an institution's or employer's policies

The following uses are the **intended purpose** of this tool:

- ✅ Personal developer productivity (moving code from phone to PC)
- ✅ Accessibility-driven text input workflows
- ✅ Personal practice and self-study with your own material
- ✅ Live demos, presentations, and content creation
- ✅ Research and educational tool development

> [!WARNING]
> If you are a student: the real skill is in your head, not in a tool. Building genuine problem-solving ability will serve your career far longer than any shortcut. Use tools to learn faster — not to avoid learning.

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for full terms.

The MIT License permits use, modification, and distribution. It does **not** grant permission to use this software unethically, dishonestly, or in violation of any applicable rules, regulations, or policies.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

> [!NOTE]
> Contributions that add features specifically designed to evade proctoring, detection systems, or academic monitoring will be **rejected without review**. Contributions must align with the tool's legitimate productivity purpose.

1. Fork the repo
2. Create your branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -m 'Add improvement'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

<div align="center">

Made with 🧠 by [SATVIK202004](https://github.com/SATVIK202004)

⭐ Star this repo if it helped your **legitimate** workflow

**Build real skills. Use tools responsibly.**

</div>
