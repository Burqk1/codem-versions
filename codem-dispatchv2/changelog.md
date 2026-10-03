## 2.0.1 - 2026-10-03

- Version check on server start, console update notice
- New command: codem-dispatchv2:version
- Language files: locales/en.json and locales/tr.json
- All alert and panel texts read from the locale file
- Panel and call cards use game blur glass background

### Changed files

fxmanifest.lua: version 2.0.1, locale, versionchecker
config/Config.lua: Locale and VersionChecker added
shared/locale.lua: new
locales/en.json: new
locales/tr.json: new
server/versionchecker.lua: new
