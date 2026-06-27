---
title: "Toward a Theory of Situation Awareness — Endsley 1995"
aliases: ["Toward a Theory of Situation Awareness — Endsley 1995"]
type: source
tags: [situation-awareness, human-factors, dynamic-systems, cognitive-systems, SA]
created: 2026-06-27
updated: 2026-06-27
sources: [1995-endsley-situation-awareness]
---

**Citation:** Endsley, M. R. (1995). Toward a theory of situation awareness in dynamic systems. *Human Factors*, 37(1), 32–64. DOI: 10.1518/001872095779049543

**Raw file:** `Endsley_MR_Toward_a_Theory_of_Situation_Awaren.pdf`

## Summary
Defines and formalises situation awareness (SA) as a three-level construct: perception of environmental elements, comprehension of their meaning, and projection of future states. The dominant theoretical framework for understanding operator knowledge and performance in dynamic systems. Directly relevant to understanding how AI changes clinician SA in medical imaging.

## The Three Levels of SA

![[Endsley-SA-model.jpg]]

| Level | Description | Question answered |
|-------|-------------|------------------|
| **Level 1 — Perception** | Detection and recognition of relevant cues in the environment | "What is happening?" |
| **Level 2 — Comprehension** | Integration of multiple cues into a coherent understanding of current situation | "What does it mean?" |
| **Level 3 — Projection** | Prediction of future states based on current understanding | "What will happen next?" |

> [!important]
> Most automation failures degrade **Level 2 comprehension** and **Level 3 projection** — the system feeds information (Level 1) but the operator cannot integrate it into coherent situational understanding. Out-of-the-loop problems are fundamentally SA failures.

## Key Factors Affecting SA

### System factors
- **Automation**: takes operator out of control loop → reduces Level 1 perception of system state → degrades Level 2/3
- **Interface design**: well-designed displays support SA; cluttered displays degrade it
- **Workload**: high cognitive workload reduces SA by consuming attentional resources

### Individual factors
- **Mental models**: richer mental models improve Level 2 comprehension and Level 3 projection
- **Goals**: SA is goal-directed — operators attend to information relevant to their current goals
- **Experience**: expertise allows faster Level 1 pattern recognition, freeing resources for Level 2/3

## Out-of-the-Loop (OOTL) Problem
- Automated systems that manage routine tasks → operator stops monitoring → loses perception of system state (Level 1 SA failure)
- When automation alerts operator to a problem → operator must rapidly reconstruct SA at all three levels
- Recovery takes time → errors occur during the recovery window
- This is the SA dimension of the [[Ironies of Automation]]

## Implications for AI in Medical Imaging
- AI diagnostic assistants that display only flags and recommendations (not underlying data) deprive clinicians of Level 1 SA → clinician cannot verify AI's reasoning
- Supporting Level 2 comprehension requires showing clinicians what the AI "saw" (attention maps, probability scores) — not just the conclusion
- Long-term use of AI assistants may reduce clinicians' SA mental models, reducing capacity to perform independently

## Cross-references
- [[Situation Awareness]]
- [[Ironies of Automation]]
- [[Trust in Automation]]
- [[Levels of Automation]]
- [[Human-Centered AI Evaluation]]
- [[AI-Human Role Separation]]
- [[Automation Bias]]
