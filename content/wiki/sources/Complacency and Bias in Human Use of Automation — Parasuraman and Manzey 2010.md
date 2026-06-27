---
title: "Complacency and Bias in Human Use of Automation — Parasuraman and Manzey 2010"
aliases: ["Complacency and Bias in Human Use of Automation — Parasuraman and Manzey 2010"]
type: source
tags: [automation-complacency, automation-bias, human-factors, attentional, monitoring]
created: 2026-06-27
updated: 2026-06-27
sources: [2010-parasuraman-manzey-complacency-bias]
---

**Citation:** Parasuraman, R., & Manzey, D. H. (2010). Complacency and bias in human use of automation: An attentional integration. *Human Factors*, 52(3), 381–410. DOI: 10.1177/0018720810376055

**Raw file:** `ParasuramanManzeyHF2010.pdf`

## Summary
Integrative review distinguishing and relating two failure modes in human-automation interaction: **automation complacency** (reduced monitoring of automation) and **automation bias** (commission and omission errors from over-reliance). Proposes an attentional resource account of both phenomena.

## Key Distinctions

| Concept | Definition | Error consequence |
|---------|-----------|------------------|
| **Automation complacency** | Reduced monitoring effort; monitoring without vigilance; passivity | Omission errors — failures to detect alerts |
| **Automation bias** | Active over-reliance on automation output as decision heuristic | Commission errors — acting on wrong automation; omission errors — failing to act when automation doesn't flag |

> [!note]
> Complacency is a monitoring failure (how much attention operators pay to automation); bias is a decision failure (how heavily operators weight automation in choices). Both co-occur in practice but are separable constructs.

## Attentional Integration Account
- Both complacency and bias arise from **attentional resource constraints**
- When automation is reliable, attention naturally shifts away (rational behaviour that becomes problematic at the margin)
- Workload and attentional capacity mediate both effects: high workload → operators rely on automation as cognitive shortcut → both complacency and bias increase

## Evidence
- Complacency measured by: detection rates for automation-generated alerts; monitoring frequency
- Bias measured by: commission errors (following wrong automation); omission errors (missing unflagged items)
- Both effects are robust across aviation, process control, military systems — and increasingly demonstrated in medicine

## Moderators

**Increase complacency and bias:**
- High automation reliability (paradoxically — operators learn to trust and stop checking)
- High workload
- Long monitoring periods (vigilance decrement)

**Reduce complacency and bias:**
- Adaptive automation (automation that varies, keeping operators engaged)
- Automation reliability feedback
- Training on failure modes
- Explicit "check the automation" prompts in procedures

## Relevance to AI in Medical Imaging
- Both effects documented in clinical settings: Dratsch et al. 2023 (automation bias in mammography) and [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]] both show evidence of bias with high-reliability AI
- High reliability AI creates a complacency risk: if 99% accurate, operators stop checking the 1% — the cases where errors matter most
- Connects to [[Automation Bias Systematic Review — Goddard et al. 2012]] and [[Ironies of Automation]]

## Cross-references
- [[Automation Bias]]
- [[Trust in Automation]]
- [[Ironies of Automation]]
- [[Situation Awareness]]
- [[Human-Centered AI Evaluation]]
- [[AI-Human Role Separation]]
