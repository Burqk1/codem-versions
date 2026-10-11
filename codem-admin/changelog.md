## 0.1.4 - 2026-10-11

- Config.StaffName: staff shown by character, Steam or Discord name
- Discord name: server nickname, display name or username
- Custom display name per staff member (Staff page)
- Staff messages open as a large card in the middle of the screen
- Config.StaffMessage: card position and duration
- Chat and direct messages window larger and centered
- Version checker added

### Changed files

fxmanifest.lua: version 0.1.4, new server files
shared/config.lua: Config.StaffName, Config.StaffMessage
shared/actions.lua: staff:rename
sql/codem-admin.sql: codem_b_admin_staff_names table
server/core/discordname.lua: new
server/core/versionchecker.lua: new
server/core/players.lua: staff name source
server/core/actor.lua: staff name source
server/core/db.lua: custom staff names
server/actions/staff.lua: staff:rename, staff names in lists
server/actions/session.lua: staff name, rename flag
server/actions/chat.lua: centered direct message
server/actions/players.lua: centered staff message
client/modules/actions.lua: centered staff message
locales/: new texts
web/build/: rebuilt
