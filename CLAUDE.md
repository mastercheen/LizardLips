# LizardLips

## Purpose
Mobile-first bubble shooter game (codename: LizardLips). Starting from a Puzzle Bobble-style base and evolving into something with more depth — think Grindstone-style progression (map, levels, shop, power-ups) rather than roguelite.

## Tech Stack
- **Frontend:** Vanilla HTML/CSS/JavaScript (single-file game)
- **Rendering:** HTML5 Canvas
- **Target:** Mobile browsers (touch-first, mouse fallback)
- **Hosting:** Docker container on home media server

## File Structure
```
LizardLips/
├── CLAUDE.md
├── Docs/
│   └── index.html        # Main game file (playable)
└── .claude/
    └── settings.local.json
```

## Current State
- Single HTML file with complete Puzzle Bobble clone
- 14-column grid with smaller bubbles for more precision
- Save/load system using localStorage (auto-saves, continue button)
- Touch controls, combo system, levels, particle effects
- Mobile-optimized with proper viewport handling and iOS fixes
- Grid properly centered with correct wall collision boundaries
- Ceiling drop mechanic (drops after N shots without a match)
- Special bubble types: rainbow (wild card), bomb (explodes neighbors), star (bonus points)

## Architecture Decisions
- **2025-02-11** — Single-file architecture for simplicity and easy Docker deployment
- **2025-02-11** — localStorage for saves (simple, no backend needed)
- **2025-02-11** — 14 columns chosen for better precision vs original 10
- **2026-02-11** — Special bubbles use extensible `SPECIAL_TYPES` config object for easy addition of future types

## Track 1: Polish Current Game
Priority features to add:
- [ ] Star rating per level (time/shots)
- [x] Special bubble types (star, bomb, rainbow)
- [x] Ceiling drop mechanic (pressure)
- [ ] Pre-designed levels (not just random)
- [ ] World/level select screen

## Track 2: Bigger Vision (Grindstone-style)
Design direction:
- World map with level nodes
- Increasing difficulty, new mechanics per world
- Currency → shop for power-ups
- Equipment/loadout to bring into levels
- Boss encounters
- Daily challenges

## Known Issues / TODOs
- No git repository initialized yet
- Game branding still says "Bubble Blast" — needs LizardLips identity

## Next Session
- Star rating per level or pre-designed levels
- Initialize git repo when ready
