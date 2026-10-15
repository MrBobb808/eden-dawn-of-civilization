# EDEN: Dawn of Civilization
## Design blueprint — version 0.1

### North star
A Scripture-guided multigenerational village simulation where the player experiences biblical milestones and gradually develops a living civilization. Key biblical outcomes are fixed; fictional everyday activities make the world interactive. Art direction: richly shaded hand-drawn pixel art, approximately 48–64px character sprite height in the full art release, expressive faces, layered outdoor environments, day/night transitions, living vegetation, water, and individually animated activities.

### Player fantasy
1. **Belong:** Begin as Adam, name creatures, tend and keep the garden.
2. **Witness:** Encounter Genesis narrative events through reverent Scripture-led cutscenes.
3. **Build:** Establish a practical homestead and help family members survive.
4. **Guide:** Watch individual people learn, work, form families, and pass down skills.
5. **Explore:** Revisit persistent settlements in differing lineages and biblical eras.

### Distinction between canon and invention
- Display a conspicuous opening disclosure and annotate story entries as Scriptural or dramatisation.
- Use verified KJV passages and references for all direct biblical quotations.
- Do not create a humanoid appearance for God or invent extended speech and attribute it to Him.
- Scripted outcomes: creation of Eve, serpent's temptation, Fall, clothing and expulsion, Cain and Abel's roles, Abel's death, Cain's departure, Cain's city named after Enoch, Seth's birth.
- Cain's fictional surrounding activities, Seth's “Valley” settlement, exact architecture, character dialogue, tasks, periods between events, and gameplay events are imaginative additions.
- The original Garden cannot be reopened as an occupied settlement once the Genesis 3 expulsion takes place; the Adam/Eve home east of Eden persists.
- Abel does not have an independent long-term descendant settlement (no lineage asserted in Genesis).

### Campaign beats
| Quest | Chapter | Action | Biblical anchor |
|---|---|---|---|
| The First Calling | I | Tend three plots | Genesis 2:15 |
| Names of the Living | I | Name four representative creatures | Genesis 2:19–20 |
| Not Good to Be Alone | I | Reach quiet glade and hear narrated Scripture | Genesis 2:18–23 |
| Life Together | I | Gather fruit and speak with Eve | Genesis 2:23–25 |
| The Broken Trust | II | Experience fixed narrative chapter | Genesis 3:1–24 |
| Beyond Eden | II | Till three fields | Genesis 3:17–19, 23 |
| A Place to Gather | II | Build a family shelter (fictional mechanic) | Genesis 3:23 |
| The First Brothers | III | Tend Cain's field and Abel's flock | Genesis 4:1–2 |
| Two Offerings | III | Experience fixed tragic narrative | Genesis 4:3–16 |
| The Generations | IV | Unlock multiple settlements | Genesis 4:17–26 |

### Core systems to deepen next
- **Villager AI:** personal needs (hunger, rest, social belonging), priorities, profession schedules, routine tasks, mood, age, friendships, parenting, family relationships; no player micromanagement required.
- **Generations:** genealogy with recorded relationships; young learn from elders; new families settle independently; time-step controls; aging and births sensitively designed, with canon genealogy protected.
- **Farming:** clear land, till, seed, water, grow, harvest, storage, shortages, weather and soil quality; farming outside Eden notably different.
- **Animals:** names, caretaking, nutrition, breeding, animal ages, temperament, sheep husbandry after Genesis 4, transport resources; some systems unlocked as the biblical narrative develops.
- **Fishing:** fishing spots, lines/nets as progression tech, seasonal species, cooking, storage, river ecosystems. Technological particulars and chronology should be labeled invented.
- **Clothing/crafting:** Scripture-derived provision of skins as a story moment, followed later by fictional clothing craft systems with textile and hide resources; distinguish the two explicitly.
- **Skills and instruction:** lessons from Adam and later elders; gardening, stewardship, cooperation, carpentry, shepherding, remembering what Scripture records; skills pass between generations.
- **Construction:** building placement, work orders, materials, stages of erection, shared storehouses and homes; different architectural styles across regions.
- **World events:** mist, storms, good harvests, discovery, new births, material shortages, herd movements; events affect resources without overwriting canon events.
- **Multi-settlement simulation:** scenes always retain their state and villagers; later background offline progress must be bounded, transparent, and catch-up capped; no predatory time gates.
- **Narrative interface:** scroll-like story chapters, short KJV quotations and citation references, accessible journal, story archive, era indicators, annotations explaining imagined content.

### First production art pass
- Hand-painted, 24-frame directional walk cycles for Adam/Eve and 8 for idle; face portraits separate.
- Environment atlas: several tree families, 6 garden beds, grass/flowers/stones/water tiles, harvest stages, animals with 4–8 animation frames.
- Pixel-art resolution target ~480x270 or 640x360 with integer nearest-neighbor scaling; render text HUD natively at screen resolution.
- Color direction: warm honey-gold highlights, sage and emerald leaves, flowing turquoise rivers, parchment and walnut-brown panels, misty mountains, lavender sunrise. Post-Fall world more amber, muted, earthy.
- Avoid the crisp geometric “SVG look”; use clusters of hand-placed pixels, pigment-like variation, local shadows, nuanced material texture, and animated secondary motion.

### Accessibility and platforms
- Start with browser desktop + mobile; large interactive hotspots for touch, text-sized controls, option to reduce motion, pause during story reading, clearly visible objectives, persistent auto-save with manual export added later.
- Keep per-village villager simulation step-based and capped to avoid runaway CPU use on mobile.

### Technology plan
- Current prototype: self-contained Canvas 2D + CSS UI + browser localStorage, no build prerequisites.
- Production migration: Phaser + TypeScript + hand-authored texture atlases, animation state machines, deterministic world state persisted to IndexedDB; React optionally for HUD and codex screens.
- Assets: Aseprite, LibreSprite, Krita, or pixel painting over pre-rendered Blender models. Blender can still be valuable for blockout, lighting reference, and prerendered sprites even though final style is 2D.
- Source control: separate repository once gameplay foundation is approved; shipping from a staging deployment after visual and input testing.

### Honest MVP scope
The current browser prototype implements quest flow, basic map movement, four animal naming interactions, repeated garden plots, an orchard, an initial build action, a fishing click, Genesis-themed teaching circle, settlement switching, story journal, simple family view, and local saves. It is *not* yet a complete generational simulation: breeding, births, relationships, multiple autonomous work schedules, character sprite atlases, detailed farming cycles, and permanent village production are planned milestones.