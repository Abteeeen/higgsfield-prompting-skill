# Seedance 2.0 Format Playbooks — Official Prompt Modes & VFX Language

> Compiled July 2026 from Higgsfield's official Complete Prompting Guide, the 4K VFX guide, and the Seedance 4K film breakdown. This file covers the format-specific prompt patterns that the general guides don't: Transformations, Orbs, POVs, Fights, Animation, and video-to-video VFX levels.

**Universal rule (applies to every format): always specify shot structure upfront** — number of shots, total duration, aspect ratio. E.g. `Total: 15s / 6 shots / 16:9`.

---

## 1. Transformations (highest-performing format)

The escalation arc: **calm → threat → transformation → aftermath**. Number every shot, describe the exact action, build clear escalation.

**Standard opening block (verbatim):**
```
Montage, multi-shot action Hollywood movie, don't use one camera angle or single cut,
cinematic lighting, photorealistic, 35mm film quality, professional color grading,
sharp focus, high detail texture, film grain, depth of field mastery, ARRI ALEXA aesthetic.
```

- Write each shot individually (Shot 1…Shot 6), one camera + one action per shot.
- Typical inputs: 3–4 reference images.
- Use speed-ramping at the transformation peak.

## 2. Orbs (single continuous first-person shot)

The camera IS the character's eyes. One shot, 15 seconds, no cuts.

**Core instruction block (verbatim):**
```
Single continuous shot, first-person POV perspective, the camera IS her eyes,
hyper-chaotic handheld motion, completely unstabilized, violent raw human movement,
constant micro-jitters, aggressive head swings, abrupt jerks, frequent over-rotation
and harsh correction, moments of near motion blur loss, no smoothness at all,
no stabilization.
```

- Keep the character's **hands always visible in frame** — it sells the POV.
- Specify VFX **inline inside the action** with brackets:
  `[VFX: branching electric circuits pulsing with white-blue current, sparks jumping between fingers]`
- Enumerate every SFX sequentially: `SFX: electric crackle, sphere hum surge, energy burst, ...`
- Speed control keywords: `RAMPS TO SLOW MOTION` … `SNAPS BACK`.

## 3. POVs (locked perspective)

Lock the perspective and never break it. The critical line — be explicit about what the camera is NOT doing:

```
One continuous shot, POV [role] perspective in [location], no cuts, no zoom,
natural head movement.
```

Without "no cuts, no zoom," Seedance defaults to cutting between angles.

## 4. Fights

Requirements: clear location, a power mismatch, a defined escalation arc.

- **Describe choreography beat-by-beat — Seedance executes literally.** Generic "they fight" fails; "she grabs a creature mid-leap and overloads it… second attack, she slams both hands down releasing a radial lightning surge" works.
- Use speed-ramping and slow motion at impact moments.
- Typical inputs: 2 reference images (the two fighters).

## 5. Animation

- Break the 15 seconds into timed segments with explicit descriptions per segment.
- Use a keyframe image as the style reference: "The @image is the first keyframe and style reference."
- Describe physics precisely: particle simulation, dust, energy VFX.
- Keep one character keyframe across ALL scenes for consistency.

---

## 6. Video-to-Video VFX — The 3 Difficulty Levels

From the official 4K VFX guide. **Always run VFX at 4K** — faces, lip-sync, and fine detail hold at 4K where they warp and fall apart at 1080p.

### Level 1 — World Swap (locked subject)
Keep actor and wardrobe identical; transform the surroundings. Trigger on an in-clip action with a timestamp: "At about 2.2 seconds, on his finger snap with his right hand up beside his head…"

### Level 2 — Single Element Change (locked scene)
Locked-off shot; add or morph one component (head catches fire; hand becomes a cybernetic arm in 6 sequential stages; creatures appear behind the subject).

### Level 3 — Handheld Cinematic (hardest)
Preserve the actor's performance AND a moving handheld camera while rebuilding the whole world (wing-walker on a biplane, jungle temple collapse, sauropods in a rainy forest).

### Lock-header language (verbatim patterns)

