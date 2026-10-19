## 1.0.7 - 2026-10-19

- Dive sonar: arrow, rough distance and false signals
- Dive crate sparkles and glows when you are close
- Underwater open animation before the crate reward
- Dive board starts full, every dive type on offer
- New admin commands /fishdive and /fishtournament
- Missing dive crate model printed once in F8
- Config.Locale back to 'en'
- Version checker reports new releases on start

### Changed files

fxmanifest.lua: version 1.0.7
client/dives.lua, server/dives.lua: sonar, glow, board
server/tournament.lua: /fishtournament
config/dives.lua: sonar, openAnim, glow, max 12
config/main.lua: Config.Locale en
server/versionchecker.lua: new
locales/*.json: sonar and command texts
html/: rebuilt

## 1.0.6 - 2026-10-12

- Version checks start with the next update
