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
