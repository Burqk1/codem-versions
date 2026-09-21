## 1.0.3 - 2026-09-21

- Key Bindings: changes never saved, FiveM denied rbind
- Key changes now queue up, hold F10 to write them
- Old key is removed, not left active next to the new one
- Other scripts sharing the old key are bound back
- Saved keys are read back from the game to confirm
- Unsaved key changes are dropped when the menu closes
- Map: SetBlipCategory groups can now be hidden
- First hide of a group scans it once, then it is instant
- Hiding blips overlay locks the panel during the scan
- Removed auto rescans that dragged the map cursor around
- Stepping a grouped row no longer sticks on one blip
- Blip list opens faster, dump chunk adapts to 63 bytes
- Map waits for live legend rows before accepting hides
- Unlisted group shows a reopen hint instead of failing
- New Config.SaveBindsKey, default F10, players can rebind
- New locale keys under keybind, ui.keymap and ui.map

### Changed files

client/client.lua: save key flow, blip groups, scan cache
config.lua: Config.SaveBindsKey
locales/en.json, tr.json: save banner and map overlay keys
web/src/components/Keymap.tsx: pending banner, hold to save
web/src/components/MapView.tsx: scan overlay, panel lock
web/src/index.css, types.ts: overlay styles, new messages
html/: rebuilt
