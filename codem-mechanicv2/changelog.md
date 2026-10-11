## 1.3 - 2026-10-11

- French language added (locales/fr.json)
- UI texts read from locales at runtime, no rebuild needed
- New locale = copy en.json, translate, set Config.Locale
- Config.CleaningKit.removeChance: chance a use removes kit
- Fixed: chameleon paints 223-242 had no effect
- carcols_gen9 and carmodcols_gen9 meta files added
- Vanilla flatbed no longer replaced, tow job uses cdmflatbed
- cdmflatbed model and vehicles.meta updated
- Spray gun mist shows on painters who stream in later
- Lighter nitro prop, flatbed and stance loops

### Changed files

fxmanifest.lua: version 1.3, gen9 meta files
locales/fr.json: new
shared/locale.lua: locale tables passed to the UI
client/cl_core.lua: appReady sends the locale tables
html/: rebuilt, locales loaded at runtime
config/config.lua: Locale comment, removeChance
server/sv_repair.lua: cleaning kit remove chance
asset/meta: carcols_gen9.meta, carmodcols_gen9.meta
client/cl_spraygun.lua: remote mist waits for the ped
client/cl_boostprop.lua: lighter prop loop
client/cl_flatbed.lua: lighter bed loop
client/cl_ride.lua: stance pose every 250 ms
codem-flatbed: cdmflatbed model, vehicles.meta
codem-mechanicv2-props: vanilla flatbed files removed

## 1.2 - 2026-09-07

- Muted backfire, anti-lag, two-step stay muted after respawn
- Mute is stored on the tuning record via popbang:persist RPC
- Server checks driver seat, plate and that the part is fitted
- Works with Config.Backfire disabled, systems are separate
- Mute survives cart purchases and orders while part is fitted
- Removing the part clears its mute, reinstall starts unmuted
- Browsing the catalog no longer empties the cart
- Unconfirmed previews revert on panel exit and on purchase
- Removing a cart item also drops its live preview

### Changed files

client/cl_carpanel.lua: mute toggle persisted via RPC
client/cl_ride.lua: re-applies stored mute flags on enter
server/sv_popbang.lua: new popbang:persist RPC with checks
server/sv_tuner.lua: CarryPopbangOff keeps mute flags on buy
server/sv_tickets.lua: order persistence keeps mute flags
web/src/App.tsx: cart and preview separated, html rebuilt

## 1.1 - 2026-09-04

- Plate transfer now moves tuning data to the new plate
- Preview no longer changes the vehicle's plate
- One canonical plate key across caches and database
- Padded plate rows from older versions migrated on start
- Tuning build persists on rows with old padded plates
- Version checker reports new releases on server start
- Console command codem-mechanicv2:version re-checks manually

### Changed files

shared/utils.lua: added NormalizePlate and PlateKey
server/sv_vehdata.lua: props writer, transfer fix, migration
server/sv_tuner.lua: extras cache keyed by canonical plate
server/sv_inspect.lua: condition cache, saveCondition, RPCs
server/sv_tickets.lua: order plate and props via helpers
server/sv_detailing.lua: uses the shared plate helpers
server/sv_neon.lua: uses the shared plate helpers
server/sv_policenitro.lua: uses the shared plate helpers
client/cl_tuner.lua: preview plate restore fix
client/cl_detailing.lua: uses the shared plate helpers
client/cl_tickets.lua: uses the shared plate helpers
server/versionchecker.lua: new, update notice and changelog
fxmanifest.lua: loads versionchecker.lua, version 1.2
