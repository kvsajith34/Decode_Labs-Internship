# Audit Methodology

**Audit Framework:** GuardRail AI — Safety, Bias & Red-Team Audit Framework  
**Document Type:** Methodology Reference  
**Author:** Venkata Sai Ajith Kancheti

---

## Overview

GuardRail AI follows a structured, multi-phase audit methodology adapted from established AI safety evaluation frameworks including NIST AI RMF (Risk Management Framework), the EU AI Act high-risk system requirements, and academic red-teaming literature. The methodology is designed to produce reproducible, evidence-based findings suitable for professional portfolio documentation and real-world deployment decisions.

---

## Phase 1 — Scope Definition

Before testing begins, the audit scope is defined across three dimensions:

**Model Scope:** Which AI models are being audited and in what capacity (text generation, image generation, conversational assistant).

**Risk Domain Scope:** Which categories of harm are within scope — physical harm enablement, privacy violations, misinformation, bias and discrimination, and psychological manipulation.

**Use Case Scope:** The fictional deployment scenario (a company preparing to launch a public-facing AI assistant) grounds all test design decisions. Tests are designed to reflect realistic user interactions in that context, not purely academic adversarial scenarios.

---

## Phase 2 — Prompt Pack Design

All test prompts are designed using three core principles:

**1. Controlled variation:** For bias tests, paired prompts are constructed that are identical in every detail except the variable under test (e.g., candidate name). This isolates the variable's effect on model output.

**2. Ecological validity:** Safety test prompts are modeled on realistic user requests that a public AI assistant might plausibly receive — not implausible edge cases. This ensures findings are relevant to actual deployment risk.

**3. GitHub safety:** All prompts that could cause harm if extracted are marked `[REDACTED]` in published documentation. The test result and model behavior are recorded; the harmful prompt text is not. This aligns with responsible disclosure norms in security research.

---

## Phase 3 — Test Execution

Tests are executed using the following protocol:

**Parallel execution:** Both text models (Grok and ChatGPT) receive the same prompt within the same testing session to minimize time-gap variability.

**Fresh context:** Each audit area begins a new conversation window. Models are not allowed to "learn" from prior test responses within a session.

**Single-attempt primary recording:** The first response to each prompt is the primary data point. Follow-up interactions are recorded separately as secondary data (used in refusal consistency testing only).

**Verbatim response capture:** Response summaries paraphrase the model's output for GitHub safety. Key phrases are quoted where exact wording is critical to the finding (e.g., vocabulary differences in bias tests).

---

## Phase 4 — Scoring

Each test is scored on a **1–5 scale** defined per audit area (see `scoring_rubric.md`). Scores are assigned immediately after response capture to avoid recency bias in evaluation.

**Weighted area averages** are calculated for each model:

| Audit Area | Weight |
|------------|--------|
| Safety Boundaries | 30% |
| Bias & Fairness | 25% |
| Hallucination Risk | 25% |
| Refusal Quality | 20% |

The 30% weight on safety reflects its primacy in deployment risk: a model that enables harm is a critical failure regardless of high scores elsewhere.

Image generation bias is scored independently on the same 1–5 scale but is not included in the weighted text model average, as Gemini 3.5 Flash is evaluated as a separate component.

---

## Phase 5 — Evidence Collection

Screenshots are captured for each audit area as corroborating evidence. All screenshots are:
- Annotated with red bounding boxes highlighting the specific behavior being documented
- Named with descriptive filenames matching the test ID
- Stored in `screenshots/` without modification to the model's original output

---

## Phase 6 — Analysis & Reporting

Findings are synthesized across five deliverables:
1. Area-level result files (in `test_results/`)
2. Cross-model comparison matrix
3. Risk register mapping findings to deployment risks
4. Safety scorecard summarizing performance
5. Guardrails framework proposing mitigations

---

## Limitations of This Methodology

See `docs/limitations.md` for a full discussion. Key constraints include single-run testing per prompt, reliance on single-auditor observation, and the scope restriction to English-language prompts only.

---

## Ethical Stance

See `docs/ethical_testing_note.md` for the full ethical framework governing this audit. In summary: no harmful information was extracted or published, all red-team test prompts were designed to test refusal behavior rather than elicit harmful outputs, and all findings are reported in the spirit of improving AI safety rather than exposing exploits.
