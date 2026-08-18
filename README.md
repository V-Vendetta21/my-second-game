# Star Catcher

A tiny arcade game in a single HTML file. Pick a hero, pick a planet, catch falling stars before they leak into your base.

## Heroes
- **Tank** - huge frame, crushes stars on contact with an expanding shockwave; heavy and slow to drag
- **Bolt** - blistering speed, fires lightning bolts from its sides that catch stars
- **Rock** - fires cone volleys of rocky projectiles every second that catch stars too

## Difficulties & planets
- 3 difficulties (Easy / Medium / Hard) x 3 planets each = 9 levels.
- Planets unlock in order within a difficulty; progress is saved in your browser.
- Each planet has a star target - catch that many stars to clear it.

## Base health
- Your base has 10 HP. Every star that slips past costs 1 HP.
- The slim vertical bar on the right edge shows base health.
- Hearts restore 1 HP. At 0 HP it's game over.

## How to play
- Select a hero, hit Start, then pick an unlocked planet.
- **Drag**: hold the hero icon and drag it across the sky to catch stars (also works with touch).
- WASD or arrow keys work as an alternative.
- Gold stars are worth 50x your combo, hearts restore HP, chains build a combo multiplier.
- **Bombs** fall too (dark spheres with a lit fuse and red glow, ~8% of drops, slower than stars, beeping faster as they near your base). If one reaches the base it explodes for **3 HP damage** - catch it to defuse it safely.
- P pauses, M toggles sound. Best score is saved in your browser.

## Run locally
```
python -m http.server 8080
```
Then open http://localhost:8080
