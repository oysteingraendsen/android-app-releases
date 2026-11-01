# android-app-releases

Signed APKs and update manifests for my Android apps. The source code is private.
Everything here is written by the release workflow, so don't edit it by hand.

## Apps

| App | Latest | Obtainium | Download | Obtainium title filter |
|-----|--------|-----------|----------|------------------------|
| Birthdays | 0.2.0 | [Add to Obtainium](https://apps.obtainium.imranr.dev/redirect?r=obtainium://app/%7B%22id%22%3A%22io.github.oysteingraendsen.birthdays%22%2C%22url%22%3A%22https%3A%2F%2Fgithub.com%2Foysteingraendsen%2Fandroid-app-releases%22%2C%22author%22%3A%22oysteingraendsen%22%2C%22name%22%3A%22Birthdays%22%2C%22additionalSettings%22%3A%22%7B%5C%22filterReleaseTitlesByRegEx%5C%22%3A%5C%22%5Ebirthdays%20%5C%22%2C%5C%22includePrereleases%5C%22%3Afalse%2C%5C%22fallbackToOlderReleases%5C%22%3Atrue%7D%22%7D) | [APK](https://github.com/oysteingraendsen/android-app-releases/releases/download/birthdays-v0.2.0/birthdays-0.2.0.apk) | `^birthdays ` |
| Todo | 0.2.0 | [Add to Obtainium](https://apps.obtainium.imranr.dev/redirect?r=obtainium://app/%7B%22id%22%3A%22io.github.oysteingraendsen.todo%22%2C%22url%22%3A%22https%3A%2F%2Fgithub.com%2Foysteingraendsen%2Fandroid-app-releases%22%2C%22author%22%3A%22oysteingraendsen%22%2C%22name%22%3A%22Todo%22%2C%22additionalSettings%22%3A%22%7B%5C%22filterReleaseTitlesByRegEx%5C%22%3A%5C%22%5Etodo%20%5C%22%2C%5C%22includePrereleases%5C%22%3Afalse%2C%5C%22fallbackToOlderReleases%5C%22%3Atrue%7D%22%7D) | [APK](https://github.com/oysteingraendsen/android-app-releases/releases/download/todo-v0.2.0/todo-0.2.0.apk) | `^todo ` |

Open this page on the phone and tap **Add to Obtainium**: Obtainium opens with the app
already set up, including its release title filter. Without Obtainium installed, the link
offers to get it.

## Layout

| What | Where |
|------|-------|
| APK for app `<app>`, version `X.Y.Z` | Release `<app> X.Y.Z` (tag `<app>-vX.Y.Z`) → asset `<app>-X.Y.Z.apk` |
| Latest-version manifest the app reads | `<app>/update.json` |

Each app has its own tag prefix and folder, so many apps can share this one repo.
All apps are signed with the same release key (certificate SHA-256 starts with `3B:FE:DD:9C`).

## Installing

- **First time:** tap **Add to Obtainium** above, or tap **APK** and install it.
- **Updates:** the app checks `<app>/update.json` on startup and installs new versions itself.
- **Obtainium by hand:** add this repo's URL and set *Filter release titles by regular
  expression* to the app's filter from the table. Every app needs its own entry and filter.
