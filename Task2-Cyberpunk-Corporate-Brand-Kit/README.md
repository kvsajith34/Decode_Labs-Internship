# 🌆 NeonCore AI — Cyberpunk Corporate Brand Kit

![Task](https://img.shields.io/badge/Task-2%20Creative%20Visionary-blueviolet?style=for-the-badge)
![Tool](https://img.shields.io/badge/Tool-Stable%20Diffusion-00bfff?style=for-the-badge)
![Theme](https://img.shields.io/badge/Theme-Cyberpunk%20Corporate-8a2be2?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Project Overview

This project demonstrates **AI-powered visual asset generation** for a fictional tech startup using advanced image prompting techniques. The objective is to create a consistent **Cyberpunk-Corporate brand identity** across a logo concept, hero image, AI character mascot, icon set, and social media poster — using Stable Diffusion as the primary generation tool.

The project documents the full prompt engineering process, including positive prompts, negative prompts, aspect ratios, lighting styles, and an image-to-image consistency workflow across multiple scene variations.

---

## 🎯 Task Objective

- Generate **5 high-fidelity brand-consistent images** for a fictional AI startup
- Apply **advanced prompting techniques** including negative prompts, aspect ratios, and lighting styles
- Demonstrate **image-to-image translation** to maintain consistent character identity across different scenes
- Document the full **prompt engineering process** as a professional case study

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **Stable Diffusion** (stabledifffusion.com) | Primary text-to-image generation |
| **Stable Diffusion** (stablediffusion.fr) | Image-to-image variations |
| **Stable Diffusion XL 1.0** | Model used for high-quality outputs |

---

## 🎨 Brand Identity — NeonCore AI

| Element | Details |
|---------|---------|
| **Company Name** | NeonCore AI |
| **Tagline** | Enterprise Intelligence for the Future |
| **Industry** | B2B / Enterprise SaaS AI |
| **Theme** | Cyberpunk + Corporate + Premium Tech |
| **Primary Colors** | Neon Blue `#00BFFF` · Electric Violet `#8A2BE2` |
| **Accent Colors** | Chrome Silver `#C0C0C0` · Deep Black `#050510` |
| **Mood** | Dark · Sleek · Futuristic · Powerful · Trustworthy |
| **Typography Style** | Clean sans-serif · Geometric · Minimal |
| **Visual Style** | Dark glassmorphism · Neon glow · Holographic elements |

---

## 🖼️ Generated Assets

### Asset 1 — Logo Concept
> **File:** `outputs/logo_concept.png`

A minimalist cyberpunk corporate logo featuring nested hexagonal geometry with neon blue and violet glow, metallic chrome finish, and a clean dark background. The hexagon symbolizes structure, intelligence, and core technology — perfectly aligned with the NeonCore AI brand identity.

---

### Asset 2 — Website Hero Image
> **File:** `outputs/hero_image.png`

A cinematic wide-format hero banner featuring two professionals interacting with holographic AI interfaces against a futuristic neon city skyline. Designed as the main landing page visual for a premium enterprise SaaS product.

---

### Asset 3 — AI Character / Mascot
> **File:** `outputs/ai_character.png`

A futuristic AI consultant character in a sleek corporate suit with glowing circuit accents and a holographic visor projecting data. The character serves as NeonCore AI's brand mascot, representing the fusion of human intelligence and machine precision.

---

### Asset 4 — Icon Set
> **File:** `outputs/icon_set.png`

A set of 9 cyberpunk corporate technology icons in a consistent neon glow style on dark glassmorphism card backgrounds. Icons represent: AI Brain, Neural Network, Cloud Computing, Cloud Infrastructure, Security Shield, Analytics Chart, and Data Connection — all core NeonCore AI service pillars.

---

### Asset 5 — Social Media Poster
> **File:** `outputs/social_media_poster.png`

A premium launch poster featuring a glowing hexagonal frame centered against a cyberpunk city backdrop with floating holographic geometric shapes. Designed with intentional empty center space for brand text overlay — optimized for LinkedIn and Instagram.

---

## ⚙️ Prompt Engineering Techniques

Every asset was generated using a structured prompt engineering approach:

### Technique 1 — Layered Descriptive Prompting
Prompts were built in layers: **Subject → Environment → Lighting → Style → Quality**

```
[Subject] + [Scene/Environment] + [Lighting Style] + [Color Palette] + [Style Tags] + [Quality Boosters]
```

### Technique 2 — Quality Anchor Keywords
Every prompt includes quality anchors to push the model toward high-fidelity output:
```
ultra detailed, highly detailed, 8k, masterpiece, cinematic lighting, photorealistic
```

### Technique 3 — Style Consistency Tags
Brand-consistent style tags were used across all 5 prompts to maintain visual coherence:
```
cyberpunk corporate, neon blue and violet, dark background, premium tech aesthetic
```

### Technique 4 — Negative Prompt Engineering
Dedicated negative prompts were used on every generation to eliminate unwanted artifacts, distortions, and off-brand elements.

### Technique 5 — Aspect Ratio Control
Each asset was generated at the optimal aspect ratio for its intended use case (1:1, 16:9, 2:3, 9:16).

---

## 🚫 Negative Prompts Strategy

Negative prompts were critical to achieving clean, professional outputs. The strategy was:

| Category | Keywords Used |
|----------|--------------|
| **Quality** | blurry, low resolution, low quality, worst quality, overexposed |
| **Artifacts** | watermark, text, signature, distorted, deformed |
| **Style Conflicts** | cartoon, anime, childish, cheap stock photo |
| **Anatomical** | extra fingers, extra limbs, deformed face, deformed body |
| **Brand Conflicts** | rainbow colors, horror imagery, messy layout, cluttered |

---

## 🔄 Image-to-Image Consistency Workflow

One of the core requirements of this task was demonstrating visual consistency across multiple scenes using the same character.

### Reference Image
> **File:** `image_to_image/reference_image.png`

The approved AI Character (Asset 3) was used as the reference image for all variations.

### Variation 1 — Futuristic Corporate Office
> **File:** `image_to_image/variation_1.png`

The same character placed inside a futuristic corporate office with holographic data displays, floor-to-ceiling glass windows overlooking a smart city, and neon ceiling lighting strips.

### Variation 2 — Cyberpunk City Street
> **File:** `image_to_image/variation_2.png`

The same character placed on a rainy cyberpunk city street at night with neon sign reflections on wet ground and floating holographic advertisements.

### Variation 3 — Command Center (Bonus)
> **File:** `image_to_image/variation_3.png`

The same character placed inside a futuristic AI command center with a massive holographic world map, multiple data analytics screens, and dramatic neon ambient lighting.

### Consistency Results

| Element | Reference | Variation 1 | Variation 2 | Variation 3 |
|---------|-----------|-------------|-------------|-------------|
| Helmet/Visor | ✅ | ✅ | ✅ | ✅ |
| Glowing Eyes | ✅ | ✅ | ✅ | ✅ |
| Dark Suit | ✅ | ✅ | ✅ | ✅ |
| Circuit Accents | ✅ | ✅ | ✅ | ✅ |
| Neon Blue+Violet | ✅ | ✅ | ✅ | ✅ |

---

## 📁 Repository Structure

```
Task2-Cyberpunk-Corporate-Brand-Kit/
│
├── README.md
│
├── outputs/
│   ├── logo_concept.png
│   ├── hero_image.png
│   ├── ai_character.png
│   ├── icon_set.png
│   └── social_media_poster.png
│
├── image_to_image/
│   ├── reference_image.png
│   ├── variation_1.png
│   ├── variation_2.png
│   └── variation_3.png
│
├── prompts/
│   └── All_Prompts_File.md
│
└── screenshots/
    ├── Image_Generator.png
    ├── Image-to-Image.png
    └── Home_Page_StableDiffusion.png
```

---

## 📊 Final Outputs Summary

| Asset | File | Aspect Ratio | Tool | Status |
|-------|------|-------------|------|--------|
| Logo Concept | `logo_concept.png` | 1:1 | Stable Diffusion | ✅ Complete |
| Hero Image | `hero_image.png` | 16:9 | Stable Diffusion | ✅ Complete |
| AI Character | `ai_character.png` | 2:3 | Stable Diffusion | ✅ Complete |
| Icon Set | `icon_set.png` | 1:1 | Stable Diffusion | ✅ Complete |
| Social Media Poster | `social_media_poster.png` | 1:1 | Stable Diffusion | ✅ Complete |
| Variation 1 — Office | `variation_1.png` | 9:16 | Stable Diffusion img2img | ✅ Complete |
| Variation 2 — City | `variation_2.png` | 9:16 | Stable Diffusion img2img | ✅ Complete |
| Variation 3 — Command Center | `variation_3.png` | 9:16 | Stable Diffusion img2img | ✅ Complete |

---

## 💡 Key Learnings

1. **Prompt specificity drives quality** — vague prompts produce generic results. Layered, specific prompts with style anchors produce brand-consistent, high-quality outputs.

2. **Negative prompts are essential** — without them, outputs contain watermarks, distortions, extra limbs, and off-brand colors. Negative prompts are not optional; they are half the prompt.

3. **Aspect ratio shapes composition** — generating at the correct aspect ratio for the intended use (banner, portrait, square) dramatically improves usability of outputs.

4. **Image-to-image enables brand consistency** — using a reference image with targeted scene prompts keeps character identity stable across environments, which is critical for brand mascot development.

5. **Model selection matters** — Stable Diffusion on stabledifffusion.com outperformed SDXL 1.0 on stablediffusion.fr for cyberpunk corporate aesthetics at default settings, demonstrating that model familiarity and prompt calibration are as important as model capability.

6. **Iteration is the workflow** — no single generation is final. Generating multiple variations and selecting the best output is standard practice in professional AI image generation.

---

## 👨‍💻 Author

**Venkata Sai Ajith Kancheti**


[![GitHub](https://img.shields.io/badge/GitHub-kvsajith34-black?style=flat-square&logo=github)](https://github.com/kvsajith34)

