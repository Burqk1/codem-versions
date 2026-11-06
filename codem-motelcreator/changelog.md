## 1.0.8 - 2026-11-06

- Fix: server resmon spikes from world loads
- Access data loads once per player, world data is cached
- Tablet money and staff actions no longer reload everyone
- Fix: re-selecting a locked MLO door saved the wrong heading
- The door fix needs the latest codem-lib
- Fix: zones and door locks lost during a slow refresh
- Fix: drawtext points use their saved distances
- Removed debug prints from the tablet open check

### Changed files

fxmanifest.lua: version 1.0.8
client/world.lua, main.lua, interact.lua, doorlock.lua
client/placement/door.lua
server/endpoints.lua, main.lua, mlo.lua, players.lua
server/repository.lua, security.lua, write.lua
