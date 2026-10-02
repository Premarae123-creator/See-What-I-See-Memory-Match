# See What I See: Memory Match v9.1 HOTFIX

Fixes:
- Restores the missing I See Money number-selection lobby. The v9 HTML insertion target did not match the actual lobby markup, so the picker never rendered.
- Players can select one or more available numbers 1–32 and lock them before gameplay.
- Host START GAME now gives clear feedback and only starts after every player has locked at least one number.
- I See Money still has no end-game leaderboard.
- Keeps server-synchronized automatic random card reveals, side pick chart, same-room replay, and winner animation.

Render:
Build: npm install
Start: npm start
