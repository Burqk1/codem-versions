## 2.0 - 2026-10-19

- Brand new racing tablet UI built from scratch
- New home screen with top racers, top crews and live races
- Tracks page shows every route on a map preview
- New hall of fame, profile, crew and store pages
- Store opens on a category hub, GC balance always visible
- Joining races needs no permission by default
- Route creation open to everyone by default
- Race password checked on the server
- Vehicle class read from the server, not the client
- Route edit and delete limited to the route owner
- Player passwords no longer sent with racer profiles
- Players can no longer give themselves race permission
- SQL injection in board and store queries fixed
- Store purchases locked against double buys and swaps
- Vehicle no longer stays frozen after the countdown
- Racers no longer stuck in a race after disconnecting
- Season rollover and crew rename data fixed
- Notifications no longer replay when the tablet opens
- racingtablet item and image in the installation folder
- New UI texts in all languages

### Changed files

fxmanifest.lua: version 2.0, ui_page ui/dist/index.html
config/config.lua: OnlyJoinRaceAuthorizePlayers false
config/config.lua: OnlyRouteCreationAuthorizePlayers false
client: race flow, LOAD_PERMISSIONS message
server: security, ownership and purchase checks
ui/: new tablet UI (replaces the old html UI)
installation/: items.md, images/racingtablet.png
locales: new UI keys

## 1.13 - 2026-09-02
- Sezon sistemi guncellendi
- Crew davet hatasi duzeltildi

## 1.12 - 2026-08-05
- Daily competitive odul dengesi
