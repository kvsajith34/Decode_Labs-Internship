# Ethical Testing Note

**Audit Framework:** GuardRail AI — Safety, Bias & Red-Team Audit Framework  
**Document Type:** Ethical Disclosure  
**Author:** Venkata Sai Ajith Kancheti

---

## Statement of Ethical Intent

This audit was conducted in the spirit of responsible AI safety research. The goal of red-teaming in this context is not to cause harm, extract dangerous information, or expose models to public ridicule — it is to identify safety weaknesses before they can affect real users in a deployment context.

Every decision in this audit's design was guided by the principle: **test safety behavior, not safety boundaries.** The question is always "does the model refuse?" — not "what happens if the model doesn't?"

---

## Prompt Handling Policy

### Redaction of Harmful Prompts

All test prompts in the `safe_red_team` category that could cause harm if extracted, copied, or repurposed have been replaced with `[REDACTED]` in all public documentation. What is recorded in the published files is:

- The **category** of the request (e.g., "dangerous medical self-treatment")
- The **intended test behavior** (e.g., "request for specific drug dosages without medical supervision")
- The **model's response** (summarized, not verbatim)
- The **score** and **auditor's finding**

The actual harmful prompt text was used only during the testing session and is not stored in any published file.

### Why Redaction Matters

Publishing red-team prompts — even in a research context — creates a reusable jailbreak resource. A reader who finds this repository should not be able to extract a ready-made collection of prompts for bypassing AI safety systems. Redaction ensures this audit is a safety contribution, not a safety liability.

---

## No Harmful Information Was Extracted

In every safety test in this audit, the test was evaluated on whether the model **refused** the request. In cases where a model produced a partial response before refusing, the partial content was noted as an audit finding (score: 2 or 3) but was not reproduced in documentation.

No medical dosage instructions, security bypass methods, personal data aggregation outputs, misinformation content, or manipulation scripts from any model response are published anywhere in this repository.

---

## Bias Testing Ethical Stance

Bias tests in this audit use real, safe prompts — but they are designed to reveal differential treatment, not to encourage it. The finding that a model treats identical profiles differently based on name is documented as a bias risk, not as a recommendation to use biased models.

The paired comparison methodology treats every demographic group with equal respect. No group is used as the "normal" baseline against which others are compared. Both prompts in each pair are equally valid; the goal is equal treatment of both.

---

## Image Audit Ethical Stance

The image generation audit documents observed demographic patterns in AI-generated images. These observations are made in a neutral, analytical tone:

- "The model generated a male-presenting figure for this role" — not "the model is sexist"
- "7 of 8 images featured light skin tones" — not "the model discriminates against dark-skinned people"

The goal is measurement and documentation, not condemnation. Training data patterns drive generation patterns — this is a systemic observation about AI development practices, not an accusation against any individual or organization.

---

## Responsible Disclosure Commitment

The findings of this audit are disclosed publicly as a portfolio and learning resource. Any specific weaknesses observed in named models are reported as audit findings in the context of this controlled test — not as vulnerabilities suitable for active exploitation.

If during testing a model produced an output that represented a previously unknown safety risk, that finding would be reported to the model provider through responsible disclosure channels before being published.

---

## Compliance with Terms of Service

All testing in this audit was conducted through publicly available interfaces (grok.com, Google AI Studio, Bing Image Creator) within the normal terms of use of each platform. No API access was used in ways that circumvent rate limits or safety systems. No automated mass testing was conducted.

---

## Summary

| Ethical Commitment | How It Was Met |
|-------------------|---------------|
| No harmful information extracted or published | All harmful prompt categories are redacted |
| No exploitation of model weaknesses | Findings are reported as audit evidence, not reusable exploits |
| Demographic groups treated with equal respect | Paired comparison methodology; neutral documentation language |
| Image findings reported analytically, not accusatorially | Neutral observation language throughout |
| Terms of service compliance | Public interfaces only; no automated bypass |
| Responsible disclosure commitment | Material safety findings would be reported to providers |
