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

## 1.0.8 - 2026-09-29

- New exports: OpenSettings, OpenKeybinds
- New exports: OpenMap, OpenStatistics
- Config.DisableMenu: ESC is left alone, pages open by export
- Config.ShowMap: removes the Map entry, shortcut and OpenMap
- Config.RegisterCommands: turns the chat commands off
- Fixed: hovering a blip did not select its legend row
- Fixed: blip counter flickered (13/14/13) while cycling
- See docs/menu-api.md for the export reference

### Changed files

client/client.lua: exports, config switches, map focus, step
config.lua: DisableMenu, ShowMap, RegisterCommands
docs/menu-api.md: direct pages, menu-less setup
web/src/App.tsx: direct page open and close
web/src/components/useSettings.ts: start on Key Bindings
web/src/components/QuickMenu.tsx: Map entry follows ShowMap
html/: rebuilt
