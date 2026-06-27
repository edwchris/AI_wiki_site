---
title: "Developing and Implementing AI Tools in Radiology — Multisociety 2023"
aliases: ["Developing and Implementing AI Tools in Radiology — Multisociety 2023"]
type: source
tags: [ai-implementation, radiology, multisociety-statement, procurement, governance, monitoring]
created: 2026-06-27
updated: 2026-06-27
sources: [2023-multisociety-ai-tools-radiology]
---

**Citation:** ACR, CAR, ESR, RANZCR & RSNA (2023). Developing, purchasing, implementing and monitoring AI tools in radiology: practical considerations. A multi-society statement. *Insights into Imaging* (and simultaneously in JACR, Canadian Assoc. Radiologists J., JMIRO, Radiology: AI). DOI: 10.1186/s13244-023-01541-3

**Societies:** American College of Radiology (ACR), Canadian Association of Radiologists (CAR), European Society of Radiology (ESR), Royal Australian and New Zealand College of Radiologists (RANZCR), Radiological Society of North America (RSNA)

**Raw file:** `s13244-023-01541-3.pdf`

## Summary
Practical lifecycle guidance for radiology departments on selecting, integrating, and governing AI tools; operationalizes the ethical principles from [[Ethics of AI in Radiology — Geis et al. 2019]].

## Lifecycle Framework

### Development Phase
- Training data must be diverse, demographically representative, and documented for bias
- External validation on held-out datasets from multiple institutions required before claims of generalizability
- Intended use population must be specified and validated

### Procurement Phase
- Require vendors to provide validation evidence on **local** population data, not just published benchmarks
- Evaluate transparency: documented training data demographics, known failure modes, model type
- Contract requirements: performance benchmarks, monitoring obligations, failure reporting

### Implementation Phase
- Staff training: not just how to use the system, but how and when to override it
- Clinical integration with PACS, EHR, and existing workflows
- Pilot deployment with defined success criteria before full rollout
- Patient information and consent processes where required

### Monitoring Phase
- Ongoing **performance drift detection**: systematic comparison of AI output vs. ground truth over time
- Dataset shift monitoring: alert when input data characteristics diverge from training distribution
- Incident reporting: structured mechanism for staff to flag suspected AI errors
- Regular re-validation cycles, especially after patient population or equipment changes

## Key Tensions
- Vendor transparency vs. IP protection: practical procurement guidance often conflicts with the full transparency called for in [[Ethics of AI in Radiology — Geis et al. 2019]]
- Speed of AI adoption vs. rigor of validation: commercial pressure to deploy early conflicts with safety requirements

## RANZCR Relevance
RANZCR's involvement (alongside ACR/ESR/RSNA) reflects growing international alignment on AI governance, directly applicable to Australian and New Zealand radiology practice.

## Cross-references
- [[AI Implementation in Radiology]]
- [[AI Ethics in Radiology]]
- [[Ethics of AI in Radiology — Geis et al. 2019]]
- [[Deep Learning in Medical Imaging]]
- [[Human-Centered AI Evaluation]]
- [[Diversity of Ultrasound Practice — Sidhu et al. 2023]]
