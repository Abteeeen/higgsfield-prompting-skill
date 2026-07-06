# Seedance 2.0 Multimedia Prompting Guide

This guide details the integration of image, video, and audio reference files with text instructions in Seedance 2.0.

---

## Text Prompting

In a multimodal generation, text prompting functions as the steering wheel for reference files.

### Text Anchors for Multimodal Control
When you provide reference files, you must use specific text syntax to tell the model how to interpret them. Without the proper text references, the model will ignore the uploaded assets. The text prompt maps the relationship:
* `"@Image1's character as the subject"` tells the model to keep the subject's face/identity.
* `"reference @Video1's camera movement"` applies the camera motion path from the video.
* `"BGM references @Audio1"` maps the background audio file.

---

## Multimedia/Video/Image Prompting

Multimedia/video/image prompting is the core differentiator of Seedance 2.0. Instead of relying solely on text descriptions, you can feed the model up to 9 images, 3 video clips, and 3 audio files (maximum of 12 combined assets).

### The @ Reference Syntax
The model uses a specific parsing engine for `@` references:
| Reference Type | Syntax Example |
|---|---|
| First Frame | `@Image1 as the first frame` |
| Last Frame | `@Image2 as the last frame` |
| Character Outfit | `wearing the outfit from @Image2` |
| Motion Reference | `@motion` or `reference @Video1's action choreography` |

### Video-to-Video VFX & Source Lock
Seedance 2.0 allows you to modify existing footage using a text prompt. To prevent the model from morphing the subject, use a **Source Lock Header** in your prompt:
```text
@source: Original clip — preserve his identity, face, hair, wardrobe, 
expression and every gesture, and the exact handheld framing, lens and camera motion, 
unchanged throughout.
```

### Input Limits & Formats
* **Images**: Up to 9 (JPEG, PNG, WebP; max 30MB each). *Note: System blocks realistic human faces in uploaded images for safety.*
* **Videos**: Up to 3 (MP4, MOV; max 50MB, 2-15s total).
* **Audio**: Up to 3 (MP3, WAV; max 15MB each, ≤15s).

---

## External Resources & Citations
- **GitHub**: Get the specialized Claude skills for video rendering from [rediumvex/ai-video-generator-claude](https://github.com/rediumvex/ai-video-generator-claude).
- **Hugging Face**: See multi-modal spaces and web UI setups at [huggingface.co/spaces](https://huggingface.co/spaces).
- **Twitter/X**: Read video-to-video workflow breakdowns from [@theromanknox](https://x.com/theromanknox).
