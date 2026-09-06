## 1.2 - 2026-09-04

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

## 1.2.1 - 2026-09-07

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
