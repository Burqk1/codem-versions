## 1.0.1 - 2026-11-14

- Work clothes at the entrance lockers before any station works
- New resource codem-butcher-clothes: ensure it in server.cfg
- Config.Uniform turns the clothes rule on or off
- Shift guide outlines the next station to use
- Other players see work animations with the tool in hand
- Patty press runs the whole tray, plucking hands the hen over
- Mince tray goes only to the machine the order needs
- Choice list scrolls with the mouse wheel
- New texts in all 30 languages

### Changed files

fxmanifest.lua: version 1.0.1
client/uniform.lua, client/pose.lua, server/pose.lua: new
client/cue.lua, client/engine.lua, client/buttons.lua
server/delivery.lua, shared/stations.lua, shared/facility.lua
config/config.lua: Config.Uniform
locales/*.lua: new texts
build/: rebuilt
codem-butcher-clothes: new resource
