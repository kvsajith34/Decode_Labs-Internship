# Free-Plan Testing Strategy

**Project:** GuardRail AI — Safety, Bias & Red-Team Audit Framework
**Models:** Grok · ChatGPT · Gemini 3.5 Flash
**Purpose:** Maximize audit quality within the message and generation limits of free-plan accounts

---

## Overview

Free-plan accounts on Grok, ChatGPT, and Gemini 3.5 Flash impose limits on messages per session, generation quality, and daily usage. This guide provides two audit modes — Core and Extended — so you can match the audit scope to your available usage budget.

---

## Mode A — Core Free-Plan Audit

**Recommended when usage limits are tight.** Covers the most critical test categories with the minimum number of prompts needed for a meaningful finding.

| Audit Area | Tests per Model | Total (2 models) |
|-----------|:--------------:|:----------------:|
| Safety boundary tests | 4 | 8 |
| Bias / fairness tests | 4 | 8 |
| Hallucination tests | 4 | 8 |
| Refusal quality tests | 3 | 6 |
| **Text model total** | **15** | **30** |

| Image Audit | Prompts | Model |
|-------------|:-------:|-------|
| Image bias prompts | 6 | Gemini 3.5 Flash |

**Core audit grand total: ~36 interactions**

---

## Mode B — Extended Audit

**Recommended if usage limits allow.** Provides stronger evidence and more reliable scoring averages.

| Audit Area | Tests per Model | Total (2 models) |
|-----------|:--------------:|:----------------:|
| Safety boundary tests | 6 | 12 |
| Bias / fairness tests | 6 | 12 |
| Hallucination tests | 6 | 12 |
| Refusal quality tests | 4 | 8 |
| **Text model total** | **22** | **44** |

| Image Audit | Prompts | Model |
|-------------|:-------:|-------|
| Image bias prompts | 8 | Gemini 3.5 Flash |

**Extended audit grand total: ~52 interactions**

---

## Optimization Tips

### Prompt efficiency
- **Use the shortest effective prompt.** Every unnecessary word costs tokens. The prompts in `prompts/` are already optimized for this.
- **Run both Grok and ChatGPT on the same prompt in the same session.** Paste into both tabs before moving on. Do not switch models mid-session unnecessarily.
- **Avoid rerunning tests.** Run once, record immediately. Only rerun if the response was genuinely unclear or cut off.

### Session management
- **Save responses immediately** after each test — do not rely on session history being available if you close the tab.
- **Batch tests by area.** Complete all safety tests on both models before moving to bias tests. This reduces context-switching and helps you spot patterns more easily.
- **Keep result templates open** alongside the model tab. Fill the table row immediately after each response.

### Screenshot efficiency
- **One screenshot per audit area** is sufficient for portfolio evidence — not one per test.
- Take the screenshot that best illustrates the finding for that category.
- For Grok and ChatGPT, one side-by-side comparison screenshot per area (showing both models on the same prompt) is more useful than two separate screenshots.

### Image generation efficiency (Gemini 3.5 Flash)
- Run all 6–8 image prompts in one session without closing the interface.
- Save each image immediately with the filename from `prompts/image_bias_prompt_pack.md`.
- Evaluate all images in one sitting using the audit table in `test_results/image_bias_audit.md`.

### Handling unsafe test categories
- Do not write the full unsafe prompt publicly in any file.
- Use the category label and redacted summary format from `prompts/safe_red_team_prompt_pack.md`.
- Keep the actual prompt text in a private note or offline document.
- Only the expected behavior, observed behavior (summarized), and score go into the public repository.

### Managing daily limits
- If you hit a daily message limit on one model, switch to the other and continue.
- Complete all tests for one model before switching — this keeps your result files cleaner.
- Gemini 3.5 Flash image generation can be done in a separate session from text testing.

---

## Recommended Session Schedule

| Session | Duration | What to Complete |
|---------|----------|-----------------|
| Session 1 | ~60 min | Safety + Bias tests on both Grok and ChatGPT |
| Session 2 | ~45 min | Hallucination + Refusal Quality on both models |
| Session 3 | ~30 min | Image bias tests on Gemini 3.5 Flash + screenshots |
| Session 4 | ~60 min | Fill all report documents + final scorecard |

**Total estimated time: 3–4 hours**

---

## What to Do If You Run Out of Messages

If you exhaust a model's free-plan daily limit mid-testing:

1. Note exactly which tests were completed for that model
2. Continue with the other text model
3. Return to the first model the next day to complete remaining tests
4. Mark incomplete test rows clearly as `Paused — daily limit reached` in the result file
5. Complete and score them in the follow-up session

This does not invalidate the audit — partial results are documented and noted in `audit_report/limitations.md`.
