## 1.3 - 2026-09-19

- Fixed Dynamic Weather turning itself off right after enabling
- The toggle stayed off and getAreas still reported dynamic=false
- Cause: an active weather override forced every area to static
- Overrides now keep the dynamic setting and the schedule intact
- Clearing an override returns areas to their saved schedule
- Panel and map show the override weather while one is active
- Version checker prints new releases on server start
- Manual re-check: codem-dynamicweather:version in the console

### Changed files

server/main.lua: override no longer clears the dynamic flag
client/main.lua: schedule skipped on overridden areas
html/index.js, html/index.css: panel rebuilt
server/versionchecker.lua (new)
config/Config.lua: Config.VersionChecker added
fxmanifest.lua: version 1.3, version checker registered

## 1.2

- Discord webhook logs for weather, zone and forecast changes
- Logs show who made the change plus the before -> after values
- Alerts when someone without permission tries to open the panel
- Set up in the new server-only config/Logs.lua

### Changed files

config/Logs.lua
server/logs.lua
server/main.lua
locale/en.lua
locale/tr.lua
fxmanifest.lua
