# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.2.0 (2026-11-21)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.2.0-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.2.0/VeePeeEn-1.2.0-setup.exe) | 27.1 MB | `229b8a06dc5c16814b1ab8fc54681aecce90c38c6e9f5ee1ed8da860bc88a84d` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.2.0/VeePeeEn-android-arm64-v8a.apk) | 15.4 MB | `8b049746bfe8fb714c3cdf34621911defbde942674633e227ca796e37a98253a` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.2.0/VeePeeEn-android-armeabi-v7a.apk) | 15.8 MB | `0b21d82c8f94abf1dc7f2716191d25b4a3778bcdedd7e7d38051620603f37597` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.2.0/VeePeeEn-android-universal.apk) | 30.1 MB | `5d7c33a2dc0d27fedf5b2293c450e00a118b9c03b0e4dcceb092fd99a6f2245d` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.2.0/VeePeeEn-win64.zip) | 36.0 MB | `9c5da652d116efcf8fa34a1bfefc99660aa09e479e3968ca740fe8285e6483ee` |

Install on Windows: run `VeePeeEn-1.2.0-setup.exe` (per-user install, no admin needed to
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
