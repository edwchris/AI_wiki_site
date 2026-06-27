---
title: "Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025"
aliases: ["Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025"]
type: source
tags: [role-separation, radiology, human-ai, workflow, automation-bias, ai-autonomy]
created: 2026-06-27
updated: 2026-06-27
sources: [2025-rajpurkar-topol-role-separation]
---

**Citation:** Rajpurkar, P. & Topol, E.J. (2025). Beyond assistance: The case for role separation in AI-human radiology workflows. *Radiology*, 316(1). DOI: 10.1148/radiol.250477

**Raw file:** `10.1148_radiol.250477.pdf`

## Core Argument
The dominant "assistive AI" paradigm — AI augments and supports radiologist decision-making — is failing in practice. The proposed alternative is **role separation**: assigning distinct, non-overlapping tasks exclusively to AI or to the human radiologist.

## Why Assistive AI Underperforms
- Radiologists have no calibrated framework for when to trust AI vs. themselves
- **Automation bias**: humans anchor on AI output even when incorrect → trust miscalibration
- **Automation complacency**: reduced vigilance when AI is present as a safety net
- Combined human+AI can underperform each alone in certain task types → see [[Human-AI Synergy]] meta-analysis

> "We're stuck between distrust and dependence, and missing out on the full potential of AI." — Rajpurkar

## Proposed Role Separation Model
1. Map each radiology sub-task and empirically measure AI vs. radiologist performance
2. Assign each task **exclusively** to the demonstrably superior performer
3. AI and radiologist execute their respective tasks independently (no cross-review)
4. Results integrated at report level

**AI-assigned tasks (candidates):** image pre-processing, anomaly flagging for well-characterized conditions, worklist prioritization, measurement automation, structured data extraction

**Radiologist-assigned tasks (candidates):** complex differential diagnosis, uncertain or rare findings, clinical context integration, patient communication, medico-legal accountability

## Critique and Open Questions
- Does not address cases where AI and human judgment both contribute necessary information
- Removes human oversight precisely where AI may fail silently
- Requires validated task-level benchmarks that do not yet exist for most radiology sub-tasks
- Accountability may actually become more complex, not less

## Cross-references
- [[Pranav Rajpurkar]]
- [[Eric Topol]]
- [[AI-Human Role Separation]]
- [[Human-AI Synergy]]
- [[AI Ethics in Radiology]]
- [[AI vs. Clinicians — Nagendran et al. 2020]]
