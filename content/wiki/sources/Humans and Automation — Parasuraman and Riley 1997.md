---
title: "Humans and Automation — Parasuraman and Riley 1997"
aliases: ["Humans and Automation — Parasuraman and Riley 1997"]
type: source
tags: [human-factors, automation, trust-in-automation, misuse, disuse, complacency, automation-levels, human-machine-interaction]
created: 2026-06-27
updated: 2026-06-27
sources: [1997-parasuraman-riley-humans-automation]
---

# Humans and Automation — Parasuraman and Riley 1997

**Full citation:** Parasuraman R, Riley V. Humans and automation: Use, misuse, disuse, abuse. *Hum Factors*. 1997;39(2):230–253.

**DOI:** 10.1518/001872097778543886

> [!note] Source page written from domain knowledge. Raw file is PDF (`raw/parasuraman.pdf`); PDF extraction is unavailable in current environment.

---

## What it is

A foundational theoretical paper in human factors establishing a taxonomy for understanding how humans interact with automated systems. Introduces the four-outcome model (use, misuse, disuse, abuse) and the stage × level framework for describing automation. One of the most-cited human factors papers; foundational for all subsequent work on automation bias, trust, and complacency.

## The Stage × Level Framework

Automation can operate at four functional stages of human information processing:

| Stage | Description | Examples |
|-------|-------------|---------|
| 1. Information acquisition | Sensing, detecting, filtering, enhancing | TCAS detection, radar, patient monitoring alarms |
| 2. Information analysis | Integration, prediction, inference, representation | Diagnostic algorithms, situation assessment tools |
| 3. Decision/action selection | Suggesting, recommending, action selection | Clinical decision support, autopilot mode selection |
| 4. Action implementation | Executing selected actions, completing tasks | Infusion pumps, ventilators, robotic surgery |

At each stage, automation level ranges from **1** (fully manual — human does everything) to **10** (fully autonomous — computer does everything, ignores human). The appropriate level depends on the costs and benefits of automation at that stage for that task.

## Four outcomes of human–automation interaction

> [!important] The central contribution of Parasuraman & Riley 1997: automation is not simply "on" or "off." The human–automation relationship produces four distinct outcome patterns, each with different causes and remedies.

| Outcome | Definition | Cause | Risk |
|---------|-----------|-------|------|
| **Use** | Appropriate engagement with automation | Good design, calibrated trust | Baseline appropriate |
| **Misuse** | Over-reliance; complacency; automation bias | Trust exceeds reliability; passive monitoring | Errors pass undetected |
| **Disuse** | Under-reliance; rejection; ignoring | Trust below reliability; poor interface; past failure | Loss of automation benefit |
| **Abuse** | Imposing automation on humans without adequate consideration | Design decisions by developers without human factors input | Skill decay, overload, alienation |

### Misuse (over-reliance)
- The "automation bias" problem: humans bias their decisions toward automation outputs even when automation is wrong
- Two manifestations:
  - **Omission errors**: failure to notice that automation has failed (not looking)
  - **Commission errors**: complying with an incorrect automation recommendation (over-trusting)
- Caused by: monitoring fatigue during nominal operations; trust calibration to average reliability not worst-case reliability

### Disuse (under-reliance)
- Humans reject reliable automation because of past failures, poor interface design, or cultural resistance
- Paradox: people may simultaneously show automation bias for one task and disuse for another
- Relevant to algorithm aversion (see [[Algorithm Aversion — Dietvorst et al. 2015]])

### Abuse (design problem)
- Automation imposed by designers/managers without considering human capability, workload, or situation
- Creates skill gaps, reduces human situational awareness, and creates brittleness when automation fails

## Trust in automation

Parasuraman & Riley define trust as "the attitude that an agent will help achieve an individual's goals in a situation characterized by uncertainty and vulnerability."

Key principles:
- **Calibration**: trust should match automation reliability; over-trust and under-trust are both problematic
- **Overtrust develops from reliability**: humans learn to trust automation that has been reliable, then fail to monitor it during low-frequency failures
- **Trust does not transfer**: trust in one automated system does not automatically extend to similar systems

## Situation awareness effects

High automation reduces active engagement, which degrades situation awareness:
- Passive monitoring requires less cognitive engagement than active control
- Leads to "out of the loop" problem: when automation fails, human cannot quickly re-establish manual control
- Most dangerous at Stage 4 (action implementation) — automation that acts without human confirmation

## Connections

- [[Automation Bias]] — the misuse category; this paper is the theoretical source for the concept
- [[Trust in Automation]] — core theoretical framework established here
- [[Algorithm Aversion — Dietvorst et al. 2015]] — the disuse pattern; algorithm aversion as a specific form of disuse
- [[Ironies of Automation]] — Bainbridge 1983 predicted the same problems a decade earlier; Parasuraman & Riley provide the taxonomic framework
- [[Situation Awareness]] — Stage 1–3 automation directly affects Endsley's SA model
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — human factors section draws on this framework implicitly
- [[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]] — deskilling = Stage 4 abuse + disuse effects over time

## Significance

The single most influential theoretical paper in the human factors of automation. The four-outcome taxonomy is the standard framework for analysing human–automation interaction. Any discussion of AI deployment in clinical settings needs to address which outcome pattern is being produced.
