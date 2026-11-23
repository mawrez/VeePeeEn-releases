# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.4.0 (2026-11-23)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.4.0-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.0/VeePeeEn-1.4.0-setup.exe) | 29.9 MB | `01e659e97b7e279cc72ed370ce2049ea7d09cb02525af3ab98e36862f8308893` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.0/VeePeeEn-android-arm64-v8a.apk) | 16.1 MB | `3da82795a167fd3788a9a90c29b331de8caa5ff73fccafcd6109e63ec72dd182` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.0/VeePeeEn-android-armeabi-v7a.apk) | 16.4 MB | `0c7c7e60eecb5ed76fc5eacd4a333bbd0077046b1e3d11f0839f55264caad501` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.0/VeePeeEn-android-universal.apk) | 31.3 MB | `70adae9aa138e89307758c9a25df96a7a106791eee5e6d0268c6e0f8f3ab4c2f` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.0/VeePeeEn-win64.zip) | 39.7 MB | `7d76687987cadcd7170de4ec90a9d1f7240f3d48196226bd048a8afc475e1c50` |

Install on Windows: run `VeePeeEn-1.4.0-setup.exe` (per-user install, no admin needed to
install; VeePeeEn asks for admin when it starts because TUN mode needs it). Installed apps update
themselves from inside the app (Update button in the header).

Android: install the `universal` APK, or the one for your CPU (`arm64-v8a` for almost all phones).

## Layout

- `latest.json` — update manifest read by the app (version, notes, file names, SHA-256, sizes).
- `v<version>/` — the files of each release, also attached to GitHub release `v<version>`.
- `.github/workflows/release.yml` — on every change to `latest.json`, creates/updates the release.

`latest.json`:

```json
{
  "version": "1.2.0",
  "tag": "v1.2.0",
  "published": "2026-11-21T10:00:00Z",
  "notes": "…",
  "windows": {
    "name": "VeePeeEn-1.2.0-setup.exe",
    "path": "v1.2.0/VeePeeEn-1.2.0-setup.exe",
    "url": "https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.2.0/VeePeeEn-1.2.0-setup.exe",
    "sha256": "…",
    "size": 0
  },
  "android": { "universal": { "name": "…", "path": "…", "sha256": "…", "size": 0 } }
}
```
