# Seedance 2.0 Advanced Prompting Techniques

This guide covers production-grade prompting structures, character consistency workflows, and the Omni Reference system.

---

## Text Prompting

Advanced text prompting involves structuring instructions as structured JSON objects or using highly technical lighting and camera lexicons.

### Production-Grade JSON Prompt Structure
The JSON format maps parameters directly to Seedance 2.0's rendering parameters:
```json
{
  "scene_duration": "15 seconds",
  "audio": {
    "music": "NO background music, no soundtrack, no score",
    "sound": "natural diegetic SFX only: steam curling, heavy metal impacts"
  },
  "style": {
    "environment": "tactical noir laboratory: matte black surfaces, steel grills",
    "lighting": "High-contrast chiaroscuro: aggressive cobalt-blue rim lights",
    "effects": "volumetric fog, heat distortion"
  },
  "camera_language": {
    "general": "aggressive hand-held movement, whip-pans, bullet-time pauses",
    "lenses": "24mm for wide action, 100mm macro for textures"
  }
}
```

### Advanced Lexicon
* **Lighting**: Use color temperatures + directional adjectives, e.g., "High-contrast chiaroscuro with warm amber key and cold cyan rim lights."
* **Audio Specification**: Declare whether audio is `diegetic` (real-world sounds in the scene) or `cinematic` (soundtrack overlay).

---

## Multimedia/Video/Image Prompting

Advanced multimedia prompting integrates multi-layered character consistency sheets and complex input coordinate references.

### Character Consistency Pipeline
To hold character identity across cuts without drift:
1. **Build the Face (Soul Cinema)**: Generate clean front views of the face.
2. **Build the Outfit (Soul Cinema)**: Generate clothing layers separately.
3. **Fuse into Master (Nano Banana Pro)**: Combine face + outfit into a reference sheet.
4. **Clean the Sheet**: Erase faces from the profile/back views, leaving only one clear face on the front view. This prevents model confusion.
5. **Establish Visual Anchors**: Use highly detailed geometric descriptors (e.g., "a black leather jacket with three silver zippers on the left sleeve" instead of just "a jacket").

### The Omni Reference "Ingredient" System
Omni Reference involves uploading multiple specialized assets (e.g., character face, location background, product design) into one single generation slot. The model merges these "ingredients" using the reference syntax `<<<image_N>>>`:
* `character_identity: <<<image_1>>>`
* `product_or_subject: <<<image_2>>>`

### Speed Ramping
Specify speed ramping curves inside your prompt segments to synchronize with physical motion:
* `1x -> 0.2x (the impact)`: Real-time action slowing down into bullet-time at the peak moment.
* `1.5x -> 0.3x`: Energetic speed ramp followed by a heavy slow-motion dramatic pause.

---

## External Resources & Citations
- **GitHub**: Review storyboard-to-prompt conversion toolkits at [elementsix/elementsix-skills](https://github.com/elementsix/elementsix-skills).
- **Hugging Face**: Access diffusion parameter specifications and model cards at [huggingface.co/docs/diffusers](https://huggingface.co/docs/diffusers).
- **Twitter/X**: Follow [@RourkeHeath](https://x.com/RourkeHeath) for advanced Omni Reference tutorials and Google Drive skill downloads.
