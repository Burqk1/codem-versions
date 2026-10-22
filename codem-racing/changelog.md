## 2.0.4 - 2026-10-22

- New Config.Spectate: false turns live spectating off
- Finished, DNF or departed racers can no longer be watched
- Their stream stops and viewers are told it ended

### Changed files

fxmanifest.lua: version 2.0.4
config/config.lua: Config.Spectate
server/spectate.lua: refuse when off or racer out
server/race.lua, server/lobby.lua: stop stream when out
client/main.lua: spectate permission to the tablet
ui/dist/: rebuilt

## 2.0.3 - 2026-10-20

- Achievement badges can be moved between profile slots
- Badges saved with a text slot number are shown again
- Broken or doubled badge slots cleaned when a profile loads

### Changed files

fxmanifest.lua: version 2.0.3
server/data/racers.lua: slot check on load
server/profile.lua: move a badge between slots
ui/dist/: rebuilt

## 2.0.2 - 2026-10-19

- New: watch a racer's screen live from a live race
- New store showroom view for vehicles
- Achievement badges show name and description on hover
- Custom vehicle classes get their own colour on race cards
- Daily competitive races keep going past midnight
- Config.CompetitiveRaceMinimumPlayers = 1 now honoured
- About 200 unused old tablet images removed

### Changed files

fxmanifest.lua: version 2.0.2
client/spectate.lua, server/spectate.lua: live watching
server/lobby.lua, server/livedetails.lua: watch, players
server/dailycompetitive.lua: daily race schedule
config/config.lua: CompetitiveRaceStartTime comment
locales/*.lua: watch texts, 30 languages
ui/dist/: rebuilt

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
