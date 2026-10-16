## 0.1.4 - 2026-10-11

- Config.StaffName: staff shown by character, Steam or Discord name
- Discord name: server nickname, display name or username
- Custom display name per staff member (Staff page)
- Staff messages open as a large card in the middle of the screen
- Config.StaffMessage: card position and duration
- Chat and direct messages window larger and centered
- Same player actions on Players, Live Map and compact menu
- Armor and Ped Menu added to the full panel actions
- Ped Menu picks from a list with previews
- New Watch Screen action: one player's screen in a 16:9 window
- New permission player.watch for screen streams, separate from Spectate
- Screen streams stop when the panel closes
- Stream tiles are 16:9, no more cropped view
- Leaving spectate reopens the panel where it was
- "Message sent" feedback, empty messages are refused
- Live map shows character names
- Vehicle Database: give a model to an online or offline player
- Vehicle Database loads 100 models at a time, search on the server
- Unknown vehicle models can no longer be given
- Given vehicles are placed for the running garage script
- ServerConfig.fivemanage: FiveManage keys in server/config.lua
- More player commands in the command palette
- Command palette: removed player rows that did nothing
- Version checker added
- New texts in all 8 languages

### Changed files

fxmanifest.lua: version 0.1.4, new server files
shared/config.lua: Config.StaffName, Config.StaffMessage
shared/actions.lua: staff:rename
sql/codem-admin.sql: codem_b_admin_staff_names table
server/config.lua: ServerConfig.fivemanage
server/core/discordname.lua: new
server/core/versionchecker.lua: new
server/core/players.lua: staff name source
server/core/actor.lua: staff name source
server/core/db.lua: custom staff names
server/core/catalog.lua: player.watch permission
server/core/vehiclecatalog.lua: known model check
server/actions/staff.lua: staff:rename, staff names in lists
server/actions/session.lua: staff name, rename flag
server/actions/chat.lua: centered direct message
server/actions/players.lua: centered staff message
server/actions/spectate.lua: watch uses player.watch
server/actions/map.lua: character names
server/actions/vehicles.lua: paged catalog, model check
server/actions/reports.lua: FiveManage keys from config
client/main.lua: menu state for spectate
client/modules/spectatecam.lua: reopen the panel after spectating
client/modules/actions.lua: centered staff message
locales/: new texts, all languages
web/build/: rebuilt
