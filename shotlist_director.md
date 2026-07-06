# Shotlist Director Mode — Script + Assets → Connected Multi-Scene Shotlist

> Built-in replication of Higgsfield's official `higgsfield-seedance-shotlist-director.skill`, reconstructed from the official [3-Step AI Ads workflow](https://higgsfield.ai/blog/cinematic_headphones). Use this mode when the user has (or needs) a script and multiple assets, and wants per-scene generation prompts for a multi-scene video (ad, trailer, short film, music video).

---

## Input Contract

Collect from the user (build whatever is missing):

1. **Script / creative brief** — even one paragraph works; expand it into scenes yourself.
2. **Element list** — every recurring asset with an exact `@name` and one-line role:
   ```
   @hero — main character
   @boss — side character
   @headphones — product, cream with orange ring
   @sneakers — prop
   @kitchen — apartment kitchen, stove + door
   @stadium — running track
   ```
3. **Asset images** attached for each element (or asset-generation prompts if they don't exist yet — see `elements_and_consistency.md` Section 3).
4. **Delivery target** — total runtime, aspect ratio, platform.

Remind the user: add each asset under **Elements** in Higgsfield with the **identical name** — matching names auto-attach the right images to every generated prompt.

## Output Contract

Return ONE connected shotlist with exactly this structure:

```
=== STYLE PREFIX (prepend to every prompt) ===
[one unified style header — lens, lighting, color, skin, acting, physics,
composition, continuity, technical, audio]

=== SCENE 1 — [location] ===
--- 1a: [cut title] ---
[style prefix reference] + [scene lighting modifier] + [characters/elements
present] + CUT 1..N descriptions
--- 1b: [cut title] ---
...

=== SCENE 2 — [location] ===
--- 2a ... ---
...

=== EDIT NOTES ===
[match-cuts, planned transitions, which seconds to keep]
```

**Why this structure:** change the style prefix once → it updates every scene; edit one named prompt → the rest stay locked. Each named prompt (1a, 1b, 2a…) is one independent Seedance generation.

## Rules for Writing the Shotlist

1. **Style prefix is law.** Write it once, glue it to every prompt. Per-scene prompts may only override lighting/environment for that location (e.g. "Bright, genuinely sunny midday, strong direct sunlight from high and frontal" for an exterior).
2. **Every cut gets:** camera (framing + FOV/lens + movement), characters/elements by `@name`, action written beat-by-beat, and duration (2–3s per cut, 15s max per generation).
3. **Elements by name in every cut** where they appear: "picks up the cream headphones (@headphones) from the counter."
4. **Wardrobe/state changes = element swaps**, never text instructions. Mid-scene dry→sweaty means CUT 4 switches from `@s_hero` to `@s_hero_wet`.
5. **Choreography beat-by-beat.** "He dances" produces flailing. Write: "first two crisp head nods, chin dipping on each beat; then his shoulders roll back one at a time — right, then left… a light quarter-spin on the ball of his foot."
6. **Plan match-cuts at the prompt stage.** End a scene and open the next on the same gesture (a double ear-cup tap) so the edit stitches itself. Record these in EDIT NOTES.
7. **Spatially locked scenes get a schematic element** (`@street_schematic`) plus a text lock: "@skydancer POSITION LOCKED: immediately to the right of the fire hydrant. Fixed and identical across all cuts."
8. **Audio in generation = diegetic only** (dialogue + environmental SFX, no music, no subtitles). Music comes in post, or as an `@music_track` audio element when movement must lock to rhythm.
9. **Product hero shots:** use the body-rig/snorricam pattern — "camera rigged to Hero's body, snorricam-style — zero relative motion between the lens and his head" — product stays tack-sharp while the world blurs.
10. **Keep each named prompt under ~3,000 characters** (platform limit ~3,000–3,500).

## The Canonical Style Prefix (adapt, don't reinvent)

```
8K IMAX commercial, 16:9 widescreen. Photorealistic — no 3D render, no game engine.
Lighting: Natural light only — soft, even morning daylight, gentle atmospheric haze.
Key light from sky. No contre-jour, no rim backlight. No artificial lightning.
Color: 60:30:10 — dominant / secondary / accent.
Camera: Physical cine lens. 180° shutter motion blur.
Skin: Pore-level realism — vellus hair, asymmetric moles, capillary flush.
Acting: Hollywood — micro-pauses before reactions, precise eye-line, living eyes
with catch-lights, chest rise from breathing. Characters never standing, always reacting.
Physics: Gravity and inertia respected — mass has real weight, correct contact
shadows. No floating props.
Composition: Rule of thirds + golden ratio. Every person moving from frame one.
Continuity: Characters, props, environment identical across every cut. No identity drift.
Technical: 24fps smooth motion. 8K detail. No jitter.
Audio: Diegetic dialogue and environmental SFX only. No music. No subtitles.
```

## Worked Example (condensed from the official headphones ad)

**Brief:** 30s headphones ad — hero blocks out a noisy morning, runs, dances down the street.

**Elements:** `@hero`, `@s_hero` (athletic), `@s_hero_wet` (sweat-soaked), `@headphones`, `@sneakers`, `@bag`, `@moka_cream`, `@mug_cream`, `@skydancer`, `@kitchen`, `@stadium`, `@street_schematic`, `@music_track`.

**Scene 1 — Kitchen (1a, 1b, 1c):**
- **1a** (3 cuts): behind-hero 35mm slow follow → window shows neighbor mowing → "a quiet 'heh' tugs one corner of his mouth" → CUT 2: 50mm push-in, "lifts them over his ears in one smooth motion; the cushioned cups seal and the roar drops into a low muffled hum — shoulders dropping a full inch."
- **1b** (5 cuts, product-focused coffee montage): high-angle 12° FOV tele on @moka_cream — every action lands "on the beat" that leaks faintly from the headphones; worm's-eye 84° FOV at burner level: "the igniter clicks — tick, tick — and the gas catches GRADUALLY: one small blue jet lights first, then the flame creeps around the burner ring jet by jet."
- **1c** (3 cuts, dancing exit): 50mm macro on @bag zip → 35mm pan following beat-by-beat groove to the garden doors → side close-up: "taps the orange-ringed ear cup twice — tap, tap — a small knowing smile."

**Scene 2 — Stadium (2a, 2b, 2c):** each cut opens on the same ear-cup tap (match-cut chain). Broadcast grammar: worm's-eye 84° sprint-over-camera, 8° super-telephoto through heat shimmer with handheld tremor, ground-skimming 12° on the strike zone. CUT 4 of 2a swaps to `@s_hero_wet`.

**Scene 3 — Street (6 cuts):** `@street_schematic` locks hydrant → @skydancer → @hero on one line; overhead drone confirms "from above: hydrant — @skydancer — @hero, all three in one line"; final 107° low angle, @skydancer towering; diegetic line: "I'm on my way."

**EDIT NOTES:** double-tap gesture bridges scenes 1→2→3; keep ~2s per cut; music added in post except street scene (locked to @music_track).

## Generation Strategy

- Generate each named cut separately; run 5–20 attempts per cut; expect ~30–50% rejection.
- 720p, no audio, until the prompt locks; then 1080p/4K + audio.
- Change ONE variable per retry. Watch the FULL clip — failures cluster at the 5–8s mark.
