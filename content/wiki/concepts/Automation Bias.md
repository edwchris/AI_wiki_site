---
title: "Automation Bias"
aliases: ["Automation Bias"]
type: concept
tags: [automation-bias, human-factors, cognitive-bias, clinical-decision-support, over-reliance, complacency]
created: 2026-06-27
updated: 2026-06-27
sources: [1997-parasuraman-riley-humans-automation, 2012-goddard-automation-bias-systematic-review]
---

# Automation Bias

The tendency of human operators to over-rely on automated systems, accepting their outputs as a heuristic substitute for independent judgment.

> **Formal definition (Mosier & Skitka 1996, as cited in Goddard 2012):** Over-acceptance of computer output as a heuristic replacement of vigilant information seeking.

---

## Two Error Types

| Error | Description | Example |
|-------|-------------|---------|
| **Commission** | Following incorrect automated advice | Radiologist accepts AI's false-negative; misses pathology |
| **Omission** | Failing to act because automation gave no prompt | Clinician doesn't look for condition AI did not flag |

Commission errors are the classic definition; omission errors are a broader manifestation (also called automation-induced complacency).

---

## How Common Is It?

From [[Automation Bias Systematic Review — Goddard et al. 2012]]:
- **RR = 1.26** (95% CI 1.11–1.44) — erroneous CDSS advice is followed 26% more often than the base rate
- **6–11%** of previously correct decisions reversed incorrectly after bad CDSS advice
- Effect is "fairly robust and generic across research fields" — not specific to any domain

---

## What Makes It Worse (Mediators)

- **Miscalibrated trust** — believing the system is more reliable than it is (strongest driver)
- **Task inexperience** — novices are more susceptible
- **High workload / time pressure** — forces heuristic reliance
- **Command-style interfaces** — "the AI says X" vs. "the AI found Y" frames

> [!warning]
> Automation bias is often worse when actual automation reliability is *high but imperfect* — users learn to trust the system over many correct outputs and fail to catch the rare errors.

---

## What Reduces It (Mitigators)

### System design
- Frame output as **information, not commands** (status displays > recommendation displays)
- Show **dynamic confidence levels** — uncertainty should be visible
- **Reduce visual prominence** of automated advice
- Require active confirmation before flagged items are dismissed

### Training & culture
- Train users explicitly to **recognise DSS error patterns**
- Make **individual accountability** explicit — users must own the decision
- Cultivate workplace norms that treat AI as advisory, not authoritative

> [!important]
> Training helps but is not sufficient alone — system design changes are required to structurally reduce bias.

---

## Automation Bias vs. Algorithm Aversion

These are opposite failure modes:

| Bias | Direction | Cause |
|------|-----------|-------|
| Automation bias | Over-trust automation | Miscalibrated high trust; workload |
| Algorithm aversion | Under-trust automation | Loss aversion; prior AI errors; desire for control |

Both lead to suboptimal human–AI performance. The goal is **calibrated trust** — appropriate reliance matched to actual system reliability.

---

## Relevance to AI in Medical Imaging

- [[Automation Bias in Mammography — Dratsch et al. 2023]]: RCT demonstrating automation bias *in vivo* — radiologists followed incorrect AI BI-RADS suggestions significantly more often
- [[Human-AI Interaction in Radiology — Kocak and Cuocolo 2026]]: trainee accuracy dropped from **80% → 20%** when AI provided incorrect suggestions — strongest in-vivo magnitude reported in this wiki
- [[Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025]] cites automation bias as the central failure of assistive AI models
- [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]] observes clinicians accepting AI outputs without independent verification (commission pattern)
- [[AI-Human Role Separation]] proposes structural role separation as a design-level mitigator

---

## Related Pages
- [[Automation Bias Systematic Review — Goddard et al. 2012]] — systematic review; RR 1.26
- [[Humans and Automation — Parasuraman and Riley 1997]] — theoretical framework; "misuse" category
- [[Algorithm Aversion]] — opposite failure mode (under-reliance)
- [[Algorithm Aversion — Dietvorst et al. 2015]] — empirical source for the opposite effect
- [[AI-Human Role Separation]]
- [[Human-AI Synergy]]
- [[Human-Centered AI Evaluation]]
- [[AI Ethics in Radiology]]
- [[Tacit and Explicit Knowledge]] — practitioners with richer tacit knowledge may be less susceptible to omission errors
