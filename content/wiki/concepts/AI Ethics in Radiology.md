---
title: "AI Ethics in Radiology"
aliases: ["AI Ethics in Radiology"]
type: concept
tags: [ai-ethics, radiology, fairness, transparency, accountability, governance, bias]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-geis-ethics-ai-radiology, 2023-multisociety-ai-tools-radiology]
---

Ethical principles governing the development, deployment, and clinical use of AI systems in radiology and medical imaging; articulated through multisociety consensus statements and ongoing regulatory development.

## Core Principles
Drawn from [[Ethics of AI in Radiology — Geis et al. 2019]] (joint statement: ACR, RSNA, ESR, SIIM, ESMI, CAR, AAPM):

1. **Beneficence** — AI use must benefit patients; purely commercial applications without patient benefit are ethically problematic
2. **Non-maleficence** — clear harm pathways from AI errors; accountability must be assigned before deployment, not after
3. **Fairness** — AI can encode and amplify biases across demographic groups, comorbidities, and acquisition settings
4. **Transparency** — known failure modes must be disclosed; model interpretability is desirable but contested
5. **Patient autonomy** — patients should have meaningful consent over AI use of their imaging data
6. **Justice** — AI should not widen health inequities; deployment in resource-poor settings requires specific consideration

## Bias Taxonomy
- **Demographic bias**: under-representation of race, sex, age in training data
- **Technical bias**: equipment variation, acquisition protocol differences between training and deployment
- **Comorbidity bias**: confounding by co-occurring conditions not the target of the model
- **Label bias**: training labels reflect the biases of the annotating clinicians → [[AI Ground Truth]]

## Accountability Gaps
- When AI contributes to a diagnostic error: radiologist, vendor, or deploying institution?
- Current legal frameworks (tort, products liability) do not cleanly assign liability for AI-mediated errors
- Differs from traditional software: AI behavior is emergent, not fully specified by developers

## Transparency vs. IP Tension
- Vendors resist disclosure of training data or model internals (competitive concern)
- Regulators and clinicians need transparency to assess safety and fitness for purpose
- Emerging middle ground: regulatory-only disclosure, algorithmic auditing by trusted third parties

## Regulatory Landscape (as of 2023)
- **US (FDA)**: 510(k) SaMD pathway for most static AI; adaptive AI (learns post-deployment) has unresolved regulatory status
- **EU AI Act**: radiology AI classified as high-risk; mandatory transparency, human oversight, and conformity assessment
- **Australia (TGA)**: SaMD pathway; RANZCR has released AI implementation guidance aligned with [[Developing and Implementing AI Tools in Radiology — Multisociety 2023]]

## Cross-references
- [[AI Implementation in Radiology]]
- [[Ethics of AI in Radiology — Geis et al. 2019]]
- [[Developing and Implementing AI Tools in Radiology — Multisociety 2023]]
- [[Deep Learning in Medical Imaging]]
- [[Human-Centered AI Evaluation]]
- [[AI Ground Truth]]
