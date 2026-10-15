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
