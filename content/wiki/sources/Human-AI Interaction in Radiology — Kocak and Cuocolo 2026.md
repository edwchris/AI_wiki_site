---
title: "Human-AI Interaction in Radiology — Kocak and Cuocolo 2026"
aliases: ["Human-AI Interaction in Radiology — Kocak and Cuocolo 2026"]
type: source
tags: [human-AI-collaboration, radiology, automation-bias, deskilling, governance, workflow-integration, narrative-review]
created: 2026-06-27
updated: 2026-06-27
sources: [2026-kocak-cuocolo-human-ai-radiology]
---

**Citation:** Kocak, B., & Cuocolo, R. (2026). Human–AI interaction and collaboration in radiology: from conceptual frameworks to responsible implementation. *Diagnostic and Interventional Radiology*. DOI: 10.4274/dir.2026.263780 (online ahead of print, January 2026)

**Raw file:** `2026.263780.pdf` (DOI suffix: `dir.2026.263780`)

**Type:** Narrative review

## Core Argument
Most AI studies in radiology evaluate algorithms in isolation. This review pivots to how radiologists and AI *actually interact* in clinical workflows — and finds that workflow integration, cognitive effects, and governance determine whether performance gains survive real-world deployment.

> [!warning] Tension with Vaccaro et al. 2024
> Kocak & Cuocolo present "diagnostic complementarity" — the principle that human and AI errors partially overlap, enabling mutual compensation — as a positive design basis for collaboration. However, [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]] (meta-analysis, 106 experiments) found average human–AI synergy is *negative* (g = −0.23): combined performance is worse than the best single agent on average. The complementarity principle holds theoretically but does not reliably emerge in practice without careful task decomposition.

> [!important]
> "Performance gains are fragile when workflow integration, cognitive effects, and governance are neglected."

## Conceptual Frameworks

**Diagnostic complementarity** — human and AI errors only *partially* overlap, enabling mutual compensation. This is the theoretical basis for human–AI collaboration outperforming either alone. Contrast with [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]] which found synergy is negative on average — the key variable is whether error sets are truly independent.

**Human-AI symbiosis** — radiologists supply clinical context and judgment; AI supplies pattern recognition and throughput. Neither replaces the other's distinct contribution.

## Workflow Integration Models

| Model | Description |
|-------|-------------|
| Decision support | AI marks suspicious regions with confidence scores before human review |
| Safety net | AI reviews after human, flags potentially missed findings |
| AI-supported screening | Reduces secondary reader requirement while maintaining detection |
| Triage / worklist | Routes critical/urgent findings to front of queue immediately |

**Mammography finding**: "AI as supporting reader" workflow maintained diagnostic performance while reducing secondary readings by up to **87%**.

## Cognitive and Professional Impacts

### Automation Bias
- Trainee accuracy dropped from **80% → 20%** when AI provided incorrect suggestions (mammography study)
- Uncritical acceptance especially pronounced in trainees with less independent baseline experience
- Connects to [[Automation Bias]] and [[Automation Bias Systematic Review — Goddard et al. 2012]]

### Algorithmic Aversion
- 47.2% of respondents anticipated *increased* workload despite AI — under-trust as well as over-trust is a problem
- Driven by false positives, validation concerns, bias awareness
- Connects to [[Trust in Automation — Lee and See 2004]]

### Deskilling Risk
- Heavy automation impairs perceptual skill and differential diagnosis acquisition in trainees
- Connects to [[Ironies of Automation]], [[Deliberate Practice]], [[AI Education in Medical Imaging]]

### Counterintuitive Workload Effects
- AI *increased* burnout in some settings (Chinese survey: dose-response relationship between AI use and emotional exhaustion)
- Mechanism: alert fatigue, verification burden, responsibility ambiguity

## Governance Requirements

| Element | Detail |
|---------|--------|
| Multidisciplinary oversight | Committees for procurement, deployment, monitoring |
| Post-market surveillance | Track performance drift from population/protocol changes |
| Explainability | Saliency maps align poorly with radiologist needs (localization utility 0.024–0.16) |
| AI literacy | Three tiers: foundational / clinical user / expert |
| Liability | Final radiologist supervision legally essential; liability remains with clinician |

## Emerging Technologies Covered
- **Vision-language models**: draft report generation and summarisation; currently lack specialised reasoning — "constrained, task-specific roles" only
- **Physician-in-the-loop active learning**: continuous model refinement through feedback from routine practice
- **Uncertainty quantification**: systems defer complex cases to expert review rather than forcing a classification

## Significance
One of the most current (2026) and comprehensive synthesis papers on human–AI collaboration in radiology. Directly applicable to ultrasound/sonography context even though imaging modality is different. The governance framework here complements [[Implementing AI Decision Support in Radiology — JMIR 2026]] (NASSS approach) and [[Developing and Implementing AI Tools in Radiology — Multisociety 2023]] (lifecycle guidance).

## Cross-references
- [[Human-AI Synergy]]
- [[Automation Bias]]
- [[Trust in Automation]]
- [[Ironies of Automation]]
- [[Levels of Automation]]
- [[Deliberate Practice]]
- [[AI Education in Medical Imaging]]
- [[AI Implementation in Radiology]]
- [[AI-Human Role Separation]]
- [[Implementing AI Decision Support in Radiology — JMIR 2026]]
- [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]]
- [[Automation Bias Systematic Review — Goddard et al. 2012]]
