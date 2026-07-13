<div align="center">

# 🎃 Survivor — 2D Survival & Management Game

> *A fully browser-based 2D survival game built with pure HTML5 Canvas & JavaScript. No dependencies. No install. Just open and play.*

[![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20Mobile-blue?style=flat-square)](https://github.com)
[![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=flat-square)](package.json)
[![Game Type](https://img.shields.io/badge/Genre-Survival%20%7C%20Management-purple?style=flat-square)](https://github.com)

<br/>

```
  🌲🌲🌲   You are 🎃   🌲🌲🌲
  🌲    Survive the dark world    🌲
  🌲🌲   Hunt · Farm · Fight   🌲🌲
```

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Unique Features](#-unique--exclusive-features)
- [Game Locations](#-game-locations)
- [Gameplay Mechanics](#-gameplay-mechanics)
- [Controls](#-controls)
- [Crafting System](#-crafting-system)
- [Inventory & Items](#-inventory--items)
- [Enemy System](#-enemy-system)
- [Leveling & Progression](#-leveling--progression)
- [Day/Night Cycle & Weather](#-daynight-cycle--weather)
- [Tips & Strategy](#-tips--strategy)
- [How to Run](#-how-to-run)
- [Project Structure](#-project-structure)
- [Technical Details](#-technical-details)
- [Roadmap](#-roadmap)
- [Known Issues](#-known-issues)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌍 Overview

**Survivor** is a fully self-contained 2D survival game built with **zero external libraries** using only HTML5 Canvas, CSS, and vanilla JavaScript. You play as 🎃 — a lone survivor who must manage vital needs, upgrade their shelter, raise farm animals, craft weapons, and battle the undead lurking in the dark forest.

The game runs entirely in the browser with no server, no backend, and no build tools required. Just open `survival_game.html` and play.

---

## ✨ Features

### Core Systems

| Feature | Description |
|---|---|
| 🏠 Safe House | Your home base with all essential equipment |
| 🐄 Barn / Stable | Raise and manage farm animals interactively |
| 🌲 Dark Forest | Dangerous outdoor zone for resource gathering and combat |
| ❤️ Survival Stats | Real-time HP, Hunger, and Stamina bars |
| 🌙 Day/Night Cycle | 6 time phases with gameplay effects |
| 🎒 Inventory System | Collect, store, consume, and equip items |
| 📦 Chest Storage | Transfer items between backpack and home chest |
| ⚒️ Crafting Bench | Craft weapons, tools, and structures |
| 🧟 Zombie AI | Smart enemies that track and damage the player |
| ⭐ XP & Leveling | Gain experience and level up for permanent stat boosts |

---

## 🚀 Unique & Exclusive Features

These features go beyond the original specification and make the game richer:

### 🌦 Dynamic Weather System
Five distinct weather types affect visibility and atmosphere:
- ☀️ Sunny — clear visibility, full movement
- ⛅ Cloudy — slight atmosphere change
- 🌧 Rainy — animated rain drops fall across the screen
- 🌫 Foggy — reduced ambient light
- ⛈ Stormy — rain + darkness combined

Weather changes randomly every 60 seconds.

### ⭐ Full XP & Level-Up System
- Every action grants EXP (combat, crafting, harvesting, cooking)
- Visual level-up banner appears on screen
- Each level permanently increases: Max HP (+15), Attack (+3), Defense (+1)
- EXP bar visible beneath the player character at all times

### ☠️ Zombie Poison Mechanic
- Some zombies can poison the player on contact
- Poison drains HP over time with a purple glow effect
- Cure with 🌿 Herb, or wait for the poison to expire naturally

### 💀 Fast Zombie Variant
- Rare (30% spawn chance) fast purple zombie — `💀`
- Moves 60% faster than standard zombies
- Has less HP but is far more dangerous
- Drops rare loot including 🌿 Herb

### 🔥 Campfire System
- Place and toggle a campfire in the safe house
- Required to cook raw meat on the stove
- Provides a warm light radius during night phases (radial gradient glow)
- Visual orange light spread across the home screen at night

### 🏹 Ranged Bow & Arrow Combat
- Craft the 🏹 Bow at the crafting bench
- Click anywhere on screen in the forest to shoot arrows
- Projectiles travel in real-time and deal damage on hit
- Allows safe combat from outside zombie melee range

### 🗺 Live Minimap
- Always-visible minimap (top-right corner)
- Shows player position (gold dot)
- In the forest: shows resources (green) and zombies (purple)
- Updates every frame in real-time

### 📋 Quest / Objective System
- Progressive quest list guides new players step-by-step
- Quests auto-complete based on in-game actions
- Covers: barn collection, forest exploration, combat, crafting, cooking, sleeping, gem-hunting

### 💎 Rare Gem Drops
- Gems drop randomly from mining stone (15% chance) and rare zombies (15% chance)
- Tracked as a collectible — future updates will use them for trading/upgrades

### 🏆 Score & Kill Counter
- Persistent score displayed in the top-right HUD
- Score increases from kills (+25), surviving days (+10×day), and crafting (+30)
- Kill counter tracks total zombie eliminations

---

## 🗺 Game Locations

### 🏠 Safe House
Your primary base of operations. Contains:

| Object | Interaction | Effect |
|---|---|---|
| 🛏 Bed | Click (night only) | Restores full stamina + 30 HP, skips to next morning |
| 📦 Chest | Click | Opens chest ↔ inventory transfer UI |
| 🍳 Stove | Click | Starts cooking meat (requires campfire active) |
| ⚒️ Crafting Bench | Click or press `C` | Opens crafting recipe menu |
| 🌳 Apple Tree | Click | Picks 1–2 apples (resets each new day) |
| 🐴 Horse | Click | Opens travel menu to Barn or Forest |
| 🔥 Campfire | Click | Toggles fire on/off |
| 🦃 Turkeys | Click (within range) | Hunt for 🍖 raw meat |

> **Note:** You must have 🌾 Grass in inventory to travel to the Dark Forest (horse needs feeding).

---

### 🐄 Barn
A dynamic animal management zone. Animals wander freely. Click them to interact.

| Animal | Product | Cooldown | Slaughter Drops |
|---|---|---|---|
| 🐔 Chicken | 🥚 Egg | 30 sec | 🍖 Meat |
| 🐄 Cow | 🥛 Milk | 30 sec | 🍖 Meat + 🦌 Hide |
| 🐑 Sheep | 🧶 Wool | 30 sec | 🍖 Meat + 🦌 Hide |

Animals reset their "ready" status on each new day. Slaughtering permanently removes the animal.

---

### 🌲 Dark Forest
The most dangerous zone. Resources respawn each new day.

| Resource | Item Dropped | Tool Bonus |
|---|---|---|
| 🌲 Tree | 🪵 Wood (×1) | 🪓 Axe → ×2 wood |
| 🪨 Stone | 🪨 Stone (×1) | None (standard) |
| 🌿 Herb Patch | 🌿 Herb (×1) | None (click once per day) |
| 💀/🧟 Zombie | 🌾 Grass, 🌿 Herb, 💎 Gem | Sword/Bow for faster kills |

> Zombies spawn continuously from screen edges. Difficulty scales with current day.

---

## 🎮 Gameplay Mechanics

### Survival Stats

```
❤️  HP        — Reaches 0 = Game Over
🍖  Hunger    — Drains over time. At 0, HP begins draining slowly
😴  Stamina   — Drains while moving. Restores during night or sleep
```

### Hunger Management
- Hunger drains at a constant rate passively
- At 0 hunger: HP drains at ~0.008 per ms
- Foods that restore hunger:

| Item | Hunger Restored |
|---|---|
| 🍎 Apple | +30 |
| 🥚 Egg | +20 |
| 🥛 Milk | +25 |
| 🥩 Cooked Meat | +60 |

### Cooking Flow
```
🦃 Kill Turkey / 🐄 Slaughter Animal
        ↓
    🍖 Raw Meat (in inventory)
        ↓
    🔥 Light Campfire
        ↓
    🍳 Click Stove (queues up to 3)
        ↓
    ⏱ 4 seconds per piece
        ↓
    🥩 Cooked Meat ready!
```

---

## 🕹 Controls

### Keyboard

| Key | Action |
|---|---|
| `W A S D` | Move player |
| `Arrow Keys` | Move player (alternative) |
| `H` | Return to Safe House (from any location) |
| `C` | Open Crafting Bench |
| `I` | Open Chest / Inventory |
| `E` | Interact (shortcut) |

### Mouse / Touch

| Action | Effect |
|---|---|
| Click on animal (Barn) | Open animal interaction menu |
| Click on zombie (Forest) | Attack (melee or bow) |
| Click on tree/stone (Forest) | Harvest resource |
| Click on herb patch (Forest) | Collect herb |
| Click on item (Inventory bar) | Consume / Equip / Unequip |
| Click on chest slot | Move item to/from chest |
| D-Pad buttons (mobile) | Move player |

---

## ⚒️ Crafting System

Open the crafting bench by clicking ⚒️ or pressing `C`. Crafted items are automatically equipped.

| Item | Wood | Stone | Effect |
|---|---|---|---|
| 🪓 Axe | 3 | 2 | Doubles wood harvest; +40% damage |
| ⚔️ Sword | 2 | 5 | Doubles melee damage |
| 🏹 Bow | 4 | 1 | Enables ranged attacks (click to shoot) |
| 🔦 Torch | 2 | 0 | Improves night visibility (future use) |
| 🧱 Stone Wall | 0 | 8 | Base defense structure (future use) |

> Items that can't be crafted (missing materials) appear greyed out with 50% opacity.

---

## 🎒 Inventory & Items

### Full Item Reference

| Emoji | Key | Name | Use |
|---|---|---|---|
| 🪵 | `wood` | Wood | Crafting material |
| 🪨 | `stone` | Stone | Crafting material |
| 🍎 | `apple` | Apple | +30 Hunger |
| 🍖 | `meat` | Raw Meat | Must be cooked first |
| 🥩 | `cookedMeat` | Cooked Meat | +60 Hunger |
| 🥚 | `egg` | Egg | +20 Hunger |
| 🥛 | `milk` | Milk | +25 Hunger |
| 🧶 | `wool` | Wool | Future: crafting clothes |
| 🦌 | `hide` | Animal Hide | Future: armor crafting |
| 🌿 | `herb` | Medicinal Herb | +30 HP, cures poison |
| 🌾 | `grass` | Fresh Grass | Required to ride horse to forest |
| 💎 | `gem` | Rare Gem | Future: trading/upgrades |
| 🪓 | `axe` | Axe | Equippable tool/weapon |
| ⚔️ | `sword` | Sword | Equippable weapon (×2 dmg) |
| 🏹 | `bow` | Bow | Equippable ranged weapon |
| 🔦 | `torch` | Torch | Night light tool |
| 🧱 | `wall` | Stone Wall | Defense structure |

### Chest Transfer
- Click **Chest 📦** to open the two-panel transfer UI
- Left panel = your inventory | Right panel = chest storage
- Click any item to transfer it in the corresponding direction

---

## 🧟 Enemy System

### Standard Zombie 🧟
- Speed: 1.1 px/frame
- HP: 80
- Drops: 🌾 Grass, sometimes 🌿 Herb
- Rare drop: 💎 Gem (15%)

### Fast Zombie 💀
- Speed: 1.8 px/frame (63% faster)
- HP: 40
- Drops: 🌾 Grass, 🌿 Herb
- Rare drop: 💎 Gem (15%)
- Can **poison** the player on contact (8s duration, drains HP)

### Spawn Rate
Zombies spawn from random screen edges. Spawn probability increases with each day:
```
Spawn chance = 0.003 × (1 + day × 0.1) per frame
Max zombies  = 8 + day number
```

### Combat Damage Formula
```
Player deals: (base_attack + (level-1) × 3) × weapon_multiplier
  Sword multiplier: ×2.0
  Axe multiplier:   ×1.4
  No weapon:        ×1.0

Zombie deals: (5 - defense × 0.5) per 500ms of contact
```

---

## ⭐ Leveling & Progression

### EXP Sources

| Action | EXP Gained |
|---|---|
| Kill zombie (normal) | 15 + (day × 2) |
| Hit zombie | +5 per hit |
| Harvest resource | +5 |
| Hunt turkey | +8 |
| Pick apple | +3 |
| Craft item | +20 |
| Sleep / new day | — |

### Level Up Effects
Each level permanently upgrades:
- ❤️ Max HP +15 (and heals to full)
- ⚔️ Attack +3
- 🛡 Defense +1
- 📈 Next level requires ×1.6 more EXP than previous

---

## 🌙 Day/Night Cycle & Weather

### Time Phases

| Phase | Icon | Duration | Effect |
|---|---|---|---|
| Morning | 🌅 | ~18s | Normal gameplay |
| Noon | ☀️ | ~18s | Normal gameplay |
| Afternoon | 🌤 | ~18s | Normal gameplay |
| Sunset | 🌇 | ~18s | Normal gameplay |
| Night | 🌙 | ~18s | Dark overlay, stamina regenerates, can sleep |
| Midnight | 🌑 | ~18s | Darkest overlay, campfire glow visible |

- New day resets: Apple tree, herb patches, forest resources, animal readiness
- Sleep (click bed at night) skips to morning instantly

### Weather System

| Weather | Icon | Visual Effect |
|---|---|---|
| Sunny | ☀️ | Clear |
| Cloudy | ⛅ | Atmosphere only |
| Rainy | 🌧 | Animated rain drops |
| Foggy | 🌫 | Reduced ambiance |
| Stormy | ⛈ | Rain + dark overlay |

Weather changes every 60 seconds randomly.

---

## 💡 Tips & Strategy

### Early Game (Days 1–3)
1. **Collect apples** from the tree first — free early food
2. **Hunt turkeys** in the yard for raw meat
3. **Light the campfire** and cook all your meat before going to bed
4. Travel to the forest only with at least 🌾 Grass in inventory
5. In the forest, **stay near edges** and collect nearby resources before zombies arrive
6. Return home with `H` if HP drops below 40

### Mid Game (Days 4–8)
1. Craft 🪓 Axe first — doubles your wood income
2. Then craft ⚔️ Sword — makes zombie combat far easier
3. Keep 🌿 Herbs stocked — antidote for poison and HP heal
4. Max out chest storage with 🪵 Wood and 🪨 Stone for crafting reserves
5. Milk the 🐄 Cow and collect 🥚 Eggs daily for easy hunger management

### Late Game (Day 9+)
1. Craft 🏹 Bow for safe ranged zombie farming
2. Focus on XP: fast zombies (💀) give the most drops per kill
3. Stack armor (Defense) through leveling to survive longer forest runs
4. Check the quest panel — completing objectives gives bonus score

### Combat Tips
- **Kite enemies:** click to attack one, back away, click again — repeat
- **Bow priority:** always target fast zombies first with ranged attacks
- **Poison cure:** herb cures instantly; always carry at least 1
- **Don't stack zombies:** avoid letting 3+ surround you simultaneously

---

## 🚀 How to Run

### Option 1 — Direct File (Simplest)
```bash
# Download the file and open it
open survival_game.html
# or double-click the file in your file manager
```

### Option 2 — Local Server (Recommended)
```bash
# Python 3
python -m http.server 8000
# Then open: http://localhost:8000/survival_game.html

# Node.js
npx serve .
# Then open: http://localhost:3000/survival_game.html
```

### Option 3 — GitHub Pages
1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, root `/`
4. Visit `https://yourusername.github.io/survivor/survival_game.html`

### Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| Mobile Chrome | ✅ Full touch support |
| Mobile Safari | ✅ Full touch support |

> **No installation. No npm. No build step. Zero dependencies.**

---

## 📁 Project Structure

```
survivor/
│
├── survival_game.html      # The entire game — single self-contained file
│
├── README.md               # This file
└── LICENSE                 # MIT License
```

The entire game — including all logic, UI, styles, and assets (emoji-based) — lives in a **single HTML file** (~900 lines). No external scripts, no CSS files, no image assets.

---

## 🔧 Technical Details

### Architecture

```
HTML5 Canvas (2D rendering)
  └── Game Loop (requestAnimationFrame)
        ├── update(dt)
        │     ├── updateTime()       — phase/day/weather ticks
        │     ├── updatePlayer()     — WASD + D-pad movement
        │     ├── updateZombies()    — AI tracking + combat
        │     ├── updateAnimals()    — barn animal wandering
        │     ├── updateParticles()  — visual FX system
        │     ├── updateArrows()     — projectile physics
        │     ├── updateRain()       — weather animation
        │     └── updateStove()      — async cook queue
        └── draw()
              ├── drawHome/Barn/Forest()
              ├── drawPlayer()
              ├── drawParticles()
              └── drawHUD()
```

### Key Design Decisions

- **Single-file architecture** — zero build tooling, maximum portability
- **Delta-time movement** — `dt`-based updates ensure consistent speed across all frame rates
- **`Math.hypot()` for all distance checks** — precise diagonal distance for combat range validation
- **Isolated D-pad & keyboard inputs** — pointer events isolated per button to prevent stuck-key issues on mobile
- **Emoji-based graphics** — no image loading, no CORS issues, no asset pipeline

### Performance
- Particle system capped and cleaned each frame
- Zombie count capped at `8 + day` to prevent frame drops
- Rain uses pre-allocated drop array (120 drops, no reallocation)
- Minimap renders to a separate offscreen canvas at 80×60

---

## 🗺 Roadmap

### Version 1.1 — Crafting Expansion
- [ ] Stone axe → Iron axe upgrade path
- [ ] Armor crafting (🦌 Hide → leather armor)
- [ ] Arrow crafting (limited ammo for bow)

### Version 1.2 — Base Defense
- [ ] Wall placement system (grid-based)
- [ ] Night raids — zombies attack the safe house
- [ ] Wolf enemies (🐺) that spawn at midnight

### Version 1.3 — Visual Polish
- [ ] Particle effects for tree falling (leaf burst)
- [ ] Zombie death splatter particles
- [ ] Footstep trail effect when running
- [ ] Screen shake on taking damage

### Version 1.4 — World Expansion
- [ ] Cave dungeon location (new zone)
- [ ] Merchant NPC (trade gems for rare items)
- [ ] Fishing mechanic at riverside location

### Version 2.0 — Multiplayer (Long-term)
- [ ] WebSocket-based co-op (2 players)
- [ ] Shared chest / divided resource roles
- [ ] PvP arena mode

---

## 🐛 Known Issues

| Issue | Status | Workaround |
|---|---|---|
| Animals may walk into screen corners briefly | Low priority | They bounce back automatically |
| Bow projectiles don't render rotation angle | Cosmetic only | No gameplay impact |
| Torch item crafted but night vision not yet implemented | Planned v1.3 | Item acts as placeholder |
| Stone Wall crafted but placement not interactive | Planned v1.2 | Item added to inventory |
| Apple tree doesn't visually show "empty" state | Planned | Message shows when empty |

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# 1. Fork the repository
# 2. Clone your fork
git clone https://github.com/yourusername/survivor.git

# 3. Make your changes in survival_game.html
# 4. Test in a browser

# 5. Submit a pull request
```

### Contribution Guidelines
- Keep the **single-file architecture** — do not introduce build tools or external dependencies
- Test on both **desktop and mobile** before submitting
- New features should include a quest entry in the `QUESTS` array
- Maintain the **emoji-only graphics** style (no image assets)
- Comment complex logic with inline `//` comments

### Good First Issues
- Add sound effects using the Web Audio API
- Add a settings panel (volume, show/hide minimap)
- Implement the torch night-vision mechanic
- Add save/load via `localStorage`

---

## 📄 License

```
MIT License

Copyright (c) 2026 Survivor Game

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

<div align="center">

**Built with ❤️ using zero dependencies — just HTML, CSS, and JavaScript**

⭐ If you enjoyed this project, please give it a star!

`🎃 Survive · 🌲 Explore · ⚔️ Fight · 🏠 Build`

</div>
