# GENERATION SHIP: THE LAST WAKE
## Art Style Guide - Achieving 3D Depth in 2D

---

## CORE PHILOSOPHY

**Challenge:** Create the feeling of massive 3D spaces, dramatic scale, and cinematic depth using only 2D hand-drawn art.

**Solution:** Use advanced 2D techniques that create the illusion of three-dimensional space through parallax layering, perspective painting, dramatic lighting, and camera work.

**Goal:** Players should feel the vastness of the empty ship, the scale of the hibernation bays, and the loneliness of being a tiny figure in enormous spaces—all in 2D.

---

## TECHNIQUE 1: AGGRESSIVE PARALLAX LAYERING

### What It Is
Multiple background layers scrolling at different speeds to create perceived depth. The more layers and the greater the speed difference, the stronger the 3D illusion.

### Implementation for Generation Ship

**Standard Areas (Corridors, Rooms):** 5 layers
- **Layer 1 (Farthest):** 20% camera speed - Deep background, space through windows, distant ship structure
- **Layer 2:** 40% camera speed - Far walls, large machinery, architectural elements
- **Layer 3:** 60% camera speed - Mid-distance objects, furniture, secondary structures
- **Layer 4:** 100% camera speed - Playable layer, platforms, interactive objects
- **Layer 5 (Foreground):** 130% camera speed - Pipes, cables, atmospheric framing elements

**Massive Areas (Hibernation Bays, Hydroponics):** 7 layers
- **Layer 1:** 10% - Distant pod rows fading into darkness (creates "thousands" feeling)
- **Layer 2:** 25% - Far pod rows, barely lit
- **Layer 3:** 40% - Mid-distance pods with visible details
- **Layer 4:** 60% - Near pods, full detail visible
- **Layer 5:** 100% - Walkway (playable layer)
- **Layer 6:** 120% - Close pod edges, framing elements
- **Layer 7:** 150% - Foreground atmospheric elements (mist, hanging cables)

### Why This Works
The separation between layer speeds creates the perception of traveling through 3D space. When character moves, distant objects barely move while close objects whip past—exactly like real 3D.

### Reference Games
- **Oxenfree** - Master class in parallax depth, creates incredible sense of space
- **Night in the Woods** - Uses parallax to make 2D town feel expansive and real
- **Hollow Knight** - Deep parallax in background creates vast cavern feeling

---

## TECHNIQUE 2: 2.5D PERSPECTIVE (ANGLED VIEW)

### What It Is
Instead of pure flat side-scrolling, use a slight angled perspective where the character appears to walk "into" the screen slightly, not just left-to-right.

### Implementation for Generation Ship

**Camera Angle:**
- Slight 3/4 angle (approximately 15-20 degrees off pure side view)
- Character appears to walk into depth, not just across screen
- Floors and platforms painted with perspective converging to vanishing point
- Creates sense of "going somewhere" not just "moving sideways"

**Environment Painting:**
- All backgrounds painted with consistent perspective lines
- Vanishing points guide eye into depth
- Corridors recede dramatically
- Rooms feel like spaces you could walk around in

**Character Rendering:**
- Character sprite painted to match perspective angle
- Slight foreshortening when appropriate
- Shadow placement reinforces depth angle

### Why This Works
Pure side-scrolling feels flat. Adding even a slight angle tricks the brain into perceiving depth. The character feels like they're navigating 3D spaces.

### Reference Games
- **Inside (Playdead)** - Perfect example of 2.5D creating spatial depth
- **Little Nightmares** - Side-scrolling but feels completely 3D due to perspective
- **Limbo** - Uses perspective and depth of field brilliantly

---

## TECHNIQUE 3: DRAMATIC CAMERA WORK

### What It Is
Dynamic camera behavior that emphasizes scale and creates cinematic moments, making spaces feel larger than they are.

### Implementation for Generation Ship

**Scale Reveals:**
- **Entering hibernation bay:** Camera zooms out slowly over 2 seconds, revealing thousands of pods
- **Character becomes tiny** on screen, emphasizing isolation and scale
- **Zoom out maximum:** Character is 1/4 normal size, environment dominates

