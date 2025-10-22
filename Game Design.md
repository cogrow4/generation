# GENERATION SHIP: THE LAST WAKE
## Game Design Document

---

## EXECUTIVE SUMMARY

**Genre:** 2D Side-Scrolling Narrative Exploration Game  
**Platform:** PC (Steam), Mac, Linux, Nintendo Switch  
**Engine:** Godot 4.x  
**Target Playtime:** 8 hours  
**Art Style:** Hand-drawn, painterly, cinematic  
**Target Audience:** 18-40, narrative-focused players  

**Core Pitch:**
You wake alone on a generation ship after 107 years. Your pod's failure triggered an electrical cascade killing 100,000 hibernating passengers. You can save them by manually restarting the reactor—but the radiation will kill you. Explore the empty ship, discover the conspiracy, and choose: sacrifice yourself, save yourself, or do nothing.

---

## 1. CORE GAMEPLAY

### Game Type
- **Exploration-focused** narrative game
- **No combat** - pure atmosphere and story
- **Walking simulator** with light puzzles
- **Metroidvania-lite** progression (keycard gating)
- **Hard sci-fi grounded** in real physics

### Core Loop
1. Explore ship sections
2. Find terminals and read lore
3. Collect keycards/items to unlock new areas
4. Discover story pieces (including technical/scientific details)
5. Progress toward final choice

### Player Verbs
- Walk (left/right)
- Jump (small, for platform navigation)
- Interact (read terminals, open doors, collect items)
- Toggle flashlight
- Manage inventory

---

## 1.5 SCIENTIFIC GROUNDING

### Ship Design - The GSS Exodus

**Propulsion System:**
- **Bussard Ramjet** fusion drive (theoretical but scientifically plausible)
- Collects interstellar hydrogen using massive magnetic field (200km diameter)
- Fuses hydrogen in fusion reactor for thrust
- Current velocity: 0.12c (12% speed of light = 35,946 km/s)
- Acceleration phase lasted 15 years, coasting since year 15

**Ship Specifications:**
- Length: 847 meters
- Rotating habitat ring: 400m diameter
- Rotation: 2 RPM (generates ~1g artificial gravity via centrifugal force)
- Mass: 2.4 million tonnes (mostly hydrogen fuel and radiation shielding)

**Reactor Type:**
- **Deuterium-Tritium Fusion Reactor** (tokamak design)
- Operating temperature: 150 million °C (plasma core)
- Magnetic confinement: 15 Tesla superconducting magnets
- Power output: 2.4 GW (enough for entire ship)
- Fuel: Deuterium from ship's water, Tritium bred from lithium blanket

**Radiation in Reactor Chamber:**
- **Primary hazard:** High-energy neutrons (14.1 MeV from D-T fusion)
- **Secondary:** Gamma rays from neutron interactions with shielding
- **Exposure rate:** 847 rads/hour = 8.47 Gray/hour
- **Shielding:** Borated polyethylene + lead + water (degraded after 107 years)
- **Fatal mechanism:** Neutron radiation causes acute radiation syndrome
  - Destroys rapidly dividing cells (bone marrow, intestinal lining)
  - Causes DNA double-strand breaks beyond repair capacity
  - Death occurs from infection, internal bleeding, organ failure

**Why Manual Override Is Necessary:**
- Stellar radiation (gamma ray burst) induced single-event upsets in control systems
- Redundant computer systems corrupted
- Physical realignment of magnetic confinement coils required
- Human presence needed to verify plasma stability during restart sequence

**Time Dilation Effects:**
- At 0.12c, time dilation factor: γ = 1.0072
- For every 100 years on ship, 100.72 years pass on Earth
- Negligible but technically accurate (mentioned in navigation logs)

### Hibernation Technology

**Principle:**
- **Induced Metabolic Torpor** (based on real research in therapeutic hypothermia)
- Core body temperature reduced to 10°C
- Metabolism reduced to 1/50th normal rate
- Cellular preservation via cryoprotectant perfusion

**Technology:**
- **Cryoprotectants:** Glycerol-based solution prevents ice crystal formation
- **Electromagnetic nerve block:** Prevents neural degradation during stasis
- **Automated medical monitoring:** EEG, heart rate, blood oxygen
- **Stasis field generators:** Suppresses aging processes at cellular level (mild sci-fi element, but grounded in suspended animation research)

**Power Requirements:**
- 2.4 kW per pod for cooling and monitoring
- 240 MW total for 100,000 pods
- Emergency network created dangerous single point of failure

