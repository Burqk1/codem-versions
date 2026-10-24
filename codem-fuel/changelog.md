## 1.0.1 - 2026-10-24

- Version checker reports new releases on server start
- Console command codem-fuel:version re-checks manually
- Default language is English (Config.Locale = 'en')

### Changed files

fxmanifest.lua: version 1.0.1, server/versionchecker.lua
shared/config.lua: Config.VersionChecker, Config.Locale
server/versionchecker.lua: new

## 1.0.0 - 2026-10-24

- Version checker reports new releases on server start
- Console command codem-fuel:version re-checks manually

### Changed files

fxmanifest.lua: server/versionchecker.lua
shared/config.lua: Config.VersionChecker
server/versionchecker.lua: new
