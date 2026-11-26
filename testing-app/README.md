# Giga Meter test builds (staging)

These installers are for testing only. They talk to the **staging** backend,
are **not signed**, and are x64 only. Do not install them on a school's PC.

| Installer | Built from | Updates |
|---|---|---|
| [Giga-Meter-Setup-2.0.4-staging.exe](https://github.com/unicef/giga-meter-app-links/raw/main/testing-app/Giga-Meter-Setup-2.0.4-staging.exe) | `release-candidate/2.0.4` at 513db13 (with the ping fix, #138) | Off (staging builds have the updater switched off) |
| [Giga-Meter-Setup-2.0.3-staging.exe](https://github.com/unicef/giga-meter-app-links/raw/main/testing-app/Giga-Meter-Setup-2.0.3-staging.exe) | tag `v2.0.3` | Never finds an update (its feed points at a local test server) |

## How to test

- Windows SmartScreen may warn that the installer is from an unknown publisher,
  because these builds are not signed: choose "More info", then "Run anyway".
- To test the upgrade, install 2.0.3, register, then run the 2.0.4 installer
  over it. The registration and the measurement history should be kept.
- Analytics events from these builds carry `app_mode: stg`.

## Before installing the real release

A PC with the 2.0.4 test build is not offered the real 2.0.4: the version
number is the same and the updater is off. Uninstall it first (Windows
Settings, Apps). Uninstalling also removes the app's local data and
registration on that PC.

## Checksums (SHA-256)

```
a3615e2c2404548177b5600124f497ba678de015b260c60706d0b2011a2f4754  Giga-Meter-Setup-2.0.4-staging.exe
a3df91bd424a87b589505c7011e081c6523d625ae471f14790df3e17748e7720  Giga-Meter-Setup-2.0.3-staging.exe
```
