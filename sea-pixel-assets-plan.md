# Pixel Art Game Assets on itch.io — Research Summary & Sea Niche Plan

## 1. Selling on itch.io: The Basics

- Itch.io has **weak organic discovery** — no strong recommendation algorithm, browse pages get flooded daily, so a good asset alone will not sell itself.
- Without promotion, expect only a trickle of sales (single digits to low dozens).
- **What actually drives sales:**
  - Reddit posts (r/gamedev, r/IndieDev, r/gameassets, r/PixelArt) — short-term spike (24–72 hrs), can drive dozens of sales if well-received
  - Charity/seasonal bundles — huge exposure, little direct revenue, but great for building a following and reviews
  - SEO — descriptive titles/tags get indexed by Google, slow burn but compounds over months
  - None of this compounds well as a one-off — sustained income comes from **releasing multiple assets, building a following, and reusing each promo cycle across your whole catalog**

## 2. What the Biggest Sellers Do (Kenney, KayKit, top tilesets/icon packs)

Common patterns across itch.io's actual top sellers:
1. **Free content first** — most started with free packs to build trust/discovery
2. **Broad utility, narrow enough to be searchable** (e.g. "RPG tileset," "UI SFX")
3. **Consistent output over time** — dozens of packs, not one-offs
4. **Compatibility clarity** — explicit Unity/Godot/Unreal/RPG Maker tagging
5. **Years of accumulated reviews** — social proof compounds

## 3. Niches Explored (Saturation Comparison)

| Niche | Saturation | Notes |
|---|---|---|
| Farming sim | High | Crops, tools, animals, tilesets all heavily covered (Stardew-style). Weakest opportunity of all explored. |
| Cafe / restaurant sim | Medium | Tons of food/drink icon packs; **service-loop UI (order tickets, mood meters) and customer animations are thin** |
| Pirate / sea | Medium-low | Ships, portraits, beach tiles covered; **underwater/diving and functional UI are thin** — strongest overall opportunity found |
| Cyberpunk | High | Very mature market — even UI/HUD packs already exist in volume (e.g. 280-icon packs). Toughest entry point. |

## 4. Deep Dive: The Sea / Pirate Niche

### Already well-covered (avoid direct competition here)
- Beach/island tilesets (from free basics to full survival-island packs)
- Fish sprite sheets (loose packs of 35–384 fish/icons)
- Pirate ship tilesets and modular ship builders
- Standalone sea creatures (crabs, jellyfish, sharks, turtles) — mostly simple/static
- Underwater backgrounds and cave scenes
- Occasional single big boss monster (giant squid, kraken)

### Real gaps identified
1. **Deep-sea depth progression system** *(strongest gap found across the entire research)*
   - Layered zones: shallow reef → twilight zone → abyss, each visually/mechanically distinct
   - Diving-suit HUD: oxygen meter, depth gauge, pressure warning
   - Bioluminescent creature variants for the deepest zone
2. **Sea monster attack-animation sets**
   - Most existing monsters are single static bosses (idle/death only)
   - Gap: multiple monster types with full attack cycles (telegraph → strike → retreat), plus environmental danger cues and a bestiary/lore portrait set
3. **Cozy tidepool & beachcombing pack**
   - Beach packs are generic sand/palm-tree tiles; tidepool life (starfish, anemones, shells) and a beachcombing/collecting UI (shell jar, driftwood pile, collection log) are missing
   - Distinct "cozy beach exploration" audience vs. pirate-adventure buyers
4. **Naval combat & ship management UI** / **Exploration & treasure-map UI**
   - Ship art is common, but cannon-aim reticles, hull-damage bars, crew rosters, island-hopping map screens with fog-of-war are largely absent
5. **Sailor/crew activity animations**
   - Ship tiles are static; rope-tying, cannon-loading, sail-hoisting, storm-bracing animations are scarce

## 5. Decision: Focus on the Sea Niche

**Chosen theme:** Sea environment, beach/island, sea animals, sea monsters, and pirates — built as a connected catalog rather than one isolated pack.

### Proposed pack sequence (each stands alone, but they compound into a bundle later)

| Order | Pack | Why |
|---|---|---|
| 1 (launch) | **Deep-sea depth progression** — reef/twilight/abyss tiles, oxygen/depth HUD, bioluminescent creatures | Least-covered idea found in the entire research; hardest to copy; strong differentiator |
| 2 | **Sea monster attack-animation set** | Reuses established palette/style; fills the multi-phase combat animation gap |
| 3 | **Cozy tidepool & beachcombing pack** | Same style, taps into the separate "cozy game" buyer segment |
| 4 | **Pirate ship + crew** (naval UI + crew animations) | Ties the whole catalog together into one "ocean world," sellable as a bundle later (Kenney/KayKit style) |

### General execution notes (from earlier discussion)
- Tools: Aseprite (or free Piskel/LibreSprite to start)
- Lock one resolution (16x16 or 32x32) and a tight palette (8–16 colors) per pack for consistency
- Release a free sample/mini-version of each pack to build trust and discoverability
- Write buyer-focused listings: exact sprite counts, animation frame counts, supported engines, file formats, license terms
- Tag and title for search (itch tags + Google-indexed titles)
- Promote via Reddit (r/PixelArt, r/gamedev, r/IndieDev, cozy-game-dev Discords), apply to bundles once you have a small catalog, and let SEO compound over time

---
*Next step: build a full spec sheet (tile list, palette, dimensions, sprite counts) for Pack 1 — the deep-sea depth progression pack.*