**Why Pods Fail After 80 Years:**
- Superconducting coil degradation in cooling systems
- Cryoprotectant crystallization in long-term storage
- Electromagnetic field generator component fatigue
- Cheap manufacturing (Project Closure cost-cutting)

### The Electrical Cascade Explained

**Network Architecture:**
- All pods connected via shared power bus (cost-saving measure)
- Emergency wake draws 847 amps (35x normal load)
- Your pod failure created voltage spike: 847V through 240V system
- **Cascade mechanism:** Transient overvoltage propagates through network
  - Damages voltage regulators in each pod
  - Creates secondary surges as damaged regulators fail
  - Exponential failure spread (like electrical domino effect)

**Why It's Fatal:**
- Life support circuits fail → temperature regulation lost
- Monitoring systems fail → can't detect occupant distress  
- Stasis field generators fail → metabolic activity resumes without wake protocol
- Result: Occupants die from organ failure in their sleep

**Why Reactor Restart Fixes It:**
- Cold shutdown completely de-energizes power grid
- Full restart reboots all systems with fresh power initialization
- Network reconfigures to isolated pod circuits (failsafe mode)
- Clean electrical state purges cascade damage

### Navigation & Astrometry

**Original Destination (Fake):**
- Star system designation: X-7721
- Coordinates: α 18h 42m 16.4s, δ +39° 40′ 11″ (points to empty space)
- Distance: 127 light years
- ETA at 0.12c: 1,058 years (passengers would die in hibernation regardless)

**Actual Destination - Planet PE-7742:**
- Star: Red dwarf (M-type), 0.4 solar masses
- Planet: Terrestrial, 1.2 Earth masses
- Orbital radius: 0.15 AU (close to dim star)
- Temperature: 15°C average (tidally locked but thick atmosphere distributes heat)
- Atmosphere: Nitrogen-Oxygen, 0.87 bar pressure
- Habitability Index: 0.87 (Earth = 1.0)
- Distance from current position: 35 light-years
- ETA at 0.12c: 292 years (but ship has coasted 107, so 35 more years)

**How It Was Discovered:**
- Ship's automated spectroscopy array (continuous 107-year survey)
- Transit method detected orbital signature
- Atmospheric analysis via transmission spectroscopy
- Oxygen spectral lines (biosignature - life may exist)

### Real Physics Constraints

**Why The Journey Takes So Long:**
- Can't exceed 0.12c (ramjet collection efficiency drops at higher speeds)
- No FTL (warp drives, hyperspace - pure fiction)
- No suspended animation beyond what's described
- Time is absolute - no shortcuts

**Why Communication Is Impossible:**
- Earth is 50+ light-years away
- Signal would take 50+ years to reach Earth
- Earth may not even be listening (127 other ships sent to die)
- Ship's transmitter designed for short-range only

**Life Support Reality:**
- Closed-loop system: water recycled, oxygen from plants
- Hydroponics produces food (realistic capacity)
- Carbon dioxide scrubbers (chemical, not magical)
- Waste converted to fertilizer (realistic biology)

---

## 2. CONTROLS & MOVEMENT

### Input (Keyboard/Gamepad)
- **Movement:** A/D or Left Stick
- **Jump:** Space / A Button
- **Interact:** E / X Button  
- **Flashlight:** F / Y Button
- **Inventory:** Tab / Start
- **Pause:** ESC / Start

### Movement Feel
- Side-scrolling with slight 2.5D perspective
- Walk speed: 120 pixels/second (deliberate, not rushed)
- Jump: Small hop for platforms (not platformer-heavy)
- No running/sprinting (reinforces pacing)

### Camera
- Follows player horizontally
- Zooms out in large rooms (shows scale)
- Zooms in slightly when reading terminals (intimacy)
- Smooth lerp follow (cinematic feel)

---

## 3. CORE SYSTEMS

### Interaction System
- **Context-sensitive E prompt** appears near interactive objects
- **Terminals:** Pause game, display text with next/previous navigation
- **Doors:** Automatic (near player) or locked (require keycard)
- **Items:** Collected to inventory automatically
- **Power boxes:** Insert power cell, flip switch to restore power

### Inventory System
- **12-slot grid** (simple, not resource management)
- **Key items:** Keycards (Blue, Red, Green, Gold)
- **Consumables:** Power cells (15 total), repair kits (8 total)
- **Collectibles:** Personal effects (151 optional lore items)
- No weight limit, no crafting

