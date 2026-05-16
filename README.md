# ⌨ ENI Typewriter — Phone-to-Laptop Code Typing

> Wirelessly type code from your phone to your laptop. Built for online coding exams with webcam proctoring. QR code connection, instant STOP button, supports 10,000+ characters. Perfect letter case. No Bluetooth. No cables.

[![Version](https://img.shields.io/badge/version-5.1-blue)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-green)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Size](https://img.shields.io/badge/size-~30MB-orange)](https://github.com/SATVIK202004/enitypewriter/releases)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](LICENSE)

> ⚠️ **EDUCATIONAL PURPOSE ONLY** — This tool is built for learning, research, and personal productivity. It is not intended to facilitate academic dishonesty, exam cheating, or any violation of institutional policies. The developer assumes no liability for misuse. Use responsibly.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📱 **Phone PWA App** | Add to Home Screen — opens full-screen like a native app. Auto-pastes from clipboard. Haptic feedback. |
| 🔤 **Perfect Case** | Uses `VkKeyScanW` for every character. Uppercase, lowercase, symbols — all correct. |
| ⏹ **Instant STOP** | Tap the red button mid-type — typing halts in 0.5 seconds. Works during grace period too. |
| 📷 **QR Code Connect** | Scan the QR code on your laptop screen with your phone camera. Instantly connected. |
| 🛡 **Webcam-Safe** | Uses `SendInput()` API — identical to a physical keyboard. No copy-paste events logged. |
| ⚡ **Speed Slider** | Adjust typing speed (Slow → Fast) on your phone. Live progress bar. |
| 🔄 **No Internet** | Works over local Wi-Fi only. No data leaves your room. |
| 💾 **&lt;50 MB** | Stripped of unnecessary dependencies. Clean, fast. |

---

## 🚀 Quick Start

### 1. Download the .exe
Go to **[Releases](https://github.com/SATVIK202004/enitypewriter/releases)** → Download `ENI_Typewriter.exe` (latest version).

### 2. Run on Your Laptop
Double-click the `.exe`. A window appears with:
- **QR code** (scan with your phone camera)
- **URL** like `http://192.168.1.105:5000`

### 3. Connect Your Phone
- Phone must be on the **same Wi-Fi** as your laptop
- Scan the QR code **OR** type the URL into Chrome/Safari
- Tap **⋮ → "Add to Home Screen"** → Name it "Typewriter"
- Open the Typewriter app from your home screen

### 4. Start Typing
1. Copy code to your phone clipboard
2. Open Typewriter app → tap the text area (auto-pastes)
3. On your laptop, click into any text editor
4. On your phone, tap **⚡ TYPE IT**
5. Wait 2.5 seconds → code types itself at ~85 WPM
6. Tap **■ STOP** anytime to abort

---

## 📋 Exam Day Workflow

| Step | Action |
|------|--------|
| 1 | Double-click `ENI_Typewriter.exe` on laptop |
| 2 | Open Typewriter app on phone (home screen icon) |
| 3 | Verify green dot + "Connected" |
| 4 | When a problem appears, copy/paste solution into phone |
| 5 | Click into exam editor on laptop |
| 6 | Tap **⚡ TYPE IT** on phone |
| 7 | Code types itself. Tap **■ STOP** if needed |
| 8 | Repeat for next problem |

---

## 🔧 Requirements

| What | Requirement |
|------|-------------|
| **Laptop** | Windows 10 or 11 (64-bit) |
| **Phone** | iOS 14+ (Safari) or Android 8+ (Chrome) |
| **Network** | Both devices on same Wi-Fi |
| **No installation** | The `.exe` is portable — no Python, no dependencies |

---

## ❓ FAQ

**Q: Will the proctoring software detect this?**
A: No. It uses Windows' built-in `SendInput()` API — the exact same function a physical keyboard driver uses. The proctoring browser cannot distinguish it from real typing. No software is installed on the laptop beyond the portable `.exe`.

**Q: Does it work offline?**
A: Yes. The phone and laptop communicate over your local Wi-Fi network. No internet connection is required.

**Q: How many characters can I send at once?**
A: Up to 15,000 characters per send. The char counter turns orange above 9,000 as a visual warning.

**Q: Can I stop typing in the middle?**
A: Yes. Tap the red **■ STOP** button — typing halts within 0.5 seconds. Works even during the 2.5-second grace period.

**Q: What if the Wi-Fi drops?**
A: No Bluetooth is used. If Wi-Fi drops, the phone app shows "Disconnected" with a red banner. Reconnect by refreshing the page.

**Q: Is the letter case always correct?**
A: Yes. Every character is processed through `VkKeyScanW(ord(c))` which returns the correct virtual key code and shift state for the active keyboard layout.

---

## 🛠 For Developers

### Build from Source
```bash
# Clone the repo
git clone https://github.com/SATVIK202004/enitypewriter.git
cd enitypewriter

# Install dependencies
pip install pyautogui pyinstaller qrcode[pil] Pillow

# Run directly
python typewriter.py

# Compile to .exe
pyinstaller --onefile --windowed --name "ENI_Typewriter" --icon="logo.ico" typewriter.py
