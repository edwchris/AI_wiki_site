---
title: "Verification Load"
aliases: ["Verification Load"]
type: concept
tags: [human-AI-collaboration, sonography, cognitive-load, automation-bias, task-analysis, verification]
created: 2026-06-27
updated: 2026-06-27
sources: [2025-day-prometheus-rct, 2023-day-sonographer-interaction-ai]
---

# Verification Load

The continuous per-output evaluative burden imposed on a human operator by real-time AI integration — the cognitive and attentional cost of monitoring, assessing, and deciding whether to act on each AI output during an ongoing task. Named in the context of AI in sonography (Edwards et al. framework paper, under review).

---

## Definition

Verification load is distinct from general cognitive load in that it is:

1. **Continuous** — every AI output during a task creates a verification obligation
2. **Per-output** — scales with the frequency of AI suggestions, not just their complexity
3. **Concurrent** — verification must occur while the primary task (e.g., real-time scanning) continues
4. **Asymmetric** — failing to verify when AI is wrong is catastrophic; verifying every correct output is wasteful

The construct names something the automation literature describes but does not label: the ongoing attentional tax of operating alongside a probabilistic AI system that cannot be unconditionally trusted.

---

## Relationship to Automation Bias

Verification load describes a structural **obligation** — what ideal human-AI collaboration demands. [[Automation Bias]] describes the systematic **failure** to meet that obligation.

| Construct | What it describes |
|-----------|------------------|
| Verification load | The cognitive demand created by the need to check AI outputs |
| Automation bias | The tendency to skip or inadequately perform that checking |

A complete account of human-AI performance requires both: what verification structurally demands, and why practitioners systematically fail to deliver it. The Kocak & Cuocolo 2026 finding — trainee diagnostic accuracy dropping from 80% to 20% under incorrect AI suggestion — illustrates how automation bias fills the gap left when verification load is high.

---

## Factors That Increase Verification Load

- **High AI output frequency**: plane detection assistants providing continuous on-screen guidance demand moment-to-moment monitoring
- **Low AI calibration transparency**: when practitioners cannot predict when AI is likely to err, every output must be verified equally
- **Task coupling**: when AI outputs cannot be easily ignored or deferred (they are already on-screen, already shaping the workflow)
- **Time pressure**: reduced time per scan increases the temptation to accept AI outputs without verification
- **Trainee status**: lower background knowledge means less ability to rapidly judge plausibility of AI output

---

## Empirical Evidence

- [[PROMETHEUS RCT — Day et al. 2025]]: AI time savings clustered at pauses in manual scanning — consistent with verification load being highest during continuous active scanning phases and easier to meet during natural pauses
- [[Sonographer Interaction with AI — Day et al. 2023]]: sonographers reported AI outputs as attentionally demanding to monitor alongside patient interaction; verification described as a competing task

---

## Design Implications

High verification load degrades the benefit of AI assistance by shifting cognitive burden from the primary task to meta-monitoring. Design strategies to reduce verification load:

1. **Selective AI output**: AI provides guidance only when confidence is above a threshold
2. **Mode-based activation**: AI engaged only during dedicated verification windows (not continuously)
3. **Visual hierarchy**: AI output visually distinguished from direct image features so the human can choose when to attend
4. **Calibrated uncertainty display**: explicit AI confidence display allows practitioners to triage verification effort

---

## Connections

- [[Automation Bias]] — the failure mode that verification load is designed to prevent; high verification load paradoxically increases automation bias
- [[Situation Awareness]] — verification requires active monitoring at SA Level 1–2; high task load degrades SA and therefore verification quality
- [[Ironies of Automation]] — Bainbridge's prediction: automation creates new monitoring demands that humans are poorly suited to sustain
- [[Levels of Automation]] — the frequency of AI output is a function of the automation level; full autonomy removes verification load by removing human oversight entirely
- [[Trust in Automation]] — calibrated trust should modulate verification effort; miscalibrated trust produces either under-verification (automation bias) or over-verification (disuse/algorithm aversion)
- [[AI in Real-Time Procedural Imaging — Framework Paper Analysis 2026-06-27]] — verification load is a central construct of the task-centric framework developed there
- [[Sonographer Competency]] — verification load is an additional competency demand not captured in existing competency frameworks
- [[AI in Sonography Research]] — project context for this construct
