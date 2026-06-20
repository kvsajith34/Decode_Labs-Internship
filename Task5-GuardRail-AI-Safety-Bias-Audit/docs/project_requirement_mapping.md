# Project Requirement Mapping

**Project:** GuardRail AI — Safety, Bias & Red-Team Audit Framework
**Models:** Grok · ChatGPT · Gemini 3.5 Flash
**Document Type:** Requirement Traceability Matrix — Completed
**Author:** Venkata Sai Ajith Kancheti

---

## Core Requirement Mapping

| Project Requirement | Implementation | Status |
|--------------------|---------------|--------|
| Text model safety testing | Grok and ChatGPT — 6 tests each (`test_results/safety_test_results.md`) | ✅ Complete |
| Bias / fairness testing | 3 paired comparisons × 2 models (`test_results/bias_test_results.md`) | ✅ Complete |
| Hallucination testing | H-01 to H-04 × 2 models (`test_results/hallucination_test_results.md`) | ✅ Complete (Core) |
| Refusal quality evaluation | R-01 to R-04 × 2 models (`test_results/refusal_quality_results.md`) | ✅ Complete |
| Image bias audit | 8 prompts — Gemini 3.5 Flash (`test_results/image_bias_audit.md`) | ✅ Complete |
| Model comparison | Grok vs ChatGPT (`test_framework/model_comparison_matrix.md`) | ✅ Complete |
| Guardrails proposal | 5-layer framework (`test_framework/guardrails_framework.md`) | ✅ Complete |
| Evidence collection | Screenshots in organized subfolders (`screenshots/`) | ✅ Complete |
| Risk scoring system | 1–5 rubric, 7 dimensions (`test_framework/scoring_rubric.md`) | ✅ Complete |
| Risk register | 13 risks rated (`audit_report/risk_register.md`) | ✅ Complete |
| Executive summary | Findings documented (`audit_report/executive_summary.md`) | ✅ Complete |
| Full audit report | All 12 sections filled (`audit_report/full_ai_audit_report.md`) | ✅ Complete |
| Safety scorecard | All scores recorded (`audit_report/safety_scorecard.md`) | ✅ Complete |
| Final recommendations | Prioritized actions (`audit_report/final_recommendations.md`) | ✅ Complete |
| Free-plan optimization | Strategy documented (`docs/free_plan_testing_strategy.md`) | ✅ Complete |
| Ethical disclosure | Responsible testing note (`docs/ethical_testing_note.md`) | ✅ Complete |
| Project reflection | Personal reflection (`docs/final_reflection.md`) | ✅ Complete |
| Public portfolio README | Project README (`README.md`) | ✅ Complete |

---

## Evidence Gap Note

| Gap | Detail | Action Required |
|-----|--------|----------------|
| H-05, H-06 not executed | Core Free-Plan Audit only ran H-01 to H-04 | Execute in extended audit if usage allows |
