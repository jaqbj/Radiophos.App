# Radiophos

Internet radio with an 80s/90s green-phosphor terminal look: 50,000+ stations from the
Radio Browser directory, a wireframe globe that flies to where each station is, live
visualizations, recording and scheduled recording, and seasonal full-screen scenes.

This repository is where Radiophos is published and where you can report bugs and ideas.
The app's source code is kept elsewhere.

## Download (1.0 beta)

| Platform | Get it |
| --- | --- |
| macOS 14 or later (Apple silicon and Intel) | `Radiophos-1.0-beta-10.dmg` under [Releases](https://github.com/jaqbj/Radiophos.App/releases) or in [`releases/`](releases) |
| iPhone (iOS 17.6 or later) | TestFlight: https://testflight.apple.com/join/j44bQsTm |
| Windows 10 (version 2004) or 11, 64-bit | `Radiophos-1.0-beta-1-windows-x64.zip` under [Releases](https://github.com/jaqbj/Radiophos.App/releases) or in [`releases/`](releases) |
| Android 7 or later, phones | `Radiophos-1.0-beta-1-android-arm64.apk`, same places |
| Android tablets and older devices | `Radiophos-1.0-beta-1-android-universal.apk` (larger; works on every device) |
| iPad | Later |

What's new and what doesn't work yet: [release notes](RELEASE-NOTES-1.0-beta.md).
Privacy: [the app collects nothing](PRIVACY.md).

## Installing on a Mac

1. Open the dmg and drag Radiophos into Applications.
2. Open Radiophos from Applications. It is notarized by Apple, so macOS asks once
   whether to open an app downloaded from the internet: click Open.
3. Radiophos lives in the menu bar (top right, by the clock). Open the window from there.

## Installing on Windows

1. Unzip anywhere (for example Documents\Radiophos) and run `radiophos.exe`.
2. The app isn't signed yet, so the first time Windows SmartScreen may say "Windows
   protected your PC": click **More info**, then **Run anyway**.
3. Closing the window keeps Radiophos in the tray (bottom right, maybe under ^); quit
   from the tray menu. To remove it, quit and delete the folder (turn off Start at login
   in Setup first).

## Installing on Android

1. Download the APK on the phone and open it. Android asks to allow installing apps from
   your browser or file manager: allow it for that app.
2. Updates install over the previous version and keep your settings. If you had a very
   early test build (alpha 1 to 3) and Android says the app can't be installed,
   uninstall the old one first.
3. Radiophos asks for notifications (playback controls and scheduled recordings) and,
   the first time you pick Spectrum, Scope or VU, for the microphone: Android needs that
   permission to let an app read its own sound. Nothing is recorded or sent.

## Feedback

Open an issue here: what you did, what you expected, what happened, and your device and
system version. Screenshots help.

## Credits and license

Stations from [Radio Browser](https://www.radio-browser.info/) (community-run). Country
outlines from [Natural Earth](https://www.naturalearthdata.com/), time zone locations
from the [IANA time zone database](https://www.iana.org/time-zones). Radiophos is MIT
licensed; © 2026 Jakub Januszewski.