**Intimate Moments:**
- **Reading terminals:** Camera zooms in slightly, focuses on character and screen
- **Creates contrast** between vast empty spaces and personal story moments
- **Zoom in:** Character is 1.5x normal size, feels close and personal

**Cinematic Pans:**
- **Discovering key areas:** Camera pans slowly ahead of player, revealing environment
- **Player walks into pre-revealed space** creating anticipation
- **Example:** Approaching reactor - camera pans to show massive glowing core before you reach it

**Environmental Framing:**
- **Camera shifts vertically** to show tall spaces (reactor chamber, pod stacks)
- **Tilts slightly** for dramatic effect in key moments
- **Pulls back** when player looks up (shows ceiling/upper areas)

### Why This Works
Static camera makes everything feel same-scale. Dynamic camera creates variety, emphasis, and emotional beats through framing.

### Reference Games
- **Gris** - Camera work is a character itself, creates incredible sense of scale
- **Journey** - (3D but principles apply) Camera emphasizes tiny character in vast world
- **Ori and the Blind Forest** - Camera zoom and pan creates emotional moments

---

## TECHNIQUE 4: LIGHTING AS DEPTH

### What It Is
Using multiple light sources at different "depths" with proper shadowing to create the illusion of 3D space.

### Implementation for Generation Ship

**Layered Lighting:**
- **Background lights** (far pods, distant screens) - dim, blue, atmospheric
- **Midground lights** (machinery, near pods) - medium brightness, cast soft shadows
- **Foreground lights** (player flashlight, close terminals) - bright, cast sharp shadows
- **Character receives lighting** from all layers based on position

**Shadow Complexity:**
- **Character casts shadow on floor** (playable layer)
- **Character casts shadow on background** when close to walls
- **Foreground objects cast shadows on character** (creates depth sense)
- **Multiple shadow directions** from multiple light sources

**Godot Implementation:**
- Multiple **Light2D** nodes at different z-indices
- **Normal maps** on key objects (walls, floors, character) for realistic light interaction
- **Occlusion** properly set up so shadows cast across layers
- **Volumetric lighting** shader for god rays through grating

**Dramatic Lighting Scenarios:**

**Hibernation Bay:**
- Thousands of small blue pod lights at various depths
- Creates layered glowing field
- Character lit from below by nearby pods
- Atmospheric fog particles visible in light

**Reactor Chamber:**
- Massive orange glow from core (background)
- Character silhouetted against it (rim lighting)
- Foreground shadows are long and dramatic
- Heat shimmer effect distorts light

**Corridors:**
- Ceiling lights create pools of light
- Character moves through light and shadow
- Flashlight cuts through darkness dramatically
- Shadows reveal depth of corridor

### Why This Works
Light behaves three-dimensionally. Proper lighting with layered shadows convinces the brain it's seeing 3D space even in 2D.

### Reference Games
- **Mark of the Ninja** - 2D but lighting creates incredible depth perception
- **Don't Starve** - Simple art but lighting creates strong spatial sense
- **Moonlighter** - Top-down but lighting principles create depth

---

## TECHNIQUE 5: FORCED PERSPECTIVE PAINTING

### What It Is
Painting backgrounds with strong perspective lines, vanishing points, and size gradation that creates the illusion of deep 3D space on a 2D plane.

### Implementation for Generation Ship

**Corridor Design:**
- Paint with strong single-point perspective
- Floor lines converge to vanishing point
- Ceiling lines converge to same point
- Pipes, cables follow perspective lines
- Objects get smaller as they recede
- Creates "tunnel into distance" effect

**Large Chamber Design:**
- Two-point perspective for rooms
- Walls recede at angles
- Floor tiles painted smaller as they go back
- Equipment scaled down with distance
- Creates sense of massive space

**Vertical Spaces:**
- Three-point perspective for tall areas (reactor, pod stacks)
- Things get smaller going up
- Emphasizes height and scale
- Character feels tiny at bottom

**Detail Gradation:**
- **Foreground:** High detail, sharp edges, strong contrast
- **Midground:** Medium detail, readable but softer
- **Background:** Low detail, suggestion rather than precision, faded
- Creates atmospheric depth (depth of field effect)

