## 2.0.9 - 2026-10-24

- Emergency.ChatMessages = false keeps messages out of chat
- New emergency messages then only show in dispatch
- Answers with /r still go to chat

### Changed files

fxmanifest.lua: version 2.0.9
config/Config.lua: DispatchConfig.Emergency.ChatMessages
server/emergency.lua: chat message only when enabled

## 2.0.8 - 2026-10-20

- Alerts hidden while the pause menu is open

### Changed files

fxmanifest.lua: version 2.0.8
client/nui.lua: pause menu watch
dist/: rebuilt

## 2.0.7 - 2026-10-15

- New alert field delay for alerts sent from other scripts
- delay = false: call skips DelayZones, reaches units at once
- delay = number: call waits that many seconds (0-3600)
- Without delay the zone delay works as before

### Changed files

fxmanifest.lua: version 2.0.7
client/alerts.lua: delay passed on from client alerts
server/sanitize.lua: delay read and checked
server/main.lua: per-alert delay before the zone delay
gitbook/: delay documented

## 2.0.6 - 2026-10-12

- New DispatchConfig.AlertPosition: call card Top / Right
- Pixels at 1080p, scales with the resolution
- Default keeps the old position (26, 26)

### Changed files

fxmanifest.lua: version 2.0.6
config/Config.lua: DispatchConfig.AlertPosition
client/nui.lua: position sent to the UI
dist/: rebuilt

## 2.0.5 - 2026-10-11

- Alerts show their details by default (plate, vehicle, units)
- On-screen cards and F3 list rows are open without a click
- Clicking a list row opens call number, waypoint, respond
- Long alert titles wrap to two lines everywhere

### Changed files

fxmanifest.lua: version 2.0.5
dist/: rebuilt, alerts open by default

## 2.0.4 - 2026-10-09

- Units on a call can carry a short note and up to 6 tags
- Note and tags show next to the unit in the call details
- New server export SetUnitNote (used by codem-mdtv2)

### Changed files

fxmanifest.lua: version 2.0.4
server/main.lua: SetUnitNote export
dist/: rebuilt, unit note and tags

## 2.0.3 - 2026-10-04

- Delay zones: alerts inside reach units delay seconds late
- Officer codes and 911 messages are never delayed
- Same alert while one is waiting is dropped as duplicate
- SendDispatchAlert returns true when the alert was delayed

### Changed files

fxmanifest.lua: version 2.0.3
server/main.lua: delay zones, waiting duplicates
server/officercodes.lua: officer codes skip the delay
config/Config.lua: DispatchConfig.Zones.DelayZones

## 2.0.2 - 2026-10-03

- Cards show the call number (Call #1043)
- Walk and drive with the calls panel open
- The key that opens the calls panel closes it too
- 911 lines: per-player cooldown, default 30 s, per line
- /kod takes any code; 99, 0, 33 stay priority
- Call signs from codem-mdtv2: unit name or badge number
- Calls panel uses the alert card, header removed
- Alerts show above HUD scripts, below codem-phone
- Opening or closing the panel clears on-screen alerts
- Respond raises the unit count at once
- 911 card no longer shows the /r reply line

### Changed files

fxmanifest.lua: version 2.0.2
client/handler.lua: walk with panel, key closes it
client/nui.lua: layer above the HUD
server/emergency.lua: per-line cooldown
server/officercodes.lua: any code, sender name
server/responders.lua: call sign from codem-mdtv2
shared/jobs.lua: line Cooldown
config/Config.lua: Emergency and OfficerCodes keys
locales/en.json: callNo, panel keys removed
locales/tr.json: callNo, panel keys removed
dist/: rebuilt

## 2.0.1 - 2026-10-03

- Version check on server start, console update notice
- New command: codem-dispatchv2:version
- Language files: locales/en.json and locales/tr.json
- All alert and panel texts read from the locale file
- Panel and call cards use game blur glass background

### Changed files

fxmanifest.lua: version 2.0.1, locale, versionchecker
config/Config.lua: Locale and VersionChecker added
shared/locale.lua: new
locales/en.json: new
locales/tr.json: new
server/versionchecker.lua: new
