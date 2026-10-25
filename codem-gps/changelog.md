## 1.0.5 - 2026-10-25

- Discord logs: GPS on, off and channel changes
- Webhook is set in the new config_server.lua (server only)
- 21 new languages, 30 in total
- Config.Items false turns that GPS off
- Wrong Config.Items value warns and uses the default
- Item images in install/images
- Sight cone no longer blinks on callsign or colour change

### Changed files

config_server.lua: new, Discord webhook
server/webhook.lua: new, batched Discord logs
server/main.lua: logs, Config.Items false
client/main.lua: sight cone kept on restyle
shared/utils.lua: Config.Items check
config.lua: Items and Locale comments
locales/*.json: 21 new languages, log texts
install/: item images, README, items.md
html/: web build
fxmanifest.lua: version 1.0.5, new server files

## 1.0.4 - 2026-10-23

- Members in one vehicle show as one blip, the driver's
- Vehicle blips show a sight cone, only on the driver
- Siren keeps the vehicle icon and pulses the blip colour
- Config.Blips.SirenIcon = true brings back the siren icon
- Config.Blips.MergeVehicles turns shared vehicle blips off
- Walk and drive while the GPS is open
- Typing in a field keeps the keyboard in the GPS
- Escape that closes the GPS no longer opens the pause menu
- Config.Blips.Types: foot cone is now indicator

### Changed files

fxmanifest.lua: version 1.0.4
client/main.lua: vehicle blips, sight cone, siren, input
server/main.lua: vehicle crews, siren with vehicle kind
config.lua: SirenIcon, MergeVehicles, blip types
html/: web build

## 1.0.3 - 2026-10-19

- Map legend no longer flickers on busy channels
- Own job listed per member, other jobs under Other Players
- Job change inside the same group regroups the legend
- In a vehicle the blip points where the vehicle faces

### Changed files

fxmanifest.lua: version 1.0.3
client/main.lua: legend grouping by job, vehicle heading
server/main.lua: member job, reconnect on job change

## 1.0.2 - 2026-10-17

- No blip flicker when members get in or out of vehicles
- Own group and other groups listed apart in the map legend
- Member blips shown on both the pause map and the minimap

### Changed files

fxmanifest.lua: version 1.0.2
client/main.lua: blip reuse, legend category, blip display

## 1.0.1 - 2026-10-16

- GPS device can be dragged anywhere, position reset in Settings
- New Device size setting, 50 to 130 percent, kept per player
- Config.CallsignMaxLength default 30 (was 10)
- New dark green colour at the end of Config.Colors
- Far away members no longer pile up on the minimap edge

### Changed files

fxmanifest.lua: version 1.0.1
client/main.lua: device size, short range member blips
config.lua: CallsignMaxLength 30, dark green colour
locales/*.json: ui_size, ui_position
html/: rebuilt

## 1.0.0 - 2026-10-05

- First release: team GPS for Qbox, QBCore and ESX through codem-lib
- GPS device screen opened by the item or /gps: power key, team list by distance, route to a member, settings
- Callsign: each player enters their code on the GPS, it shows next to their name on the map and in the team list and is kept between sessions
- Groups by job and grade decide who can use the GPS, on duty only if wanted
- GPS channels: players only see the members of their channel; preset channels per group (LSPD, EMS, joint) and free numbered channels
- Map blips in the group colour with a sprite for on foot, car, bike, helicopter, plane and boat
- Built for low server usage: positions are read on the server, only members who moved are sent, one update per group, nearby members are tracked by the player's own game
- Turns off when the job or duty changes, the item is lost or the player logs out
- Blip size and names can be changed per player
- Nine languages: English, Turkish, German, French, Spanish, Portuguese, Italian, Polish and Dutch
- Version checker reports new releases on server start
