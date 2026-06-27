---
title: NASSS Framework
aliases:
  - NASSS Framework
type: concept
tags:
  - implementation-science
  - sociotechnical
  - health-technology
  - adoption
  - sustainability
  - AI-implementation
created: 2026-06-27
updated: 2026-06-27
sources:
  - 2017-greenhalgh-nasss
  - 2026-jmir-ai-dss-radiology-nasss
---

# NASSS Framework

**Nonadoption, Abandonment, Scale-up, Spread, and Sustainability** — a sociotechnical framework for evaluating why health technologies fail to be adopted or sustained in real-world clinical settings.

Developed by Greenhalgh et al. ([[Beyond Adoption — NASSS Framework — Greenhalgh et al. 2017]], *J Med Internet Res* 2017;19(11):e367). Based on a hermeneutic systematic review of 28 implementation frameworks plus 6 empirical case studies (400+ hours observation, 165 interviews) across UK healthcare. Applied to AI decision support in radiology in [[Implementing AI Decision Support in Radiology — JMIR 2026]].

---

## The Seven Domains

![[12916_2019_1463_Fig1_HTML.png]]

| Domain | Key question |
|--------|-------------|
| **1. The condition** | How complex is the health problem being addressed? Is it well-defined or contested? |
| **2. The technology** | How complex is the technology itself? Is it a simple tool or a "black box" with unpredictable outputs? |
| **3. The value proposition** | Who benefits, who bears costs, and how are these distributed across stakeholders? |
| **4. The adopter system** | Who are the intended users? What are their skills, attitudes, and existing workflows? |
| **5. The organisation** | Does the organisation have the infrastructure, leadership, and capacity to support adoption? |
| **6. The wider context** | What regulatory, policy, financial, and cultural factors shape adoption? |
| **7. Embedding and adaptation** | Can the technology adapt to local context over time, and can the context adapt to the technology? |

---

## Simple vs. Complex Technologies

NASSS distinguishes between:
- **Simple technologies**: well-defined function, predictable outputs, easy to learn → adoption is mainly an organisational challenge
- **Complex technologies**: unpredictable outputs, contested evidence, high interpretive flexibility (e.g. AI in clinical imaging) → adoption is a sociotechnical challenge requiring ongoing negotiation

> [!important]
> AI clinical decision support sits firmly in the "complex" category — it has contested evidence, opaque outputs, unpredictable performance across populations, and disrupts existing professional roles. NASSS predicts that technical performance alone will not determine adoption outcomes.

---

## Why Technologies Fail: NASSS Explanations

Most health IT failures are not technical — they arise when:
- The **value proposition** is captured by developers/vendors but costs fall on clinicians
- The **adopter system** is not meaningfully engaged in design or rollout
- The **organisation** lacks governance capacity to monitor and respond to performance drift
- **Embedding** is treated as a one-time event rather than continuous adaptation

This aligns with [[Computer Technology and Clinical Work — Wears and Berg 2005]], which made the same argument two decades earlier for CPOE and clinical decision support.

---

## Application to AI in Radiology (JMIR 2026)

The JMIR 2026 study applied NASSS to an AI DSS deployment in hospital radiology and found:
- Domain 2 (Technology complexity): AI outputs were opaque; radiologists did not know when to override
- Domain 4 (Adopter system): radiologists not involved in selection; resistance emerged post-deployment
- Domain 5 (Organisation): no governance structure for ongoing performance monitoring
- Domain 7 (Embedding): system treated as "deployed and done"; no adaptation mechanism

**Key finding**: sociotechnical complexity, not technical performance, drove the gap between pilot success and routine use failure.

---

## Related Pages
- [[Trisha Greenhalgh]] — lead developer of the NASSS framework
- [[Beyond Adoption — NASSS Framework — Greenhalgh et al. 2017]] — primary source
- [[Implementing AI Decision Support in Radiology — JMIR 2026]] — applied NASSS to radiology AI DSS
- [[AI Implementation in Radiology]]
- [[Human-Centered AI Evaluation]]
- [[Computer Technology and Clinical Work — Wears and Berg 2005]]
- [[Human-AI Interaction in Radiology — Kocak and Cuocolo 2026]]
- [[Trust in Automation]]
- [[Ironies of Automation]]
- [[AI Chasm]] — NASSS explains why technically sound AI fails to cross the chasm
