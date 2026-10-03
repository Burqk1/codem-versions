## 2.0.1 - 2026-10-03

- Unit status wheel on F6 (PoliceConfig.UnitRadial)
- Statuses: Available, Operation, On a Call, Training
- Assign dialog: x next to On call removes the officer
- New export GetCallSign: unit name or badge number
- Dispatch Calls filters: All and My Calls
- Case template previews stay inside their row

### Changed files

fxmanifest.lua: version 2.0.1, UnitRadial.lua
client/Police/UnitRadial.lua: new, status wheel
server/Police/Units.lua: statuses, GetCallSign
config/Police/Config.lua: PoliceConfig.UnitRadial
locales/en.json: statuses, remove from call
locales/tr.json: statuses, remove from call
ui/dist: rebuilt

## 2.0 - 2026-10-03

- New React tablet UI, every page reads live server data
- Units board: create, join, status; assign units to calls
- dispatch_assign: assign, unassign, priority, close calls
- Live dispatch calls, call history tab, Code 7 switch
- Personnel page: status, duty time, prime time, phone
- Discipline: warnings, reprimands, history, limit notice
- Certifications with pictures, levels, departments
- Default certification list changed, old ids not shown
- Framework, inventory, billing, phone from codem-lib
- Security: real source on server, permission checks
- Live description and location sync on cases, reports
- Database: live search, key holders, shared keys filter
- Evidence lockers load 50 at a time, no freeze on open
- Statistics: dispatch responses per officer
- Fixed: CCTV cursor blocked WASD and zoom
- Fixed: license SQL error, Invalid Date, case lock
- Locales load from Lua, no rebuild after edits
- New tables: officer warnings, reprimands, duty totals
- New table: dispatch responses; certifications level
- Requires updated codem-lib and codem-dispatchv2

### Changed files

fxmanifest.lua: version 2.0, new scripts, certificates
config/Police/Config.lua: certs, discipline, prime time
config/Config.lua: framework and inventory keys removed
sql/mdt.sql: 4 tables, certifications level column
server/versionchecker.lua: new
server/Police/Units.lua: new, units and call assignment
server/Police/Personnel.lua: new, discipline, duty totals
server/Police/DispatchStats.lua: new, response stats
server/Police/*: permission checks, paging, live sync
client/Police/Units.lua: new
client/Police/*: new UI callbacks
modules/: framework, inventory, billing via codem-lib
locales/en.json: new UI keys
locales/tr.json: new UI keys
certificates/: new badge pictures
ui/dist: rebuilt

## 1.3 - 2026-09-02
- Overview istatistik ekrani eklendi
- CCTV kayit sistemi iyilestirildi
- Web panel yetki kontrolleri duzeltildi

## 1.2 - 2026-08-10
- Warrant sure ayari eklendi
- Evidence locker bug fix
