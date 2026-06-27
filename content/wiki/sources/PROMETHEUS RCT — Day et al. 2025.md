---
title: "PROMETHEUS RCT — Day et al. 2025"
aliases: ["PROMETHEUS RCT — Day et al. 2025"]
type: source
tags: [rct, fetal-ultrasound, ai-clinical-deployment, sonography, obstetrics, nejm-ai]
created: 2026-06-27
updated: 2026-06-27
sources: [2025-day-prometheus-fetal-ultrasound]
---

**Citation:** Day, T.G. et al. (2025). AI to assist in the fetal anomaly ultrasound scan: A randomized controlled trial. *NEJM AI*. DOI: 10.1056/AIoa2400747

**Full name:** PROMETHEUS — Prospective tRial of Machine lEarning To Help fEtal Ultrasound Scanning

**Raw file:** `Day et al. - 2025 - AI to Assist in the Fetal.pdf`

## Study Design
- Single-centre RCT, open-label crossover
- 78 pregnant participants (26 with fetal congenital heart disease); 58 sonographers
- Each participant scanned twice: AI-assisted vs. standard unassisted scan
- **AI role**: identifies and saves 13 standard image planes; measures 4 biometric parameters; does NOT autonomously diagnose CHD

## Results

| Metric | AI-assisted | Standard | Significance |
|--------|------------|---------|-------------|
| Sensitivity (fetal malformation) | 88.9% | 81.5% | p = NS |
| Specificity | 98.0% | 92.2% | p = NS |
| Scan duration | 11.4 min | 19.7 min | **p < 0.001** |
| Cognitive load | Reduced | Baseline | Reported |

## Key Findings
- AI assistance significantly reduced scan time (~42%) and sonographer cognitive load
- Diagnostic performance (sensitivity/specificity) was not significantly different — maintained, not improved
- AI acts as a workflow tool (automating image capture and measurement) rather than a diagnostician
- Sonographer remains responsible for interpretation; AI handles the mechanical and administrative components

## Significance
- First prospective RCT of AI in routine fetal anomaly screening — directly addresses the methodological critique in [[AI vs. Clinicians — Nagendran et al. 2020]]
- Demonstrates that workflow-focused AI (not diagnostic AI) can deliver real clinical benefits
- Aligns with [[AI-Human Role Separation]] concept: AI takes defined sub-tasks; human retains diagnostic authority

## Limitations
- Single-centre; generalizability uncertain
- No long-term follow-up on patient outcomes
- AI model's performance across different ultrasound equipment and patient populations untested

## Cross-references
- [[Thomas Day]]
- [[AI in Sonography]]
- [[Human-AI Synergy]]
- [[AI-Human Role Separation]]
- [[AI vs. Clinicians — Nagendran et al. 2020]]
- [[Human-Centered AI Evaluation]]
