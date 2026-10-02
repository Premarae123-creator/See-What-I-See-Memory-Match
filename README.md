# See What I See: Memory Match v6

Multiplayer reliability update:
- Join Room now joins the host's existing room immediately from the room-code screen; the joining player no longer configures a separate game.
- Lobby shows the host's selected mode, category, card count, host crown, and all joined players. Only the host gets START GAME.
- Turn Battle reveal bug fixed: server-revealed card values are rendered locally while the card is open, so cards no longer appear blank.
- Final leaderboard moved off the game board to its own GAME OVER / FINAL LEADERBOARD screen.
- Server records the multiplayer elapsed time and final scores for the results screen.
- WebRTC signaling rewritten for small rooms: media-ready peers are paired deterministically instead of both sides racing to create offers.
- Added extra STUN fallback and track attachment for camera/mic enabled after a peer connection exists.

Testing camera/mic:
1. Deploy over HTTPS (Render is fine).
2. Join the same room from two separate devices/browsers.
3. Turn camera/mic on for both and allow browser permissions.
4. Each device should show its own preview plus the remote participant.

Note: Peer-to-peer WebRTC can still fail on restrictive carrier/corporate networks without a TURN relay. If that occurs consistently after this signaling fix, the production upgrade is to add a TURN server/SFU.

Render:
Build command: npm install
Start command: npm start
