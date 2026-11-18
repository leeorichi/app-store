# Leeorichi App Store & OTA Hub 📱💻🚀

Personal Multi-Platform App Showcase, Direct Distribution & Over-The-Air (OTA) Serverless Hub (Android & macOS).

Hosted globally via **GitHub Pages** with Fastly Edge CDN.

## 🌐 Live Web Showcase
👉 **Custom Domain:** **[https://leeorichi.is-a.dev](https://leeorichi.is-a.dev)**  
👉 **GitHub Pages Origin:** **[https://leeorichi.github.io/app-store/](https://leeorichi.github.io/app-store/)**

---

## 📂 Repository Structure

```text
app-store/
├── index.html                           # Showcase Landing Page & Mini App Store
├── style.css                            # Modern Glassmorphic Dark UI
├── reelcast/                            # Project 1: ReelCast (Android & Android TV)
│   ├── version.json                     # OTA Update API endpoint for ReelCast
│   ├── ReelCast-v1.1.2.apk              # Versioned APK
│   ├── ReelCast-latest.apk              # Latest APK permanent link
│   └── icon.svg                         # Vector Icon
├── sync-clipboard/                      # Project 2: Sync Clipboard (E2EE) (Android & macOS)
│   ├── version.json                     # OTA Update API endpoint for Sync Clipboard
│   ├── SyncClipboard-v1.0.3.apk         # Versioned APK
│   ├── SyncClipboard-latest.apk         # Latest APK permanent link
│   ├── SyncClipboard-macOS-universal.zip# macOS Universal App
│   └── icon.svg                         # Vector Icon
├── mactools/                            # Project 3: MacTools (macOS Menu Bar System Monitor)
│   ├── version.json                     # OTA Update API endpoint for MacTools
│   ├── MacTools-v1.1.1-macOS-universal.zip # Versioned Universal Binary Release
│   ├── MacTools-latest.zip              # Latest ZIP permanent link
│   ├── MacTools-macOS-universal.zip     # Universal Binary permanent alias
│   └── icon.svg                         # Vector Icon
└── tiyo2mp3/                            # Project 4: TiYo2mp3 (Android Media Downloader)
    ├── version.json                     # OTA Update API endpoint for TiYo2mp3
    ├── TiYo2mp3-v1.0.2.apk              # Versioned APK
    ├── TiYo2mp3-latest.apk              # Latest APK permanent link
    └── icon.svg                         # Vector Icon
```

---

## 📡 OTA Endpoints

### 1. ReelCast (Android & Android TV)
- **Version Endpoint:** `https://leeorichi.github.io/app-store/reelcast/version.json`
- **Latest APK Download:** `https://leeorichi.github.io/app-store/reelcast/ReelCast-latest.apk`

### 2. Sync Clipboard (Android & macOS)
- **Version Endpoint:** `https://leeorichi.github.io/app-store/sync-clipboard/version.json`
- **Latest APK Download:** `https://leeorichi.github.io/app-store/sync-clipboard/SyncClipboard-latest.apk`
- **macOS Universal App:** `https://leeorichi.github.io/app-store/sync-clipboard/SyncClipboard-macOS-universal.zip`

### 3. MacTools (macOS 13+)
- **Showcase Link:** `https://leeorichi.github.io/app-store/#mactools`
- **Version Endpoint:** `https://leeorichi.github.io/app-store/mactools/version.json`
- **Latest App Download (ZIP):** `https://leeorichi.github.io/app-store/mactools/MacTools-latest.zip`
- **Universal App (M-Series & Intel):** `https://leeorichi.github.io/app-store/mactools/MacTools-v1.1.1-macOS-universal.zip`

---

## 📱 Apps Overview

| App Name | Platform | Version | Showcase Link | Download |
| :--- | :--- | :--- | :--- | :--- |
| **ReelCast** | Android / TV | `v1.1.2` | [#reelcast](https://leeorichi.github.io/app-store/#reelcast) | [Tải APK](https://leeorichi.github.io/app-store/reelcast/ReelCast-latest.apk) |
| **TiYo2mp3** | Android | `v1.0.2` | [#tiyo2mp3](https://leeorichi.github.io/app-store/#tiyo2mp3) | [Tải APK](https://leeorichi.github.io/app-store/tiyo2mp3/TiYo2mp3-latest.apk) |
| **Sync Clipboard** | Android / macOS / Web | `v1.0.3` | [#sync-clipboard](https://leeorichi.github.io/app-store/#sync-clipboard) | [Tải APK](https://leeorichi.github.io/app-store/sync-clipboard/SyncClipboard-latest.apk) • [Tải macOS](https://leeorichi.github.io/app-store/sync-clipboard/SyncClipboard-macOS-universal.zip) |
| **MacTools** | macOS Universal | `v1.1.1` | [#mactools](https://leeorichi.github.io/app-store/#mactools) | [Tải macOS ZIP](https://leeorichi.github.io/app-store/mactools/MacTools-latest.zip) |

---

## 🚀 How to Add a New App / Release

1. **New Release for an Existing App (e.g. MacTools):**
   - Build universal `.app` bundle and zip into `mactools/MacTools-vX.Y.Z-macOS-universal.zip` and `mactools/MacTools-latest.zip`.
   - Update `mactools/version.json` with new `versionCode`, `versionName`, and `changelog`.
   - Commit & push:
     ```bash
     git add .
     git commit -m "release(mactools): update to vX.Y.Z"
     git push origin main
     ```

2. **Add a Brand New App:**
   - Create a new directory, e.g. `myapp/`.
   - Add `version.json`, release binaries (`.apk` or `.zip`), and `icon.svg`.
   - Add a new App Card inside `index.html`.
   - Commit & push.
