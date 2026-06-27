---
title: "Human-AI Synergy"
aliases: ["Human-AI Synergy"]
type: concept
tags: [human-ai-collaboration, synergy, augmentation, decision-making, meta-analysis]
created: 2026-06-22
updated: 2026-06-22
sources: [2024-12-vaccaro-human-ai-meta-analysis]
---

# Human-AI Synergy

The question of when combining humans and AI produces better outcomes than either alone.

---

## Key Distinctions

| Term | Definition | Baseline |
|------|------------|----------|
| **Human-AI Synergy** | Human–AI group beats *both* human alone *and* AI alone | max(human, AI) |
| **Human Augmentation** | Human–AI group beats human alone | human alone |

> [!important]
> Synergy is the stronger, more practically relevant bar. If you just want the best outcome and can choose freely, you'd use whichever single agent performs better — so only synergy justifies the overhead of combining them.

Human augmentation is still meaningful when full automation is impossible for legal, ethical, or safety reasons (e.g., medical decisions requiring human sign-off).

---

## What the Evidence Shows

From [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]] (meta-analysis of 106 experiments, 370 effect sizes, 2020–2023):

- **Average synergy**: g = −0.23 (negative — human–AI *worse* than best-alone on average)
- **Average augmentation**: g = +0.64 (positive — human–AI better than humans alone)
- High heterogeneity (I² ≈ 98%) — the average masks important variation by context

---

## Moderators of Synergy

### Task Type (strongest design-level moderator)
- **Decision tasks** (choose among options): g = −0.27 — losses; 85% of the literature
- **Creation tasks** (open-ended output): g = +0.19 — gains; only ~10% of the literature

**Why creation tasks work better**: Creative tasks often have a high-value insight component (humans) + large routine generation component (AI). Decision tasks typically have both agents completing the whole task, with humans making the final call — a setup that doesn't exploit complementarity.

### Relative Performance (strongest empirical moderator)
- **When human > AI alone**: synergy g = +0.46 (significant)
- **When AI > human alone**: synergy g = −0.54 (significant)

**Mechanism hypothesis**: When humans are generally better than the AI, they are also better calibrated at knowing *when* to trust the AI versus their own judgment. When AI is better, humans are poor judges of when to defer, creating drag on AI performance.

### Non-Significant Moderators (surprising)
These factors received heavy research attention but do not significantly affect synergy:
- AI explanation provided
- AI confidence score displayed
- Expert vs. non-expert participants
- Division of labour (too few studies to detect)

> [!warning]
> The null result for explanations and confidence is controversial — it contradicts much XAI (Explainable AI) research intuition and may reflect study design issues or the narrow accuracy metric used.

---

## Conditions for Achieving Synergy

Synergy requires three things (Donahue et al. 2022):
1. Humans are better at *some* subtasks
2. AI is better at *other* subtasks
3. The system correctly allocates subtasks to whichever partner is best

Most current human–AI systems violate (3): they present the whole task to both, with humans making the final call. Predetermined subtask delegation is rare in the literature (only 3 of 106+ experiments) but shows early positive signals.

---

## Implications for System Design

- **Favor creation/generative tasks** for human–AI collaboration — most promising for synergy
- **Check relative capability first** — deploying AI where it underperforms humans risks no synergy even if augmentation seems positive
- **Design task decomposition** — split the task so AI handles components where it clearly dominates
- **Don't rely on explanations alone** — adding AI explanations without task redesign doesn't reliably improve outcomes

---

## Related Pages
- [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]] — meta-analysis source
- [[Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021]] — mechanism: models capture know-what but not know-how → [[AI Ground Truth]]
- [[Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025]] — proposes role separation as solution to assistive AI failure → [[AI-Human Role Separation]]
- [[PROMETHEUS RCT — Day et al. 2025]] — RCT showing AI as workflow tool (not decision aid) achieves positive outcomes → partial role separation in practice
- [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]] — real-world case where human+AI underperformed benchmark prediction
- [[Human-AI Interaction in Radiology — Kocak and Cuocolo 2026]] — comprehensive synthesis of collaboration models, cognitive impacts, and governance
- [[MIT Center for Collective Intelligence]]
- Human Augmentation — see above; same page
