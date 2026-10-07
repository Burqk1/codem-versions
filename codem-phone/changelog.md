## 3.12 - 2026-10-07

- New number is written into the phone item you used
- Item images for the 8 Andromeda phones added
- Item images split into images/ios and images/android
- burnerchip.png and powerbank.png added
- Item lists for ox_inventory and qb-inventory added

### Changed files

fxmanifest.lua: version 3.12
client/main.lua: used phone item sent to number setup
server/main.lua: used phone item passed on
modules/inventory/server.lua: findEmptyPhoneItemLike
[INSTALLATION]/images: ios/, android/, new images
[INSTALLATION]/itemlist: ox and qb item lists

## 3.11 - 2026-10-05

- New phone system Andromeda (Android) next to iFruit OS
- Galaxy-style body in 8 colours, One UI home and lock
- App drawer, folders, edit mode, themed icons, gestures
- Notification panel, heads-up cards, live status pills
- Own Settings, Phone, Messages, Gallery, Clock, Notes
- Own Email, Maps, Pulse, Voice Recorder, Galaxy Store
- Config.Android: player choice or phone item decides
- Config.Android.Items: Andromeda items and body colour
- Calendar is a default app, removed from the store

### Changed files

fxmanifest.lua: version 3.11
config/Config.lua: Config.Android, Android phone items
client/main.lua: phone item picks the system
server/main.lua: system setting locked by item mode
config/DefaultPhoneData.json: Calendar default app
config/AppStore.json: Calendar removed
html/: rebuilt

## 3.10 - 2026-10-04

- Call ending during video no longer leaves the camera on
- Video session, camera and input lock reset on every call end
- Phone pose restored after video instead of the stuck selfie
- Stopping video sends a single end message to the game
- Input lock after video follows whether the phone is open

### Changed files

fxmanifest.lua: version 3.10
client/defaults/call.lua: video teardown on every call end
web/src/state/calls.ts: clearCall drops the video session
html/: rebuilt

## 3.09 - 2026-10-04

- App open/close animation works in game (Chromium 103)
- Dialogs pop in with the same fix
- Closing apps drop inner blur, finish on transition end
- Home wallpaper blur drawn once, less GPU work
- Dragging an icon to the edge turns one page per 900 ms
- codem-payphone now ships in the same download

### Changed files

fxmanifest.lua: version 3.09
html/: rebuilt

## 3.08 - 2026-09-28

- Bank: transfers to online players no longer vanish
- Bank: failed credit refunds the sender
- MBox: partial pickup, the rest stays in the locker
- Services: calls-off switch is saved and survives relog
- Services: duty and calls switches show the real state
- Twix/Instashot: profiles with empty badge open again
- Photos: gallery no longer empty right after joining
- Server waits for phone load before answering app RPCs
- Messages: no notifications to phones in airplane mode
- Messages: sending is refused while in airplane mode
- Valet: codem-garagesv2 support through its exports
- Valet: garage script is re-detected when it starts late
- Valet: state column wins over stale stored column
- Valet: new Impounded status, chip, filter and action line
- Valet: console command valetdiag <serverId>

### Changed files

server/defaults/bank.lua: identifier lookup, refunds
modules/framework/qb/server.lua: offline credit result
modules/framework/esx/server.lua: offline credit result
server/mbox.lua: partial pickup
server/defaults/services.lua: saved calls switch, load
server/socials/twix.lua: badge and username guards
server/socials/instashot.lua: badge guard
server/main.lua: PhoneSyncInFlight flag
server/utils/utility.lua: CheckPlayerData waits for sync
server/defaults/message.lua: airplane checks
modules/garage/server.lua: garagesv2 branch, detection
modules/garage/client.lua: CollectVehicle handover
server/valet.lua: SpawnVehicleAt, reasons, valetdiag
client/valet.lua: Impounded status
config/Config.lua: GarageScript comment
locales/\*.json: mboxPickupPartial, valet impounded keys
html/: rebuilt

## 3.04 - 2026-09-24

- Hive: custom roles with permissions, hierarchy and colors
- Hive: old admins migrated to an auto-created Admin role
- Hive: members panel slides from the right, grouped by role
- Hive: member profile card with Manage Roles and Kick
- Hive: private channels limited to selected roles
- Hive: hidden channels filtered server-side, list and pushes
- Hive: channel sheet redesign, content height, lock icon
- Hive: channel gear button, edit and delete work again
- Hive: Turkish and accented letters allowed in channel names
- Hive: hive photo on the left rail, create and settings
- Hive: edit your display name and photo from the drawer
- Hive: sender names in chat use their top role color
- Valet: long vehicle names no longer break the garage grid
- Schema lives in sql/phone.sql only, asql applies it at boot
- Runtime CREATE TABLE and ADD COLUMN removed from Lua files

### Changed files

sql/phone.sql: hive roles, member roles, channel roles, icon
server/socials/hive.lua: roles, channel access, profile, utf8
client/socials/hive.lua: new role and profile RPC forwards
server/defaults/bank.lua: runtime ADD COLUMN removed
server/defaults/call.lua: runtime ADD COLUMN removed
server/defaults/message.lua: runtime CREATE TABLE removed
server/defaults/services.lua: waits for asql, no ALTER
server/trove.lua: runtime ADD COLUMN removed
server/restaurant.lua: EnsureColumn migrations removed
server/numberchange.lua: table moved to phone.sql
web/src/state/hive.ts: roles, permissions, channel visibility
web/src/apps/hive/Sheets.tsx: roles, member card, channels
web/src/apps/hive/HiveApp.tsx: members panel, lock icon, rail
web/src/apps/hive/MessageList.tsx: role-colored sender names
web/src/apps/hive/hive.css: side panel, card, roles, switches
web/src/apps/valet/vlx.css: grid minmax, two-line model name
locales/\*.json: hive roles, channels, members, profile
html/: rebuilt