### Progression Gates
- **Keycards unlock sections:**
  - Blue: Engineering, Medical
  - Red: Hibernation Control, Life Support
  - Green: Reactor Approach
  - Gold: Reactor Core (requires all 3 previous cards)
- **Power cells** restore electricity to unpowered sections
- **Story flags** unlock critical paths automatically

### Flashlight System
- Toggle on/off with F key
- **Battery:** 4 minutes continuous use
- Recharges at terminals/charging stations
- Visual: Cone of light in facing direction
- Creates dramatic atmosphere in dark areas

---

## 4. GAME STRUCTURE

### Acts (8-Hour Playtime)

**ACT 1: AWAKENING (45-60 min)**
- Wake in hibernation bay
- Learn basic controls
- Access first terminal, discover 107 years passed
- Reach Command Deck outer door (locked)
- Terminals: 8 | Collectibles: 5

**ACT 2: THE EMPTY SHIP (90-120 min)**
- Explore residential areas (frozen lives)
- Restore power to sections
- Find Blue Keycard
- Discover stellar event logs
- Terminals: 18 | Collectibles: 35

**ACT 3: THE TRUTH (90-110 min)**
- Access engineering and archives
- Discover the conspiracy (Project Closure)
- Learn about electrical cascade you triggered
- Find Red Keycard
- Terminals: 15 | Collectibles: 20

**ACT 4: THE HOPE (120-150 min)**
- Access navigation, find habitable planet PE-7742
- Explore hibernation bays (see the scale)
- Access all ship sections
- Find Green Keycard
- Understand what must be done
- Terminals: 28 | Collectibles: 63

**ACT 5: THE CHOICE (90-120 min)**
- Collect Gold Keycard
- Final exploration (can revisit entire ship)
- Reach Reactor Core
- Make final decision
- Terminals: 18 | Collectibles: 28

### Ship Layout (25-30 Distinct Areas)

**BOW (Command Section)**
- Command Deck, Navigation, Observation Deck

**UPPER RING**
- Residential Quarters A & B
- Medical Center
- Recreation Complex
- Hydroponics A & B
- Engineering Upper
- Life Support

**LOWER RING**
- Hibernation Bays 1-8 (massive scale rooms)
- Engineering Lower
- Storage Sections
- Cargo Bays

**STERN**
- Reactor Approach
- Reactor Control
- Reactor Core Chamber

---

## 5. PUZZLES & OBSTACLES

### Power Restoration
- Find power cells scattered in areas
- Insert into breaker boxes
- Flip switches to restore power
- Powers lights, doors, terminals in section

### Door Types
- **Automatic:** Open when player approaches
- **Locked:** Require specific keycard
- **Damaged:** Require repair kit to fix
- **Bulkhead:** Require story progression

### Environmental Puzzles (Minimal)
- Power routing (choose which systems to power)
- Finding alternate routes (vents, ladders)
- Simple logic (clues in environment for codes)

**Design Philosophy:** Puzzles should not frustrate or block story progress. If player is stuck >5 minutes, puzzle is too hard.

---

## 6. LORE DELIVERY

### Terminals (87 Total)
- **Personal (34):** Emails, journals, daily life
- **Command (12):** Mission logs, classified conspiracy files
- **Engineering (18):** Technical specs, cascade diagnostics, reactor physics
- **Medical (8):** Health records, psych evaluations, radiation effects
- **Navigation (6):** Star charts, PE-7742 discovery, astrometry data
- **Life Support (9):** Automated logs showing indifferent systems
- **Scientific (bonus):** Explanations of ship systems for interested players

**Scientific Detail in Terminals:**
Players who read engineering/navigation terminals will encounter:
- Bussard ramjet operation principles
- Fusion reactor technical specifications
- Radiation types and biological effects
- Relativistic physics (time dilation calculations)
- Spectroscopic analysis of PE-7742
- Hibernation technology medical data

**Design Philosophy:** Science is optional flavor for interested players, never required for progression. Casual players can skip technical terminals, science enthusiasts can dive deep.

### Personal Effects (151 Total - Optional)
- Personal tablets (47)
- Photographs (34)
- Children's drawings (23)
- Letters (29)
- Mementos (18)

Each has 2-4 sentences of description text.

### Environmental Storytelling
- Frozen moments (dinner table set, toys mid-play)
- Staged scenes (wedding setup, classroom lesson)
- Visual details (posters, schedules, personal items)

---

## 7. THE FINAL CHOICE

### Location: Reactor Core Chamber

