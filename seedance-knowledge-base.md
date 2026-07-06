# Seedance 2.0 — Complete Knowledge Base for AI Content Creation
> **Compiled from:** Higgsfield Official Blog, Reddit (r/HiggsfieldAI, r/seedance2pro, r/seedance), GitHub (dexhunter, rediumvex, elementsix), Twitter/X, YouTube tutorials, and third-party guides
> **Last Updated:** July 2026

---

## TABLE OF CONTENTS
1. [What is Seedance 2.0](#what-is-seedance-20)
2. [Platforms & Access](#platforms--access)
3. [Core Capabilities](#core-capabilities)
4. [Input/Output Specifications](#inputoutput-specifications)
5. [The @ Reference System](#the--reference-system)
6. [Prompt Engineering Master Guide](#prompt-engineering-master-guide)
7. [Content Creation by Genre](#content-creation-by-genre)
   - [Cinematic & Film](#cinematic--film)
   - [Sci-Fi & Fantasy](#sci-fi--fantasy)
   - [Anime & Animation](#anime--animation)
   - [3D & CGI](#3d--cgi)
   - [Advertising & Marketing](#advertising--marketing)
   - [VFX & Real Footage Integration](#vfx--real-footage-integration)
   - [Social Media Content](#social-media-content)
   - [K-Pop & Music Videos](#k-pop--music-videos)
   - [Faceless YouTube Channels](#faceless-youtube-channels)
   - [Business & Corporate](#business--corporate)
   - [Gaming Content](#gaming-content)
   - [Educational & Explainer](#educational--explainer)
8. [Production Workflow](#production-workflow)
9. [Tool Ecosystem](#tool-ecosystem)
10. [Claude Skills & Prompt Builders](#claude-skills--prompt-builders)
11. [Common Mistakes & Fixes](#common-mistakes--fixes)
12. [Monetization Strategies](#monetization-strategies)
13. [Community Tips & Tricks](#community-tips--tricks)
14. [GitHub Resources](#github-resources)
15. [Reddit Communities](#reddit-communities)
16. [Character Consistency Master Guide](#character-consistency-master-guide)
17. [Animated Short Film Pipeline](#animated-short-film--complete-production-pipeline)
18. [Omni Reference System (Rourke Heath)](#omni-reference--the-ingredient-system-rourke-heath-method)
19. [Advanced JSON-Structured Prompt Format](#advanced-json-structured-prompt-format-production-grade)
20. [15 Best Tested Prompts (AtlasCloud)](#15-best-tested-prompts-from-atlascloud)
21. [70-Prompt Catalog (Imagine.Art)](#70-prompts-across-14-categories-from-imagineart)
22. [Quick Reference: Prompt Templates](#quick-reference-prompt-templates)

---

## What is Seedance 2.0

Seedance 2.0 is ByteDance's multimodal AI video generation model — the world's first model to accept **text, images, video clips, AND audio** simultaneously in a single generation. It produces cinematic output with **native synchronized audio** (not added in post) and maintains character consistency across cuts.

**Key differentiator vs competitors:** Instead of just a text prompt, Seedance 2.0 accepts up to **9 images, 3 video clips, and 3 audio files** as reference inputs (up to 12 total combined files) alongside your text prompt. This makes it a "show, don't just tell" model.

**Output:** 480p–1080p (4K on Higgsfield), 4–15 second clips, multiple aspect ratios, watermark-free.

**Developer:** ByteDance (via BytePlus enterprise infrastructure)

---

## Platforms & Access

| Platform | Model Version | Special Features |
|----------|--------------|------------------|
| **Higgsfield.ai** | Seedance 2.0 (full) + Enhanced Fast | 4K output, Unlimited plan, Claude integration, MCP, Canvas, Elements system |
| **Dreamina (CapCut)** | Seedance 2.0 Mini | Integrated with CapCut editing, faster iteration |
| **Runway** | Seedance 2.0 | Via partnership |
| **Magnific** | Seedance 2.0 | Upscaling + generation |
| **fal.ai** | Seedance 2.0 | API access for developers |
| **ImagineArt** | Seedance 2.0 | Drag-and-drop camera presets |

**Higgsfield exclusives:**
- 4K resolution (only on Higgsfield)
- Seedance Unlimited (30-day, unlimited generations at 480p/720p)
- Elements system for reusable assets
- Claude skills integration
- MCP (Model Context Protocol) for automated workflows

**Pricing on Higgsfield:**
- Credit-based: priority queue, 1080p, parallel jobs
- Unlimited: $XX for 30 days, 480p/720p, standard queue, 1 concurrent job
- Audio adds 50-100% credit cost

---

## Core Capabilities

1. **Multimodal Input** — Text + up to 9 images + 3 video clips + 3 audio files per generation
2. **Native Audio Generation** — Video and sound created together; lip sync in 8+ languages (English, Chinese, Japanese, Korean, Spanish, etc.)
3. **Camera Control via Natural Language** — "dolly in", "truck left", "arc shot", "crane up", "orbital move"
4. **Character Consistency** — @character references + Soul ID for persistent identity across generations
5. **Video-to-Video VFX** — Add effects to real footage with prompt only; no green screen, no rotoscoping
6. **Multi-Shot Storytelling** — Up to 6+ shots in a single 15-second generation with dialogue
7. **First & Last Frame Control** — Specify start and end frames for precise transitions
8. **Speed Ramping** — 24fps→240fps and back, bullet-time effects
9. **10-bit Color** — >1 billion colors (set bitrate to High), eliminates banding
10. **Physical Accuracy** — Real-world physics: gravity, inertia, collision, wind, fabric movement

---

## Input/Output Specifications

### Input Limits

| Type | Max Count | Formats | Max Size |
|------|-----------|---------|----------|
| Images | 9 | jpeg, png, webp, bmp, tiff, gif | 30 MB each |
| Videos | 3 | mp4, mov | 50 MB each, 2–15s total |
| Audio | 3 | mp3, wav | 15 MB each, ≤15s total |
| **Combined** | **12 total** | — | — |

### Output

- Duration: 4–15 seconds (user-selectable)
- Resolution: 480p (640×640) to 4K (3840×2160 on Higgsfield)
- Audio: Native stereo, synced to visuals
- Watermark: None

### Restrictions
- No realistic human faces in uploaded reference images (platform compliance — system blocks them)
- Reference videos slightly increase generation cost

---

## The @ Reference System

This is THE most critical part of Seedance 2.0 prompting. Every uploaded asset gets assigned a role with `@`:

| Purpose | Syntax |
|---------|--------|
| First frame | `@Image1 as the first frame` |
| Last frame | `@Image2 as the last frame` |
| Character appearance | `@Image1's character as the subject` |
| Scene/background | `scene references @Image3` |
| Camera movement | `reference @Video1's camera movement` |
| Action/motion | `reference @Video1's action choreography` |
| Visual effects | `completely reference @Video1's effects and transitions` |
| Rhythm/tempo | `video rhythm references @Video1` |
| Voice/tone | `narration voice references @Video1` |
| Background music | `BGM references @Audio1` |
| Sound effects | `sound effects reference @Video3's audio` |
| Outfit/clothing | `wearing the outfit from @Image2` |
| Product | `product details reference @Image3` |
| Style reference | `@style` — applies lighting, palette, mood |
| Motion reference | `@motion` — replicates camera behavior |

**Combo Example:**
```
@Image1's character as the subject, reference @Video1's camera movement and action choreography, BGM references @Audio1, scene references @Image2
```

---

## Prompt Engineering Master Guide

### The Golden Rule
> **ALWAYS specify shot structure upfront: number of shots, total duration, aspect ratio.**

### The 4-Part Prompt Structure (from Higgsfield)

1. **Subject & Action** — Who/what is in frame, what they're doing
2. **Setting** — Where it happens
3. **Camera Movement** — Specific cinematic terms
4. **Mood / Atmosphere** — Lighting, color, feel

### Weak vs. Strong Prompt

**❌ WEAK:** "A battle inside a blood vessel... it looks intense and dramatic."

**✅ STRONG:** "Sweeping wide shot of two colossal armies clashing inside a vast blood vessel... Handheld camera drifts and shakes... Deep crimson and slate-blue plasma... vast cinematic scale and relentless motion."

### Camera Language Reference

**Basic:**
- Push in / Slow push — Camera moves toward subject
- Pull back — Camera moves away
- Pan left/right — Horizontal rotation
- Tilt up/down — Vertical rotation
- Track / Follow shot — Follow subject
- Orbit / Revolve — Circle around subject

**Advanced:**
- Hitchcock zoom (dolly zoom) — Push in + zoom out (vertigo)
- Fisheye lens — Ultra-wide distorted
- Whip pan — Fast horizontal pan with motion blur
- Crane shot — Vertical movement
- First-person POV — Subjective camera
- Dutch angle — Tilted horizon

**Shot Sizes:**
- Extreme close-up (ECU) — Eyes, mouth, detail
- Close-up (CU) — Face fills frame
- Medium close-up (MCU) — Head and shoulders
- Medium shot (MS) — Waist up
- Full shot (FS) — Entire body
- Wide / Establishing shot — Full environment

### Time-Segmented Prompts (for 10s+ clips)
```
0–3s:   [opening scene, camera, action]
3–6s:   [mid-section development]
6–10s:  [climax or key action]
10–15s: [resolution, ending, branding]
```

### Style Header Template (for cinematic ads)
```
Style: 8K large-format. Photorealistic — no 3D render, no game engine.
Cinematography: naturalistic large-format look, available-light realism, deep contrast.
Lighting: Natural light only. Key light from sky/windows.
Color: 60:30:10 — dominant/secondary/accent.
Camera: Physical cine lens. 180° shutter motion blur.
Audio: Environmental SFX only. No music. No subtitles.
```

---

## Content Creation by Genre

### Cinematic & Film

**Key principle:** Pre-production > Generation. Build ALL assets (characters, locations, props) before animating a single frame.

**Character Pipeline (3-step):**
1. Build the Face (Soul Cinema) — Lock bone structure, eyes, presence
2. Build the Outfit (Soul Cinema) — Every detail separately (belt, bandage, accessories)
3. Fuse into Master (Nano Banana Pro) — Merge face + outfit into production-ready sheet

**Reference Sheet Prompt:**
```
Create a professional character reference sheet based strictly on the uploaded reference image.
Two horizontal rows. Top: four full-body views (front, left profile, right profile, back).
Bottom: three close-up portraits (front, left, right).
Clean neutral background. Maintain perfect identity consistency.
```

**Scene prompt structure:**
```
Style prefix: [lighting, camera, color, audio specs]
Scene header: [location, time, mood]
Shot 1: [camera + action description]
Shot 2: [camera + action description]
...
Total: [duration] / [shot count] / [aspect ratio]
```

### Sci-Fi & Fantasy

**Monster/Creature Design:**
```
A massive alien creature with arachnid-like body structure.
Glowing molten core visible at the chest.
Textured surface mixing hardened shell, wet organic tissue, cracked stone-like hide.
White background, soft shadow, product-render style lighting.
```

**Mech Design (tied to pilot personality):**
```
Bipedal mech suit, white and dark navy panel armor, lightweight silhouette.
Broad angular shoulder plates, open glass cockpit.
Large long-barrel weapon mounted on shoulder.
```

**World Building Prompt:**
```
Highly cinematic, photorealistic live-action still of a vast abandoned urban plaza.
Hybrid architectural fusion of East Asian and European design.
Cold greys, steel blues, muted greens, warm rust accents.
IMPORTANT: No humans, no silhouettes. Maintain strong negative space.
```

**Dragon/Fantasy Flight Prompt:**
```
A lone rider tears through a violent storm across jagged snow-capped mountain peaks
on the back of a flying dragon, shot in full third person.
Single continuous shot, one take no cuts, cinematic oner.
Photorealistic, 8K ultra-high-definition, 35mm film quality.
```

### Anime & Animation

**Anime Style Configuration:**
```
Bold anime/illustration style: clean flat cel-shading, thick confident outlines,
limited color palette with warm amber and muted tones.
Maintain consistent 2D anime illustration aesthetic throughout all frames.
```

**Multi-Style Animation (8 scenes, different styles each):**
- Scene 1: Anime/paper cutout style
- Scene 2: Claymation
- Scene 3: 3D Pixar-style CGI
- Scene 4: Hand-drawn sketch
- Scene 5: Retro 80s anime
- Scene 6: Watercolor
- Scene 7: Stop-motion
- Scene 8: Mixed-media

**Key for anime consistency:** Use same character keyframe across ALL scenes. Create once in Soul Cinema, reuse everywhere.

**Watch/Prop sheet for cross-style consistency:**
```
Prop sheet of a wristwatch, multiple orthographic views (front, side, back, top),
exploded view showing internal components, detailed material breakdown,
cinematic lighting, soft warm light and subtle shadows.
```

### 3D & CGI

**Pixar-Style Multi-Shot (15s, 6 shots):**
```
Multi-shot 3D animated feature, 15s / 6 shots / 16:9
Pixar-quality glossy CGI, expressive cartoon performance, dappled jungle daylight.
(1) push-in, orange monster bounces, waving: "Okay — today's the day!"
(2) close-up, dragon holds map, eyes wide: "Wait..."
```

**CGI Product Commercial:**
```
Hypermotion, CGI commercial video, 15sec, 10 scenes/cuts.
Crisp text renders — suitable for Times Square / Sphere billboards.
```

### Advertising & Marketing

**3-Step Ad Workflow (Higgsfield Official):**

**Stage 1 — Build Assets:**
- Product sheet (GPT Image 2): Front & 3/4 views
- Hero character sheet (Soul Cinema): Close-up + full-body front/back
- Character variants (athletic, soaked, etc.)
- Side characters (boss, etc.)
- Locations (kitchen, stadium, street, office — all at 3/4 angle for depth)
- Props (shoes, bag, moka pot, mug)

**Stage 2 — Prompting Framework:**
1. Download Claude Skill
2. Upload to Claude (Customize → Skills)
3. Attach ALL assets with element list:
```
@hero — main character
@boss — side character
@headphones — product
@kitchen — apartment kitchen
@stadium — running track
@street — Brooklyn corner
@office — boss's office
```
4. Skill writes connected shotlist: style prefix + named per-scene prompts
5. Change prefix once → updates every scene

**Stage 3 — Generate Scenes:**
- 5 scenes minimum (kitchen, stadium, street, office, packshot)
- Each scene: 1a, 1b, 2a, 2b... naming convention
- Edit keeper seconds from dozens of generations

**Style Header for Ads:**
```
Style: 8K IMAX commercial, 16:9 widescreen. Photorealistic.
Lighting: Natural light only — soft, even morning daylight.
Camera: Physical cine lens. 180° shutter motion blur.
Skin: Pore-level realism.
Acting: Hollywood — micro-pauses, precise eye-line.
Physics: Gravity and inertia respected.
Composition: Rule of thirds.
```

**Luxury Skincare Campaign (15s multi-shot):**
- Clean white aesthetic
- Macro product shots
- Golden ratio composition
- Diamond-grade clarity

### VFX & Real Footage Integration

**The 4-Step VFX Workflow:**

1. **Shoot raw footage** — stable, well-lit, camera movement as desired
2. **Claude analyzes clip** — extracts subject, performance, camera, lighting
3. **Describe idea to Claude** — writes optimized prompt with source lock
4. **Paste & generate in Seedance 4K** — native 4K output

**Critical: Source Lock Header**
```
@source: Original clip — preserve his identity, face, hair, wardrobe, 
expression and every gesture, and the exact handheld framing, lens and camera motion, 
unchanged throughout.
```

**VFX Effects Catalog:**
- **World Swap** — Change environment (desert, neon city, volcanic, clouds)
- **Element Addition** — Creature crawling out of screen, lizards on buildings
- **Body Transformation** — Hand→Robot, Hand→Invisible, Hand→Lava, Head on Fire
- **Character/Mount Addition** — Riding alien creature through floating islands

**Key Rule:** Always run VFX at 4K — at 1080p, fine details (faces, lip-sync, edges) warp.

**3 Levels of VFX Difficulty:**
- Level 1: Swap the world around you (keep subject, change environment)
- Level 2: Change one element (add fire, transform hand, add lizard)
- Level 3: Complete scene replacement (alien world, creature mounts)

### Social Media Content

**Platform-Specific Optimization:**
- **TikTok/Reels/Shorts:** 9:16 vertical, hook in first 2s, loop potential
- **YouTube:** 16:9 widescreen, 8–15s clips
- **LinkedIn:** Professional aesthetic, 1:1 or 16:9

**Viral Hook Patterns (from rediumvex Claude skills):**
1. Pattern interrupt — unexpected visual in first 2 seconds
2. Curiosity loop — reveal partially, make viewer need to see more
3. Dopamine trigger — satisfying visual payoff
4. Contrast reveal — before/after transformation
5. Motion hook — kinetic energy from frame 1

**Faceless Channel Workflow:**
1. Stock footage / generated backgrounds
2. Text overlay + voiceover
3. B-roll from Seedance generations
4. Kinetic typography for emphasis

### K-Pop & Music Videos

**Zephyr Series Pipeline (first-ever K-Pop AI series):**
1. Build character faces (Soul Cinema)
2. Build outfits separately (every detail)
3. Fuse face + outfit → master character sheet (Nano Banana Pro)
4. Build world/environment assets
5. Build monster/mech assets
6. Animate everything with Seedance 2.0

**Director's Rule:** "Every character gets introduced twice — once in the cabin to establish who she is, once in action to establish what she can do."

**Character prompt template:**
```
Young Asian female (age 20), slim, very attractive K-pop idol level beauty,
flawless skin, soft symmetrical features, expressive eyes.
Short/mid-length slightly messy stylish hair.
Outfit: futuristic mechanic techwear — shorts, layered fabrics, straps.
White studio background, soft cinematic lighting.
```

### Faceless YouTube Channels

**Monetization Workflow:**
1. Niche selection (finance, history, tech, motivation)
2. Script writing (Claude/ChatGPT)
3. Voice generation (ElevenLabs)
4. Visual generation (Seedance 2.0 for B-roll)
5. Edit in CapCut/DaVinci Resolve
6. Thumbnail with AI (SOUL 2.0 or similar)
7. Upload with SEO optimization

**Reported income potential:** $39,500/month using Claude Fable 5 + Higgsfield MCP

### Business & Corporate

**Use Cases for Local Businesses:**
- Daily/weekly promotional videos for social media
- Customer reviews → visual stories
- Educational clips about products/services
- Behind-the-scenes content
- Product demos

**SaaS Launch Video Structure:**
- 0–2s: Hook (problem statement visually)
- 2–6s: Solution reveal (product UI)
- 6–10s: Benefits montage
- 10–15s: CTA + branding

### Gaming Content

**Gaming Montage Prompt:**
```
First-person POV hoverbike, organic camera shake.
0:04–0:05 — The jolt, time violently freezes into extreme slow-motion.
240fps macro insect detail, then snaps back to 24fps.
```

**Sports/FIFA Content:**
- Close tracking dribble shots
- Low-angle orbit camera movement
- Dramatic goal finish with knee slide
- Anime-style football (2D cel-shaded)

### Educational & Explainer

**Structure:**
```
@Image1 as first frame: clean title card
0–3s: Problem statement with visual metaphor
3–8s: Core concept explained with animated diagrams
8–12s: Real-world application example
12–15s: Summary + call to action
```

---

## Production Workflow

### Pre-Production Checklist
1. [ ] Write script/creative brief
2. [ ] Generate character reference sheets (Soul Cinema → Nano Banana Pro)
3. [ ] Generate location references (Soul Cinema / Cinema Studio 3.0)
4. [ ] Generate product/prop sheets (GPT Image 2 / Nano Banana Pro)
5. [ ] Create Elements in Higgsfield (exact name matching!)
6. [ ] Download Claude prompt-building skill
7. [ ] Upload all assets to Claude with element list

### Generation Strategy
1. Start at 720p to validate prompts (cheaper, faster)
2. Prototype WITHOUT audio first
3. Change ONE thing per iteration (prompt OR reference)
4. Watch FULL clip — problems appear at 5-8 second mark
5. Lock prompt at 720p, then scale to 1080p/4K
6. Add audio only after visual is locked

### Post-Production
- Stitch multiple 15s clips together (Seedance max = 15s)
- Color grade for consistency
- Add music/sound design
- Edit in CapCut, DaVinci Resolve, or Premiere

### Credit Management
- Audio adds 50-100% credit cost — skip until final render
- Reference videos increase cost
- 4K uses more credits than 1080p
- Use Unlimited plan for iteration/volume; credit mode for final delivery

---

## Tool Ecosystem

### Higgsfield Tool Suite

| Tool | Purpose | Best For |
|------|---------|----------|
| **Seedance 2.0** | Video generation | Final output |
| **Seedance 2.0 Enhanced Fast** | High-throughput video | Volume iteration |
| **Soul Cinema** | Photoreal image generation | Character faces, locations |
| **SOUL 2.0** | AI photodumps, moodboards | Style exploration |
| **Nano Banana Pro** | Image editing, prop sheets | Character sheets, prop design |
| **GPT Image 2** | Product sheets, edits | Product shots, layout maps |
| **Cinema Studio 3.0** | Cinematic location stills | World building |
| **Popcorn** | Character consistency | Persona persistence |
| **Higgsfield Cast** | Character creation | Pre-built archetypes |
| **Higgsfield MCP** | Automated workflows | Claude integration |
| **Elements** | Reusable asset library | Cross-generation consistency |
| **Canvas** | Multi-clip timeline | Full video assembly |

### Complementary Tools (outside Higgsfield)
- **Claude/ChatGPT** — Prompt writing, script generation
- **ElevenLabs** — Professional voice generation
- **CapCut/DaVinci Resolve** — Final editing
- **Topview.ai** — AI drama studio for scripted content
- **Google AI Studio** — Past Forward app for image editing

---

## Claude Skills & Prompt Builders

### Official Higgsfield Skill
- **higgsfield-seedance-shotlist-director.skill** — Generates connected multi-scene shotlists from script + assets
- **higgsfiled-seedance-footage-vfx.skill** — Analyzes your footage and writes VFX prompts
- **prompt-builder.skill** — General Seedance prompt generation

### Community GitHub Skills

| Repository | Description | Author |
|------------|-------------|--------|
| **dexhunter/seedance2-skill** | Comprehensive prompt writing guide (EN + 中文) | dexhunter |
| **rediumvex/ai-video-generator-claude** | 10 specialized skills (viral hooks, SaaS, luxury, faceless, etc.) | Roman Knox |
| **songguoxs/seedance-prompt-skill** | Claude Code skill for Seedance prompts | songguoxs |
| **elementsix/elementsix-skills** | Storyboard transformation into Seedance prompts | elementsix |
| **sheldonivish/video-prompt-builder** | Shot-by-shot prompt generation from creative briefs | sheldonivish |

### How to Use Claude Skills
1. Download `.skill` or `.md` file
2. In Claude: Customize → Skills → Upload
3. Start fresh chat, attach skill + all assets
4. Provide plain-English brief → skill outputs production-ready Seedance prompt

---

## Common Mistakes & Fixes

| Mistake | Problem | Fix |
|---------|---------|-----|
| Vague prompts | Inconsistent output | Always include subject + action + setting + camera |
| Wrong workflow | Text-to-video for specific person = wrong face | Use image-to-video with reference |
| 1080p immediately | Wasted credits on tests | Start at 720p, upgrade after prompt locks |
| Changing multiple variables | Can't identify what worked | Change ONE thing per generation |
| Only checking first frame | Missing mid-clip drift/freeze | Watch ENTIRE clip |
| Too-short prompts | Generic results | Describe at least 4 parts |
| Camera instructions ignored | Generic terms | Use specific: "dolly in", "crane up", "arc right" |
| Character inconsistency | Face drift | Add visual anchors (hair, clothing); use Soul ID |
| Jerky transitions | Gap between clips | Use first-and-last-frame capability |
| Ignoring audio mode | Credit waste | Prototype without audio; add only at final pass |

---

## Monetization Strategies

### Direct Revenue
1. **Higgsfield Earn** — Monetize directly on platform
2. **Freelance AI video creation** — $350–500+ per commercial
3. **Faceless YouTube channels** — $39,500+/month reported
4. **AI UGC Ads for Meta** — Test 40+ variants weekly at $0 cost
5. **Paid partnerships** — Brand deals using AI-generated content

### Agency Model
- Build creative agency offering AI video production
- Platforms for finding clients: Toptal, YunoJuno, Contra, Superside, VidMob
- Service: script → character generation → video generation → editing → delivery

### Content Creator Path
1. Niche down (fashion, tech, finance, sports)
2. Build consistent visual style using Soul ID
3. Post daily across TikTok/Reels/Shorts
4. Monetize via sponsorships + platform programs

---

## Community Tips & Tricks

### From Reddit (r/HiggsfieldAI, r/seedance2pro, r/generativeAI)

**From Higgsfield's Head of Prompt Engineering (AMA):**
- Write specific instructions, paste to Claude or Gemini
- They work better for Seedance prompting than ChatGPT
- The @reference syntax and timeline prompting take 1-2 days to click
- Use structured workflows for series; skip for one-offs

**Community Discoveries:**
- "The most underused feature is audio as input" — r/Seedance_v2
- "Seedance handles rhythm changes and camera movement well" — r/seedance2pro
- "Build stylized characters to avoid uncanny valley with real faces" — r/generativeAI
- "The whole thing is built shot by shot, separate 15s prompts edited together" — r/HiggsfieldAI
- "Don't start posting AI slop content" — Instagram creator community warning
- "Japanese animators use Grok for 3D previs → Seedance for polished anime" — Instagram

### From Twitter/X
- @higgsfield_ai: Official Higgsfield account
- @theromanknox (280K+): Seedance prompt skills creator
- @RourkeHeath: Claude + Higgsfield prompting tutorials
- @metricsmule: Prompt bundles for Seedance

### Production Insights
- ~100 generations for a 2-3 minute polished trailer
- Hundreds of generations discarded during production
- 20-30 hours for a 3-minute animated short film
- Each scene gets 5-20 generation attempts before picking the keeper

---

## GitHub Resources

| Repository | URL | What It Offers |
|------------|-----|----------------|
| dexhunter/seedance2-skill | github.com/dexhunter/seedance2-skill | Full prompt engineering guide, @ reference syntax, camera language, domain templates |
| rediumvex/ai-video-generator-claude | github.com/rediumvex/ai-video-generator-claude | 10 specialized Claude skills (viral, SaaS, luxury, faceless, podcast, course, testimonial, avatar, before-after, personal brand) |
| songguoxs/seedance-prompt-skill | github.com/songguoxs/seedance-prompt-skill | Claude Code custom skill for Seedance prompt generation |
| elementsix/elementsix-skills | github.com/elementsix/elementsix-skills | Storyboard-to-Seedance transformation |
| sheldonivish/video-prompt-builder | awesomeskills.dev | Shot-by-shot prompt builder from creative briefs |

---

## Reddit Communities

| Subreddit | Focus |
|-----------|-------|
| r/HiggsfieldAI | Official Higgsfield community, AMAs, tutorials |
| r/seedance2pro | Advanced Seedance 2.0 techniques |
| r/seedance | General Seedance discussion |
| r/Seedance_v2 | Tips, underused features |
| r/generativeAI | Broader AI generation discussion |
| r/advertising | Seedance impact on ad industry |
| r/artificial | General AI discussion |
| r/SaaSStartups | Business use cases |

---

## Quick Reference: Prompt Templates

### Standard Cinematic Template
```
[Style header with lighting/camera/audio specs]

@character [name] in [setting], [time of day].
[Shot 1]: [camera move], [action description].
[Shot 2]: [camera move], [action description].
...
Total: [duration] / [shot count] / [aspect ratio]
```

### VFX Template (with source lock)
```
Use <<>> as the direct source. Camera must follow with 100% accuracy.
Preserve subject identity, face, wardrobe, expression, gestures, 
camera motion unchanged.

[Description of what to ADD or CHANGE]
[Description of new world/element/effect]
[Lighting/grade/audio specs]
```

### Multi-Shot Transformation Template
```
Montage, multi-shot action Hollywood movie.
Photorealistic, 35mm film quality, ARRI ALEXA aesthetic.

Shot 1: [calm/intro scene]
Shot 2: [threat/conflict arrival]
Shot 3: [reaction/catalyst moment]
Shot 4: [transformation/action peak]
Shot 5: [climax/resolution]
Shot 6: [return to calm/new normal]

Total: 15s / 6 shots / 16:9
```

### Product Commercial Template
```
Style: 8K commercial, photorealistic, 16:9 widescreen.

@product on [surface] in [setting].
Camera: [move], [lighting], [atmosphere].
No people, no text, no logos.
[Action description around product].
```

### Anime Template
```
<<>> is the character AND style reference — 
[aesthetic description: cel-shading, outlines, palette].
Maintain consistent 2D anime illustration aesthetic throughout.

0–4s: [opening scene with anime-specific expressions]
4–10s: [action sequence with speed lines, Dutch angles]
10–14s: [resolution with stylized UI elements]
```

---

## Character Consistency Master Guide

### Why Characters Drift
Seedance 2.0 juggles two jobs: keeping a recognizable face AND delivering motion that feels alive. When forced to choose, it picks MOTION over identity. This is why faces drift — especially past 5-8 seconds.

### The 3-Step Character Pipeline (from Higgsfield's Zephyr K-Pop Series)
1. **Build the Face (Soul Cinema):** Run the same base prompt across multiple generations until bone structure, eyes, and presence are right
   ```
   Young Asian female (age 20), slim, very attractive K-pop idol level beauty,
   flawless skin, soft symmetrical features, expressive eyes.
   White studio background, soft cinematic lighting.
   ```
2. **Build the Outfit (Soul Cinema):** Every detail separate — belt, bandage, fabric layer
   ```
   Full body shot, [outfit description], white studio background,
   soft cinematic lighting, realistic.
   ```
3. **Fuse Into Master (Nano Banana Pro):** Merge face + outfit into ONE production-ready reference sheet

### The 4 Rules That Actually Hold Consistency

**Rule 1 — Reference Sheet Format**
```
Create a professional character reference sheet based strictly on the uploaded reference image.
Two horizontal rows:
Top: four full-body views (front, left profile, right profile, back).
Bottom: three close-up portraits (front, left, right).
Clean neutral background. Maintain perfect identity consistency.
```

**Rule 2 — Erase Duplicate Faces**
When reference sheets have faces in every view, the model gets confused about which face to track. Erase face details from profile/back views — leave only one clear face on the front view.

**Rule 3 — Visual Anchors > Generic Descriptions**
- ❌ "She has brown hair" → ✅ "She has a short asymmetrical bob with bright magenta tips"
- ❌ "He's wearing a jacket" → ✅ "He wears a black leather jacket with three silver zippers on the left sleeve"
- Seedance 2.0 latches onto specific geometric/texture details better than vague categories

**Rule 4 — Fewer, Clearer Anchors > Many Vague Ones**
When Seedance gets overloaded with 8+ descriptors, it picks motion over identity. Limit to 3-5 distinctive visual anchors per character.

### The Medium Guide (from @social_18794)
> "I didn't set out to fix identity drift. I just wanted the same character to walk across a room twice without turning into a cousin."
> 
> Key insight: Seedance is "reference-first" — it reads the UPLOADED IMAGE more than the text description. If your character drifts, fix the reference image, not the prompt.

---

## Animated Short Film — Complete Production Pipeline

### From MindStudio (3-minute film in 20-30 hours for under $50)

**Step 1 — Write the Script (with AI)**
- 2-3 page script → ~15-20 scenes, each 5-8 seconds
- For every scene: one-sentence visual brief + dialogue
- Example: "EXT. ROOFTOP, DUSK — MAYA stands at the edge, looking down at the city. Wind blows her jacket. WIDE SHOT."

**Step 2 — Design Characters in GPT Image 2**
- Lock character designs BEFORE any video generation
- Multiple poses and expressions per character
- Save as character reference sheets (used later in Seedance)
- Keep backgrounds simple/transparent
- Consistent art style descriptor (e.g., "2D watercolor animation")
- **Spend 2-4 hours here. Highest-leverage step.**

**Step 3 — Generate Scene Backgrounds Separately**
- Separate backgrounds from characters → more control, easier reuse
- Generate a few variations per location, reuse across relevant clips
- Prevents jarring background style shifts between cuts

**Step 4 — Record Voice Lines in ElevenLabs FIRST**
- Record ALL dialogue before video generation
- Export each line as separate .mp3/.wav: `scene_03_maya_line1.mp3`
- Duration tells you required clip length (4.2s audio → 4-5s video)

**Step 5 — Generate Video Clips in Seedance 2.0**
- Generate 15-25 individual clips (expect 30-50% rejection for drift/motion issues)
- For EACH scene: character reference + background + specific prompt
- Keep a spreadsheet: prompt, #generations, selected clip, duration

**Step 6 — Music & Sound Design**
- ElevenLabs music generation or royalty-free (Epidemic Sound, Artlist)

**Step 7 — Edit in Video Editor**
- DaVinci Resolve (free), CapCut, or Premiere Pro
- Assemble clips, sync audio, add transitions
- **Color grading is crucial** — Seedance clips vary in brightness; apply consistent LUT

### Cost Breakdown (3-Minute Short Film)
| Tool | Usage | Cost |
|------|-------|------|
| GPT Image 2 | ~100-150 image gens | $8-15 |
| Seedance 2.0 | ~60-80 video gens | $15-25 |
| ElevenLabs | Voice + SFX | $11/month |
| Music | Royalty-free | $0-15 |
| Editor | DaVinci Resolve | Free |
| **TOTAL** | | **~$34-66** |

---

## Omni Reference — The "Ingredient" System (Rourke Heath Method)

Omni Reference = uploading multiple "ingredient" images into ONE generation:
- Character sheet (face/body consistency)
- Location image
- Text reference (3D text/logo)
- Product image

The model understands context and combines them. One 15-second generation can produce a fully edited ad with VFX, text overlays, slow-motion, and explosions.

**Workflow:**
1. Download Claude "Video Prompt Builder" skill (Rourke Heath's Google Drive)
2. Upload skill to Claude: Customize → Skills → Create → Upload
3. Start message: "Write me a video prompt that creates..."
4. Optionally upload start frame — Claude incorporates it
5. Copy ONLY the shot list portion (ignore "Master Effects Inventory")
6. **Keep under 3,000 characters** — Higgsfield's limit is ~3,000-3,500

---

## Advanced JSON-Structured Prompt Format (Production Grade)

This is the format that produces Higgsfield's viral results. It's a structured JSON designed for Seedance 2.0's multimodal engine. Every field maps to a specific capability of the model.

### Reference Syntax: `<<<image_N>>>`

Different from `@Image1` — the `<<<image_N>>>` syntax is used in advanced prompt builders where you upload numbered reference images. The model maps `<<<image_2>>>` to your second uploaded reference image.

### Full Prompt Template Structure

```json
{
  "scene_duration": "15 seconds",
  "audio": {
    "music": "NO background music / or / [music description]",
    "sound": "natural diegetic SFX only: [specific sounds separated by commas]"
  },
  "style": {
    "environment": "[location description with material adjectives]",
    "lighting": "[named lighting style + specific color/source details]",
    "effects": "[atmospheric elements: steam, dust, smoke, particles, heat distortion]"
  },
  "references": {
    "character_identity": "<<<image_1>>> ([detailed appearance description])",
    "product_or_subject": "<<<image_2>>> ([detailed description])",
    "scene_background": "<<<image_3>>> ([if used])"
  },
  "camera_language": {
    "general": "[overall movement style: aggressive hand-held, smooth dolly, etc.]",
    "lenses": "[specific mm lenses for different shot types]"
  },
  "sequence": [
    {
      "time": "0-Ns",
      "hook": "[COLD OPEN technique — grab attention immediately]",
      "action": "[WHAT happens — present tense, cinematic verbs]",
      "camera": "[specific movement + lens choice for this segment]",
      "speed_ramp": "[initial speed] -> [transition speed] ([what happens])"
    }
  ]
}
```

### What Makes This Format Powerful

1. **Audio is specified as DIEGETIC, not just "add music"** — the model generates synced sound from the prompt. "No background music" is an explicit instruction the model follows.

2. **Lighting has names AND colors** — "High-contrast chiaroscuro: aggressive cobalt-blue rim lights, warm amber glow spilling from deck oven, hard specular hits on sauce and oil sheen" gives the model precise color temperatures and source directions.

3. **Speed ramping per segment** — `1.5x -> 0.3x (the chew)` creates bullet-time effects natively without post-production.

4. **Lens specification** — `24mm for wide action, 100mm macro for textures` tells the model which virtual lens to render with, affecting depth of field, bokeh, and field of view.

5. **Cold open hook** — first 3 seconds are a micro-climax (like a TV show cold open), then the timeline resets to chronological. This is a proven viral retention technique.

6. **Material adjectives** — "matte black surfaces, brushed steel, flour-dusted wood, blazing deck oven" give the model specific render targets for different surface types.

7. **Rack focus / whip pan / bullet-time / orbit** — multiple advanced camera moves per segment, not just one.

### Production Template: Food Commercial

```json
{
  "scene_duration": "15 seconds",
  "audio": {
    "music": "NO background music, no soundtrack, no score",
    "sound": "natural diegetic SFX only: [food sounds described precisely]"
  },
  "style": {
    "environment": "tactical noir [location]: matte black surfaces, [materials], faint city-night haze",
    "lighting": "High-contrast chiaroscuro: aggressive [color] rim lights on [subject], warm amber glow from [source], hard specular hits on [surface]",
    "effects": "rising [steam/dust/smoke], [particle effect], heat distortion off [source]"
  },
  "references": {
    "character_identity": "<<<image_1>>> ([appearance with clothing details, no grid/overlay/mesh])",
    "product_design": "<<<image_2>>> ([detailed food/product description])"
  },
  "camera_language": {
    "general": "aggressive hand-held movement, whip-pans, bullet-time pauses, and precision push-ins",
    "lenses": "24mm for wide action, 100mm macro for textures ([specific textures to capture])"
  },
  "sequence": [
    {
      "time": "0-3s",
      "hook": "THE [ACTION] (COLD OPEN): [Subject] holds [product] and performs [dramatic action], holding the camera's eye as [atmospheric effect occurs].",
      "camera": "extreme macro punch-in on [detail] -> quick pull-back to [wider shot].",
      "speed_ramp": "1.5x ([action]) -> 0.3x ([aftermath])"
    },
    {
      "time": "3-6s",
      "action": "CINEMATIC OPENER: [Subject] performs [process step 1], a burst of [particle] explodes toward camera. [Process step 2] in one motion.",
      "camera": "wide-angle whip-pan following [movement] -> ultra-slow-motion macro on [particle] -> violent push-in on [detail].",
      "speed_ramp": "1x -> 0.2x ([slow motion moment]) -> 1.5x ([fast motion])"
    },
    {
      "time": "6-9s",
      "action": "[MID-SEQUENCE]: [Subject] performs [process steps]. [Product] goes onto/into [destination].",
      "camera": "low-angle tracking shot along [surface] -> quick tilt following [movement] as [product] [lands/slides].",
      "speed_ramp": "1.5x -> 1x"
    },
    {
      "time": "9-12s",
      "action": "THE TRANSFORMATION: [Product changes/transforms in detail], [visual changes described], [subject reaction].",
      "camera": "extreme macro tracking shot across [transforming surface] -> rack focus to [subject]'s eyes lit by [source].",
      "speed_ramp": "1x -> 0.2x ([slow transformation]) -> 1.5x"
    },
    {
      "time": "12-15s",
      "action": "THE CLIMAX: [Subject] performs [final action], [product reveals final form], [atmospheric effects], steam curling off surface.",
      "camera": "quick macro on [detail landing] -> 360-degree orbit around [rising product] -> slow push-in on [dramatic detail] -> bullet-time pause at full stretch.",
      "speed_ramp": "1x -> 0.2x ([the pull/reveal]) -> 0.5x"
    }
  ]
}
```

### Production Template: Product/Transformation Commercial

```json
{
  "scene_duration": "15 seconds",
  "audio": {
    "music": "deep cinematic sub-bass rumble, ascending tension drone, percussive hit on transformation",
    "sound": "diegetic SFX: [specific action sounds], whoosh on whip-pans, crisp [material] impacts"
  },
  "style": {
    "environment": "[setting]: [materials], [atmosphere details]",
    "lighting": "[named style]: [color temperature] key from [direction], [accent color] rim, [surface] specular highlights",
    "effects": "[particles], [smoke/fog], [energy/light effects], [material transformation effects]"
  },
  "references": {
    "subject": "<<<image_1>>> ([detailed description])",
    "product_before": "<<<image_2>>> ([description])",
    "product_after": "<<<image_3>>> ([description — optional])"
  },
  "camera_language": {
    "general": "[style], whip-pans, bullet-time pauses, precision push-ins, 360-degree hero orbit",
    "lenses": "[wide mm] for establishing, [telephoto mm] for detail, [macro mm] for transformation close-ups"
  },
  "sequence": [
    {
      "time": "0-3s",
      "hook": "COLD OPEN: [dramatic moment from climax], [visual hook], [camera treatment].",
      "camera": "[intense opening shot] -> [transition].",
      "speed_ramp": "[fast] -> [slow on key moment]"
    },
    {
      "time": "3-8s",
      "action": "BUILD: [setup/process], [tension building], [subject action].",
      "camera": "[following movement] -> [detail shot] -> [reaction].",
      "speed_ramp": "[normal] -> [variable]"
    },
    {
      "time": "8-13s",
      "action": "TRANSFORMATION: [the change happens in detail], [visual effects], [particle/light show].",
      "camera": "extreme macro on [transforming detail] -> slow orbit -> [reveal shot].",
      "speed_ramp": "1x -> 0.15x ([the transformation]) -> 0.5x"
    },
    {
      "time": "13-15s",
      "action": "HERO SHOT: [product in final form], [branding moment], [atmospheric resolution].",
      "camera": "360-degree hero orbit -> slow push-in to final frame.",
      "speed_ramp": "0.5x -> hold"
    }
  ]
}
```

### Speed Ramping Reference

| Ramp | Effect | Use Case |
|------|--------|----------|
| `1x` | Real-time | Normal action |
| `1.5x` | Slightly fast | Energetic moves, quick transitions |
| `0.5x` | Half-speed slow-mo | Dramatic moments, reveals |
| `0.3x` | Heavy slow-mo | Reactions, impacts, drops |
| `0.2x` | Bullet-time | Explosions, transformations, particle bursts |
| `0.15x` | Near-freeze | Peak transformation moment |
| `1x -> 0.2x` | Real-time to bullet-time | Sudden dramatic pause |
| `1.5x -> 0.3x` | Fast action to slow chew/impact | Sports replays, combat hits |

### Camera Move Vocabulary for JSON Prompts

**Combined moves (use with -> between them):**
- `extreme macro punch-in on [detail] -> quick pull-back to [wider shot]`
- `wide-angle whip-pan following [subject] -> ultra-slow-motion macro on [particle] -> violent push-in on [target]`
- `low-angle tracking shot along [surface] -> quick tilt following [movement]`
- `rack focus to [subject]'s eyes`
- `360-degree orbit around [subject] -> slow push-in -> bullet-time pause`
- `extreme macro tracking shot across [surface]`

### Lighting Vocabulary

**Named styles with color specifications:**
- `High-contrast chiaroscuro` — aggressive rim lights + deep shadows
- `Available-light naturalism` — motivated by in-scene sources
- `Neon-noir` — colored practical lights, wet reflections
- `Golden-hour backlight` — warm rim, soft fill
- `Overhead industrial` — harsh top-down, deep eye shadows
- `Candle-lit intimacy` — warm flickering, shallow falloff
- `Cyberpunk ambient` — neon rim + fog + volumetric beams

**Always pair a style name with specific colors:**
"High-contrast chiaroscuro: aggressive cobalt-blue rim lights, warm amber glow spilling from deck oven, hard specular hits on sauce and oil sheen"

### Audio Specification Format

**Two modes:**

1. **Diegetic only (for realism/cinematic):**
```json
"audio": {
  "music": "NO background music, no soundtrack, no score",
  "sound": "natural diegetic SFX only: [comma-separated list of EVERY sound]"
}
```

2. **Cinematic with score (for ads/trailers):**
```json
"audio": {
  "music": "[genre] [tempo]: [instruments], [mood], [when it hits]",
  "sound": "diegetic SFX: [specific sounds]"
}
```

### The `(no grid lines, no overlay, no mesh)` Instruction

Used inside `<reference>` blocks to prevent Seedance from rendering grid overlays or mesh artifacts on character references. Always include when character identity references are used.

---

## 15 Best Tested Prompts (from AtlasCloud)

### Prompt Formula
```
[Subject/Character] + [Specific Action] + [Environment/Setting] +
[Visual Style/Aesthetic] + [Camera Movement] + [Lighting/Mood]
```

### Key Principles
- Maximize specificity: "woman in red silk dress" > "a person"
- Define action explicitly — tell the model what moves and how
- Establish mood through lighting: "golden hour backlighting"
- Specify camera: tracking shots, close-ups, drone angles
- Use real-world references: "Apple keynote style", "Wes Anderson symmetry"

### Top Performer from Each Category

**Epic Space Reveal (9/10 reliability):**
```
Sweeping drone shot ascending from misty valley floor, slowly revealing
vast mountain range at sunrise, golden light breaking through clouds,
National Geographic documentary quality, ultra-smooth camera movement
```
Settings: 16:9, 12-15s, 1080p

**Luxury Product Showcase (works for any product):**
```
A premium wristwatch floating mid-air, slowly rotating, water droplets
suspended around it catching light like diamonds, pure black background,
single dramatic spotlight, extreme macro detail, ultra-smooth rotation
```
Settings: 1:1 or 16:9, 8-10s, 1080p

**Seamless Transformation (viral potential):**
```
A transformation sequence where a vintage 1960s muscle car is parked
in a foggy forest clearing, leaves swirl around it in a growing vortex,
as the vortex peaks the car morphs piece by piece into a futuristic
hover vehicle, cyberpunk lighting with neon accents, seamless morph
```
Settings: 16:9, 8-12s, 1080p

---

## 70 Prompts Across 14 Categories (from Imagine.Art)

Categories covered: Cinematic Narrative & Drama, Action & Sports, Sci-Fi & Cyberpunk, Fantasy & Magic, Horror & Thriller, Anime & Animation, Nature & Wildlife, Food & Product, Fashion & Beauty, Architecture & Travel, VFX & Transformation, Music & Dance, Documentary & Realism, Abstract & Experimental

**Example — Street Dance Battle (90%+ success rate):**
```
Generate a 15-second photorealistic street dance battle at night.
Urban street with reflective wet pavement, neon lights, thin mist.
Young dancers form semicircle. First 5s: one dancer doing solo floor moves.
Remaining 10s: full group synchronized choreography — breaking, popping,
locking, hip-hop. Smooth cinematic camera, realistic physics.
```

**Example — Cave Exploration POV:**
```
First-person POV handheld footage with slight natural shake. Only light
is headlamp illuminating damp mossy walls. Camera moves through narrow tunnel;
hand occasionally enters frame. Audio: heavy breathing, footsteps on wet soil.
When tunnel opens, camera pauses, pans slowly over glowing crystals.
Footsteps hit rocks with sharp clacks. Explorer exhales in awe.
```

---

*Knowledge base compiled from Higgsfield official blog, Reddit communities, GitHub repositories, Twitter/X, YouTube tutorials, and third-party guides including Atlas Cloud, Imagine.Art, MindStudio, Rourke Heath/GenHQ, Medium creators, and community AMAs. All prompt examples are from published articles and community contributions.*
