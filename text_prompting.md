# Seedance 2.0 Text Prompting Guide

This guide details the core principles of constructing high-fidelity text prompts for Seedance 2.0.

---

## Text Prompting

Writing text prompts in Seedance 2.0 follows a structured methodology to ensure the model accurately captures the subject, setting, cinematography, and atmosphere.

### The 4-Part Prompt Structure
1. **Subject & Action**: Describe who or what is in the frame and what they are doing. Be highly specific (e.g., "a woman in a red silk dress" instead of "a person").
2. **Setting**: Define the environment, location, and time of day.
3. **Camera Movement**: Use precise cinematic terms like "dolly in," "crane shot," "orbital pan," or "whip pan."
4. **Mood & Atmosphere**: Specify lighting color temperatures, shadow contrast, and environmental effects (e.g., volumetric smoke, fog).

### Weak vs. Strong Prompts
* **❌ Weak Prompt**: "A battle inside a blood vessel... it looks intense."
* **✅ Strong Prompt**: "Sweeping wide shot of two colossal armies clashing inside a vast blood vessel... Handheld camera drifts and shakes... Deep crimson and slate-blue plasma... vast cinematic scale and relentless motion."

### Camera Language Reference
* **Dolly/Push In**: Moves toward the subject.
* **Dolly/Pull Back**: Moves away from the subject.
* **Dutch Angle**: Tilted horizon for tension.
* **Hitchcock Zoom (Dolly Zoom)**: Simultaneous camera push-in and lens zoom-out.
* **Extreme Close-Up (ECU)**: Focuses on minute details like eyes or hands.

---

## Multimedia/Video/Image Prompting

While text prompting is powerful on its own, Seedance 2.0 is a multimodal model. This section explains how text prompts are adjusted and integrated when combined with reference images, videos, or audio.

### Integrating Text with References
When reference images or videos are uploaded, the text prompt acts as a modifier. Instead of describing the subject's entire appearance from scratch, the text prompt focuses on the actions, lighting, and camera movement.

### Time-Segmented Prompts
For clips longer than 10 seconds, text prompts should be structured using timestamps to tell the model exactly when actions or camera moves occur:
```text
0–3s: [opening scene, camera, action]
3–6s: [mid-section development]
6–10s: [climax or key action]
10–15s: [resolution, ending, branding]
```

---

## External Resources & Citations
- **GitHub**: Discover prompt construction tools at [dexhunter/seedance2-skill](https://github.com/dexhunter/seedance2-skill).
- **Hugging Face**: Explore compatible text encoders and open models on [huggingface.co/models](https://huggingface.co/models).
- **Twitter/X**: Find quick tips on text prompt optimization from [@higgsfield_ai](https://x.com/higgsfield_ai).
