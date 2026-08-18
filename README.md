# Star Catcher

A tiny arcade game in a single HTML file. Pick a hero, pick a planet, catch falling stars before they leak into your base.

A detailed animated title card (halftone patterns in hero colors, glowing hero orbs) plays for ~2 seconds on launch.

## Heroes
- **Tank** - huge frame, crushes stars on contact with an expanding shockwave; heavy and slow to drag
- **Bolt** - blistering speed, fires lightning bolts from its sides that catch stars
- **Rock** - fires cone volleys of rocky projectiles every second that catch stars too

## Difficulties & planets
- 3 difficulties (Easy / Medium / Hard) x 3 planets each = 9 levels.
- Planets unlock in order within a difficulty; progress is saved in your browser.
- Each planet has a star target - catch that many stars to clear it.

## Endless mode (adaptive)
- **ENDLESS** card on the planet screen (or press **4**) - infinite waves, no target, survive as long as you can.
- **DDA (Dynamic Difficulty Adjustment)**: the game reads how well you're doing. Catch streaks push the difficulty up (faster spawns, faster falls, more bombs), while leaks ease it back off with a short grace period. The **ADAPT** bar in the HUD shows the current difficulty (green = relaxed, yellow = normal, red = intense).
- Difficulty also ramps with time and every **wave** (30s) warps you to a new planet.
- **Upgrades**: catching stars / defusing bombs earns XP (XP gain grows with each level). Level up and pick 1 of 3 upgrades: GROWTH (+size), SPEED, ARMOR (+HP), RICH (+score), MULTI (+projectiles per volley - extra lightning for Bolt, extra rocks for Rock, bigger shockwave for Tank), RAPID (fire rate - not offered to Tank), MAGNET (pulls stars), LUCKY (more gold stars), BOMBPROOF (touching bombs defuses them), REGEN (heal 1 HP every 8s), CRIT (chance to double score), COMBO+ (combo lasts longer), FREEZE (bombs fall slower).
- Separate endless best score is saved in your browser.

## Base health
- Your base has 10 HP. Every star that slips past costs 1 HP.
- The slim vertical bar on the right edge shows base health.
- Hearts restore 1 HP. At 0 HP it's game over.

## How to play
- Select a hero, hit Start, then pick an unlocked planet.
- **Drag**: hold the hero icon and drag it across the sky to catch stars (also works with touch).
- WASD or arrow keys work as an alternative.
- Gold stars are worth 50x your combo, hearts restore HP, chains build a combo multiplier.
- **Bombs** fall too (dark spheres with a lit fuse and red glow, ~8% of drops, slower than stars, beeping). They can't hurt your base if they slip past - but **touching one with your hero explodes it for 3 HP damage**, so dodge them. Projectiles and abilities (lightning, rocks, crush shockwave) still destroy them safely.
- P pauses, M toggles sound. Best score is saved in your browser.

## Audio
- `audio/star-warp.mp3` (cartoonish warp #4) drives the **star spawning** sound and most gameplay SFX via pitch-shifting: catches pitch up with your combo, gold stars ring higher, bombs/leaks drop deep and slow, explosions layer both tracks pitched way down.
- `audio/bolt-warp.mp3` (cartoonish warp #2) is **Bolt's lightning spawn**, and is re-pitched for defuses, level-ups, menu clicks and the endless-start fanfare.
- `audio/music.mp3` (spacey cart #2) is the **background music** - loops seamlessly (from the 10s mark on longer tracks).
- **Settings bar** (gear icon, top right): toggle music on/off and drag the volume slider. Settings are saved in your browser; M mutes everything.
- Run via `python -m http.server` (samples load over HTTP).

## Run locally
```
python -m http.server 8080
```
Then open http://localhost:8080
