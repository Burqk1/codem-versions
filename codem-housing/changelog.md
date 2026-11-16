## 1.0.3 - 2026-11-16

- MLO house zone counts as inside: points, stash, media
- Dancers, wall art and smart panel load in MLO houses
- Armed sensors catch intruders in MLO house zones
- Ring button for owned units at apartment blocks
- Doorbell guests can open an MLO door, not lock it
- [G] rings the bell at an owned MLO house
- Moved house points update at once for players inside

### Changed files

fxmanifest.lua: version 1.0.3
client/interior.lua, client/player.lua, client/main.lua
client/smartpanel.lua, client/target.lua, client/dancer.lua
client/decorate.lua, client/dynamic.lua, client/media.lua
client/wallart.lua, server/main.lua
locales/*.json: new texts
web/dist/: rebuilt

## 1.0.2 - 2026-11-15

- Smart panel works in MLO houses
- Inside the house zone counts as inside for the panel

### Changed files

fxmanifest.lua: version 1.0.2
client/smartpanel.lua, client/player.lua, client/main.lua
server/main.lua

## 1.0.1 - 2026-11-13

- Police seal: tape across the door, sealed houses refuse entry
- Lockpick item at a locked or sealed door starts a break-in
- Smart panel touch screen: door, lights, cameras, alarm, music
- Door knock (H), heard inside as 3D sound
- Admin /housebell [id] rings the bell as that player
- Houses can have up to 8 named extra exits
- Lamp light editor: move, aim, intensity, cone, reach per lamp
- Wall art and ownership plate tab, name plate, more shells
- Decoration undo/redo for every moved object
- Stashes open with [E], price fields show thousands dots
- Fix: UI stayed Turkish with another Config.Locale
- Fix: dancers sank into the floor
- Fix: Give Key list shows the player name

### Changed files

fxmanifest.lua: version 1.0.1
client/*, server/main.lua, shared/*: features above
config/*.lua: seal key, police, lockpick, exits, shells
locales/*.json: new texts
stream/shell_custom: new shell
web/dist: rebuilt

## 1.0.0

- Initial release
