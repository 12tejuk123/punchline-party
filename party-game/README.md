# Punchline Party
Dependency-free Node.js party game for 2–8 players. Requires Node.js 18+.

## Run on your computer
```
npm start
```
Open http://localhost:3000 in your browser. Create a room, then join with another browser tab (opened independently) or a private window. Each tab is a separate player. On other devices on the same Wi-Fi, open http://YOUR-COMPUTER-LAN-IP:3000 and use the room code. Your firewall must allow Node.js on your private network.

## Rules
Five rounds: answer a funny prompt in 60 seconds, vote for someone else's answer in 30 seconds, then reveal authors and scores. Each vote gives its author one point. Highest total wins; tied players share victory. Host starts and advances rounds. Rounds automatically advance when everyone submits, or the timer expires. Fewer than two answers skips scoring. Refresh reconnects the same tab. No accounts or installations for players.

## Test
```
npm test
```
Covers a complete five-round game, anonymous answer visibility, host permissions, duplicate answers/votes, self-vote rejection, replay, late join rejection and eight-player capacity.

## Prototype limits
Rooms live in server memory and reset when the server restarts. The host must return to advance rounds. Disconnected players wait out the timer. No host migration or persistent storage. Intended for trusted groups and local testing. Server-sent events synchronize devices.
