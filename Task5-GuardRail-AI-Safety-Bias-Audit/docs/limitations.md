# Limitations

**Audit Framework:** GuardRail AI — Safety, Bias & Red-Team Audit Framework  
**Document Type:** Limitations Disclosure  
**Author:** Venkata Sai Ajith Kancheti

---

## Overview

Every audit has constraints. Acknowledging limitations is not a weakness — it is a mark of intellectual honesty and professional credibility. This document describes the known limitations of the GuardRail AI audit, explains why they exist, and notes how they affect the interpretation of findings.

---

## Limitation 1 — Single-Run Testing

**What it means:** Each test prompt was submitted to each model once. AI models are stochastic — the same prompt submitted twice may produce different responses.

**Why it matters:** A model that scores 4 on a safety test might score 3 or 5 on a second run of the same prompt. Single-run results are data points, not statistical certainties.

**Impact on findings:** Low to medium. For clear pass/fail cases (model refused completely, or model complied completely), single-run results are reliable. For borderline cases (partial refusals, hedged responses), the score represents one observed behavior, not guaranteed reproducible behavior.

**Mitigation in this audit:** The refusal consistency test (R-04) partially addresses this by testing behavior across three follow-up messages. Any test that produced a borderline score is noted in the auditor observations column.

---

## Limitation 2 — Single Auditor

**What it means:** All test scores were assigned by one auditor (the author). Bias testing especially benefits from multiple independent scorers to reduce evaluator bias.

**Why it matters:** Vocabulary differences in bias tests (e.g., "confident" vs "assertive") may be assessed differently by different readers. One auditor's perception of a tone difference may not be shared by all readers.

**Impact on findings:** Medium for bias tests. Low for safety tests (pass/fail is largely objective) and hallucination tests (fabrication is verifiable).

**Mitigation in this audit:** Score criteria are defined explicitly per rubric level, reducing subjectivity. All observations include quoted or paraphrased response text so readers can assess the scoring independently.

---

## Limitation 3 — English-Language Prompts Only

**What it means:** All 30 test prompts were written in English. Model safety and bias behavior may differ substantially in other languages.

**Why it matters:** Some AI models have stronger safety training in English than in other languages. A model that refuses a harmful request in English may comply with the same request in Hindi, Telugu, or another language.

**Impact on findings:** High for any deployment targeting multilingual users. The findings of this audit apply only to English-language usage.

**Mitigation:** For a multilingual deployment, the audit would need to be extended to all supported languages. This is noted as a recommendation in `audit_report/final_recommendations.md`.

---

## Limitation 4 — Public Interface Testing Only

**What it means:** All models were tested through their publicly accessible chat interfaces. Enterprise API deployments with custom system prompts, fine-tuning, or output filters may behave differently.

**Why it matters:** Organizations deploying these models through the API typically add safety layers that are not present in the public chat interface. Conversely, some API deployments remove default safety features.

**Impact on findings:** The findings represent baseline model behavior. A customized deployment may be safer or less safe than the scores here suggest, depending on the operator's configuration.

---

## Limitation 5 — Snapshot in Time

**What it means:** AI models are updated continuously by their providers. The Grok tested today may behave differently after an update.

**Why it matters:** A finding of "strong jailbreak resistance" today may not hold after the next model update — in either direction (safety could improve or regress).

**Impact on findings:** This audit represents a snapshot. It is not a permanent certification of safety.

**Mitigation:** This is why a quarterly re-audit cadence is recommended in the guardrails framework. Periodic re-testing against the same test suite is the only way to detect behavioral drift over time.

---

## Limitation 6 — Scope Restricted to Five Audit Areas

**What it means:** This audit covers safety boundaries, bias, image bias, hallucination, and refusal quality. It does not cover: privacy compliance (GDPR, DPDPA), adversarial robustness (prompt injection attacks), copyright compliance, carbon footprint, or accessibility.

**Why it matters:** A complete AI deployment risk assessment would cover all of these areas. This audit addresses the five areas most directly relevant to user safety and fairness in a public assistant context.

**Impact on findings:** Findings are comprehensive within their scope but should not be treated as a complete AI governance assessment.

---

## Summary Table

| Limitation | Severity | Affects | Mitigation |
|-----------|---------|---------|-----------|
| Single-run testing | Medium | Borderline scores | Noted in observations; R-04 tests consistency |
| Single auditor | Medium | Bias scoring | Explicit rubrics; quoted response text |
| English only | High (for multilingual use) | All findings | Multi-language extension needed for global deployment |
| Public interface only | Medium | All findings | API behavior may differ; test in deployment context |
| Snapshot in time | High (long term) | All findings | Quarterly re-audit cadence recommended |
| Restricted scope | Low (within stated scope) | Completeness | Scope clearly defined; full governance review recommended |
