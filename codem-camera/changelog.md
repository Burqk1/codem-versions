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
