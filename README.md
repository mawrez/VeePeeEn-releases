# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.3.2 (2026-11-22)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.3.2-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.2/VeePeeEn-1.3.2-setup.exe) | 29.5 MB | `5d0671526a9732e9f7ccc5e334080a536c60f2d0a979c4e6e0d0fc21855de14c` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.2/VeePeeEn-android-arm64-v8a.apk) | 15.5 MB | `3ddfe6671356c35cbb68996ab5142d9ae42b58b4482013715d4cf1865823761b` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.2/VeePeeEn-android-armeabi-v7a.apk) | 15.8 MB | `56fc80c2531ecb4ebe4a10cf727d0b92228d87fa777eae55a8079423c7564f69` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.2/VeePeeEn-android-universal.apk) | 30.1 MB | `98430533ad6c93cd3782db538caa0359a96b39e13a03eb7e40e925d2a115c8c8` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.2/VeePeeEn-win64.zip) | 39.4 MB | `03b07a128867ce25125515178b24e7fc1433a3756df961a0f815f772325855c0` |

Install on Windows: run `VeePeeEn-1.3.2-setup.exe` (per-user install, no admin needed to
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
