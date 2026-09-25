## 2.45.5 - 2026-09-25

- Pockets for phone, wallet, cash and radio (Config.pouches)
- Each pocket takes only its own items; one slot per pocket
- Pocket row is a block in arrange mode: move, scale, turn
- Worn outfit set opens and its pieces change in place
- Clothing dropped on a wear box swaps with the set's piece
- 8 coloured parachute items, canopy by parachuteIndex
- Crafting blueprints: recipe locked until the item is used
- Blueprint item teaches its recipe for good, then is used up
- Learned blueprints stored in codem_inventory_blueprints
- Exports: LearnBlueprint, ForgetBlueprint, HasBlueprint
- Export: GetBlueprints
- Config.steal.enable = false turns robbing players off
- Item buttons without a group show in the right-click menu
- Sample lockpick recipe is locked behind lockpick_blueprint
- Fixed: Open on an outfit set closed the inventory
- Fixed: Ctrl / Alt + number fired the hotbar
- Fixed: counts from a million up spilled out of the slot
- Fixed: parachute reserve let F cut and reopen the canopy
- Fixed: parachute pack put into the pockets as a bag
- Fixed: item pictures on server builds that sandbox node fs
- Fixed: container tooltip durability from other inventories
- Fixed: a text degrade value slipped through
- Fixed: version check read codem-clothing's version
- Requires updated codem-inventory-images

### Changed files

fxmanifest.lua: server/blueprints.lua added
shared/config.lua: Config.pouches, Config.steal.enable
shared/utils.lua: pocket slots, gridEnd, steal switch
shared/clothing.lua: outfit set Open keeps inventory open
server/blueprints.lua: new, learned blueprints, recipe lock
server/inventory.lua: pocket stacking, slot count, page data
server/actions.lua: pocket checks, steal, blueprint lock
server/items.lua: blueprint field, degrade fix
server/exports.lua: blueprint exports
server/main.lua: benches sent per player
server/writer.js: pictures via codem-inventory-images
server/admin.lua: missing image resource message
server/versionchecker.lua: key codem-inventoryv2
client/main.lua: hotbar ignores modifiers, steal switch
client/items.lua: keepOpen buttons
client/weapons.lua: parachute rewritten, no reserve
client/carrying.lua: grid end without pockets
migration/: grid end without pockets
clothingitems/server/main.lua: worn set editing and swap
clothingitems/server/legacy.lua: grid end without pockets
clothingitems/client/main.lua: redress, parachute pause
data/items.lua: 8 parachutes, lockpick_blueprint
data/crafting.lua: blueprint field
locales/en.json: pouch, set swap, blueprint keys
locales/tr.json: pouch, set swap, blueprint keys
docs/: crafting blueprints, server exports
build/: rebuilt
