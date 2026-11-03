## 1.0.1 - 2026-11-03

- New: cinemas with shows, tickets, kiosks and a guard ped
- New: cinema panel with movies, screens, vault and staff
- New: ticket tax, intermissions, seek and volume
- New: muffled sound behind walls (Config.Occlusion)
- New: night glow for big screens (Config.ScreenGlow)
- New: screen tools, /tvprops, flip, curve, saved screens
- New: folder videos and music on TVs, jukebox, DJ, car radio
- Full translations for every text
- Kiosks hidden from TV lists, titles instead of links
- Turned off TVs stay off, longer remote range
- Fix: video end handling, renamed folder videos
- Fix: DJ booth crash with folder tracks
- New cinema tables and columns are added on start

### Changed files

fxmanifest.lua: version 1.0.1
config/config.lua: Cinemas, Occlusion, ScreenGlow, Folder
config/models.lua, sql/tv.sql
client/, server/, locales/, html/: rebuilt
codem-tv-props: kiosk and ticket booth models

## 1.0.0 - 2026-10-22

- First release
- TVs, big screens and vehicle screens, synced for everyone
- YouTube, Twitch, Kick, Vimeo, SoundCloud, files and more
- 24/7 channels, YouTube search, news ticker
- Cinema shows with tickets, ad screens
- Speakers: place, carry, link together, jukebox requests
- Car sound system, own speaker and jukebox props
- 30 languages

### Changed files

all files: first release
codem-tv-props: speaker and jukebox models
