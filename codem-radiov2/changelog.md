## 1.0.8 - 2026-10-08

- New handheld radio prop codem_radio with the radio screen
- New setting: how many members the on-screen list shows
- Talking members always show, even past the limit
- Long member lists split into columns
- Member list header shows no "Unnamed" for unnamed channels
- DefaultChannels: police vehicles start on 1.10

### Changed files

fxmanifest.lua: version 1.0.8, codem_radio.ytyp
stream/codem_radio.ydr: new radio prop
stream/codem_radio.ytyp: new radio prop
shared/tuning.lua: hand prop is codem_radio
config.lua: hudLimit, DefaultChannels.police
server/storage.lua: hudLimit setting
locales/*.json: hud_limit, hud_limit_all
html/: rebuilt

## 1.0.7 - 2026-10-07

- Channels without a name no longer show "Unnamed channel"; only the frequency is shown

### Changed files

fxmanifest.lua: version 1.0.7
html/: rebuilt

## 1.0.6 - 2026-10-05

- Callsign can be set per channel like nickname and colour
- New export SetCallsign(source, text) for other scripts
- codem-mdtv2 2.0.3 syncs the MDT unit name as callsign
- Vehicle radio is front seats only
- Member HUD always shows whoever is talking
- Own voice playback also on the vehicle radio

### Changed files

fxmanifest.lua: version 1.0.6
server/main.lua: SetCallsign export, rear-seat checks
server/vehicle.lua: IsFront, front-seat tracking
server/storage.lua: callsign per channel
server/channels.lua: callsign per channel
server/ambience.lua: callsign per channel
client/main.lua: front-seat checks, resync event
locales/*.json: toast_rear_seat
html/: rebuilt

## 1.0.5 - 2026-10-03

- Fixed: a phone call partner heard you through the radio filter when you pressed the radio key; calls now always sound like a call
- Fixed: muting someone on the radio muted them in the whole game; it now only mutes their radio
- Fixed: codem-inventoryv2 players stayed on the channel after dropping the radio
- Fixed: the radio item check scanned every player at once and caused a server spike; losing the radio is now caught from inventory events, list in shared/utils.lua
- Fixed: downed players could not talk but a radio click still went out
- Fixed: radio static still played in debug playback with static turned off
- Settings: radio static and click sounds can be turned off per player; /micclick toggles the same setting
- Hide me in lists moved from the settings to Config.Anonymous

### Changed files

fxmanifest.lua: version 1.0.5, shared/utils.lua added
config.lua: Anonymous replaces AllowAnonymous, static and clicks settings
shared/utils.lua: new, inventory events list
shared/tuning.lua: ItemCheckInterval removed
client/main.lua: inventory events, death check, /micclick uses the setting
client/signal.lua: radio-only mute, call partners skipped
client/fx.lua: call partners keep the call voice
server/main.lua: item poll removed
server/storage.lua: static and clicks settings, anonymous from config
locales/*.json: static and click keys, anonymous removed
html/: rebuilt

## 1.0.0 - 2026-09-29

- First release: handheld radio on pma-voice for Qbox, QBCore and ESX through codem-lib
- Only the server puts players on a radio channel, so joining a police channel through pma-voice events, exports or state bags is blocked
- Unit channels by job, grade and duty, gang, identifier, ace or a custom check; players are removed when they lose access, go off duty or drop the radio
- Player channels with an owner, ownership handover and optional password; five wrong passwords lock that channel for a minute
- Favorites, recent channels and settings saved per character
- Member list on screen with talking indicator, callsign, anonymous mode and streamer mode
- Talk animations, radio prop seen by other players, radio sounds and three screen colors
- Radio voice filter, rougher when the signal is weak
- Range and signal bars: voices get weaker and break up with distance and cut out of range
- Dashboard radio in configured vehicles, with its own name in the member list and its own talk key
- Dual watch: the dashboard radio listens to a second channel next to the handheld's and talks on it with its own button
- Radio speaker: players next to someone hear their radio, from the side it is on and muffled from a closed car; set separately for handheld and dashboard radios, with an earpiece setting to keep it private
- Background sounds behind a transmission: siren, helicopter rotor and gunshots
- Jammer: placeable item that cuts radios around it, started from a tablet terminal with an access code and a signal-lock minigame
- Radio scanner item that lists active channels nearby with their signal strength and member count
- Nine languages: English, Turkish, German, French, Spanish, Portuguese, Italian, Polish and Dutch
- Server exports: HasAccess, GetPlayerFrequency, GetPlayersOnFrequency, SetPlayerChannel, CreateChannel, RemoveChannel, GiveAccess, RemoveAccess, UpdateChannelLabel
- Client exports: Open, Close, IsOpen, IsConnected, GetFrequency
- Version checker reports new releases on server start; console command codem-radiov2:version re-checks manually
