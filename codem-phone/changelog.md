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