**Requirements to Reach:**
- All 4 keycards collected
- All ship sections explored
- Story fully understood

### Three Options Presented:

**1. SACRIFICE - Manual Reactor Restart**
- Enter reactor chamber (lethal neutron + gamma radiation)
- Exposure: 847 rads/hour for 15+ minutes = 2,100+ rads total
- Biological effect: Acute radiation syndrome, bone marrow death, GI tract destruction
- Complete cold shutdown sequence (3 min in radiation)
- Manually realign magnetic confinement coils (physical labor in radiation)
- Initiate restart, stabilize plasma (12 min in radiation)
- Ship systems restore, cascade purged, everyone survives
- You die from radiation-induced multi-organ failure within hours
- **Ending:** Everyone wakes 8 months later, reaches PE-7742 in 35 years, thrives

**Technical Detail Shown:**
- Geiger counter audio increases as you enter
- Dosimeter display: 0 rads → 500 rads → 1000 rads → 2100 rads
- Visual: Skin reddening, nosebleed, vision blur (radiation symptoms)
- Reactor display shows: Plasma temperature, magnetic field strength, neutron flux
- You watch the numbers stabilize as you die

**2. SOLITUDE - Save Yourself**
- Enter isolated engineering pod (not networked)
- Set 35-year hibernation timer
- Ship course already redirected to PE-7742
- **Ending:** You wake alone, 100,000 dead, reach paradise planet solo, eternal loneliness

**3. NOTHING - Walk Away**
- Leave reactor, return to starting bay
- Give up, wait to die
- **Ending:** You die of despair, cascade kills everyone, ship arrives empty at habitable planet

### Post-Choice
- Extended cutscene (6-10 minutes)
- Ending-specific epilogue
- Credits with ending-specific music
- Can reload save before choice to see other endings

---

## 8. AUDIO DESIGN

### Music (16 Tracks - Orchestral + Synth)

**Area Tracks:**
1. "First Breath" - Starting bay (solo cello, synth pad) - 3:00
2. "Hollow Corridors" - Main traversal (strings, piano) - 4:30
3. "Frozen Moments" - Residential (melancholic piano) - 5:00
4. "Children Never Grown" - Family areas (glockenspiel, gentle) - 4:15
5. "The Machine Endures" - Engineering (industrial, rhythmic) - 4:45
6. "Garden of Absence" - Hydroponics (woodwinds, organic) - 5:30
7. "Ten Thousand Dreams" - Hibernation bays (ethereal choir) - 6:00
8. "Command Without Purpose" - Bridge (grand but quiet) - 4:30
9. "Medical Silence" - Medical (sterile, distant) - 4:00
10. "Approach to Core" - Reactor approach (ominous brass) - 3:30
11. "Heart of Fire" - Reactor chamber (massive, slow) - 7:00

**Story Tracks:**
12. "The Lie Unveiled" - Conspiracy discovery (dissonant) - 4:00
13. "A Distant Star" - Hope discovery (rising, major key) - 5:00

**Ending Tracks:**
14. "The Last Light" - Sacrifice ending (triumphant) - 9:00
15. "Alone at World's End" - Solitude ending (solo piano) - 8:30
16. "Entropy" - Nothing ending (fading to silence) - 11:00

### Sound Effects
- **Player:** Footsteps (metal), interaction beeps, flashlight click
- **Environment:** Door hiss, terminal startup, power restoration hum
- **Atmospheric:** Ship ambience, ventilation, distant machinery
- **Special:** Alarms, Geiger counter (reactor), pod hum

### Implementation (Godot)
- Use .ogg format for music (streaming enabled)
- Use .wav for SFX (instant playback)
- Bus structure: Master > Music/SFX/Ambient
- Music crossfades between areas (3 seconds)
- Adaptive layers (add/remove based on events)

---

## 9. VISUAL STYLE

### Art Direction Summary
- **Hand-drawn** painterly style (NOT pixel art)
- **2.5D perspective** side-scrolling
- **Resolution:** 1920x1080 base
- **Character:** ~140px tall, visible brush strokes
- **Cinematic lighting** with dramatic shadows

### Key Techniques for Depth
1. **Parallax layers** (5-7 layers per area)
2. **Forced perspective** painting
3. **Dynamic camera** (zoom, pan for scale)
4. **Layered lighting** (multiple light sources at different depths)
5. **Scale contrast** (character size varies to emphasize space)

