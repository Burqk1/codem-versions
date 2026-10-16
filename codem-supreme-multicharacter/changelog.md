## 1.6 - 2026-10-16

- Version checker added, the console tells you when an update is out
- Weather: night_natural_disasters sync paused while the scene is open
- ESX: Last Location no longer spawns you under the map
- ESX: character preview uses the right model with illenium / fivem-appearance skins
- Illenium skins no longer applied on the wrong ped model at spawn
- The world no longer flashes while a new character is being created
- Screen no longer gets stuck on a fade

### Changed files

fxmanifest.lua: version 1.6, server/versionchecker.lua
client/appearance.lua: freemode model before illenium skin
client/main.lua: fade out timeout, blackout on create
client/spawn.lua: black overlay during blackout
client/bridge/weather.lua: night_natural_disasters
server/bridge/esx.lua: saved last position, preview model
server/versionchecker.lua: new

## 1.5 - 2026-10-11

- Version checker added

### Changed files

fxmanifest.lua: server/versionchecker.lua
server/versionchecker.lua: new
