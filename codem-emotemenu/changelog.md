## 1.0.2 - 2026-10-18

- Emote key binds: Shift/Alt + key per emote, saved per player
- New Config.Keys.wheel: separate quick wheel key
- Config.Keys accept mouse buttons (MOUSE_MIDDLE ...)
- Props created on the client, removed with the emote
- Scenario props cleaned up when a scenario emote ends
- Seats follow the chair when it streams in again
- Invisible players not listed for shared emotes and groups
- Favourites and slots kept when an emote is missing
- Crouch at normal speed, no double press with stealth key

### Changed files

fxmanifest.lua: version 1.0.2
client/keybinds.lua: new, emote key binds
server/storage.lua, server/main.lua: key binds saved
sql/emotemenu.sql: binds column
client/main.lua, shared/config.lua: wheel key, mouse
client/props.lua, server/props.lua: client props
client/play.lua: scenario prop cleanup
client/seats.lua, client/modules.lua: seat, crouch
client/group.lua, client/shared.lua: invisible players
locales/*.lua: new keys, 30 languages
html/: rebuilt

## 1.0.1 - 2026-10-15

- Do together works on every emote, nearby list scrolls
- New prompt bar for invites, requests and seats (no TextUI)
- Key labels no longer all show as PGDN
- Config.Keys.animposEdit checked against FiveM key names
- Hands up on the cancel key no longer cancels itself
- Fast switching no longer leaves the ped stuck in an emote
- Leftover props removed on quick stop and ped change
- Brand text under the menu title comes from locales

### Changed files

fxmanifest.lua: version 1.0.1
client/play.lua: stuck emote fix
client/props.lua, server/props.lua: leftover prop fix
client/shared.lua, server/shared.lua: do together
client/buttons.lua: prompt bar
client/group.lua, client/seats.lua: prompt bar
client/main.lua, client/nui.lua: key labels
client/animpos.lua, shared/config.lua: animpos keys
locales/*.lua: new keys, 30 languages
html/: rebuilt
