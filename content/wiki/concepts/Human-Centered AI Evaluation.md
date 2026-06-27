---
title: "Human-Centered AI Evaluation"
aliases: ["Human-Centered AI Evaluation"]
type: concept
tags: [evaluation, human-centered, ai-deployment, real-world-ai, hci, clinical-ai, methodology]
created: 2026-06-27
updated: 2026-06-27
sources: [2020-beede-human-centered-diabetic-retinopathy, 2025-day-prometheus-fetal-ultrasound]
---

Evaluation methodology that centers human users, workflows, and socio-environmental contexts alongside technical metrics; the counterpart to benchmark-only evaluation of AI systems.

## The Benchmark Problem
Standard evaluation: AUC, sensitivity, specificity on a held-out test set under controlled conditions. What it misses:
- Test data distributions differ from real deployment environments
- Users behave differently with AI than without it (automation bias, trust miscalibration)
- Clinical workflows are not neutral containers — they shape and constrain AI use
- High benchmark performance can coexist with complete clinical failure → [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]]

## Key Evaluation Dimensions
1. **Workflow fit** — does AI integrate smoothly or disrupt existing clinical workflows?
2. **Trust calibration** — can users accurately judge when to trust or override AI?
3. **Communication design** — is AI output presented in interpretable, actionable terms?
4. **Training adequacy** — are users equipped to use the system appropriately, including when to override?
5. **Patient experience** — how does AI presence affect patients (confusion, consent, relationship with clinician)?
6. **Environmental factors** — image quality, equipment variation, lighting, patient compliance, room layout

## Failure Modes Identified in the Field
From [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]]:
- Image quality degradation in real clinics (vs. controlled training environment)
- Workflow disruption: AI added friction rather than reducing it
- Automation bias: nurses felt unable to override even when suspicious of results
- Trust miscalibration: no tools to understand AI confidence or appropriate override criteria
- Patient confusion about AI role

## Evaluation Methods
| Method | When to Use |
|--------|------------|
| Ethnographic observation | Early deployment; understand workflow in context |
| Semi-structured interviews | User experience, trust, override behavior |
| Think-aloud protocols | Real-time cognitive process during AI-assisted task |
| Prospective RCT | Comparative effectiveness; both clinical and user outcomes → [[PROMETHEUS RCT — Day et al. 2025]] |
| Performance drift monitoring | Post-deployment; ongoing surveillance |

## Design Implications
- Evaluation must begin in the deployment environment, not just the lab
- User interface and explainability are as important as model accuracy
- Override mechanisms are ethically and practically necessary
- Post-deployment surveillance is part of evaluation, not an afterthought → [[AI Implementation in Radiology]]

## Cross-references
- [[AI Ground Truth]]
- [[Human-AI Synergy]]
- [[Deep Learning in Medical Imaging]]
- [[AI Ethics in Radiology]]
- [[AI Implementation in Radiology]]
- [[SERVQUAL]] — service quality framework applicable to patient-facing AI workflows; AI may improve clinical accuracy while degrading SERVQUAL Empathy/Responsiveness dimensions
- [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]]
- [[PROMETHEUS RCT — Day et al. 2025]]
