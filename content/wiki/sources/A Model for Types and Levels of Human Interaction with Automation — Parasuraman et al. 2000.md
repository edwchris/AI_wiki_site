---
title: "A Model for Types and Levels of Human Interaction with Automation — Parasuraman et al. 2000"
aliases: ["A Model for Types and Levels of Human Interaction with Automation — Parasuraman et al. 2000"]
type: source
tags: [levels-of-automation, human-factors, automation, human-machine-interaction, supervisory-control]
created: 2026-06-27
updated: 2026-06-27
sources: [2000-parasuraman-sheridan-wickens-levels-automation]
---

**Citation:** Parasuraman, R., Sheridan, T. B., & Wickens, C. D. (2000). A model for types and levels of human interaction with automation. *IEEE Transactions on Systems, Man, and Cybernetics — Part A: Systems and Humans*, 30(3), 286–297. DOI: 10.1109/3468.844354

**Raw file:** `A_model_for_types_and_levels_of_human_interact.pdf`

## Summary
Proposes a taxonomy of automation along two dimensions: **type** (what cognitive function is automated) and **level** (how much autonomy automation has). Provides a framework for designing automation systems that appropriately allocate cognitive work between human and machine. Foundational for analysing AI tool design in medicine.

## Types of Automation (Four Functions)

| Type | Cognitive Function | Example in Medical AI |
|------|-------------------|----------------------|
| **Information acquisition** | Sensing, monitoring | AI image acquisition, auto-windowing |
| **Information analysis** | Data integration, feature extraction | AI lesion detection, segmentation |
| **Decision and action selection** | Choosing among options | AI recommending diagnosis |
| **Action implementation** | Executing the selected action | Robotic surgery, automated reporting |

## Levels of Automation (10-point scale)

From fully manual to fully automated:
1. Computer offers no assistance; human does everything
2. Computer offers a complete set of action alternatives
3. Computer narrows selection to a few alternatives
4. Computer suggests a single alternative
5. Computer executes suggestion if human approves
6. Computer allows human a restricted time to veto
7. Computer executes automatically, informs human
8. Computer informs human only if it decides to
9. Computer informs human only if asked
10. Computer acts entirely autonomously

> [!note]
> Most current clinical AI operates at **Level 4** (suggesting diagnosis) or **Level 7** (flagging, with human shown result). Level 10 is aspirational and raises significant governance concerns.

## Costs and Benefits of Automation by Level

| Level | Benefit | Risk |
|-------|---------|------|
| Low (1–4) | Maintains human skill, SA, and oversight | Less efficiency gain |
| Medium (5–7) | Efficiency gains; human still engaged | Complacency risk begins |
| High (8–10) | Maximum efficiency | Skill erosion; SA failure; accountability gap |

## Implications for AI Design in Radiology
- Current AI tools are often deployed at Level 4–7 without considering SA and skill consequences
- [[AI-Human Role Separation]] implicitly moves toward high levels for specific task types, while keeping humans at Level 1–3 for other tasks
- The key design question is not "how smart can the AI be?" but "what level of automation preserves human competence for the tasks where we need it?"

## Cross-references
- [[Levels of Automation]]
- [[Situation Awareness]]
- [[Ironies of Automation]]
- [[Trust in Automation]]
- [[AI-Human Role Separation]]
- [[Human-Centered AI Evaluation]]
- [[Automation Bias]]
