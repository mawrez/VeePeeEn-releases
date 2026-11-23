# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.4.2 (2026-11-23)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.4.2-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.2/VeePeeEn-1.4.2-setup.exe) | 29.9 MB | `a1678a7f40b297808f6486f8115ad24c426b025ffadd19e2afe1c58a30060ceb` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.2/VeePeeEn-android-arm64-v8a.apk) | 16.1 MB | `8186be3e43389598d1baa9fff3cb10f5166d76858bd98062f115c2090828d52b` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.2/VeePeeEn-android-armeabi-v7a.apk) | 16.4 MB | `2f28aa8e3284d458a2c33efc5f4b1d8245e26452b8817605a6448841d32aff12` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.2/VeePeeEn-android-universal.apk) | 31.4 MB | `7408042123c7142554c0111e1e35c4a1552b824d25d5280196216135b96f7694` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.2/VeePeeEn-win64.zip) | 39.7 MB | `2734ed94bc8e9085d6b9079d0728a3d855cfc0cbc687166847c604c3d4138398` |

Install on Windows: run `VeePeeEn-1.4.2-setup.exe` (per-user install, no admin needed to
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
