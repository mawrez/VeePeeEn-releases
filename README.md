# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.4.1 (2026-11-23)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.4.1-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.1/VeePeeEn-1.4.1-setup.exe) | 29.9 MB | `9914538a5a236bb58739abf504f61fb0b02767a3db3ab674887f9d7de46b5d83` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.1/VeePeeEn-android-arm64-v8a.apk) | 16.1 MB | `b93a413efb8ece64ad0181fd96cbf4eba6d53486c14c21944e21fd28dd01be63` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.1/VeePeeEn-android-armeabi-v7a.apk) | 16.4 MB | `b1ede87cf8c32433d7308e777aaaf385efe290e8bf08d43b0f997bb57da6c39b` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.1/VeePeeEn-android-universal.apk) | 31.4 MB | `4a01ecf8709ae7a6ed8a402d13c9f77a8c037cfce6d00bded3ef9052df423ba5` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.4.1/VeePeeEn-win64.zip) | 39.7 MB | `2f9227d6380ae17988329a9a1dc71d82653dac9da44ea537a8c2e232001c5831` |

Install on Windows: run `VeePeeEn-1.4.1-setup.exe` (per-user install, no admin needed to
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
