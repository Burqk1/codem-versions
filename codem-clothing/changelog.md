## 1.0.9 - 2026-10-03

- Shop editor: the shop point can follow the ped
- Moving the ped moves the blip and target with it
- Switch under the ped spot in the Map & Ped tab
- Shops with their own ped spot start with it off
- Fixed: studio Both restarted the 2nd gender from piece 0
- Studio progress bar now matches the real frame count

### Changed files

fxmanifest.lua: version 1.0.9
server/admin.lua: shop ped linked saved
client/studio.lua: start point kept for the second gender
locales/en.lua: ped link switch keys
locales/tr.lua: ped link switch keys
html/: rebuilt

## 1.0.8 - 2026-10-03

- Shop stock can be set per texture, not only per piece
- Products picker: palette badge opens a piece's textures
- Unstocked textures never show; server checks on purchase
- Old stock lists keep working, no migration
- Hovering a card in Products shows a big preview
- Piece grid: arrow keys move, camera turns with Q / E
- New client/hooks.lua: canOpen, menuOpened, menuClosed
- Events codem-clothing:client:menuOpened / menuClosed
- Fixed: panel layout ignored the shop's Only these stock
- Fixed: hat, glasses, watch, bracelet off the slot row

### Changed files

fxmanifest.lua: version 1.0.8, client/hooks.lua
client/hooks.lua: new, menu hooks
client/creator.lua: menu hooks and events, texture data
client/admin.lua: catalog sends textures per piece
server/admin.lua: stock keys per texture, limit 20000
server/shops.lua: purchase checks the texture stock
locales/en.lua: texture picker keys, rotate hint
locales/tr.lua: texture picker keys, rotate hint
html/: rebuilt

## 1.0.7 - 2026-09-30

- Outfit limit is now Config.MaxOutfits, default 50
- Config.MaxOutfits = 0 removes the limit
- The limit also covers adding an outfit by code
- New event codem-clothing:client:skinLoading
- Inventory no longer zeroes the vest while a skin loads
- Fixed: ESX multicharacters got the shop, not the creator
- esx_skin:openSaveableMenu opens the creator like illenium
- onSubmit / onCancel of the caller are run
- Fixed: panel layout ignored the shop's Only these stock
- Steppers and grid now skip pieces the shop does not sell

### Changed files

fxmanifest.lua: version 1.0.7
client/compat.lua: openSaveableMenu opens the creator
client/spawn.lua: skinLoading event around the skin apply
server/outfits.lua: limit from Config.MaxOutfits
shared/config.lua: Config.MaxOutfits = 50
html/: rebuilt, panel steppers follow the shop stock

## 1.0.6 - 2026-09-28

- New export isClothingBlocked for inventory clothing items
- Blacklisted pieces are no longer turned into items
- Blacklist check uses gender, identifier and ace rules
- Fixed: inventory could save the previous outfit piece
- savePedClothing now takes the worn pieces from inventory
- Needs updated codem-lib, update it first
- Old codem-lib: inventory error field IsBlocked is nil

### Changed files

fxmanifest.lua: version 1.0.6
client/compat.lua: savePedClothing merges worn pieces
client/creator.lua: Creator.IsBlocked, isClothingBlocked

## 1.0.5 - 2026-09-25

- Buy for Someone: dress a mannequin, get the pieces as items
- Shelf, prices and stock follow the mannequin's body
- Cash or bank is picked in a checkout popup, not up top
- Camera button: right drag turns the character, not camera
- Second copy + button next to the slot stepper in the panel
- The + keeps its place, dimmed on an empty slot
- Ped list: ig_tony, pw_beany, pw_bobby, pw_midget_antonio
- Fixed: Michael saved as the skin when items saved on login
- Gifts and second copies need codem-inventoryv2 clothing

### Changed files

fxmanifest.lua: version 1.0.5
shared/config.lua: Config.Shops.gifts
shared/peds.lua: four ped models
server/appearance.lua: partial save needs a stored skin
server/shops.lua: gift lines given for the chosen body
client/spawn.lua: Spawn.ready()
client/compat.lua: savePedClothing waits for the skin
client/creator.lua: gift mannequin, gift:pick, ped:turn
locales/en.lua: pay, gift, spin keys; pay chip keys removed
locales/tr.lua: pay, gift, spin keys; pay chip keys removed
html/: rebuilt
