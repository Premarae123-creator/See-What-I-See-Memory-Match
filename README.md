# See What I See: Memory Match v8

Changes
- I SEE MONEY is now its own GAME MODE, not a category.
- Selecting I SEE MONEY automatically launches the special 32-card setup.
- I SEE MONEY remains multiplayer-capable for up to 32 players.
- Players may choose MORE THAN ONE number. A player can continue choosing available numbers until the $$ card is found.
- The Player Picks panel records every number selected, including multiple selections by the same player.
- Numbered card backs, wrong-card shake/fall animation, random miss voice lines, and money-winner animation remain.
- Camera/microphone multiplayer signaling was rebuilt again:
  - deterministic peer initiator selection
  - room media roster
  - explicit offer/answer exchange
  - renegotiation when camera/mic tracks are enabled
  - two public STUN endpoints
- Same-room replay and Head to Head remain.

Important camera note
WebRTC can still fail on restrictive cellular/corporate/NAT networks without a TURN relay. This build fixes the room signaling logic, but production-grade reliability across all networks requires TURN/SFU infrastructure.

Render
Build: npm install
Start: npm start
