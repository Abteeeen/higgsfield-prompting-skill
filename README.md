# HIGGY — Seedance 2.0 Prompting Wiki

Welcome to the official HIGGY Wiki, a structured knowledge base compiled for advanced AI content creation using ByteDance's **Seedance 2.0** multimodal video generation model.

## 🎬 Use This Repo as a Claude Skill

This repo is packaged as a Claude Skill: **[SKILL.md](./SKILL.md)** is the entry point, and the wiki files below are its on-demand references. Once installed, Claude automatically applies the full prompting methodology whenever you ask for a video prompt — no need to paste anything.

**Install options:**

| Where | How |
|---|---|
| **claude.ai / Claude Desktop** | Zip this folder (or download the release zip) → Settings → Capabilities (Customize) → Skills → Upload. Then just ask for video prompts in any chat. |
| **Claude Code (per project)** | Clone into `.claude/skills/higgsfield-video-prompting/` inside your project. |
| **Claude Code (global)** | Clone into `~/.claude/skills/higgsfield-video-prompting/` — available in every project. |

Zip build command: `zip -r higgsfield-video-prompting.zip . -x ".git/*"` from the repo root.

**Built-in modes:** this skill also replicates both official Higgsfield skills, so nothing else is required — **[Shotlist Director mode](./shotlist_director.md)** (script + assets → connected multi-scene shotlist with style prefix and named cuts 1a/1b/2a…) and **[Footage VFX mode](./footage_vfx.md)** (analyzes your real footage and writes locked video-to-video VFX prompts). Pair with **Higgsfield MCP** to generate directly from Claude.

---

This wiki is organized into five primary sub-topics:

1. **[Text Prompting Guide](./text_prompting.md)**
   - Covers the fundamentals of writing natural language prompts, the 4-part prompt structure, camera language, and weak vs. strong prompting comparisons.
2. **[Multimedia Prompting Guide](./multimedia_prompting.md)**
   - Explores the `@` reference system, multimodal input limits, video-to-video VFX, and first/last frame controls.
3. **[Advanced Prompting Techniques](./advanced_techniques.md)**
   - Detailed guide on the production-grade JSON prompt format, character consistency pipelines, the Omni Reference "Ingredient" System, and speed ramping.
4. **[Elements System & Character Consistency Master Guide](./elements_and_consistency.md)**
   - The Higgsfield Elements reusable-asset library (exact name matching, `@` element lists, schematic maps), Soul ID persistent identity training, the full 3-stage production workflow with verbatim asset prompts, the 2026 consistency-tool comparison (Soul ID vs Flux.2 vs LoRA vs Runway etc.), Canvas, Cinema Studio, and a consistency failure→fix cheat sheet.
5. **[Format Playbooks](./format_playbooks.md)**
   - Official per-format prompt modes (Transformations, Orbs, POVs, Fights, Animation), the 3 video-to-video VFX difficulty levels, lock-header language, inline `[VFX: ...]` brackets, the NON-IP directive, positive locks / negative blocks, and the film-stock & FOV lexicon.

---
## External Resources & Platforms
For more tools, community tips, and official repositories, refer to:
- **GitHub**: [dexhunter/seedance2-skill](https://github.com/dexhunter/seedance2-skill)
- **Hugging Face**: [ByteDance Model Space](https://huggingface.co/ByteDance)
- **Twitter/X**: [@higgsfield_ai](https://x.com/higgsfield_ai)
