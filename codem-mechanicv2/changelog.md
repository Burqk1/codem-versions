## 1.2 - 2026-09-04

- Plate transfer now moves tuning data to the new plate
- Preview no longer changes the vehicle's plate
- One canonical plate key across caches and database
- Padded plate rows from older versions migrated on start
- Tuning build persists on rows with old padded plates
- Requires the updated codem-lib - update it first

### Changed files

shared/utils.lua: added NormalizePlate and PlateKey
server/sv_vehdata.lua: props writer, transfer fix, migration
server/sv_tuner.lua: extras cache keyed by canonical plate
server/sv_inspect.lua: condition cache, saveCondition, RPCs
server/sv_tickets.lua: order plate and props via helpers
server/sv_detailing.lua: uses the shared plate helpers
server/sv_neon.lua: uses the shared plate helpers
server/sv_policenitro.lua: uses the shared plate helpers
client/cl_tuner.lua: preview plate restore fix
client/cl_detailing.lua: uses the shared plate helpers
client/cl_tickets.lua: uses the shared plate helpers
codem-lib qbcore/client.lua: GetPlate trims both ends
codem-lib esx/client.lua: GetPlate trims both ends
