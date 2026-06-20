# 🧠 Decode Labs — Generative AI Internship

> A Set of Generative AI projects built during the Decode Labs internship program, spanning full-stack AI applications, prompt engineering, visual asset generation, document intelligence, multimodal content automation, and AI safety auditing.

---

## Overview

This repository documents the end-to-end work completed during the **Generative AI Internship at Decode Labs**. Each task is a standalone, portfolio-ready project demonstrating practical skills across the Generative AI stack — from full-stack application development and advanced prompting to AI safety evaluation and visual brand generation.

All five tasks were completed independently, documented professionally, and structured for recruiter and evaluator review.

---

## Internship Focus

| Area | Coverage |
|---|---|
| **Full-Stack AI Applications** | React + FastAPI + multi-provider LLM integration |
| **Generative Image AI** | Stable Diffusion prompt engineering and brand identity |
| **RAG & Document Intelligence** | Claude Projects-based retrieval and structured extraction |
| **Multimodal Content Automation** | Whisper transcription + heuristic scoring + Streamlit |
| **AI Safety & Ethics** | Red-team testing, bias auditing, hallucination evaluation |

---

## Repository Structure

```text
Decode_Labs-Internship/
│
├── Task1-Luxury-ai-travel-planner/          ← Full-stack LLM travel concierge app
│   ├── frontend/                            ← React 19 + TypeScript + Vite + Tailwind
│   ├── backend/                             ← FastAPI + multi-provider AI routing
│   ├── .docs/                               ← System prompts, few-shot examples, test cases
│   └── README.md
│
├── Task2-Cyberpunk-Corporate-Brand-Kit/     ← AI visual brand identity (Stable Diffusion)
│   ├── outputs/                             ← Generated brand assets (5 images)
│   ├── prompts/                             ← Positive/negative prompts per asset
│   └── README.md
│
├── Task3-ClauseWise-AI-RAG-Document-Intelligence/  ← RAG document analysis system
│   ├── claude_project/                      ← System prompt, setup, knowledge files
│   ├── docs/                                ← Workflow, limitations, reflection, testing
│   ├── outputs/                             ← Dashboard, risks, dates, stakeholders, Q&A
│   ├── prompts/                             ← Prompt pack + hallucination test prompts
│   ├── sample_documents/                    ← Source PDF (World Bank CMO April 2026)
│   └── README.md
│
├── Task4-ViralClip-AI-Multimodal-Content-Engine/   ← Video-to-reel AI pipeline (Streamlit)
│   ├── app/                                 ← Streamlit application source
│   ├── outputs/                             ← Sample reel packages (MD, JSON, SRT)
│   └── README.md
│
└── Task5-GuardRail-AI-Safety-Bias-Audit/   ← AI safety red-team audit framework
    ├── audit_results/                       ← Scored test results per model
    ├── reports/                             ← Risk register, deployment verdicts
    ├── screenshots/                         ← Evidence screenshots
    └── README.md
```

---
## Completed Projects

| Task   | Project Name                             | Focus Area                                                      | Key Deliverables                                                                                                             |    Status   |
| ------ | ---------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | :---------: |
| Task 1 | Luxury AI Travel Planner                 | AI chatbot, prompt engineering, travel personalization          | Luxury travel consultant persona, AI chat interface, structured travel planning workflow, screenshots, documentation         | ✅ Completed |
| Task 2 | Cyberpunk Corporate Brand Kit            | AI image generation, branding, visual design                    | Brand identity assets, AI-generated visuals, prompt documentation, style guide, final reflection                             | ✅ Completed |
| Task 3 | ClauseWise AI RAG Document Intelligence  | Retrieval-Augmented Generation, document Q&A, citations         | RAG workflow, cited Q&A examples, hallucination testing, risk extraction, stakeholder/date analysis                          | ✅ Completed |
| Task 4 | ViralClip AI Multimodal Content Engine   | Multimodal AI, transcript analysis, short-form content planning | Transcript outputs, viral segment detection, captions, hashtags, B-roll prompts, workflow documentation                      | ✅ Completed |
| Task 5 | GuardRail AI Safety Bias Audit Framework | AI safety, bias testing, red-team evaluation                    | Safety tests, bias audit, hallucination tests, refusal-quality analysis, image-bias audit, scorecards, final recommendations | ✅ Completed |

---

## Internship Focus

| Area                               | Description                                                                                                   |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Generative AI Applications         | Built practical AI-powered systems using prompts, chatbots, multimodal workflows, and content generation.     |
| Prompt Engineering                 | Designed structured prompts for personas, brand generation, document intelligence, and safety testing.        |
| AI Safety & Evaluation             | Tested AI systems for safety boundaries, bias, hallucination risk, refusal quality, and image representation. |
| RAG & Document Intelligence        | Created document-based intelligence workflows with citation-focused outputs and hallucination controls.       |
| Multimodal AI                      | Worked with text, image, transcript, and video-planning workflows for AI content generation.                  |
| Documentation & Portfolio Building | Prepared professional README files, reports, testing evidence, screenshots, and final reflections.            |

---

## Project Highlights

### Task 1 — Luxy Travel Persona
A production-grade AI luxury travel concierge with a React 19 + TypeScript frontend and a FastAPI backend.

