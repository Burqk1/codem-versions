## 2.0.1 - 2026-10-19

- New dispatchType codem-dispatchv2 for police race alerts
- Tracks page reworked, every track shows its length
- Store: full background vehicle images no longer cut out
- Home board titles no longer overflow their card
- Config.DefaultLanguage back to "en"

### Changed files

fxmanifest.lua: version 2.0.1
client/utility.lua: codem-dispatchv2 police alert
config/config.lua: codem-dispatchv2, default language en
locales/*.lua: trackLength, 30 languages
ui/dist/: rebuilt

## 2.0 - 2026-10-19

- Full rebuild: new racing tablet UI, all Lua rewritten
- Racers, crews, tracks, store and seasons are kept
- New home: top racers, top crews and live races
- Tracks page with map preview, class records, comments
- New hall of fame, profile, crew and store pages
- Store opens on a category hub, GC balance always visible
- New Practice mode: free laps on any track, no GP / GC
- New Ghost Replay: race your best lap or the class record
- Ghost laps checked on the server before they are saved
- Checkpoints, lap times and rewards checked on the server
- Race password checked on the server, not sent to others
- Vehicle class read from the server, not the client
- Vehicle no longer stays frozen after the countdown
- Racers no longer stuck in a race after disconnecting
- DNF players no longer get race rewards
- Store purchases locked against double buys and swaps
- Route edit and delete limited to the route owner
- Route props checked against Config.PropModels
- Player passwords no longer sent with racer profiles
- Players can no longer give themselves race permission
- SQL injection in board and store queries fixed
- Season rollover and crew rename data fixed
- Notifications no longer replay when the tablet opens
- Config.Framework auto: qbox, qb, esx, vRP, standalone
- Config.Inventory auto, racingtablet item in installation
- Schema in sql/racing.sql, created and updated on start
- 30 languages, each player sees their own language
- Webhooks in config/discord.lua or convars
- Joining races and creating routes open by default
- Update: replace the folders, copy your config values over

### Changed files

fxmanifest.lua: version 2.0, ui_page ui/dist/index.html
config/config.lua: new file, copy your values over
config/vehicleclass.lua: vehicle classes moved here
config/achievements.lua: achievements moved here
config/discord.lua: webhooks, convar fallback
sql/racing.sql: schema, new ghosts table
client, server, shared: rewritten
modules/framework, modules/inventory: new bridges
locales/*.lua: 30 languages
ui/dist/: new tablet UI

## 1.13 - 2026-09-02
- Sezon sistemi guncellendi
- Crew davet hatasi duzeltildi

## 1.12 - 2026-08-05
- Daily competitive odul dengesi
