---
title: "Skills Rules and Knowledge — Rasmussen 1983"
aliases: ["Skills Rules and Knowledge — Rasmussen 1983"]
type: source
tags: [human-factors, cognitive-systems, srk-framework, skill-based, rule-based, knowledge-based, operator-performance]
created: 2026-06-27
updated: 2026-06-27
sources: [1983-rasmussen-srk-framework]
---

**Citation:** Rasmussen, J. (1983). Skills, rules, and knowledge; signals, signs, and symbols, and other distinctions in human performance models. *IEEE Transactions on Systems, Man, and Cybernetics*, SMC-13(3), 257–266. DOI: 10.1109/TSMC.1983.6313160

**Raw file:** `Skills rules and knowledge - Rasmussen seg (1).pdf`

## Summary
Introduces the SRK (Skills-Rules-Knowledge) framework, a three-level taxonomy of human cognitive performance. Foundational to human factors and cognitive systems engineering. Highly relevant to understanding how AI affects clinical decision-making and what kinds of errors occur at each cognitive level.

## The SRK Framework

| Level | Trigger | Control Mode | Example | Error Type |
|-------|---------|--------------|---------|------------|
| **Skill-based (S)** | Signals (sensory patterns) | Automated, sensorimotor | Expert sonographer adjusting probe angle by feel | Slips (automatic action misfires) |
| **Rule-based (R)** | Signs (recognized situations) | Procedural: IF condition THEN action | Clinician following a protocol | Mistakes (wrong rule applied to right situation) |
| **Knowledge-based (K)** | Symbols (abstract representations) | Deliberate reasoning and planning | Novel case requiring diagnosis from first principles | Mistakes (plan fails due to incomplete model) |

> [!note]
> Performance is not fixed at one level — experts shift fluidly across levels, operating at skill level for routine tasks and rising to knowledge level for novel problems. Experience moves tasks from knowledge → rule → skill level.

## Signals, Signs, and Symbols
The information representations that trigger each level:
- **Signals** → activate skill-based responses without conscious attention (sensory perception)
- **Signs** → trigger rule selection (pattern recognition of a known category)
- **Symbols** → require deliberate reasoning about abstract state (diagnostic inference)

## Implications for AI in Medical Imaging

### Skill-based disruption
- AI plane-detection tools (e.g., PROMETHEUS) automate sensorimotor scanning at skill level
- Risk: removes the repeated signal-response loops through which skill-based performance is developed
- Connects to [[Deliberate Practice]] — skill-based competence requires deliberate practice with feedback

### Rule-based augmentation
- AI diagnostic aids typically operate at the rule-based level — providing "IF image pattern X THEN likely diagnosis Y"
- This may cause rule-based shortcuts in clinicians who would otherwise reason from knowledge-based principles

### Knowledge-based preservation
- AI is weakest at genuine knowledge-based reasoning in novel or edge cases
- If clinicians' rule-based performance is automated, they may not develop the knowledge-based reserve needed for unusual cases
- Connects to [[AI Ground Truth]] — training labels encode rule-based clinical knowledge, not the tacit, signal-based knowledge of experts

## Cross-references
- [[Skills Rules and Knowledge]]
- [[Deliberate Practice]]
- [[Tacit and Explicit Knowledge]]
- [[AI Ground Truth]]
- [[Automation Bias]]
- [[Ironies of Automation]]
