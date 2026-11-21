# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.3.1 (2026-11-21)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.3.1-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.1/VeePeeEn-1.3.1-setup.exe) | 29.5 MB | `879ba2b1fe8bdda6c09ea7c42f20a313b4a10533f39c0c3e9400b38a91f24a6b` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.1/VeePeeEn-android-arm64-v8a.apk) | 15.4 MB | `d42a73b21054ffc1fffc0196f4b4efef2620d7bb2d433508ff0a4c04bf4d4735` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.1/VeePeeEn-android-armeabi-v7a.apk) | 15.8 MB | `d99e909d7a2c699124cffb64c73383dc160ba5424ea3ba8f298ede9a178dc1b4` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.1/VeePeeEn-android-universal.apk) | 30.1 MB | `74e2c73753365f75e28eb244fc352fe1dbed3cae0471db0c42e0fc49d2e3f443` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.1/VeePeeEn-win64.zip) | 39.4 MB | `4c5dcfa6cd31de6280de7333a776199b4b99cf3ac38d0625c2b8f822fceb5335` |

Install on Windows: run `VeePeeEn-1.3.1-setup.exe` (per-user install, no admin needed to
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