- Supports **Anthropic Claude**, **Google Gemini**, and a fully offline **demo mode** — no API keys required to run
- Features a refined dark-gold UI (`#0A0A0A` + `#C9A84C`) with Framer Motion animations and glass-morphism components
- Implements responsible AI patterns: ethical refusal logic, difficult-user handling, and CORS-secured API routing
- Includes a `.docs/` directory with system prompt documentation, few-shot examples, and before/after prompt comparisons

### Task 2 — NeonCore AI Cyberpunk Brand Kit
A professional AI-powered visual identity project using Stable Diffusion XL to generate five brand-consistent assets for a fictional enterprise AI startup.

- Documented **positive and negative prompt engineering** for each of five distinct asset types
- Applied **image-to-image translation** to maintain mascot identity consistency across multiple scenes
- Brand palette: Neon Blue `#00BFFF` + Electric Violet `#8A2BE2` with dark glassmorphism visual language
- Delivered as a professional case study — not just outputs, but the full prompting process

### Task 3 — ClauseWise AI (RAG Document Intelligence)
A Claude Projects-based document intelligence system that simulates a RAG pipeline to analyze a real 69-page World Bank economic report.

- Extracted **18 categorized risks** (High/Medium/Low), **35 dates and timeline entries**, and **62+ stakeholders**
- Built hallucination-resistant prompts with mandatory source citations and unsupported-question refusal behavior
- Produced a full 9-section **Document Intelligence Dashboard** covering forecasts for 15+ commodities
- Included quality assurance testing report and a full prompt pack for reproducibility

### Task 4 — ViralClip AI
An end-to-end video analysis pipeline that turns long-form content into platform-ready short-form reel packages.

- 7-dimensional heuristic scoring engine (hook strength, emotional intensity, shareability, and more) to identify top 5 viral moments
- Outputs complete packages per reel: hook, headline, captions, hashtags, B-roll prompts, Runway ML-ready prompts, and `.srt` subtitle files
- Clean Streamlit dashboard with one-click processing and a demo mode that runs without Whisper or FFmpeg installed
- Exports in **Markdown**, **JSON**, and **SRT** formats simultaneously

### Task 5 — GuardRail AI
A structured AI safety red-team audit framework evaluating Grok, ChatGPT, and Gemini 3.5 Flash across five risk dimensions.

- **30+ tests** conducted across safety boundaries, bias/fairness, hallucination risk, and refusal quality
- **Critical finding:** Grok generated a fake official certificate (S-03) — a guardrail failure that ChatGPT handled correctly
- **Notable positive:** Both text models scored **5.00 / 5** in bias & fairness across completed paired evaluations
- Overall audit framework score: **4.51 / 5** · Risk level: **Low-Medium**
- Delivered scored results, a risk register, and deployment verdicts for all three models

---

## Tools & Technologies

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-3178c6?style=flat-square&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776ab?style=flat-square&logo=python&logoColor=white)

**Frameworks & Libraries**

| Category              | Tools / Technologies                                                     |
| --------------------- | ------------------------------------------------------------------------ |
| AI Models & Platforms | Claude, ChatGPT, Grok, Gemini, Runway, Wispr AI                          |
| Frontend              | React, Vite, HTML, CSS, JavaScript                                       |
| Backend               | Python, FastAPI                                                          |
| AI Workflows          | Prompt engineering, RAG, multimodal content generation, red-team testing |
| Documentation         | Markdown, GitHub README, audit reports, testing reports                  |
| Design & Media        | AI image generation, brand kit creation, visual prompt design            |
| Version Control       | Git, GitHub                                                              |

---

## Skills Demonstrated

- **Prompt Engineering** — System prompts, few-shot examples, negative prompts, hallucination-resistant instruction design
- **Full-Stack Development** — React + TypeScript + FastAPI end-to-end application architecture
- **RAG Workflows** — Document ingestion, structured extraction, citation-grounded output generation
- **Multimodal AI** — Audio transcription, segment scoring, and cross-format content generation
- **AI Safety Evaluation** — Red-team testing, bias auditing, refusal quality scoring, deployment risk assessment
- **Generative Image AI** — Text-to-image and image-to-image workflows with consistent brand identity
- **Technical Documentation** — README authoring, workflow reports, prompt case studies, test documentation

---

## Key Learning Outcomes

- Designed and shipped **five distinct Generative AI project types** across a single internship
- Learned to build **responsible AI applications** — including ethical refusal logic, CORS security, and demo fallbacks that work without live API keys
- Applied structured **prompt engineering** in both conversational (RAG, concierge) and generative (image, content) contexts
- Conducted a real **AI safety red-team audit** with scored findings, formal risk registers, and deployment recommendations
- Developed professional documentation practices across all five tasks — READMEs, prompt packs, test reports, and workflow guides

---

## Final Reflection

This internship provided direct, hands-on experience building with the current Generative AI stack — not studying it, but shipping with it. Each task was designed to challenge a different skill area, and the progression from a full-stack LLM application (Task 1) through brand generation (Task 2), document intelligence (Task 3), content automation (Task 4), and AI safety evaluation (Task 5) reflects the full breadth of what Generative AI practice currently demands.

The projects are production-ready in architecture and documentation — not academic exercises. They are intended as evidence of applied capability.

---

## Author

**Venkata Sai Ajith Kancheti**

GitHub: [kvsajith34](https://github.com/kvsajith34)
