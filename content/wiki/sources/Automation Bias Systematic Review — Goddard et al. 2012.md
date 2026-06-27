---
title: "Automation Bias Systematic Review — Goddard et al. 2012"
aliases: ["Automation Bias Systematic Review — Goddard et al. 2012"]
type: source
tags: [automation-bias, clinical-decision-support, human-factors, systematic-review, cdss, over-reliance]
created: 2026-06-27
updated: 2026-06-27
sources: [2012-goddard-automation-bias-systematic-review]
---

**Citation:** Goddard, K., Roudsari, A., & Wyatt, J. C. (2012). Automation bias: a systematic review of frequency, effect mediators, and mitigators. *Journal of the American Medical Informatics Association*, 19(1), 121–127. DOI: 10.1136/amiajnl-2011-000089

**Raw file:** `19-1-121.pdf`

**PMID:** 21685142 | **PMCID:** PMC3240751

## Summary
Systematic review of automation bias in clinical decision support systems (CDSS). Defines the phenomenon, quantifies its frequency via meta-analysis, and synthesises the literature on what makes it worse (mediators) and what reduces it (mitigators).

## Definition
> Automation bias = the tendency to over-accept computer output as a heuristic replacement of vigilant information seeking.

Two error types:
- **Commission errors** — user follows incorrect automated advice (strict definition of automation bias)
- **Omission errors** — user fails to act because automation did not prompt them

## Frequency
- Meta-analysis risk ratio: **RR = 1.26** (95% CI 1.11–1.44) — erroneous advice is 26% more likely to be followed in CDSS groups vs. controls
- Negative consultations (correct pre-advice decisions changed to incorrect): **6–11%** across studies
- Effect described as "a fairly robust and generic effect across research fields"

## Mediators (Factors That Increase Automation Bias)

| Category | Factor |
|----------|--------|
| User | Task inexperience; low self-confidence in own decisions |
| Attitudinal | Miscalibrated trust in the DSS (strongest single driver); overconfidence in system accuracy |
| Environmental | High workload; time pressure; task complexity |

> [!note]
> Increased task difficulty can paradoxically *decrease* complacency — users may engage more vigilantly when they perceive higher stakes.

## Mitigators (Factors That Reduce Automation Bias)

| Strategy | Type |
|----------|------|
| Training on recognising DSS errors | Implementation |
| Emphasising user accountability for decisions | Implementation / cultural |
| Improving workplace culture around DSS use | Implementation |
| Reduced display prominence of advice | Design |
| Dynamic confidence levels on recommendations | Design |
| Providing information rather than direct commands | Design |
| Status displays vs. command-type displays | Design |

> [!important]
> The distinction between *information* and *command* framing is critical: systems that present findings (status) produce less automation bias than systems that issue recommendations (commands).

## Implications for AI in Medical Imaging
- AI tools that display a diagnosis or recommendation risk higher commission errors than tools that surface information for clinician synthesis
- This supports [[AI-Human Role Separation]] — separating information from decision reduces bias
- High workload conditions (common in clinical imaging) are a mediator → AI deployment should anticipate this
- Training alone is insufficient without system design changes

## Cross-references
- [[Automation Bias]]
- [[AI-Human Role Separation]] — role separation as structural mitigator
- [[Human-Centered AI Evaluation]] — automation bias as a key real-world failure mode
- [[Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025]] — cites automation bias as the core problem with assistive AI
- [[Human-AI Synergy]] — miscalibrated trust as mechanism for negative synergy when AI > human
