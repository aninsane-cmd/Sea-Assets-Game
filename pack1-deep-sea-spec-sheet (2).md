# Pack 1 Spec Sheet: Deep-Sea Depth Progression
**Grid:** 32x32 px | **Perspective:** Top-down | **Style:** Cohesive pixel art, 3 depth zones, one connected palette family

> **Perspective locked: Top-down.** Chosen for maximum cross-genre reuse — fits RPGs, survival, cozy/farming-adjacent, fishing, and exploration games, which is where this pack's planned series (fishing kit, tidepool/cozy pack, pirate ship) naturally lives. Side-view was considered for a dramatic "surface-to-abyss" visual but reserved for promo screenshots/GIFs only, not the actual tileset, to keep the buyer pool wide.

---

## 1. Concept

A top-down (or side-view — pick one and stay consistent) tileset + creature set + HUD
that lets a buyer build a dive from the sunlit surface down into the pitch-black abyss.
The three zones share a visual language (same tile grid, same lighting logic) but shift
palette and creature type as you go deeper — this progression is the differentiator.

---

## 2. Palette Plan — LOCKED

**Master palette: `blk-nx64-32x` (64 colors).** Indices below are locked and should be
used as-is — no off-palette colors once drawing begins (see indexed color mode note in
your workflow notes).

### Shared neutrals (used in ALL three zones)

| Role | Index | Hex | Notes |
|---|---|---|---|
| Outline | 1 | `#12173d` | Dark navy "ink" — do NOT use index 0 (`#000000`), too harsh |
| Rock / stone | 30 | `#21526b` | Muted steel-blue, doubles as neutral grey |
| Foam / highlight | 6 | `#c1d9f2` | Pale icy blue — do NOT use index 7 (`#ffffff`), too stark |

### Zone-specific ramps

| Zone | Depth (fictional) | Indices | Hex range | Use |
|---|---|---|---|---|
| Shallow Reef | 0–20m | 32–35 | `#008782` → `#78fae6` | Water, teal/mint coral, kelp |
| Shallow Reef (warm accent) | 0–20m | 40–43 | `#919b45` → `#ffaa6e` | Sand, warm coral, sunlit accents |
| Twilight Zone | 20–60m | 22–31 | `#1d1a59` → `#163755` | Full dark-blue-to-steel-blue ramp for water and rock |
| Abyss | 60m+ | 0–2 | `#000000`, `#12173d`, `#293268` | Darkest base water/rock |
| Abyss (glow accent) | 60m+ | 34–35 | `#27d3cb`, `#78fae6` | Bioluminescent creature/plant glow — pops against near-black |

### Reserved for later packs
- Indices 44–63 (warm reds/pinks) — not used in Pack 1, reserved for Pack 2's sea
  monster attack-telegraph flashes and danger/warning UI states, keeping later packs
  color-compatible with this one.

---

## 3. Tile Categories (target: ~140–160 tiles total across 3 zones)

### 3.1 Shallow Reef Zone (~55 tiles)
- Water base tiles: still water (4), light shimmer variant (4), animated caustic overlay (4 frames)
- Sand floor: plain (4 variants), with shell/pebble detail (4 variants)
- Coral formations: brain coral, fan coral, tube coral, branching coral (2 size variants each = 8)
- Kelp/seagrass: 3 types x 2 sway animation frames = 6
- Rocks: small (3), medium (3), large (2)
- Sunlight shafts (animated overlay, 3 frames)
- Decor: starfish (2 poses), shells (3 types), anemone (2 poses, 2-frame idle sway)

### 3.2 Twilight Zone (~50 tiles)
- Water base: darker still water (4), faint light-shaft overlay (3 frames)
- Rock floor: plain (4), cracked/vented (4)
- Dead coral / bare rock formations (6)
- Kelp forest (taller, darker): 2 types x 2 sway frames = 4
- Hanging particulate/marine snow overlay (looping animation, 4 frames)
- Cave entrance tile set: opening (4), interior wall (4), floor (4)
- Decor: bioluminescent plankton clusters (3 variants, pulsing glow 2-frame), shipwreck debris (4 pieces: plank, crate, rope coil, broken mast)

