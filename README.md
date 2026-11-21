# VeePeeEn releases

Release channel for **VeePeeEn** (Windows + Android). The source lives in a separate private repo;
this repo only carries the built files and the update manifest the app reads.

## Latest: 1.3.0 (2026-11-21)

| File | Size | SHA-256 |
|---|---|---|
| [`VeePeeEn-1.3.0-setup.exe`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.0/VeePeeEn-1.3.0-setup.exe) | 29.5 MB | `e71cb7b1c951cf2cc7ad6330a53c333f15f7d42c53008694bc680efce2b8ecb9` |
| [`VeePeeEn-android-arm64-v8a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.0/VeePeeEn-android-arm64-v8a.apk) | 15.4 MB | `468a72024d91987b868e45558a5db37cd34770d5a35ad627c5ad2901b6f48e92` |
| [`VeePeeEn-android-armeabi-v7a.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.0/VeePeeEn-android-armeabi-v7a.apk) | 15.8 MB | `d6ae0caa460da2a9c97cebfa850ebe8c7dbd4b79093d615234d8a9d365ab9fe5` |
| [`VeePeeEn-android-universal.apk`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.0/VeePeeEn-android-universal.apk) | 30.1 MB | `816a04cf71721df66162a4b5a95e02641369d20a1a64d11f529958abe8824e1f` |
| [`VeePeeEn-win64.zip`](https://github.com/mawrez/VeePeeEn-releases/releases/download/v1.3.0/VeePeeEn-win64.zip) | 39.4 MB | `f70e0475b1fb6df86e5ea5546847f2e9d01d2a0c461f1e5dc59dfc6995551ba0` |

Install on Windows: run `VeePeeEn-1.3.0-setup.exe` (per-user install, no admin needed to
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
