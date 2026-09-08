# ASM_Cloud — Commercial Demo Video Script (90s, layman-friendly)

**Title:** *Your files. Your drive. Your cloud.* — ASM_Cloud Private Cloud Demo
**Format:** 1920x1080, 30fps, 90 seconds, voiceover + music + captions, logo #2E6FE0
**Audience:** Families / small teams who want Dropbox without renting storage

---

## Storyboard (8 scenes)

| # | Time | Visual | Voiceover (EN, warm, confident) | On-screen Text |
|---|------|--------|----------------------------------|----------------|
| 0 | 0:00-0:06 | **Cover** — gradient #0F172A→#2E6FE0, logo animates in, HDD + host + phones orbit | "Meet ASM_Cloud — your private cloud. Your files, your drive, your cloud." | ASM_Cloud • Private • Self-Hosted • Lean |
| 1 | 0:06-0:16 | **Problem → Solution** — split screen: left public cloud $$, right home Pi + HDD | "Why rent storage when you have a drive at home? Plug an external HDD into an always-on host — a mini-PC or old laptop — and ASM_Cloud does the rest." | External HDD = Your Cloud Volume |
| 2 | 0:16-0:30 | **Server Install (2 commands)** — terminal typing `docker compose up` → Caddy HTTPS lock, `curl` register 200 | "One command brings your server online — with Postgres, secure JWT, and automatic HTTPS via Caddy. Your server, your keys." | `STORAGE_ROOT=/mnt/storage` • `POST /api/auth/register` |
| 3 | 0:30-0:45 | **Desktop (Tauri)** — MSI install → tray ● synced → Settings → Sync folder `C:\Users\You\PersonalCloud` → drag `report.pdf` → Activity Log `Uploaded` | "On Windows, Mac, Linux — install the Tauri desktop. Pick your sync folder — like Dropbox — and files sync transparently. Tray shows synced, syncing, conflict — always visible." | ~/PersonalCloud • Selective Sync • Conflict → (conflicted copy) |
| 4 | 0:45-1:02 | **Mobile (Expo)** — APK install → Login → Browse cloud → Keep offline ✓ → Camera roll auto-upload (Wi-Fi) → Run now → Photos/Camera folder appears on desktop | "On your phone — browse your cloud, keep files offline for the plane, and let camera rolls auto-upload on Wi-Fi — the #1 real use." | Browse cloud • Keep offline • Wi-Fi only |
| 5 | 1:02-1:12 | **Connect All Devices** — animated sync: desktop → server → mobile → server → second laptop, WebSocket push `sync:changes` | "Drop a file on your desktop — it pushes instantly to your phone and second laptop via WebSocket — no polling." | WebSocket /sync • ETag • Chunked 10 MB |
| 6 | 1:12-1:22 | **Share & Admin** — ShareDialog password/expiry → copy link `.../api/public/share/xfqRh...` → friend opens no login, AdminPanel quotas 5GB → storage bar | "Share any file or folder with a link — optional password and expiry. Admins manage users, quotas, and see drive usage — private, read-only links." | Public /api/public/share/:token |
| 7 | 1:22-1:30 | **Outro CTA** — logo + HDD + host + phones synced, URL `github.com/siddgithub2022/ASM_Cloud-Releases` → Download EXE/APK/IPA, docs page | "ASM_Cloud — lean, private, yours. Server EXE, Desktop EXE, Android APK, iOS IPA — download at ASM_Cloud-Releases. Your files, your drive, your cloud." | Download: Server ZIP • Desktop MSI • APK • IPA • Docs |

**Music:** Upbeat, minimal, 95 BPM, -14 LUFS. **Captions:** Burned-in, Inter, white with blue highlight for commands.

---

## Voiceover Full Script (for ElevenLabs / gTTS)

> Meet ASM_Cloud — your private cloud. Your files, your drive, your cloud. Why rent storage when you have a drive at home? Plug an external HDD into an always-on host — a mini-PC or old laptop — and ASM_Cloud does the rest. One command brings your server online — with secure login, automatic HTTPS, and your data on your drive, not someone else’s. On desktop — Windows, Mac, Linux — install, pick your sync folder, and drag files in. Tray shows synced, syncing, conflict — always visible. On your phone — browse your cloud, keep files offline for the plane, and let camera rolls auto-upload on Wi-Fi. Drop a file on your desktop — it pushes instantly to your phone and second laptop. Share any file or folder with a link — password, expiry, read-only. Admins manage users, quotas, and drive usage. ASM_Cloud — lean, private, yours. Download the Server, Desktop, and Mobile apps at ASM_Cloud-Releases. Your files, your drive, your cloud.

---

## How to Record (OBS)

1. Play `docs/demo/DEMO_VIDEO.mp4` fullscreen on 1080p monitor.
2. OBS → Display Capture → Record 1920x1080, 30fps, 8000 kbps.
3. Add voiceover track from `DEMO_SCRIPT.md` via ElevenLabs (voice: Adam, stability 50) or `gTTS`.
4. Export `ASM_Cloud-Demo-1080p.mp4` → upload to `ASM_Cloud-Releases` Releases → `Releases → v0.8.0 → Edit → Attach`.

## Files in this folder
- `DEMO_VIDEO.mp4` — 90s commercial (generated via MoviePy, 1920x1080, 30fps)
- `DEMO_STORYBOARD.pdf` — print-ready storyboard with frames
- `DEMO_SCRIPT.md` — this file
