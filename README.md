# Neon Drift Royale

Neon Drift Royale is a fast, single-file browser battle royale. Pilot a neon ship around a shrinking arena, collect orbs, level up with upgrades, and be the last ship alive. Play solo against bots, or with friends online. The whole game is one HTML file with no accounts and no install.

## How to play

- **Move:** WASD or arrow keys
- **Aim:** mouse
- **Fire:** hold the mouse button or press SPACE
- **Upgrades:** press 1, 2 or 3, or tap a card when you level up
- **Map:** TAB or M
- **Pause:** ESC
- **Touch:** the left half of the screen drags a stick to move; the right half aims and fires

The zone shrinks every 20 seconds. Outside it you lose HP. Kill drones and asteroids for XP and orbs, and hit other players for XP too. Green + pickups heal you inside the zone. Last ship alive wins.

## Multiplayer

Enter a room code in the box on the title screen (leave it empty for the default room, `public`) and press **ONLINE MATCH**. Everyone who enters the same code lands in the same room. Share this page's link and the code with friends.

Online play is peer-to-peer over WebRTC using [PeerJS](https://peerjs.com) and its free public signalling server. There is no game server. The first player to join a room hosts it: their browser relays everyone's ship position to the others. If the host leaves, the remaining players automatically elect a new host within a few seconds and the match carries on.

Peer-to-peer connections can fail on some restrictive networks (for example, some corporate or campus Wi-Fi). If the page says it could not reach the matchmaking server, check your connection and try again.

**SAME-BROWSER TABS** lets you test multiplayer with several windows of one browser, no network needed.

## Settings

- **Player:** name (up to 14 characters) and ship colour
- **Match (host or solo):** starting HP, damage multiplier, XP multiplier, zone speed (slow, normal, fast), world size (small, medium, large)
- **Bots (solo only):** number of bots and bot difficulty (easy, normal, hard)
- **Graphics:** quality (high or low), screen shake, damage numbers, FPS counter

Settings and your best results are saved in your browser's local storage.

## Run locally

Open `index.html` in a modern browser. Online play needs internet access to load PeerJS and reach the signalling server; solo play and same-browser tabs work offline.

## License

MIT
