## 1.0.6 - 2026-11-14

- /setrank sets an operator's rank (admin only)
- /show<game> switches a player's job to that minigame
- New admin webhook in server/discord.lua for rank changes
- Bruteforce: wrong codes have a twin, a miss shows where it is
- Cipher and Memory keep the first flash on a slow first frame
- Contract sets a GPS waypoint instead of a route blip
- /hacktp to the running contract when Config.Debug is on

### Changed files

fxmanifest.lua: version 1.0.6
client/main.lua, server/main.lua, server/discord.lua
config.lua: Config.AdminCommand, Config.MinigameCommands
locales/en.json, locales/tr.json: new texts
web/build/: rebuilt