```
Preserve his identity, face, mustache, hair, wardrobe, rings, expression and every
gesture, unchanged throughout.
Do not reinterpret or re-describe any of it — transfer it 1:1 from the source.
100% exact match of the original framing.
```

### Integration requirements (what makes composites believable)

- "Real soft-edged contact shadow … so he is not pasted in"
- "Match the source lens character, depth of field and grain"
- Texture realism language: "hide like a wet elephant or rhino — deeply wrinkled, cracked, sagging, asymmetric, mud-caked and matte, never smooth, glossy or inflated; eyes alive and wet with catchlights, blinking"

### The NON-IP directive

Append to every VFX/commercial prompt: `NON-IP — generic landscape/creature/design, no real brand names, logos or trademarks anywhere.`

### Audio for VFX shots

`SFX and source dialogue only` or `Diegetic SFX only` — no added music, no new dialogue beyond ambient reactions.

---

## 7. Positive Locks & Negative Blocks (from the 4K film breakdown)

Seedance has no negative-prompt field, so both go inside the prompt text:

**Positive locks** — explicit sections stating what must NOT vary: wardrobe identical across scenes, contact shadows on every surface, natural eye behavior (no artificial glow), locked white balance (e.g. 5200K), key-light direction, color grade with hex values.

**Negative block** — what not to generate:
```
no plastic CGI, no distorted anatomy, no watermarks, no weapons,
generate video without subtitles
```

---

## 8. Pro Tips (official, verbatim)

1. **Monster/creature realism:** if skin looks too smooth or plasticky, add `no 3D, no cartoon, no VFX` — it forces ultra-realism.
2. **Comedy:** write `add a visual gag in the background`.
3. **VFX precision:** specify effects inline inside the action with `[VFX: …]` brackets.
4. **Perspective lock:** without "no cuts, no zoom," Seedance will cut.
5. **Sometimes the shortest prompt is the best experiment** — e.g. the entire prompt "Fight of a 3D person with 2D".
6. **Quality comes from more specific prompts, not more iterations** — exact camera moves, lighting conditions, concrete visual detail.
7. **Start image-to-video, not text-to-video** — a sharp, front-facing, well-lit reference under 8 seconds gives the model a visual anchor and predictable output.
8. **Iteration is a dialogue:** watch the output, name the specific flaw ("waterfall spray reads flat", "wings wrong on the climb"), regenerate with only that fix.

---

## 9. Film-Stock & Texture Lexicon (proven anchors)

**Film stocks / camera bodies:** `35mm film quality` · `ARRI ALEXA aesthetic` · `Anamorphic 35mm` · `strong 35mm film look` · `heavy film grain`

**Motion feel:** `handheld shake throughout` · `hyper-chaotic handheld motion` · `natural head movement` · `operator breathing and micro-drift` · `moments of near motion blur loss`

**Focus/optics:** `shallow depth of field` · `noticeable focus breathing` · `motion blur on fast actions` · `sharp but imperfect focus` · `halation on highlights` · `soft highlight rolloff` · `subtle chromatic aberration near frame edges`

**Realism enforcement:** `practical VFX feel, minimal CGI look` · `natural imperfections` · `100% real-life shooting texture` · `slightly desaturated tones`

**FOV-based camera calls** (numbers beat adjectives): 8° super-telephoto broadcast compression · 12° tele detail · 29° portrait · 47° standard · 63° wide · 84° worm's-eye · 107° rectilinear low angle. Same for speed: "sprints at around 25 km/h" beats "runs fast."

---

## Sources

- [Seedance 2.0 — Complete Prompting Guide](https://higgsfield.ai/blog/seedance-prompting-guide)
- [AI VFX Just Got Insane — Seedance 2.0 in 4K](https://higgsfield.ai/blog/vfx_4k)
- [Recreate Our 1-Minute Seedance 4K Film](https://higgsfield.ai/blog/seedance4k-breakdown)
- [How to Create Ultra-Realistic Videos with Seedance 4K](https://higgsfield.ai/blog/Seedance-4k)
- [Generating with Seedance 2.0: Full Tutorial](https://higgsfield.ai/blog/generating-with-seedance-2-0)
