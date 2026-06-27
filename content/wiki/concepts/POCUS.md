---
title: "POCUS"
aliases: ["POCUS", "Point-of-Care Ultrasound"]
type: concept
tags: [ultrasound, POCUS, point-of-care, scope-of-practice, deskilling, non-specialist, clinical-imaging]
created: 2026-06-27
updated: 2026-06-27
sources: [2004-finberg-whither-ultrasound-specialist, 2021-kim-ai-medical-ultrasonography, 2025-karni-ai-cardiac-us-training]
---

# POCUS (Point-of-Care Ultrasound)

Bedside ultrasound performed by the treating clinician — emergency physician, intensivist, GP, anaesthetist, obstetrician — rather than a specialist sonographer. POCUS is a focused, goal-directed examination to answer a specific clinical question in real time.

---

## POCUS vs. Comprehensive Ultrasound

| Feature | POCUS | Comprehensive diagnostic ultrasound |
|---------|-------|--------------------------------------|
| Operator | Treating clinician | Specialist sonographer |
| Scope | Focused (1–3 views) | Comprehensive protocol |
| Goal | Binary clinical decision | Full diagnostic report |
| Training | Hours to days for basic | Years for expert competency |
| Report | Clinical note | Formal radiologist/sonographer report |
| Quality assurance | Variable / minimal | Accredited, structured |

---

## Why POCUS Matters for AI

POCUS is the domain where AI guidance has the most immediate transformative potential — and where the deskilling and quality risk is highest:

- **AI as enabler**: real-time probe guidance (see [[AI-Enhanced Cardiac US Training — Karni et al. 2025]]) allows less-trained operators to acquire diagnostic views, extending POCUS to settings and operators previously excluded
- **AI as quality floor**: automated image quality scoring can flag when a POCUS image is inadequate — reducing false-negative diagnostic errors from suboptimal acquisitions
- **Deskilling risk**: if operators rely on AI guidance from day one, they never develop independent image acquisition skills ([[Ironies of Automation]], [[Deliberate Practice]])
- **Standardisation gap**: Kim 2021 ([[AI in Medical Ultrasonography — Kim 2021]]) argues that POCUS proliferation — varied operators, varied technique — is the primary reason AI in ultrasound lags behind AI in CT/MRI

---

## The Professional Boundary Tension

POCUS diffusion shifts the question: *who is a legitimate ultrasound operator?*

- **Traditional model**: all diagnostic ultrasound → specialist sonographer → formal report → radiologist oversight
- **POCUS model**: goal-directed scan → treating clinician → clinical decision at bedside, no formal report
- **Hybrid/AI-guided model**: AI-assisted acquisition by any trained operator → automated preliminary analysis → clinician decision

Finberg (2004, [[Whither the Ultrasound Specialist — Finberg 2004]]) warned that POCUS diffusion would erode specialist expertise and diagnostic standards — a concern that has intensified with AI-guided acquisition tools.

---

## AI-POCUS Applications

| Domain | Application |
|--------|------------|
| Emergency / trauma | FAST exam (fluid, pneumothorax) — binary decision, well-suited to AI guidance |
| Cardiac (POCUS echo) | LV function estimation, effusion — AI guidance for probe position (Karni 2025) |
| Obstetric | Dating, lie, presentation at bedside — increasingly AI-assisted |
| Lung | Pneumonia, consolidation, pleural effusion — simple binary classification |
| Vascular access | Needle guidance — already widely AI-assisted |

---

## Related Pages
- [[AI in Sonography]]
- [[Sonographer Professional Role]]
- [[Deliberate Practice]]
- [[Ironies of Automation]]
- [[AI-Enhanced Cardiac US Training — Karni et al. 2025]]
- [[Whither the Ultrasound Specialist — Finberg 2004]]
- [[AI in Medical Ultrasonography — Kim 2021]]
- [[Psychomotor Skills in Ultrasound — Nicholls et al. 2014]]
