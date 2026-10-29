# STRANDBEEST
## A BuildThis Website Creation Prompt

Build a complete, polished, self-contained interactive website called **STRANDBEEST**: a minimalist, mesmerizing, side-scrolling mechanical walking simulation. The entire experience centers on a Theo Jansen–inspired Strandbeest walking continuously from left to right across an infinitely generated coastal landscape. The camera follows it in profile while the world scrolls past. The user adjusts the number of legs, walking speed, and terrain characteristics and watches the creature negotiate rolling dunes that gradually swell into enormous mountains, climb into the clouds, and eventually descend toward the sea again.

This is **not a game**. There are no points, objectives, enemies, collectibles, missions, or finish line. It should feel like an elegant kinetic sculpture, an interactive mechanical toy, and a quiet generative landscape artwork. The fascination comes from the authentic-looking linkage motion, contact between feet and uneven ground, and the slow transformation of the environment.

## 1. Central experience

On opening the site, the visitor immediately sees a complete side-profile Strandbeest already walking across a gently undulating beach. The background has distant layered mountains, a large sky, subtle atmospheric haze, and sparse coastal details. The creature remains approximately 35–45% of the way across the viewport as the terrain advances underneath it. Its frame and legs are drawn from thin rods, joints, crankshafts, and simple geometric forms; the moving parts are plainly visible. The movement should be fluid, purposeful, and mechanically intelligible.

The site starts automatically without a splash screen, instructions overlay, or mandatory interaction. Controls are unobtrusive and can be collapsed. It should remain satisfying to watch indefinitely.

## 2. The walking machine

The Strandbeest should be visually inspired by Theo Jansen's linkage: articulated rods, pivot joints, and a rotating crank that produces a recognizable walking-foot trajectory. Prefer an actual consistent linkage construction over arbitrary limb wiggles. Animate joints from shared crank phase with sensible offsets across adjacent leg pairs, so the machine seems driven by a common rotating shaft. Every connecting rod must preserve its apparent length throughout the cycle. Visible pivot joints should connect the rods at their endpoints.

Provide a **Leg Count** slider ranging from **2 to 64**, in increments of 2, with **16 legs** as the initial value. Leg count represents individual legs, organized in mirrored or alternating pairs. Changing the count visibly rebuilds the machine while retaining its mechanical coherence. More legs should yield a longer or more densely packed machine, rather than simply drawing disconnected feet. At high counts it may resemble a mechanical centipede. The machine must remain fully visible and leg motion must remain legible across the slider range. Dynamically adapt camera zoom, creature scale, or frame length as appropriate.

Use a **Walking Speed** slider, 0–100%, initially 45%. At zero the linkage freezes in its current phase and scrolling stops. At nonzero values crank rotation, stride advance, and world scrolling stay synchronized; feet should not appear to skate wildly along the ground.

Foot contact matters. The feet should meet the actual ground profile, not simply penetrate a flat imaginary baseline. Use a stable, understandable approach to terrain following: body height, pitch, and/or gait adapt smoothly to sampled ground elevation. Ground contact should be convincing without breaking the linkage's rod lengths. On very steep or impossible terrain, favor graceful, visibly approximate behavior rather than chaotic snapping or a broken machine. Avoid claiming exact rigid-body physics unless genuinely implemented.

## 3. Procedural landscape

Generate an endless, continuous terrain profile that scrolls smoothly from right to left. The immediate surface begins as small sand ripples and broad low dunes, with no abrupt discontinuities or harsh sawtooth edges. Terrain should be smooth and coherent across chunk boundaries and independent of frame rate. Use layered, long-wavelength undulations and smaller details rather than pure random jitter.

Provide a **Terrain Roughness** slider from 0–100%, initially 30%, affecting the amplitude and local irregularity of the walkable surface. Even at high roughness, maintain broadly walkable continuity; this is not a platformer.

Provide three **Elevation Modes**:

- **Endless Dunes:** gentle rolling terrain at roughly sea level, without dramatic overall elevation gain.
- **Climb Into the Sky (default):** very slowly increase the landscape's large-scale elevation and the scale of its hills. A beach becomes dunes, then hills, then ridgelines, then mountain heights with clouds beneath the creature. Eventually the world transitions gradually into a descent toward the coast, and the cycle can repeat. This should unfold over minutes, not seconds. Do not suddenly teleport or reset the creature or camera.
- **Wild Mountains:** stronger but still smooth elevation changes, longer ascents and descents, more extreme terrain silhouettes, and occasional dramatic high-altitude traverses.

Separate local terrain slope from the much slower regional elevation trend. As the creature climbs, move the camera vertically in a smooth, delayed way to keep it on screen. The viewer should perceive height through the changing distant world: coastlines, mountain layers, horizon, haze, clouds, and sky. Do not simply pin the creature to a fixed y-coordinate and discard all evidence of its climb.

## 4. Depth, atmosphere, and the sky

Use layered parallax scenery: foreground beach details, near hills, distant mountain ranges, horizon, clouds, and sky. Each layer moves at a distinct subtle speed. The foreground should be visually quiet enough that the linkage remains the main attraction.

As elevation rises, shift the environment naturally: beach and shoreline disappear below; the near hills become mountain ridges; clouds drift at or below the creature's altitude; distant mountain silhouettes become smaller and hazier. On descent, reverse these transitions. There should be no abrupt biome swaps or jarring palette changes.

