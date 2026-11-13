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
