# Radiophos 1.0 beta

First public beta, for **macOS**, **Windows** and **Android** (downloads) and **iPhone**
(TestFlight, coming soon). iPad follows later.

## Builds

- **Mac beta 10** (2026-11-26): small fixes from a design review. Station rows show
  country and language without stray dots; the sidebar says "Setup"; Setup's choice
  buttons wrap as whole words; Sleep is a terminal button with a pop-up of times; the
  keyboard cursor ring in lists shows only after an arrow or Tab key, not on a click.
  (Build 9 went to TestFlight only.)
- **Mac beta 8** (2026-11-15): notarized by Apple, so it opens without "Open Anyway".
  Otherwise the same as beta 7.
- **Windows and Android beta 1** (2026-11-16): first public builds, with the same
  features as the Mac and iPhone beta.

## What's in it

- **Find stations** — search 50,000+ stations by name, genre or country; filter by region
  and country; Show more up to 500. Radiophos picks the fastest Radio Browser server and
  switches if one fails.
- **Listen** — song titles where the station sends them, lock screen and Control Center on
  iPhone, media keys on the Mac and Windows, the notification and lock screen on Android
  (also with the screen off), its own volume and Mute.
- **Sleep timer** — 15 minutes to 2 hours; the sound fades out over the last 30 seconds,
  then the radio stops.
- **Views** — Globe flies to the playing station's country. **Orbit** turns the Earth slowly
  with day and night, the Sun, the Moon in its phase, and a dot where you are (from your
  time zone; no location access). **Spectrum, Scope, VU** show the music, now for nearly
  every station.
- **Favorites and playlists** (M3U/PLS files or links), and **saved songs**: tap ♡ and find
  the song later on Spotify, Apple Music or YouTube Music.
- **Recording** — record what's playing, or schedule a recording for later. Files are saved
  exactly as the station sends them (MP3, AAC…), with a tag saying which station and when.
  Recordings are for your own listening.
- **Scenes on iPhone and Android** — turn the phone sideways on a charger for a Christmas
  or Halloween display with a countdown, a clock and falling snow or leaves; import your own. At night
  it switches to a dim moving clock (or lets the screen turn off), and it can stop the
  radio after a while.
- **Car mode on iPhone** — big buttons; opens by itself when CarPlay connects.
- **Themes** — Terminal, Amber, Retro CRT, BitchX, Night Red, Modern, Modern Dark, Paper,
  or your own.
- **Mac** — in the menu bar, with a window when you want one; start at login; full keyboard
  control.
- **Windows** — in the tray with a pop-up panel, and a window with a resizable side
  column; start at login; full keyboard control (Ctrl+F search, Ctrl+Q quit).
- **Android** — tabs for Stations, Favorites, Recordings and Setup; Now Playing with the
  globe; recordings in Music/Radiophos, where you can play, share or delete them;
  scheduled recordings that run with the screen off or the app closed.

## Known limits

- **Mac:** a scheduled recording can't wake a sleeping Mac; Radiophos keeps the Mac awake
  from 10 minutes before if it's awake.
- **iPhone:** scheduled recordings run only while Radiophos is open or playing; otherwise
  you get a reminder to open it.
- **Windows:** the app isn't signed yet (SmartScreen warns once). For a scheduled
  recording Radiophos asks Windows to wake the PC 2 minutes before; whether it wakes
  depends on the power plan's "Allow wake timers" setting.
- **Android:** scheduled recordings need "Alarms & reminders" allowed (Radiophos shows
  the switch) and may start up to a minute late in deep battery saving. After
  uninstalling and reinstalling, older recordings stay in Music/Radiophos but no longer
  show in the app's list.
- On Mac and iPhone, stations sent as HLS or Opus, and a few old Shoutcast servers, play
  fine but can't be visualized.
- Radio Browser currently runs on a single server machine; if it's down, the station list
  can't load (your favorites still play).
- Stations broadcasting from Russia are hidden by default; Setup › Stations › "Show
  stations from Russia" shows them.

## Reporting problems

Open an issue in this repository with what you did, what happened, and your device and
system version.