Use restrained color and atmosphere. The scene should be evocative but not cartoonish. Soft sand, pale sea haze, muted blue-gray mountains, and warm off-white sky are suitable. Light can change slowly over a long session, but avoid distracting day/night effects unless they improve the experience. Consider delicate shadows beneath feet and subtle windblown sand when walking near the beach.

## 5. Visual direction

Default to **Minimalist Mechanical Drawing**: clean, thin, slightly warm-colored rods, dark visible joints, elegant silhouettes, a pale atmospheric landscape, and excellent spacing. Think museum installation, generative art, or a beautifully designed interactive science exhibit. The machine should feel engineered, not like a cartoon animal or a generic multi-legged robot.

Optionally provide a **Visual Style** selector:

- **Minimalist Mechanical Drawing (default):** precise linework and subdued landscape colors.
- **Atmospheric Beach:** more naturalistic dunes, richer gradients, sea haze, and sky.
- **Retro Computer Simulation:** limited palette, subtle pixel or CRT character, and technical instrumentation, without sacrificing animation smoothness or readability.

The chosen style should affect the scene meaningfully, not merely recolor the control panel. Keep the overall interface minimal in every style. No stock photographs, unrelated decorations, mascots, gradients everywhere, or oversized marketing headings.

## 6. Controls and interface

Make the animation fill the viewport. Place a compact floating control panel in a corner, using translucent or unobtrusive styling that does not obscure the walking machine. The panel includes:

1. **Leg Count:** 2–64, step 2, default 16; display the exact value.
2. **Walking Speed:** 0–100%, default 45%; display the value.
3. **Terrain Roughness:** 0–100%, default 30%; display the value.
4. **Elevation Mode:** Endless Dunes / Climb Into the Sky / Wild Mountains.
5. **Visual Style:** Minimalist Mechanical Drawing / Atmospheric Beach / Retro Computer Simulation.
6. **Pause / Resume** and **Reset Journey** controls.
7. A small optional readout of distance traveled and relative altitude. These are contemplative instrumentation, not a score.
8. A **Hide Controls** button so the user can enjoy the artwork without interface clutter.

Controls should respond immediately and smoothly. When changing leg count, avoid harsh resets of terrain or camera. When changing speed, maintain crank phase continuity. Reset Journey returns the landscape and altitude progression to the beginning while retaining the user's chosen settings, unless explicitly resetting all settings is offered as a separate action.

On small mobile screens, collapse controls into a small button or bottom drawer. The walking machine and the horizon should remain visible. Support touch, mouse, and keyboard interactions where appropriate. Do not require keyboard input for the core experience.

## 7. Motion and camera behavior

Animation should be smooth and frame-rate independent. Keep terrain generation deterministic over world coordinates so scrolling and changing controls do not produce random flicker or seams. The machine's motion, feet, terrain movement, and distance traveled should all agree on direction and speed.

Use a gentle camera that follows vertical changes with damping. On ordinary dunes, it should not bob violently. During major climbs, the camera rises gradually while background parallax communicates altitude. A subtle amount of body pitch and suspension-like motion is welcome, but avoid excessive wobble.

Avoid obvious looping background tiles, popping terrain, sudden changes in creature size, or rapidly repeating identical mountains. Keep visual performance reasonable even with 64 legs and multiple parallax layers. Use vector drawing or a canvas-based rendering approach if it best serves smooth linkage animation; the choice of implementation is secondary to the visual and interactive result.

## 8. Emotional tone

The site should be quiet, absurd, and slightly beautiful. The humor is inherent in a needlessly elaborate machine marching endlessly into increasingly impossible geography without ever reconsidering its purpose. Do not explain the joke. No achievement banners, motivational copy, pop-ups, tutorial mascots, or narration.

Sound is optional and **off by default**. If included, make it a quiet, user-enabled mechanical ticking, faint wind, or surf ambience. Never autoplay audio.

## 9. Quality bar and edge cases

- The initial page must immediately show a recognizable, moving, multi-legged Strandbeest in side profile.
- Every leg must visibly participate in a coherent gait; changing leg count must change the actual model.
- Cranks and linkages should appear physically connected and retain consistent rod lengths.
- Feet should approximately follow terrain contact, with no persistent obvious floating or deep clipping on ordinary dunes.
- The world must scroll indefinitely without terrain seams, sudden jumps, or visible end-of-world boundaries.
- Elevation Mode must produce a perceptible long-term journey from beach to high mountains and clouds, then descent; the user should not have to wait forever to see evidence of progress, but the full transition should feel gradual.
- The camera should keep the machine visible throughout elevation changes.
- Controls must actually work, including pause, reset, mobile interactions, and extreme leg counts.
- Respect reduced-motion preferences by providing a paused or low-motion initial state where appropriate.
- Ensure readable controls, keyboard focus indicators, and sufficient contrast.
- Avoid broken layouts on mobile, unnecessary external dependencies, and placeholder buttons.

## 10. What to build and what not to build

**Build the complete interactive website, not a static mockup.** Prioritize the working Strandbeest linkage, smooth scrolling terrain, adaptive elevation/camera, parallax scenery, and live controls. Deliver an experience that is delightful to leave open and watch.

Do **not** add accounts, databases, social feeds, leaderboards, achievements, shops, story mode, multiplayer, quests, or other unrelated product features. Do not replace the machine with a generic walking animation. Do not overcomplicate the interface. Avoid asking the user to make routine design decisions: use the defaults above and make thoughtful decisions where unspecified.

**Guiding sentence:** *A machine designed to walk on a beach keeps walking until the beach becomes a mountain and the mountain becomes the sky.*