**Color Temperature Shifts:**
- **Foreground:** Warmer or more saturated colors
- **Background:** Cooler, desaturated, slight blue tint
- Mimics atmospheric perspective (real-world depth cue)

### Why This Works
Our brains are hardwired to read perspective cues. Proper perspective painting triggers 3D spatial understanding automatically.

### Reference Games
- **Gris** - Masterful perspective painting creates vast, deep environments
- **Spiritfarer** - Backgrounds use perspective to feel expansive
- **Child of Light** - Painted environments with strong perspective depth

---

## TECHNIQUE 6: ATMOSPHERIC DEPTH OF FIELD

### What It Is
Simulating camera depth of field by selectively blurring/softening foreground and far background while keeping playable layer sharp.

### Implementation for Generation Ship

**Foreground Blur:**
- Pipes, cables, architectural elements in extreme foreground
- Painted with soft edges, slight blur
- Lower opacity (60-80%)
- Creates "framing" effect
- Makes middle layer (playable) feel focused

**Background Fade:**
- Distant elements progressively lose sharpness
- Far pod rows in hibernation bays painted impressionistically
- Distant corridors fade into soft suggestion
- Creates atmospheric perspective

**Focal Plane:**
- Playable layer is always sharpest
- Where character exists is "in focus"
- Guides player eye naturally
- Creates photographic/cinematic feel

**Dynamic Focus (Optional):**
- When reading terminals: Background softens slightly (blur shader)
- When entering huge rooms: Everything sharp initially, then foreground softens as player moves
- Subtle effect, not distracting

### Why This Works
Depth of field is a major 3D perception cue. Our eyes can only focus on one depth at a time. Replicating this in 2D creates spatial understanding.

### Reference Games
- **Ori and the Will of the Wisps** - Subtle depth of field creates depth
- **Gris** - Foreground elements beautifully soft and framing
- **Kentucky Route Zero** - Atmospheric fade creates vast space feeling

---

## TECHNIQUE 7: SCALE CONTRAST

### What It Is
Deliberately varying character size on screen to emphasize different spatial scales—tiny in vast areas, larger in intimate moments.

### Implementation for Generation Ship

**Character Scale Variations:**

**Massive Spaces (Hibernation bays, reactor chamber):**
- Character renders at 60-70% normal size
- Camera pulled back
- Environment dominates frame
- Creates overwhelming scale feeling
- Emphasizes loneliness and isolation

**Standard Spaces (Corridors, rooms):**
- Character at 100% normal size
- Balanced composition
- Character and environment equal weight

**Intimate Spaces (Reading terminals, small chambers):**
- Character at 120-130% normal size
- Camera closer
- Character emotions more visible
- Creates personal connection moments

**Vertical Reveal:**
- Standing at bottom of tall space: Camera shows height, character small
- Walking through corridor: Normal scale
- Sudden scale shift creates "wow" moment

### Why This Works
Scale is relative. By changing character size on screen, you communicate spatial volume without needing 3D. Players viscerally feel "this space is enormous."

### Reference Games
- **Shadow of the Colossus** - (3D but principle applies) Tiny character vs massive world
- **Journey** - Scale contrast creates emotional impact
- **Inside** - Boy's size varies to emphasize environment scale

---

## REFERENCE GAMES - DETAILED ANALYSIS

### PRIMARY REFERENCES (Study These Extensively)

**1. Oxenfree**
- **Why:** Master class in 2D parallax creating 3D space feeling
- **Study:** How backgrounds layer to create island environments that feel vast
- **Apply:** Parallax technique, atmospheric depth, character scale in space

**2. Inside (Playdead)**
- **Why:** Side-scrolling that feels completely 3D through perspective and lighting
- **Study:** Camera work, silhouette use, lighting drama, perspective angles
- **Apply:** Overall spatial feeling, loneliness atmosphere, cinematic moments

**3. Gris**
- **Why:** Hand-drawn environments that feel enormous and spatial
- **Study:** Perspective painting, camera work, scale contrasts, color progression
- **Apply:** Artistic style, emotional atmosphere, beauty in desolation

