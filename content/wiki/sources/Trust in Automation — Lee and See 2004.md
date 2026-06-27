---
title: "Trust in Automation — Lee and See 2004"
aliases: ["Trust in Automation — Lee and See 2004"]
type: source
tags: [trust-in-automation, human-factors, automation, calibration, reliance, design]
created: 2026-06-27
updated: 2026-06-27
sources: [2004-lee-see-trust-automation]
---

**Citation:** Lee, J. D., & See, K. A. (2004). Trust in automation: Designing for appropriate reliance. *Human Factors*, 46(1), 50–80. DOI: 10.1518/hfes.46.1.50_30392

**Raw file:** `lee-see-2004-trust-in-automation-designing-for.pdf`

## Summary
Comprehensive review of the concept of trust in automation and its relationship to reliance. Defines trust, identifies factors that shape it, and proposes design principles for achieving "appropriate reliance" — neither over-trust (automation bias) nor under-trust (algorithm aversion). The canonical reference on trust calibration in human-automation systems.

## Core Definitions

- **Trust**: "The attitude that an agent will help achieve an individual's goals in a situation characterised by uncertainty and vulnerability"
- **Reliance**: Actual behavioural dependence on the automation; trust influences but does not determine reliance
- **Appropriate reliance**: Reliance that matches the actual reliability of the automation across conditions

> [!important]
> Trust ≠ reliance. Operators may trust automation and choose not to rely on it (if workload is low), or rely on automation they don't fully trust (if alternatives are worse). Design must target both.

## Three Bases of Trust

| Basis | Description | Time scale |
|-------|-------------|------------|
| **Performance** | Direct observation of automation's success/failure rate | Accumulated over interactions |
| **Process** | Understanding of how/why the automation works | From training, explanations, transparency |
| **Purpose** | Belief that automation is designed with the operator's goals in mind | From context, institutional trust |

## Factors That Increase/Decrease Trust

**Increase trust:**
- Consistent and reliable performance over time
- Transparency about limitations and uncertainty
- System provides explanations that match operator mental models
- Familiarity and experience

**Decrease trust:**
- Observed errors (especially surprising ones)
- Inconsistent performance across situations
- Opacity — operator cannot assess reliability
- Prior experience with automation failures

## Calibration Problem
- Trust must be **calibrated** to actual reliability: operators who over-trust risk commission errors ([[Automation Bias]]); operators who under-trust lose efficiency benefits
- Both miscalibrations are costly in medicine: over-trust misses errors; under-trust leads to algorithm aversion and rejection of useful tools
- Trust recalibrates slowly: single failures erode trust more than equivalent successes restore it (negativity asymmetry)

## Design Principles for Appropriate Reliance
1. **Show uncertainty**: display confidence intervals, not just point estimates
2. **Communicate purpose and limitations** explicitly in training and interface
3. **Design for transparency**: allow operators to see what the automation detected, not just its conclusion
4. **Manage initial trust appropriately**: avoid both hype and unnecessary distrust in introductory training
5. **Support trust recalibration**: provide feedback on automation performance over time

## Cross-references
- [[Trust in Automation]]
- [[Automation Bias]]
- [[Automation Bias Systematic Review — Goddard et al. 2012]]
- [[Trust in Automation — Hoff and Bashir 2014]]
- [[Complacency and Bias in Human Use of Automation — Parasuraman and Manzey 2010]]
- [[Situation Awareness]]
- [[Levels of Automation]]
- [[Human-Centered AI Evaluation]]
