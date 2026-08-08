# SyMirror

![Version](https://img.shields.io/badge/version-v1.1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)
![License](https://img.shields.io/badge/license-Proprietary-red.svg)

**SyMirror** is a Windows screen mirroring tool that lets you display and control your Android device from your computer - similar to scrcpy but with enhanced features.

## ✨ Features

- **Screen Mirroring** - Display your Android screen on Windows with low latency
- **Full Input Control** - Mouse, keyboard, and touch events
- **Audio Forwarding** - Hear device audio on your PC
- **Clipboard Sync** - Copy/paste between devices
- **📸 Screenshot Capture** - Save screenshots as PNG with one click (NEW in v1.1.0!)
- **⏺ Screen Recording** - Record your device screen to MP4 (NEW in v1.1.0!)
- **Multi-Device Support** - Connect multiple Android devices
- **Wireless ADB** - Connect over TCP/IP

## 🆕 What's New in v1.1.0

### 📸 Screenshot Capture
- Click the **camera button (📷)** in the toolbar
- Captures the current device screen instantly
- Saves as PNG with timestamp: `Screenshot_YYYYMMDD_HHMMSS.png`
- Automatically saved to: `%USERPROFILE%\Pictures\SyMirror\`

### ⏺ Screen Recording
- Click the **record button (⏺)** to start recording
- **Visual feedback:** Record button turns **red** when active
- **Title bar indicator:** Shows **"• REC"** while recording
- Click the **stop button (⏹)** to finish
- Encodes to H.264 and muxes into MP4
- Automatically saved to: `%USERPROFILE%\Videos\SyMirror\`
- File format: `Recording_YYYYMMDD_HHMMSS.mp4`

### 🎨 UI Improvements
- **About Dialog fixed** - Removed stray '&' character (WinForms mnemonic issue)
- **Toolbar updated** - Added camera and record buttons with clear icons
- **Better visual feedback** - Clear status indication for active recording

## 📥 Download

**Latest Version:** [v1.1.0](https://github.com/infoamsunlocker-create/SyMirror/releases/tag/v1.1.0)

Download the `SyMirror_v1.1.0.rar` file from the releases section.

## 🚀 Quick Start

1. **Download** the latest release RAR
2. **Extract** all files to a folder on your computer
3. **Run** `SyMirror.exe` as **Administrator**
4. **Enable USB Debugging** on your Android device (Settings → Developer Options)
5. **Connect** your device via USB
6. **Start** mirroring!

## 📸 Screenshots

### Main Mirroring View
SyMirror displaying the Pixel 6a screen with full control:

![Main View](https://i.ibb.co/KYCjM2t/screenshot-main-view.png)

### Screenshot & Recording Features
New camera (📷) and record (⏺) buttons in the toolbar:

![Screenshot Feature](https://i.ibb.co/HTj9PgtZ/screenshot.png)

### Recording in Action
Screen recording with visual feedback:

![Recording](https://i.ibb.co/N2wFNdKQ/Recording.png)

### About Dialog
Developer credit and version information (UI improved in v1.1.0):

![About Dialog](https://i.ibb.co/Kzj9Yd4J/screenshot-about-dialog.png)

### Error Handling
Clear feedback when connection issues occur:

![Error State](https://i.ibb.co/PdBScns/screenshot-disconnect-state.png)

## 📋 Requirements

- Windows 10 or later (64-bit)
- Android 5.0+ with USB Debugging enabled
- .NET Runtime 6.0+ (installed automatically if missing)

## ⚠️ Important

- **Keep all DLL files** in the same folder as `SyMirror.exe`
- **Run as Administrator** for full functionality
- Do NOT delete `scrcpy-server.jar` - it's essential

## 📝 Changelog

### v1.1.0 (2026-08-05)
- **New:** Screenshot capture - click camera button to save PNG to `Pictures\SyMirror\`
- **New:** Screen recording - click record button to save MP4 to `Videos\SyMirror\`
- **Fixed:** About dialog UI - removed stray '&' character issue
- **Improved:** Recording indicator shows "• REC" in title bar when active
- **Improved:** Record button turns red and changes to ⏹ when recording

### v1.0.0 (2026-08-04)
- Initial release
- Screen mirroring with mouse/keyboard control
- Audio forwarding
- Clipboard sync
- USB and wireless ADB support

## 🔧 Troubleshooting

### Common Issues & Solutions

#### 1. Keyboard and Mouse Not Working (Xiaomi Devices)
On some devices (especially **Xiaomi**), you might face keyboard and mouse not working problem. 

**Solution:**
1. Go to **Settings** → **Developer Options**
2. Enable **USB debugging (Security Settings)** 
   > ⚠️ This is a different option from the regular `USB debugging`
3. **Reboot your device** - this is required for the setting to take effect
4. Reconnect your device and try again

#### 2. "Device Disconnected" or "Video socket closed unexpectedly"
**Solution:**
- Check your USB cable - try a different cable or port
- Reboot your Android device
- Restart SyMirror
- Ensure USB Debugging is still enabled

#### 3. ADB Connection Issues
**Solution:**
- Run `adb kill-server` and `adb start-server` in Command Prompt
- Revoke USB debugging authorizations on your device and reconnect
- Check if your device is recognized: `adb devices`

#### 4. Antivirus False Positives
Some antivirus software may flag the tool incorrectly.

**Solution:**
- Add `SyMirror.exe` to your antivirus exceptions list
- Temporarily disable antivirus while running (the tool is safe)

### General Tips
1. **Extract all files** from the RAR/ZIP (do NOT run from inside the archive)
2. **Run as Administrator** - this is essential for proper functionality
3. **Check USB Debugging** is enabled in Developer Options
4. **Try different USB cables** - some cables only support charging
5. **Restart both devices** - PC and Android

## 📜 Credits

Built with these open-source projects:
- [scrcpy](https://github.com/Genymobile/scrcpy) (Apache 2.0) - Android screen capture
- [FFmpeg](https://ffmpeg.org/) (LGPL) - Video/audio processing
- [NAudio](https://github.com/naudio/NAudio) (MIT) - Audio playback

---

**⚠️ This is a closed-source tool. No source code is provided.**
