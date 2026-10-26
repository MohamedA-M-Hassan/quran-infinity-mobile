# Download page and update file

These two files are published with GitHub Pages from a public repository (`quran-infinity-mobile`):

- `index.html` is the page the app opens when an update is needed.
- `version.json` is read by the app on launch:
  - `latest`: the newest build number (the number after `+` in `pubspec.yaml`). Older apps show an update banner.
  - `minimum`: the oldest build number that still works. Older apps show a blocking update screen.
  - `notes`: shown in the banner and the blocking screen.

To release: bump `version` in `pubspec.yaml`, build the signed APK, upload it to a GitHub release of the
repository as `Quran-Infinity.apk`, then update `version.json` (raise `minimum` only when old apps must stop).

