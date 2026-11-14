# Radiophos 1.0 beta

First public beta, for **macOS** (download) and **iPhone** (TestFlight, coming soon).
iPad, Windows and Android follow later in the beta.

## What's in it

- **Find stations** — search 50,000+ stations by name, genre or country; filter by region
  and country; Show more up to 500. Radiophos picks the fastest Radio Browser server and
  switches if one fails.
- **Listen** — song titles where the station sends them, lock screen and Control Center on
  iPhone, media keys on the Mac, its own volume and Mute.
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
- **Scenes on iPhone** — turn the phone sideways on a charger for a Christmas or Halloween
  display with a countdown, a clock and falling snow or leaves; import your own. At night
  it switches to a dim moving clock (or lets the screen turn off), and it can stop the
  radio after a while.
- **Car mode on iPhone** — big buttons; opens by itself when CarPlay connects.
- **Themes** — Terminal, Amber, Retro CRT, BitchX, Night Red, Modern, Modern Dark, Paper,
  or your own.
- **Mac** — in the menu bar, with a window when you want one; start at login; full keyboard
  control.

## Known limits

- **Mac:** the beta isn't notarized yet, so the first launch needs "Open Anyway" (see the
  readme). A scheduled recording can't wake a sleeping Mac; Radiophos keeps the Mac awake
  from 10 minutes before if it's awake.
- **iPhone:** scheduled recordings run only while Radiophos is open or playing; otherwise
  you get a reminder to open it.
- Stations sent as HLS or Opus, and a few old Shoutcast servers, play fine but can't be
  visualized.
- Radio Browser currently runs on a single server machine; if it's down, the station list
  can't load (your favorites still play).
- Stations broadcasting from Russia are hidden by default; Setup › Stations › "Show
  stations from Russia" shows them.

## Reporting problems

Open an issue in this repository with what you did, what happened, and your device and
system version.
