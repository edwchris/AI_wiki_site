---
title: "AI-Human Role Separation"
aliases: ["AI-Human Role Separation"]
type: concept
tags: [human-ai-collaboration, role-separation, automation-bias, radiology, workflow, autonomy]
created: 2026-06-27
updated: 2026-06-27
sources: [2025-rajpurkar-topol-role-separation]
---

Design paradigm for human-AI collaboration in which distinct, non-overlapping tasks are assigned exclusively to AI or to the human — rather than using AI in a joint "assistive" capacity alongside human judgment.

## The Problem with Assistive AI
Current dominant model: AI presents a recommendation; human retains final decision authority.

Failure modes:
- **Calibration problem**: clinicians have no reliable framework for when to trust AI vs. themselves
- **Automation bias**: humans anchor on AI recommendations even when they conflict with clinical judgment
- **Automation complacency**: reduced vigilance because AI provides apparent safety net
- **Anchoring + confirmation bias**: clinicians seek to confirm AI suggestion rather than independently evaluate
- Meta-analytic evidence: human+AI combined performance can be worse than AI alone in some tasks → [[Human-AI Synergy]]

## Role Separation Model (Rajpurkar & Topol 2025)
Proposed in [[Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025]]:

1. **Map** each clinical sub-task and benchmark AI vs. human performance empirically
2. **Assign** each task exclusively to the demonstrably superior performer
3. **Execute** independently — AI and human do not review each other's outputs
4. **Integrate** at a higher synthesis level (e.g., final report)

**Candidate AI tasks:** image pre-processing, anomaly flagging for well-characterized conditions, worklist prioritization, measurement automation, structured data extraction

**Candidate human tasks:** complex differential diagnosis, uncertain or rare findings, clinical context integration, patient communication, medico-legal accountability

## Contrast with Assistive Model

| Dimension | Assistive AI | Role Separation |
|-----------|-------------|----------------|
| Human oversight of AI | Always | None (by design) |
| Automation bias risk | High | Eliminated |
| Accountability clarity | Ambiguous | Clear |
| Flexibility for complex cases | High | Low |
| Integration complexity | Simple | Complex |
| Trust calibration required | Yes | No |

## Relationship to PROMETHEUS
[[PROMETHEUS RCT — Day et al. 2025]] demonstrates a practical form of partial role separation: AI handles plane detection and measurement (clearly defined mechanical tasks); sonographer retains diagnostic interpretation. This is role separation within a workflow rather than between workflows.

## Critiques
- Not suitable for cases requiring interleaved AI-human reasoning
- Removes human oversight precisely where AI may fail silently
- Requires robust task-level benchmarks that do not yet exist for most sub-tasks
- May create accountability complications rather than clarity at integration points

## Cross-references
- [[Human-AI Synergy]]
- [[Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025]]
- [[Deep Learning in Medical Imaging]]
- [[AI Ethics in Radiology]]
- [[AI in Sonography]]
- [[Human-Centered AI Evaluation]]