**4. Little Nightmares**
- **Why:** 2.5D perspective creates strong sense of navigating 3D spaces
- **Study:** How slight angle makes flat side-scrolling feel spatial
- **Apply:** Perspective technique, scale (character vs environment), atmosphere

**5. Night in the Woods**
- **Why:** 2D town that feels like a real place with depth
- **Study:** Parallax layering, how simple art creates spatial understanding
- **Apply:** Making connected spaces feel like real locations

### SECONDARY REFERENCES (For Specific Techniques)

**6. Hollow Knight**
- **Study:** Deep parallax backgrounds in caverns, lighting in 2D
- **Apply:** Creating vast underground (ship interior) feeling

**7. Mark of the Ninja**
- **Study:** How lighting creates depth in 2D stealth game
- **Apply:** Shadow and light technique, spatial awareness through lighting

**8. Ori and the Blind Forest / Will of the Wisps**
- **Study:** Depth of field in 2D, camera work, atmospheric layers
- **Apply:** Foreground/background blur, cinematic moments

**9. Kentucky Route Zero**
- **Study:** Perspective, atmospheric fade, minimalist but deep spaces
- **Apply:** Making simple art feel vast through perspective

**10. Child of Light**
- **Study:** Painted backgrounds with perspective depth
- **Apply:** Hand-painted style with forced perspective technique

**11. Limbo**
- **Study:** Silhouette with depth through lighting and parallax
- **Apply:** Using contrast and shadow to create depth

**12. Spiritfarer**
- **Study:** Cozy but expansive feeling in 2D side-scroller
- **Apply:** Making limited view feel like part of larger world

---

## TECHNICAL IMPLEMENTATION (GODOT 4)

### Parallax Layer Setup
```
ParallaxBackground
├── ParallaxLayer (Layer 1 - Farthest)
│   └── motion_scale = Vector2(0.2, 0.2)
├── ParallaxLayer (Layer 2)
│   └── motion_scale = Vector2(0.4, 0.4)
├── ParallaxLayer (Layer 3)
│   └── motion_scale = Vector2(0.6, 0.6)
├── [Playable Layer - no ParallaxLayer, just regular Node2D]
└── ParallaxLayer (Layer 5 - Foreground)
    └── motion_scale = Vector2(1.3, 1.0)
```

### Camera Zoom Control
- Use Camera2D with zoom property
- Animate zoom for dramatic moments
- Standard: zoom = Vector2(1.0, 1.0)
- Massive rooms: zoom = Vector2(0.6, 0.6)
- Intimate: zoom = Vector2(1.3, 1.3)

### Lighting Depth
- Assign z_index to Light2D nodes (-100 for far, 0 for mid, 100 for near)
- Use CanvasLayer for UI lighting separate from world
- Enable shadows on key lights only (performance)

### Blur Shader for Depth of Field
- Apply blur shader to foreground/background ParallaxLayers
- Adjust blur strength based on distance from playable layer
- Keep playable layer always sharp

---

## ART PRODUCTION GUIDELINES

### For Each Environment Area:

**1. Sketch Phase:**
- Rough perspective lines
- Establish vanishing point(s)
- Block out major elements
- Plan where character will be (focal plane)

**2. Layer Planning:**
- Decide which elements go in which parallax layer
- Ensure proper depth separation
- Plan lighting sources per layer

**3. Painting Phase:**
- Paint each parallax layer separately
- Far layers: looser, less detail, cooler colors
- Near layers: sharper, more detail, warmer colors
- Consider how layers will overlap

**4. Lighting Pass:**
- Paint lighting affecting each layer
- Account for light sources in different layers
- Ensure consistent light direction

**5. Testing:**
- Import to Godot frequently
- Test parallax movement
- Adjust layer speeds if needed
- Verify depth illusion works when moving

---

## FINAL NOTES

**The Goal:**
When a player walks through the hibernation bay, they should feel like they're in a massive 3D space filled with thousands of pods, even though it's all painted 2D layers scrolling at different speeds.

**The Test:**
If someone watching says "Wait, this is 2D??" - you've succeeded.

**The Art:**
Use these techniques not as tricks, but as artistic tools to create the emotional experience you want: loneliness, scale, beauty, desolation, hope.

---

**END OF ART STYLE GUIDE**