---
title: "Situation Awareness"
aliases: ["Situation Awareness"]
type: concept
tags: [situation-awareness, human-factors, SA, dynamic-systems, automation, out-of-the-loop]
created: 2026-06-27
updated: 2026-06-27
sources: [1995-endsley-situation-awareness, 2000-parasuraman-sheridan-wickens-levels-automation]
---

# Situation Awareness

The degree to which an operator perceives, understands, and can project the state of a dynamic environment. Developed by Mica Endsley as a framework for understanding performance in high-stakes dynamic settings such as aviation, process control, and medicine.

**Formal definition (Endsley 1988):** "The perception of elements in the environment within a volume of time and space, the comprehension of their meaning, and the projection of their status in the near future."

---

## Three Levels

![[Endsley-SA-model.jpg]]

| Level | Question | Description |
|-------|----------|-------------|
| **1 — Perception** | What is happening? | Detecting and attending to relevant cues |
| **2 — Comprehension** | What does it mean? | Integrating cues into a current situation model |
| **3 — Projection** | What will happen next? | Extrapolating current state into likely futures |

Higher levels depend on lower: you cannot comprehend what you have not perceived; you cannot project what you have not comprehended.

---

## SA and Automation

Automation poses specific threats to SA at each level:

| Level | Automation threat |
|-------|------------------|
| Perception (1) | Automation handles sensing → operator stops monitoring; loses raw data |
| Comprehension (2) | Automation hides its internal state; operator cannot build accurate mental model |
| Projection (3) | Automation's future plans are opaque; operator cannot anticipate what it will do |

This is the **out-of-the-loop (OOTL) problem**: automation keeps operators informed of outputs but not of system state → operators cannot intervene effectively when automation fails.

---

## SA in Clinical AI Contexts

| SA Failure | Medical AI manifestation |
|-----------|--------------------------|
| Level 1 failure | Radiologist presented with AI conclusions only; never sees what features triggered them |
| Level 2 failure | Clinician accepts AI "high probability" label without understanding the reasoning |
| Level 3 failure | Clinician cannot anticipate when AI is operating outside its training distribution |

Good AI design for SA:
- **Show what the AI "saw"** (attention maps, feature highlights) → support Level 1
- **Explain the diagnosis pathway** → support Level 2
- **Display confidence and uncertainty** → support Level 3

---

## Related Pages
- [[Toward a Theory of Situation Awareness — Endsley 1995]]
- [[A Model for Types and Levels of Human Interaction with Automation — Parasuraman et al. 2000]]
- [[Ironies of Automation]]
- [[Trust in Automation]]
- [[Automation Bias]]
- [[Distributed Cognition]]
- [[Human-Centered AI Evaluation]]
- [[AI-Human Role Separation]]
