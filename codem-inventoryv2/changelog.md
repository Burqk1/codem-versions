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

## 2.42.8 - 2026-09-28

- Fixed: characters undressed on join, clothes in wrong slots
- Wear box move reads the data and runs on every join
- Pocketed garment matching the ped goes back to its box
- Fixed: costume scripts (wingsuit, scuba) became clothing items
- Skin is saved from the wear boxes, not read off the ped
- Fixed: blacklisted codem-clothing pieces became items
- Fixed: carried props multiplied or stayed in the hands
- Carried prop is drawn locally for every player
- Fixed: armour reset on a slow join
- Fixed: auto reload left the clip empty
- Shop amount limit raised from 99 to 999
- Fixed: pockets missing with Config.clothing = false
- New invtest wear tests for the wear box move
- Requires updated codem-lib and codem-clothing

### Changed files

clothingitems/server/legacy.lua: data driven wear box move
clothingitems/server/main.lua: pockets, blacklist, armour
clothingitems/client/main.lua: skin from boxes, armour guard
client/carrying.lua: state bag + local prop
client/weapons.lua: clip check and fallback on reload
server/tests.lua: wear group tests
web/src/components/Pouches.tsx: new, pocket row
web/src/components/Inventory.tsx: pockets without character
web/src/components/Cart.tsx: BUY_MAX 999
build: rebuilt
codem-lib wardrobe/client.lua: save from boxes, blacklist
codem-clothing client/compat.lua: save given slots
codem-clothing client/creator.lua: isClothingBlocked export

## 2.45.9 - 2026-09-30

- Fixed: ESX name = count inventories broke the player load
- ESX items go to free slots, unknown ones listed in console
- Fixed: swap put any item into a clothes bag or wardrobe
- Fixed: taser with no ammo item said out of ammo, never fired
- Taser without an ammo item fires freely, still wears down

### Changed files

server/inventory.lua: reads the ESX name = count layout
server/backpacks.lua: skips entries that are not items
server/actions.lua: swapped item checked against the bag
clothingitems/server/main.lua: wardrobe swap checks both
client/weapons.lua: taser without a registered ammo item
