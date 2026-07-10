# IPTV Ultimate — OTA

Public update channel for the **IPTV Ultimate** app. Contains only:

- `update.json` — the OTA manifest the app polls (build number = source of truth).
- Release assets — the signed APKs (`ultimateV<build>.apk`) attached to each GitHub Release.

The application source code is private and lives elsewhere. Nothing here exposes it.

## Publishing an update

1. In the app repo: bump `pubspec.yaml`, build the release APK.
2. Create a Release here `v<version>` and upload `ultimateV<build>.apk` as an asset.
3. Edit `update.json` (build + apkUrl → the new asset) and push to `master`.

The app reads `https://raw.githubusercontent.com/Mounirmerengue/ultimate-ota/master/update.json`.
