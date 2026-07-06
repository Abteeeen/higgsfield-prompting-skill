# Footage VFX Mode — Real Video + Plain-Language Idea → Locked VFX Prompt

> Built-in replication of Higgsfield's official `higgsfiled-seedance-footage-vfx.skill`, reconstructed from the official [4K VFX guide](https://higgsfield.ai/blog/vfx_4k). Use this mode when the user uploads (or describes) real footage and wants effects added, the world swapped, or an element transformed — without morphing the subject.

---

## Workflow

1. **Analyze the clip.** When the user attaches a video, read it as a set of frames (that's how you see it) and extract, before writing anything:
   - **Subject:** identity markers — face, hair, facial hair, wardrobe items, rings/accessories, visible skin
   - **Performance:** every gesture and expression with rough timestamps ("at ~2.2s he snaps his fingers, right hand up beside his head")
   - **Camera:** handheld vs locked-off, movement path, framing, lens character, depth of field, grain
   - **Lighting:** direction, color, quality; what the new elements must match
   - If no clip is attached, ask the user to describe these four things (or upload the clip to Higgsfield and describe it).
2. **Get the change in plain language.** e.g. "swap the background to a desert at sunset right when he snaps his fingers."
3. **Classify the difficulty level** (below) — it determines how much must be locked.
4. **Write the prompt**: lock header → timed trigger → transformation description → integration specs → audio → NON-IP.
5. **Tell the user to run it in Seedance 2.0 at 4K.** Non-negotiable: faces, lip-sync and fine detail hold at 4K and warp at 1080p.

## The 3 Difficulty Levels

| Level | What changes | What's locked | Example |
|---|---|---|---|
| **1 — World Swap** | Entire environment | Subject + wardrobe + camera | Plaza → desert at sunset on a finger-snap |
| **2 — Single Element** | One component added/morphed | Everything else, locked-off shot | Head catches fire; hand → cybernetic arm in 6 sequential stages; creatures behind subject |
| **3 — Handheld Cinematic** | Whole world rebuilt | Actor performance + moving handheld camera | Wing-walker on a biplane; sauropods in rainy forest; kraken attacking ship deck |

## Prompt Template

```
@source: Original clip — preserve [his/her] identity, face, [hair, facial hair,
wardrobe items, accessories], expression and every gesture, and the exact
[handheld] framing, lens and camera motion, unchanged throughout.
Do not reinterpret or re-describe any of it — transfer it 1:1 from the source.
100% exact match of the original framing.

At about [X.X] seconds, on [the exact in-clip action/trigger], [the change
begins]: [transformation described in cinematically precise detail — stage by
stage for morphs, region by region for world swaps].

[NEW WORLD / ELEMENT DETAIL]: [materials, textures, scale, motion — use
realism-forcing language, see below].

Integration: real soft-edged contact shadow under [subject/new elements] so
[he/it] is not pasted in; match the source lens character, depth of field and
grain; [new light sources] cast onto [subject] consistently ([e.g. magenta and
cyan neon spill washing over his face from the sides, a cool rim edging his
hair and shoulder, skin kept readable against the dark]).

Audio: SFX and source dialogue only — no added music, no new dialogue.

NON-IP — generic landscape/creature/design, no real brand names, logos or
trademarks anywhere.
```

## Rules

1. **Lock language is rigid, not polite.** "Preserve… unchanged throughout", "transfer it 1:1 from the source", "100% exact match". Soft phrasing ("try to keep") invites drift.
2. **Anchor every change to an in-clip trigger with a timestamp.** "At about 2.2 seconds, on his finger snap…" — the model needs a when, not just a what.
3. **Sequential stages for transformations.** The cybernetic-arm example runs 6 stages, each mechanical step described: "slim bevelled segment caps slide over each nail in sequence, a small actuator clicks into each fingertip joint with a soft metal tap."
4. **Force realism on organic elements.** "Hide like a wet elephant or rhino — deeply wrinkled, cracked, sagging, asymmetric, mud-caked and matte, never smooth, glossy or inflated; eyes alive and wet with catchlights, blinking." Add `no 3D, no cartoon, no VFX` if output looks plasticky.
5. **Integration specs are mandatory:** contact shadows, lens/DoF/grain match, and new-world light spilling onto the locked subject. This is what separates "composited" from "shot there."
6. **Named Elements for precise creatures/objects.** Build a reference in GPT Image 2.0, add it as an Element, and scope it:
   ```
   @LIZARD: Reference of a real large monitor lizard — pebbled scaly skin, long
   claws, heavy tail. Appearance, scale-texture and color reference only; ignore
   the photo's background and lighting, do not use it for the environment.
   ```
7. **Level 3 shots: restate the camera.** The handheld path is part of the performance — describe its drift and corrections so the rebuilt world moves under the *original* camera.
8. **Always 4K output.** Budget for it; iterate composition at lower res only when the shot has no faces or lip-sync.

## VFX Effects Catalog (proven categories)

- **World Swap:** desert, neon city, volcanic terrain, above the clouds
- **Element Addition:** creature crawling out of a screen, lizards on buildings, fire, storms
- **Body Transformation:** hand → robot, hand → invisible, hand → lava, head on fire
- **Character/Mount Addition:** riding an alien creature through floating islands

## Failure → Fix

| Symptom | Fix |
|---|---|
| Subject's face morphs | Strengthen lock header; run at 4K; shorten the clip |
| New element looks pasted in | Add contact shadow + lens/grain match + light-spill lines |
| Change happens at wrong time | Timestamp + name the physical trigger action explicitly |
| Creature looks CGI | Realism-forcing texture language + `no 3D, no cartoon, no VFX` |
| Wrong creature/object design | Build a named Element reference, scope it appearance-only |
| Camera invented new moves | "the exact handheld framing, lens and camera motion, unchanged throughout" + describe the original path |
