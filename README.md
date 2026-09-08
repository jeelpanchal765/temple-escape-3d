# 🏃‍♂️ Temple Escape 3D - Ancient Realms 3D Endless Runner

A fast-paced, high-performance 3D endless runner game built with **HTML5 & Three.js (WebGL)** inspired by the classic feel of **Temple Run 2**, featuring 8 dynamic biomes, procedural blended animations, tiered collectibles, missions, achievements, daily challenges, and Web Audio synthesized soundscapes.

![Three.js r128](https://img.shields.io/badge/Three.js-r128-green?style=for-the-badge&logo=three.js)
![HTML5](https://img.shields.io/badge/HTML5-WebGL-orange?style=for-the-badge&logo=html5)
![Vercel Ready](https://img.shields.io/badge/Deploy-Vercel-black?style=for-the-badge&logo=vercel)

---

## 🎮 Key Upgraded Features

### 1. 🌅 Dynamic Environment & Biomes
- Smooth distance-based transitions across 8 distinct realms:
  - 🌅 **Day Temple** (0–500m): Sunlit sandstone flagstones, golden trim, and Aztec columns.
  - 🌿 **Jungle Sanctuary** (500–1000m): Dense canopies, mossy boulders, and floating spores.
  - 🏛️ **Ancient Ruins** (1000–1500m): Broken fluted columns, weathered ruins, and amber mist.
  - 🕳️ **Underground Cave** (1500–2000m): Cavern ceilings, glowing crystal clusters, and water drips.
  - 🌊 **Water Temple** (2000–2500m): Turquoise tiles, aqueducts, and cooling water mist.
  - 🌋 **Lava Temple** (2500–3000m): Obsidian basalt, burning braziers, and rising embers.
  - 🌙 **Night / Danger Mode** (3000m+): Moonlit darkness, glowing runes, and eerie fog.
- Real-time gradual lighting, sky gradient, fog color, and particle interpolation.

### 2. 🏃 Procedural Blended Player Animations
- Silky blended state machine:
  - **Running**: Dynamic leg swing, knee flexion, counter-arm swinging, ribbon fluttering in wind.
  - **Jumping**: Takeoff crouch -> apex air arc -> landing compression.
  - **Sliding**: Low-profile slide, dust friction trail, instant slide-cancel into jump.
  - **Stumble**: Flailing stumble stagger and camera shudder.
  - **Flame Boost**: Aerodynamic forward lean with fluttering flame wings.
  - **Death**: Dramatic knockdown with ragdoll collapse.

### 3. 💎 4-Tier Collectible System & Dynamic Formations
- **4 Collectible Tiers**:
  - 💎 **Emerald (Normal)**: Common, +100 pts.
  - 💙 **Sapphire (Rare)**: Vibrant blue glow, +250 pts.
  - 💛 **Topaz (Golden)**: Golden sparkle burst, +500 pts.
  - 🔴 **Ruby (Special)**: Pulsing crimson aura & crystal chord, +1000 pts.
- **Dynamic Formations**: Linear streaks, sine waves, zig-zag lane switches, lane-change arrows, and risk/reward placements over hazards.

### 4. 🎯 Missions System
- 3 Rotating active mission slots (Distance goals, gem hunting, jumps, slides, combo streaks).
- Real-time progress tracking with in-game completion toast notifications & gem rewards.
- Full interactive Missions screen with progress bars.

### 5. 🏆 Achievements System
- Permanent milestone achievements with sound fanfares & status tracking:
  - 🏃 *First Run*, 💎 *Gem Hoarder*, 🔥 *Speed Demon*, ⚡ *Boost Master*, 😈 *Monster Escape*, 🏆 *5000m Survivor*, 💯 *Combo Master*, 🌋 *Realm Traveler*.
- Interactive Achievements screen with unlocked / locked progress.

### 6. 📅 Daily Challenge System
- Seeded by current date (`YYYY-MM-DD`) with automatic daily resets.
- Persistent daily objectives with rewards (e.g. +500 💎).

### 7. 🎥 Polished Third-Person Camera
- Smooth spring damping tracking.
- Dynamic FOV expansion (65° -> 73° -> 80° during Flame Boost).
- Subtle banking tilt when switching lanes.
- Landing bounce spring and controlled collision trauma shake.

### 8. 🔊 Dynamic Web Audio Soundscapes
- Fully procedural synthesized Web Audio:
  - Tiered gem pickup chimes, jump whoosh, slide scrape, landing thud, demon roar, shield break.
  - Procedural ambient soundscapes per biome (Jungle wildlife, Cave water echo, Water flow, Lava bubbling rumble, Night drone).
  - Dynamic drum rhythms that scale in tempo with run speed.
  - Persistent sound toggle (`🔊 Sound` / `🔇 Muted`).

### 9. 💾 Structured Local Save System
- `templeEscapeSave_v2` object with backward-compatible migration for high scores, best distance, total gems, settings, missions, and achievements.

### 10. 🛍️ Temple Vault & Character Shop
- **5 Distinct Playable Heroes** with procedural 3D aesthetics, accessories, and unique gameplay perks:
  - 🤠 **Guy Dangerous** (Temple Explorer - Default): Balanced agility and classic styling.
  - 🦊 **Scarlett Fox** (Desert Rogue - 1,500 💎): +25% Score from Gems & 20% Faster Lane Swapping.
  - 💀 **Barry Bones** (Undead Legionnaire - 3,500 💎): +3.5s Tiki Shield duration & absorbs stumble recovery penalties.
  - 🥷 **Karma Lee** (Shadow Shinobi - 6,000 💎): Telekinetic Magnetic Aura (+40% coin range) & 30% faster boost charge.
  - 👑 **Zack Wonder** (Golden Champion - 12,000 💎): Starts run with Tiki Shield & +40% Rare/Ruby gem generation.
- **⚡ Permanent Power-Up Upgrades** (5 Tiers each):
  - 🧲 **Coin Magnet**: Duration (+3s/lvl) & attraction radius (+15%/lvl).
  - 🛡️ **Tiki Shield**: Duration (+3s/lvl) & extra damage absorb capacity.
  - 🔥 **Flame Boost**: Supersonic flight duration (+2.5s/lvl) & meter charge speed.
  - ✖️2 **Score Multiplier**: Extends 2x multiplier time & bonus points.
  - 💎 **Gem Alchemy**: Boosts spawn frequency for high-value Sapphire, Gold & Ruby gems.
- **🎒 Utilities & Consumables**:
  - 🚀 **Head Start (500m)** & ⚡ **Mega Head Start (1,500m)**: Instant supersonic rocket flight at run start.
  - ⚱️ **Revive Idol (Save Me)**: Interactive resurrection upon falling/collision.

### 11. 📱 Responsive Mobile Touch & Swipe Controls
- Ultra-responsive touch gesture engine with anti-scroll and pull-to-refresh prevention.
- Adaptive layouts for Mobile Portrait, Mobile Landscape, Tablet, and Desktop.

---

## 🕹️ Controls

| Action | Desktop Keyboard | Mobile Touch / Swipe |
| :--- | :--- | :--- |
| **Move Left** | `A` or `←` | Swipe Left / Tap `◀` |
| **Move Right** | `D` or `→` | Swipe Right / Tap `▶` |
| **Jump** | `W` / `↑` / `Space` | Swipe Up / Tap `▲` |
| **Slide** | `S` / `↓` | Swipe Down / Tap `▼` |
| **Flame Boost** | `E` or Tap Idol | Tap Demon Idol Icon |
| **Pause / Resume** | `P` or `ESC` | Tap Pause Button |

---

## 🚀 Instant Deployment (Vercel)

1. Push this repository to your GitHub.
2. Connect your GitHub repository to [Vercel](https://vercel.com).
3. Deploy! (Static site — no build configuration required).

