## 1.0.0 - 2026-10-05

- First release: team GPS for Qbox, QBCore and ESX through codem-lib
- GPS device screen opened by the item or /gps: power key, team list by distance, route to a member, settings
- Callsign: each player enters their code on the GPS, it shows next to their name on the map and in the team list and is kept between sessions
- Groups by job and grade decide who can use the GPS, on duty only if wanted
- GPS channels: players only see the members of their channel; preset channels per group (LSPD, EMS, joint) and free numbered channels
- Map blips in the group colour with a sprite for on foot, car, bike, helicopter, plane and boat
- Built for low server usage: positions are read on the server, only members who moved are sent, one update per group, nearby members are tracked by the player's own game
- Turns off when the job or duty changes, the item is lost or the player logs out
- Blip size and names can be changed per player
- Nine languages: English, Turkish, German, French, Spanish, Portuguese, Italian, Polish and Dutch
- Version checker reports new releases on server start
