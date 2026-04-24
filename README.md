# AI Prompt Templates

<div align="center">

![Banner](https://img.shields.io/badge/AI-Prompt%20Library-6366F1?style=for-the-badge&logo=robot&logoColor=white)
[![GitHub Stars](https://img.shields.io/github/stars/sourcecube/ai-prompt-templates?style=for-the-badge)](https://github.com/sourcecube/ai-prompt-templates/stargazers)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Contributors](https://img.shields.io/badge/Contributors-Welcome-FF6B6B?style=for-the-badge)](CONTRIBUTING.md)
[![PRs](https://img.shields.io/badge/PRs-Welcomed-59Crus?style=for-the-badge)](https://github.com/sourcecube/ai-prompt-templates/pulls)

**Production-ready AI prompt templates | FLUX · Midjourney · ComfyUI · Natural Language**

📺 [B站 Video Tutorials](https://space.bilibili.com/3546745917148074) · 🔗 [YouTube Channel](https://www.youtube.com/@SC2778)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Quick Start](#quick-start)
- [Repository Structure](#repository-structure)
- [Statistics](#statistics)
- [Prompts by Category](#prompts-by-category)
- [FLUX vs Stable Diffusion](#flux-vs-stable-diffusion)
- [ComfyUI Workflows](#comfyui-workflows)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

AI Prompt Templates is a curated collection of **production-ready** AI image generation prompts, covering FLUX, Midjourney, ComfyUI workflows, and natural language descriptions. Every prompt has been tested and includes parameter recommendations.

> ⚡ **Goal**: Make AI creation simpler — copy, paste, generate.

---

## Features

| Feature | Description |
|:--------|:------------|
| 🎯 **Ready to Use** | All prompts work out-of-the-box, no debugging needed |
| 📊 **Complete Parameters** | Steps, CFG, Sampler, resolution — fully specified |
| 🧪 **Tested & Verified** | Every prompt verified through actual generation |
| 🌐 **Bilingual** | English prompts + Chinese usage guides |
| 🔄 **Multiple Platforms** | FLUX, Midjourney, ComfyUI, Natural Language |
| 📚 **Structured** | Organized by type, style, and use case |

---

## Quick Start

### Step 1 — Choose Your Category

| What do you want to generate? | Where to look |
|:------------------------------|:--------------|
| Commercial portrait / photography | `prompts/FLUX/photorealistic/` |
| Cinematic visuals | `prompts/FLUX/cinematic/` |
| Illustration / concept art | `prompts/FLUX/illustration/` |
| Traditional Chinese style | `prompts/FLUX/illustration/` |
| Midjourney prompts | `prompts/MJ/` |
| Importable FLUX workflows | `prompts/ComfyUI/workflows/` |
| Natural language prompts | `prompts/Natural-Language/` |

### Step 2 — Copy & Use

1. Open the `.md` file for your chosen prompt
2. Copy the English text from the **Positive Prompt** section
3. Paste into FLUX / Midjourney / ComfyUI
4. Adjust settings using the **Parameter Recommendations** in the file

### Step 3 — Parameter Reference

```
FLUX General Parameters:
  Steps:    25–40
  CFG:      1.5–3.5
  Sampler:  euler_ancestral / dpmpp_2m / eigen Galois
  Resolution:
    1:1   → 1024×1024
    3:4   → 1024×1360 (portrait)
    3:2   → 1536×1024 (landscape)
    21:9  → 1792×768 (cinematic)
```

---

## Repository Structure

```
ai-prompt-templates/
├── README.md                         # This file
├── LICENSE                           # MIT License
├── CONTRIBUTING.md                   # Contribution guidelines
└── prompts/
    ├── FLUX/                         # FLUX prompts
    │   ├── FLUX-GUIDE.md            # FLUX writing guide
    │   ├── photorealistic/          # Photorealistic photography
    │   ├── cinematic/               # Cinematic visuals
    │   ├── illustration/            # Illustration & concept art
    │   └── concept-art/              # Concept art & design
    ├── MJ/                           # Midjourney prompts
    │   ├── photorealistic/
    │   └── illustration/
    ├── ComfyUI/                      # ComfyUI workflows
    │   └── workflows/
    └── Natural-Language/             # Natural language prompts
        ├── creative/
        └── technical/
```

---

## Statistics

| Type | Count | Description |
|:-----|:-----:|:------------|
| FLUX Prompts | 18 | Portrait · Landscape · Illustration · Concept Art |
| Midjourney Prompts | 4 | Curated selection |
| ComfyUI Workflows | 2 | FLUX-compatible |
| Natural Language Prompts | 6 | Creative + Technical |
| **Total** | **30** | All production-ready |

---

## Prompts by Category

### 🔥 FLUX Photorealistic

| Prompt | Use Case | Difficulty |
|:-------|:---------|:----------:|
| [Portrait Master](./prompts/FLUX/photorealistic/portrait-master.md) | Commercial photography | ⭐⭐⭐ |
| [Corporate Portrait](./prompts/FLUX/photorealistic/portrait-corporate.md) | Resume / professional photos | ⭐⭐ |
| [Passport Photo](./prompts/FLUX/photorealistic/portrait-passport.md) | Visa / ID documents | ⭐⭐ |
| [Product Render](./prompts/FLUX/photorealistic/product-render.md) | E-commerce hero images | ⭐⭐⭐ |
| [Food Photography](./prompts/FLUX/photorealistic/food-photography.md) | Culinary content | ⭐⭐⭐ |
| [Wildlife Photo](./prompts/FLUX/photorealistic/wildlife-photo.md) | Nature photography | ⭐⭐⭐ |
| [Street Night China](./prompts/FLUX/photorealistic/street-night-china.md) | Urban night scenes | ⭐⭐⭐ |
| [Fashion Tokyo](./prompts/FLUX/photorealistic/fashion-street-tokyo.md) | Street fashion | ⭐⭐⭐ |
| [Cyberpunk City](./prompts/FLUX/photorealistic/cyberpunk-city.md) | Sci-fi urban scenes | ⭐⭐⭐ |
| [Aerial Shanghai](./prompts/FLUX/photorealistic/aerial-shanghai.md) | Cityscape aerial | ⭐⭐⭐ |
| [Scandinavian Interior](./prompts/FLUX/photorealistic/interior-scandinavian.md) | Interior design | ⭐⭐ |

### 🎬 FLUX Cinematic

| Prompt | Use Case | Difficulty |
|:-------|:---------|:----------:|
| [Cinematic Portrait](./prompts/FLUX/cinematic/portrait-cinematic.md) | Short video thumbnails | ⭐⭐⭐ |
| [Mountain Epic](./prompts/FLUX/cinematic/mountain-epic.md) | Wallpapers / posters | ⭐⭐⭐⭐ |
| [Wuxia Hero](./prompts/FLUX/cinematic/wuxia-hero.md) | Chinese martial arts | ⭐⭐⭐⭐ |
| [Interstellar Ship](./prompts/FLUX/cinematic/interstellar-ship.md) | Sci-fi concept | ⭐⭐⭐⭐ |

### 🎨 FLUX Illustration & Concept Art

| Prompt | Use Case | Difficulty |
|:-------|:---------|:----------:|
| [Chinese Goddess Wuxia](./prompts/FLUX/illustration/chinese-goddess-wuxia.md) | Traditional Chinese art | ⭐⭐⭐ |
| [Dragon Knight](./prompts/FLUX/illustration/dragon-knight.md) | Game concept art | ⭐⭐⭐ |
| [Ink Landscape](./prompts/FLUX/illustration/ink-landscape.md) | Chinese aesthetics | ⭐⭐⭐ |
| [Chinese Landscape](./prompts/FLUX/illustration/chinese-landscape.md) | Landscape art | ⭐⭐⭐ |
| [Architecture Future](./prompts/FLUX/concept-art/architecture-future.md) | Futuristic architecture | ⭐⭐⭐ |
| [Mech Warrior](./prompts/FLUX/concept-art/mech-warrior.md) | Mecha design | ⭐⭐⭐ |
| [Underwater World](./prompts/FLUX/concept-art/underwater-world.md) | Fantasy environments | ⭐⭐⭐ |
| [Warriors Charge](./prompts/FLUX/concept-art/warriors-charge.md) | Battle scenes | ⭐⭐⭐⭐ |

### 🌟 Midjourney Prompts

| Prompt | Use Case | Category |
|:-------|:---------|:--------:|
| [Emotional Portrait](./prompts/MJ/photorealistic/emotional-portrait.md) | Portrait photography | photorealistic |
| [Vintage Camera](./prompts/MJ/photorealistic/vintage-camera.md) | Vintage photography | photorealistic |
| [Chinese Goddess](./prompts/MJ/illustration/chinese-goddess.md) | Traditional Chinese | illustration |
| [Fantasy Dragon](./prompts/MJ/illustration/fantasy-dragon.md) | Western fantasy | illustration |

### ⚙️ ComfyUI Workflows

| Workflow | Description |
|:---------|:------------|
| [Portrait Workflow](./prompts/ComfyUI/workflows/flux-portrait-workflow.md) | FLUX portrait with ControlNet & LoRA |
| [Cinematic Workflow](./prompts/ComfyUI/workflows/flux-cinematic-workflow.md) | FLUX cinematic with post-processing |

> **How to install**: Download the `.md` file, copy the JSON or node configuration, and import into ComfyUI.

### 📝 Natural Language Prompts

| Prompt | Use Case | Category |
|:-------|:---------|:--------:|
| [Brand Story](./prompts/Natural-Language/creative/brand-story.md) | Brand storytelling | creative |
| [Children's Book](./prompts/Natural-Language/creative/childrens-book.md) | Illustration for kids | creative |
| [Profile Avatar](./prompts/Natural-Language/creative/profile-avatar.md) | Personal avatars | creative |
| [Product Showcase](./prompts/Natural-Language/technical/product-showcase.md) | E-commerce display | technical |
| [Tech Infographic](./prompts/Natural-Language/technical/tech-infographic.md) | Tech diagrams | technical |
| [Video Thumbnail](./prompts/Natural-Language/technical/video-thumbnail.md) | YouTube / B站 thumbnails | technical |

---

## FLUX vs Stable Diffusion

FLUX uses **natural language prompts** — fundamentally different from traditional SD keyword-stacking:

| Feature | FLUX ✅ | Stable Diffusion ❌ |
|:--------|:------:|:------------------:|
| Prompt Style | Complete natural sentences | Comma-separated keywords |
| Sentence Length | Long sentences work perfectly | Degrades past 75 tokens |
| Negative Prompts | Usually not needed | Required but limited effect |
| Quality Tags | Unnecessary | `masterpiece, best quality` needed |
| Resolution Sensitivity | Low | High — wrong ratios degrade quality |

### Style Comparison

❌ **Old SD Style** (deprecated):

```
masterpiece, best quality, 1girl, blonde hair, blue eyes,
white dress, flower field, sunny, professional photography
```

✅ **FLUX Style** (recommended):

```
A young woman with blonde hair and bright blue eyes wearing a flowing white dress
stands in a field of wildflowers. Golden hour sunlight creates a warm, ethereal glow.
Shot on medium format film with soft bokeh.
```

> 💡 Want to master FLUX writing? Check out [FLUX-GUIDE.md](./prompts/FLUX/FLUX-GUIDE.md)

---

## ComfyUI Workflows

FLUX workflows ready for import into ComfyUI:

#### Portrait Workflow
- **Features**: ControlNet + LoRA + Post-processing
- **Models**: flux1-dev.safetensors + flux-controlnetPortrait-v10
- **Use case**: Commercial portrait photography

#### Cinematic Workflow
- **Features**: Enhanced color grading + upscaling
- **Models**: FLUX Dev + 4x-UltraSharp upscaler
- **Use case**: Film-style visuals, posters, backgrounds

> **Installation**: Download the `.md` file → copy the JSON configuration → paste into ComfyUI

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on:
- Quality standards
- File format specifications
- Submission process

### Quick Checklist Before Submitting

- [ ] Prompt works out-of-the-box (no debugging required)
- [ ] Includes complete parameter recommendations
- [ ] Contains effect description and clear use cases
- [ ] Uses natural language style (not keyword-stacking)
- [ ] English is grammatically correct, no garbled text
- [ ] File naming follows convention (lowercase + hyphens)

---

## Video Tutorials

| Tutorial | Platform | Status |
|:---------|:---------|:-------|
| FLUX Prompt Writing Guide | B站 | ✅ Published |
| ComfyUI FLUX Workflow Setup | B站 | ✅ Published |
| Natural Language Prompting | B站 | 🔄 In production |

---

## License

This project is licensed under the [MIT License](./LICENSE).

---

<div align="center">

⭐ If this helps you, please star the repo!

🔗 [B站主页](https://space.bilibili.com/3546745917148074) ·
[YouTube](https://www.youtube.com/@SC2778) ·
[GitHub Issues](https://github.com/sourcecube/ai-prompt-templates/issues) ·
[Pull Requests](https://github.com/sourcecube/ai-prompt-templates/pulls)

*Making AI creation simpler*

</div>