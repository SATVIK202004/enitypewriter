# ⌨ ENI Typewriter — Phone-to-Laptop Code Typing

> Wirelessly type long code snippets from your phone to your laptop. QR code pairing, instant STOP, supports 15,000+ characters. No Bluetooth. No cables.

[![Version](https://img.shields.io/badge/version-5.1-blue)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-green)](https://github.com/SATVIK202004/enitypewriter/releases)
[![Size](https://img.shields.io/badge/size-~30MB-orange)](https://github.com/SATVIK202004/enitypewriter/releases)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](LICENSE)

---

## What It Does

ENI Typewriter lets your phone act as a wireless keyboard for your laptop. Copy any block of code or text on your phone — tap one button — and it types itself into whatever editor is focused on your laptop.

Built for situations where transferring large text blocks between devices is inconvenient: no cables, no cloud paste, no email-to-yourself.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📱 **Phone PWA** | Add to Home Screen for a full-screen native app feel. Auto-pastes from clipboard on open. |
| 🔤 **Perfect Case** | Uses `VkKeyScanW` for every character — uppercase, lowercase, and symbols all render correctly. |
| ⏹ **Instant STOP** | Tap the red button mid-type to halt within 0.5 seconds. |
| 📷 **QR Code Pairing** | Scan the QR on your laptop screen to connect instantly — no manual URL entry needed. |
| ⚡ **Speed Slider** | Adjust typing speed from slow to fast. Live progress bar shows remaining characters. |
| 🔒 **Local Only** | Communicates over your local Wi-Fi. No data leaves your network. |
| 💾 **< 50 MB** | Portable `.exe` — no installation, no Python, no dependencies needed on the laptop. |

---

## 🚀 Quick Start

### 1. Download

Go to **[Releases](https://github.com/SATVIK202004/enitypewriter/releases)** → download `ENI_Typewriter.exe`.

### 2. Run on Your Laptop

Double-click the `.exe`. A window opens showing:
- A **QR code** to scan with your phone
- A local URL like `http://192.168.1.105:5000`

### 3. Connect Your Phone

- Both devices must be on the **same Wi-Fi**
- Scan the QR code or enter the URL in Chrome/Safari
- Tap **⋮ → Add to Home Screen** → open from there for the best experience

### 4. Type

1. Copy your code to your phone clipboard
2. Open the Typewriter app — it auto-pastes into the text area
3. Click into your target editor on the laptop
4. Tap **⚡ TYPE IT** on your phone
5. Watch it type. Tap **■ STOP** anytime to abort.

---

## 🔧 Requirements

| | Requirement |
|---|---|
| **Laptop** | Windows 10 or 11 (64-bit) |
| **Phone** | iOS 14+ (Safari) or Android 8+ (Chrome) |
| **Network** | Both devices on the same Wi-Fi |

---

## ❓ FAQ

**Q: How many characters can I send at once?**  
Up to 15,000. The character counter turns orange above 9,000 as a heads-up.

**Q: Does it work without internet?**  
Yes. The phone and laptop communicate only over your local Wi-Fi.

**Q: What if Wi-Fi drops mid-type?**  
The app shows a red "Disconnected" banner. Refresh the page to reconnect.

**Q: Is letter case always correct?**  
Yes. Every character goes through `VkKeyScanW(ord(c))`, which returns the correct virtual key and shift state for the active keyboard layout.

**Q: Can I stop mid-type?**  
Yes — tap **■ STOP** and typing halts within 0.5 seconds, including during the initial grace period.

---

## 🛠 Build from Source

```bash
git clone https://github.com/SATVIK202004/enitypewriter.git
cd enitypewriter

pip install flask pyautogui pyinstaller qrcode[pil] Pillow

# Run directly
python typewriter.py

# Build .exe
pyinstaller --onefile --windowed --name "ENI_Typewriter" --icon="logo.ico" typewriter.py
```

---

## License

MIT — see [LICENSE](LICENSE).