### 3.3 Abyss Zone (~45 tiles)
- Water base: near-black still water (3), pressure-distortion overlay (3 frames)
- Ocean floor: silt/mud (4), volcanic vent floor with bubble animation (4, 3-frame bubble loop)
- Rock spires / trench walls (6)
- Bioluminescent flora: glowing tube worms (3, pulsing 2-frame), anglerfish-lure-style glowing fungus (2, 2-frame)
- Hydrothermal vent (animated, 4-frame smoke/particle effect)
- Decor: sunken wreck hull fragment (3), ancient ruin fragment optional (3) — treat ruins as a stretch goal, not core scope

---

## 4. Creature Roster (target: 8–10 creatures, each with idle + swim animation)

> **Top-down note:** unlike a side-view swim cycle, top-down creatures generally need **4-directional** (or at minimum a base + horizontal-flip) movement sprites so they read correctly swimming in any direction the player might see them from above. Simpler creatures (jellyfish, anemones) can often get away with a single rotating/omnidirectional sprite since they don't have a strong "facing," but fish, turtles, eels, and the squid need at least up/down/left-right variants. Factor this into your frame counts below — treat the "4-frame swim loop" figures as **per direction**, not a one-time total.

| Creature | Zone | Frames needed |
|---|---|---|
| Reef fish (small school variant, 3 color variants) | Reef | 4-frame swim loop x3 |
| Sea turtle | Reef | 4-frame swim loop |
| Clownfish/anemone pair | Reef | 4-frame swim + 2-frame anemone sway |
| Jellyfish | Twilight | 4-frame pulse-swim loop, 2 color variants |
| Anglerfish | Twilight/Abyss | 4-frame swim + 2-frame lure glow pulse |
| Giant squid (small/mid size, not boss-scale) | Twilight | 4-frame swim, 2-frame idle drift |
| Bioluminescent jelly (abyss variant) | Abyss | 4-frame pulse-swim, glow overlay |
| Deep-sea eel | Abyss | 4-frame swim loop |
| Vent crab | Abyss | 3-frame walk cycle |

*(Optional stretch: one larger "abyss guardian" creature idle-only, reserved as a teaser for Pack 2's monster-attack pack — don't fully animate it here, just tease it.)*

---

## 5. HUD / UI Elements (target: ~20–25 pieces)

- Oxygen meter: full bar frame + 5-stage fill states + low-oxygen warning pulse (2-frame)
- Depth gauge: dial or vertical bar style, with numeric readout background panel
- Pressure warning icon (static + 2-frame flash for danger state)
- Dive computer panel frame (background box for HUD elements to sit in)
- Flashlight/beam cone overlay (semi-transparent, for optional lighting effect use)
- Bubble particle set: 3 sizes x 3-frame rise-and-pop animation
- Compass/direction indicator (simple dial, 8-direction states)
- Collection/inventory icon set: sample vial, camera, flashlight, knife (4 icons, matching pixel style)

---

## 6. File & Delivery Structure

```
DeepSeaDepthProgression/
├── tiles/
│   ├── reef/
│   ├── twilight/
│   └── abyss/
├── creatures/
│   ├── reef/
│   ├── twilight/
│   └── abyss/
├── hud/
├── spritesheets/        (packed versions of the above, per category)
├── palette/
│   └── master-palette.png + .gpl/.pal file
├── preview/
│   └── promo screenshots + animated GIF previews
└── README.txt           (grid size, license, engine compatibility notes)
```

- Deliver both **individual PNGs** and **packed spritesheets** (buyers expect both)
- Include a Tiled/Godot/Unity-ready tileset file if feasible (adds perceived value)
- Note transparency: export all sprites on transparent PNG backgrounds

---

## 7. Suggested Scope for v1 vs. Free Sample

- **Free sample:** Reef zone only — water tiles, 2 coral types, 1 kelp, 2 reef fish, oxygen meter HUD piece. Enough to be useful standalone, but clearly a taste of the full pack.
- **Full paid pack:** All 3 zones + full creature roster + full HUD set as scoped above.

---

## 8. Naming & Tagging Checklist (for the itch.io listing)

- Title should include: "32x32," "pixel art," "underwater/deep sea," "tileset," and either "diving" or "ocean" depending on final framing
- Tags: Pixel Art, Underwater, Ocean, Tileset, Asset Pack, 2D, Top-Down (or Side-Scroller — match your chosen perspective), Sci-fi/Survival if applicable
- List supported engines explicitly once exported (Unity, Godot, RPG Maker, etc.)
- State license terms clearly at the top of the page (commercial use allowed? attribution required?)

---
*Next possible step: pick top-down vs. side-view perspective and lock the master palette file before drawing begins.*
