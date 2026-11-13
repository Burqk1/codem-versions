## 1.0.3 - 2026-11-13

- Fix: F8 error on pumps without a jerry can set down

### Changed files

fxmanifest.lua: version 1.0.3
client/target.lua: pick up option check

## 1.0.2 - 2026-11-12

- Fill a jerry can at the pump: set it down, buy on the screen
- Overfilled fuel runs over onto the ground
- New Config.JerryCan.nozzle, tune it with /fuelnozzle
- Litres in the held can shown with its ammo count
- Fix: empty jerry cans can be filled again (durability min 1)
- Old empty cans fixed on join, admin /jerryfix
- Fix: pump screen gets prices right after it is assigned
- lc_gas_stations is false by default

### Changed files

fxmanifest.lua: version 1.0.2
client/jerrycan.lua, server/jerrycan.lua: litres, /jerryfix
client/nozzles.lua, server/nozzles.lua: can at the pump
server/pumps.lua: can filling, overflow
client/target.lua: fill and pick up options
client/tuner.lua: can nozzle tuning
client/screens.lua: screen data sent on assign
shared/config.lua: JerryCan.nozzle, lc_gas_stations false
locales/en.lua, locales/tr.lua: jerry can texts

## 1.0.1 - 2026-10-24

- Version checker reports new releases on server start
- Console command codem-fuel:version re-checks manually
- Default language is English (Config.Locale = 'en')

### Changed files

fxmanifest.lua: version 1.0.1, server/versionchecker.lua
shared/config.lua: Config.VersionChecker, Config.Locale
server/versionchecker.lua: new

## 1.0.0 - 2026-10-24

- Version checker reports new releases on server start
- Console command codem-fuel:version re-checks manually

### Changed files

fxmanifest.lua: server/versionchecker.lua
shared/config.lua: Config.VersionChecker
server/versionchecker.lua: new
