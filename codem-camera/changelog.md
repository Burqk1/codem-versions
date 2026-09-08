## 1.2 - 2026-09-08

- Fixed Fivemanage uploads failing silently, so no photo was ever saved when Fivemanage was the selected provider
- Fivemanage now uploads through the server instead of the NUI, so the API key never reaches the game client
- Fivemanage endpoints moved to the current v3 API
- Framing a photo now re-uploads correctly on Fivemanage instead of losing the framed image
- The provider name in UploadConfig.lua is no longer case sensitive

### Changed files

config/UploadConfig.lua: provider value lowercased, Fivemanage v3 endpoints
server/upload.lua: Upload.Fivemanage added, provider name normalised
server/main.lua: serverUpload handles the fivemanage provider
client/main.lua: fivemanage routed through the server

## 1.1 - 2026-09-05

- Fixed a script error firing every few seconds that also stopped players who walked up later from seeing a photo in someone's hand or an open album
- Album pages now fill their texture instead of a small corner of it, cutting video memory per page from about 58 MB to 2.4 MB while rendering sharper - fixes the large FPS drop when opening the album
- Version checker reports new releases on server start
- Console command codem-camera:version re-checks manually

### Changed files

config/Config.lua: album page uv and pageRes
server/handsync.lua: Reading table declared before it is used
server/versionchecker.lua: new
codem-camera-props/stream/album.ydr: page UVs remapped to fill 0..1
