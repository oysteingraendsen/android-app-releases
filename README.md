# android-app-releases

Signed APKs and update manifests for my Android apps. The source code is private.
Everything here is written by the release workflow, so don't edit it by hand.

## Layout

| What | Where |
|------|-------|
| APK for app `<app>`, version `X.Y.Z` | Release `<app>-vX.Y.Z` → asset `<app>-X.Y.Z.apk` |
| Latest-version manifest the app reads | `<app>/update.json` |

Each app has its own tag prefix and folder, so many apps can share this one repo.
All apps are signed with the same release key (certificate SHA-256 starts with `3B:FE:DD:9C`).

## Installing

- **First time:** open [Releases](../../releases), download the newest `<app>-*.apk` and install it.
- **Updates:** the app checks `<app>/update.json` on startup and installs new versions itself.
- **With Obtainium:** add this repo's URL and set the release tag filter to `^<app>-v`.
