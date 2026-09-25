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
