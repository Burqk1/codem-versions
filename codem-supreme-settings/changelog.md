## 1.0.6 - 2026-09-25

- Key Bindings: GTA controls are editable, click a key and press
- In-use key: the game's assign question shows, Enter yes, Esc no
- Restore All Defaults is an action now: click, confirm, reload
- Leave question explains: No, bind the required action, leave
- Fixed: map key opened and closed the map in one press
- Fixed: "Preparing the map" pass on every map open
- Fixed: dark blurred box under the toast after a blip click
- Fixed: game bindings took 10-60 s to apply after leaving
- Fixed: the click that started listening was taken as Mouse 1
- Fixed: conflict question could not be answered from the menu

### Changed files

client/client.lua: gtaBind, leaveKeymap, restore, map key
locales/en.json: keymap hint keys; map.preparing removed
locales/tr.json: keymap hint keys; map.preparing removed
html/: rebuilt

## 1.0.7 - 2026-09-27

- Map legend rebuilt on the game's own rows and selection
- Hidden groups stay hidden after the legend rebuilds
- Removed the black "Reading group names" pass on search
- Hiding a group no longer tours the cursor over the map
- Unhidden rows no longer vanish for 2-3 seconds
- Hidden blips stay hidden on the minimap and in the world
- Mouse 4 / Mouse 5 can be bound in Key Bindings
- Waypoint accept polls the row, no fixed 350 ms wait
- New "N hidden - Show all" chip in the map header
- Hidden lists reset once (new storage keys)
- Debug commands removed; pausehiddenclear stays

### Changed files

client/client.lua: legend rewrite, show all, mouse 4/5
locales/en.json: map.showAll, keybind.mouse4/5
locales/tr.json: map.showAll, keybind.mouse4/5
html/: rebuilt
