---
title: "Skills Rules and Knowledge"
aliases: ["Skills Rules and Knowledge"]
type: concept
tags: [srk-framework, human-factors, cognitive-systems, rasmussen, error-taxonomy, expertise]
created: 2026-06-27
updated: 2026-06-27
sources: [1983-rasmussen-srk-framework]
---
of the 
# Skills, Rules, and Knowledge (SRK Framework)

Jens Rasmussen's (1983) three-level taxonomy of human cognitive performance. Explains how expert operators shift between automated sensorimotor, procedural, and deliberate cognitive modes — and what kinds of errors occur at each level.

---

## Three Levels

| Level | Control Mode | Trigger | Error Type | Example |
|-------|-------------|---------|-----------|---------|
| **Skill-based (S)** | Sensorimotor, automatic | Signals (perceptual patterns) | Slips — correct intention, wrong execution | Expert adjusting probe by feel |
| **Rule-based (R)** | Procedural: IF sign → THEN action | Signs (recognised situation categories) | Mistakes — wrong rule for the situation | Applying screening protocol to wrong presentation |
| **Knowledge-based (K)** | Deliberate planning and inference | Symbols (abstract concepts) | Mistakes — incomplete/wrong mental model | Novel case requiring first-principles diagnosis |

---

## The Rasmussen Ladder

Performance moves **up** the levels when a situation is:
- Novel or unfamiliar
- Ambiguous or conflicting with expectations
- High stakes with uncertain outcome

Performance moves **down** when a situation is:
- Familiar and well-practiced
- Time-pressured (forces heuristics)

**Expert advantage**: experts can handle more situations at lower (faster, less effortful) levels because they have more compiled rules and skills.

---

## AI and the SRK Framework

| Level | AI relationship |
|-------|----------------|
| **Skill** | AI automates sensorimotor tasks (probe navigation, plane detection) → removes practice opportunities → skill-level expertise cannot develop |
| **Rule** | AI provides IF-THEN recommendations → clinicians may accept rules without developing knowledge-based understanding |
| **Knowledge** | AI is weakest here — novel, out-of-distribution cases require knowledge-based reasoning that AI cannot provide reliably |

**The deskilling risk**: if AI handles routine tasks at skill and rule levels → clinicians only face knowledge-level situations → but without skill/rule experience, they lack the foundation for reliable knowledge-level performance. See [[Deliberate Practice]] and [[Ironies of Automation]].

---

## Error Implications

- **Slips** (skill level): hard to prevent through training alone; require design solutions (checklists, forcing functions)
- **Rule mistakes**: prevented by better rule selection — relevant to AI that flags wrong rules
- **Knowledge mistakes**: most dangerous; result from flawed mental models — relevant to AI opacity (clinician cannot build accurate model of AI's logic)

---

## Related Pages
- [[Skills Rules and Knowledge — Rasmussen 1983]]
- [[Deliberate Practice]]
- [[Ironies of Automation]]
- [[Tacit and Explicit Knowledge]]
- [[Automation Bias]]
- [[Situation Awareness]]
- [[AI Education in Medical Imaging]]
