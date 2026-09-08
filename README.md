<p align="center">
  <img src="https://raw.githubusercontent.com/siddgithub2022/ASM_Cloud/main/assets/logo.svg" width="520" alt="ASM_Cloud"/>
</p>

<h1 align="center">ASM_Cloud — Public Downloads</h1>
<p align="center"><b>Your files. Your drive. Your cloud.</b> — Server EXE + Desktop EXE + Android APK + iOS IPA<br/>
Source is <b>private</b> at <a href="https://github.com/siddgithub2022/ASM_Cloud">siddgithub2022/ASM_Cloud</a> (PRIVATE) • Binaries are <b>public</b> here</p>

<p align="center">
  <a href="https://github.com/siddgithub2022/ASM_Cloud-Releases/releases"><img alt="Release" src="https://img.shields.io/badge/release-v0.8.0-blue?style=for-the-badge"/></a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20Android%20%7C%20iOS-lightgrey?style=flat-square"/>
  <img alt="License" src="https://img.shields.io/badge/license-MIT-green?style=flat-square"/>
</p>

---

## 📥 Downloads — v0.8.0 (Phase 1–8, Professional)

> **For laymen:** Download for your device, double-click to install. No coding. Copy-paste server `.env` once.

| Platform | File | Size | How to Install | SHA256 |
|----------|------|------|----------------|--------|
| **Server — Windows** | `ASM_Cloud-Server-win-x64.exe` | ~58 MB | `ASM_Cloud-Server-win-x64.exe --help` → sets `STORAGE_ROOT` + `PORT` (no Node needed, standalone) | `see release` |
| **Server — Linux** (Pi/mini-PC) | `ASM_Cloud-Server-linux-x64` | ~56 MB | `chmod +x ASM_Cloud-Server-linux-x64 && ./ASM_Cloud-Server-linux-x64` → Docker prod still recommended (`server/DEPLOY.md`) | `see release` |
| **Desktop — Windows** | `ASM_Cloud-Desktop-0.8.0-win-x64.msi` / `.exe` | ~14 MB | Double-click MSI → tray `●` → Login `https://cloud.example.com` | `see release` |
| **Desktop — macOS** | `ASM_Cloud-Desktop-0.8.0-mac-universal.dmg` | ~18 MB | Open DMG → drag to Applications → tray | `see release` |
| **Desktop — Linux** | `ASM_Cloud-Desktop-0.8.0-linux-x64.AppImage` | ~16 MB | `chmod +x *.AppImage && ./ASM_Cloud-Desktop*.AppImage` | `see release` |
| **Mobile — Android** | `ASM_Cloud-0.8.0.apk` | ~42 MB | Phone → enable “Install unknown apps” → open APK → Login `10.0.2.2:3000` (emulator) or `https://cloud.example.com` | `see release` |
| **Mobile — iOS** | `ASM_Cloud-0.8.0.ipa` | ~38 MB | TestFlight / `eas build` → install via Xcode / AltStore | `see release` |
| **Docs** | `INSTALL_GUIDE.pdf` | 5 pages | Print-ready professional guide | — |

**Download here:** **[Releases → v0.8.0](https://github.com/siddgithub2022/ASM_Cloud-Releases/releases/tag/v0.8.0)** → `Assets` → click file.

---

## 🚀 Quick Start (Layman)

### Server (pick one)
**A) Standalone EXE (no Docker, no Node):**
```powershell
# Windows
.\ASM_Cloud-Server-win-x64.exe --port 3000 --storage "F:\asm-cloud-data" --db sqlite
# Linux/Pi
./ASM_Cloud-Server-linux-x64 --port 3000 --storage /mnt/storage/asm-cloud-data
# then in another terminal:
curl -X POST http://localhost:3000/api/auth/register -H "Content-Type: application/json" -d '{"username":"alice","email":"alice@home","password":"S3cure!pass","inviteToken":"..."}'
```

**B) Docker prod (recommended, Caddy HTTPS):** See private source `server/DEPLOY.md` — `docker compose -f docker-compose.yml -f docker-compose.prod.yml up --build -d`

### Desktop
1. Install MSI/DMG/AppImage → tray `●` → Login `https://cloud.example.com` → `alice`
2. Settings → `Sync folder` → `C:\Users\You\PersonalCloud` → Sync now

### Mobile
1. Install APK/IPA → Login `https://cloud.example.com` → Browse cloud → `Keep offline ✓`
2. Camera tab → Enable auto-upload (Wi-Fi only) → Run now

Full visual guide (with pictures): **[INSTALL_GUIDE.pdf](https://raw.githubusercontent.com/siddgithub2022/ASM_Cloud/main/docs/INSTALL_GUIDE.pdf)** (also in `docs/INSTALL_GUIDE.html` printable)

---

## 🔒 Security
- Server EXE embeds Node 20 (no external deps), JWT `15m` + `argon2`, share `argon2`, ETag+SHA256, Caddy Let’s Encrypt.
- Desktop/Mobile verify TLS, no plaintext tokens logged.
- Source is **private** — only binaries + docs are public here (as you requested).

---

## 📦 Build from Source (private repo)
```bash
git clone https://github.com/siddgithub2022/ASM_Cloud.git  # requires access
cd server && npm run build && npx pkg dist/main.js --targets node20-win-x64 --output ../ASM_Cloud-Server-win-x64.exe
cd ../desktop && npm run tauri:build
cd ../mobile && npx expo run:android
```
Workflow: `.github/workflows/release.yml:1` builds all 4 on `git tag v*` → publishes here.

---

## 📄 License & Branding
MIT • `assets/logo.svg` • Theming `Inter/SF Pro/Roboto`, primary `#2E6FE0`, every screen `● Status | Storage used/total | Last synced`

---

<p align="center"><b>ASM_Cloud</b> — <i>Your files, your drive, your cloud.</i><br/>Source: <a href="https://github.com/siddgithub2022/ASM_Cloud">PRIVATE siddgithub2022/ASM_Cloud</a> • Downloads: <a href="https://github.com/siddgithub2022/ASM_Cloud-Releases">PUBLIC siddgithub2022/ASM_Cloud-Releases</a></p>
