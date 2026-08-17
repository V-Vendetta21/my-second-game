# Star Catcher

A tiny arcade game in a single HTML file. Pick a hero, pick a planet, catch falling stars before they leak into your base.

## Heroes
- **Tank** - huge frame, huge reach, slow
- **Bolt** - blistering speed, small target
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
- Move with WASD or arrow keys (drag on touch screens).
- Gold stars are worth 50x your combo, hearts restore HP, chains build a combo multiplier.
- P pauses, M toggles sound. Best score is saved in your browser.

## Run locally
```
python -m http.server 8080
```
Then open http://localhost:8080
