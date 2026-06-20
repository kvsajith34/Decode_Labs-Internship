# Guardrails Generation Prompt

**Project:** GuardRail AI — Safety, Bias & Red-Team Audit Framework
**Purpose:** Documents the meta-prompt used to generate the guardrails framework using an AI model after test results are collected
**Models Referenced:** Grok · ChatGPT · Gemini 3.5 Flash
**Output File:** `test_framework/guardrails_framework.md`
**Author:** Venkata Sai Ajith Kancheti

---

## About This File

This document shows the prompt engineering approach used to generate the initial guardrails framework. Use this prompt in either Grok or ChatGPT after completing all test results — fill in the `[FINDINGS SUMMARY]` section with your actual scores and observations first.

This demonstrates prompt engineering as a professional skill: using structured context injection, role framing, and explicit output specification to generate consulting-grade deliverables.

---

## Master Guardrails Generation Prompt

> Replace all `[placeholder]` fields with your actual test results before running.

```
You are a Senior AI Safety Engineer producing a professional guardrails framework 
for a company planning to deploy a public-facing AI assistant. You have just 
completed a safety, bias, hallucination, and refusal quality audit of two candidate 
AI models (Grok and ChatGPT) and an image generation model (Gemini 3.5 Flash).

Based on the audit findings below, produce a detailed, professional Guardrails 
Framework document in Markdown format.

## Audit Findings Summary

Text Model Testing (Grok and ChatGPT):

Safety Boundary Results:
- Grok safety area average: [X]/5
- ChatGPT safety area average: [X]/5
- Key failure points: [describe any tests scoring below 4]
- Jailbreak resistance: [note S-06 result]

Bias and Fairness Results:
- Grok bias area average: [X]/5
- ChatGPT bias area average: [X]/5
- Key bias patterns: [describe findings from B1 to B3]

Hallucination Risk Results:
- Grok hallucination area average: [X]/5
- ChatGPT hallucination area average: [X]/5
- Most common failure: [describe — fabricated citations / statistics / events]

Refusal Quality Results:
- Grok refusal quality average: [X]/5
- ChatGPT refusal quality average: [X]/5
- Weaknesses noted: [describe any partial compliances or poor tone]

Image Generation Audit (Gemini 3.5 Flash):
- Image bias score: [X]/5
- Dominant representation pattern: [describe gender/skin tone distribution]
- Roles with strongest stereotyping: [list]

## Your Task

Produce a Guardrails Framework with these exact sections:

1. Executive Purpose — Why guardrails are necessary for this deployment (2 paragraphs)
2. Layer 1 — Input Filtering
3. Layer 2 — System Prompt and Context Hardening
4. Layer 3 — Output Review
5. Layer 4 — Human-in-the-Loop Triggers
6. Layer 5 — Monitoring and Continuous Audit
7. Bias Mitigation Specifics — Based on findings from Grok and ChatGPT
8. Image Generation Guardrails — Based on Gemini 3.5 Flash findings
9. Implementation Priority Matrix — Table: guardrail, priority (Critical/High/Medium), effort (Low/Medium/High)
10. Success Metrics — Measurable KPIs confirming the guardrails are working

Write in professional consulting language. Use tables where appropriate. 
Reference Grok, ChatGPT, and Gemini 3.5 Flash specifically in the bias 
mitigation and image sections.
```

---

## How to Use This Prompt

1. Complete all 30+ tests across all audit areas
2. Fill in every `[placeholder]` with your real scores and observations
3. Run in Grok or ChatGPT
4. Copy the output into `test_framework/guardrails_framework.md`
5. Review and update any sections that need adjustment based on your specific findings

---

## Prompt Engineering Techniques Used

| Technique | Application |
|-----------|-------------|
| Role assignment | "You are a Senior AI Safety Engineer" — establishes expert persona |
| Context injection | `[FINDINGS SUMMARY]` section provides structured audit data |
| Output specification | Numbered sections with exact names prevent the model from improvising structure |
| Format directives | "use tables where appropriate", "professional consulting language" |
| Model specificity | Instructs the model to reference Grok, ChatGPT, and Gemini 3.5 Flash by name |
