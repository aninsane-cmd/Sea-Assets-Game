# Pack 1 Spec Sheet: Deep-Sea Depth Progression
**Grid:** 32x32 px | **Style:** Cohesive pixel art, 3 depth zones, one connected palette family

---

## 1. Concept

A top-down (or side-view — pick one and stay consistent) tileset + creature set + HUD
that lets a buyer build a dive from the sunlit surface down into the pitch-black abyss.
The three zones share a visual language (same tile grid, same lighting logic) but shift
palette and creature type as you go deeper — this progression is the differentiator.

---

## 2. Palette Plan

Lock a palette **per zone**, all pulled from one master 32–40 color file so they blend
if used together.

| Zone | Depth (fictional) | Palette mood | Suggested color count |
|---|---|---|---|
| Shallow Reef | 0–20m | Bright turquoise, coral pink/orange, sandy yellow | 12–14 colors |
| Twilight Zone | 20–60m | Deep blue-violet, dim teal, fading light shafts | 10–12 colors |
| Abyss | 60m+ | Near-black navy/charcoal, single bioluminescent accent (cyan or magenta) | 6–8 colors + 1–2 glow accents |

Keep a shared "neutral" set (rock grey, dark outline color, foam white) used in all three
zones so transitions tile seamlessly.

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