### Reference Games
- Oxenfree (parallax depth)
- Inside (lighting, atmosphere)
- Gris (painterly style, scale)
- Little Nightmares (2.5D perspective)
- Kentucky Route Zero (perspective, atmosphere)

---

## 10. TECHNICAL SPECIFICATIONS

### Godot 4.x Implementation

**Scene Structure:**
```
/scenes
├── /ship_sections (25-30 scenes)
├── /ui (HUD, inventory, terminal reader, pause)
├── /systems (autoload singletons: GameManager, AudioManager, SaveSystem)
└── player.tscn
```

**Key Nodes:**
- **CharacterBody2D** for player
- **Camera2D** with lerp follow
- **ParallaxBackground** with multiple ParallaxLayers
- **Light2D** for dynamic lighting
- **Area2D** for interaction zones
- **AnimatedSprite2D** for character animations
- **TileMap** for platforms and floors

**Save System:**
- Auto-save at terminals
- Auto-save entering new sections
- Single save slot (reinforces choice permanence)
- Tracks: position, inventory, flags, terminals read, areas unlocked

**Performance Targets:**
- 60 FPS on mid-range PC
- 30 FPS minimum on Nintendo Switch
- Load times < 3 seconds between areas

---

## 11. DEVELOPMENT SCOPE

### Team Size Estimates
- **Solo developer:** 12-18 months
- **Two-person team:** 8-12 months
- **3-4 person team:** 6-9 months

### Core Roles Needed
- **Programmer:** Godot systems, mechanics, UI
- **Artist:** Character, environments, animations (hand-drawn)
- **Writer:** 87 terminal entries + 151 item descriptions (~50,000 words)
- **Composer:** 16 orchestral/synth tracks
- **Sound Designer:** SFX library

### Budget Estimates (If Outsourcing)
- Art: $2,000-$4,000
- Music: $1,500-$3,000
- Sound: $500-$1,000
- **Total:** $4,000-$8,000

---

## 12. ACCESSIBILITY

### Visual
- Adjustable text size (small/medium/large)
- High contrast mode option
- Colorblind-friendly (keycards have symbols + colors)

### Audio
- Subtitles for all audio (if any voice)
- Visual indicators for important sounds
- Adjustable volume per bus (music/SFX/ambient)

### Gameplay
- No time pressure anywhere
- No complex inputs required
- No quick-time events
- Flashlight battery recharges (never permanently lost)
- Save frequently (no punishing deaths)

### Content Warnings (Displayed at Start)
- Themes of death and mortality
- Isolation and loneliness
- Institutional oppression
- Radiation sickness (ending 1)

---

## 13. SUCCESS METRICS

**The game succeeds if players:**
1. Feel genuinely alone throughout (atmospheric success)
2. Care about the 100,000 passengers by the end (emotional investment)
3. Struggle with the final choice (moral weight)
4. Want to discuss their decision afterward (engagement)
5. Remember the atmosphere weeks later (lasting impact)

**The game fails if players:**
1. Rush through terminals without reading (story disengagement)
2. Don't understand the stakes (clarity failure)
3. Make the choice without hesitation (no moral conflict)
4. Find the atmosphere boring rather than lonely (tone failure)
5. Forget the experience quickly (no impact)

---

## 14. UNIQUE SELLING POINTS

1. **Genuine moral weight** - No "correct" answer, all choices valid
2. **True loneliness** - No NPCs, no AI companions, purely alone
3. **Earned emotion** - Learn about people before deciding their fate
4. **Atmospheric mastery** - Hand-drawn 2D feeling like 3D space
5. **Meaningful consequence** - You triggered the problem, you face the cost
6. **Systemic evil** - Commentary on institutional murder, not monster horror

---

## 15. MARKETING POSITIONING

**Genre Tags:** Walking Simulator, Narrative, Exploration, Atmospheric, Sci-Fi, Choices Matter

**Comparison Points:**
- "Like SOMA but 2D and focused on sacrifice vs survival"
- "Combines Tacoma's environmental storytelling with The Walking Dead's moral weight"
- "Inside's atmosphere meets Gone Home's narrative exploration"

**Key Art Concepts:**
- Tiny character silhouette in massive blue-lit hibernation bay
- Character standing before orange reactor glow
- Empty corridor with single flashlight beam

**Trailer Focus:**
- Show the loneliness (empty spaces)
- Hint at the discovery (conspiracy documents)
- Present the choice (reactor vs isolation)
- Never spoil endings
- Emphasize atmosphere and emotion

---

**END OF GAME DESIGN DOCUMENT**