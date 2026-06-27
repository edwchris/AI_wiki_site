---
title: "Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020"
aliases: ["Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020"]
type: source
tags: [human-centered-ai, clinical-deployment, diabetic-retinopathy, ai-failure, real-world-ai, chi]
created: 2026-06-27
updated: 2026-06-27
sources: [2020-beede-human-centered-diabetic-retinopathy]
---

**Citation:** Beede, E., Baylor, E., Hersch, F., Iurchenko, A., Wilcox, L., Ruamviboonsuk, P., & Vardoulakis, L. (2020). A human-centered evaluation of a deep learning system deployed in clinics for the detection of diabetic retinopathy. In *Proceedings of the 2020 CHI Conference on Human Factors in Computing Systems* (CHI '20). DOI: 10.1145/3313831.3376718

**Raw file:** `3313831.3376718.pdf`

## Context
Evaluated Google Health's deep learning system for diabetic retinopathy (DR) detection deployed in real clinical settings. The system had previously achieved >90% AUC on benchmark datasets, exceeding ophthalmologist performance in controlled trials.

## Study Design
- Qualitative: ethnographic observation + semi-structured interviews
- 11 clinics across Thailand (range of resource levels)
- Participants: nurses, patients, clinic administrators
- Method: human-centered design evaluation of post-deployment experience

## Key Findings

### 1. Image Quality Degradation
- Clinic cameras, patient positioning, lighting, and compliance differed substantially from training data
- Real-world image quality was systematically lower than benchmark test data → model performance dropped

### 2. Workflow Disruption
- AI was inserted into existing screening workflows without workflow redesign
- Nurses found the system slowed their work rather than augmenting it
- Equipment logistics (camera placement, cable management) created physical barriers

### 3. Automation Bias
- Nurses felt unable to override AI recommendations even when they suspected errors
- Lack of training on when and how to disagree with the system
- AI framed as authoritative; nurses lacked the conceptual tools to challenge it

### 4. Patient Confusion
- Patients were not informed about the AI's role; many thought the camera was a standard test
- Some patients were confused or distressed by AI-generated referrals they didn't understand

### 5. Trust Miscalibration
- No tools provided to help nurses understand when AI output was reliable vs. uncertain
- Nurses either over-trusted or wholesale rejected the system — no calibrated middle ground

## Core Finding
> A system achieving near-human benchmark performance can fail systemically in real clinical deployment due to socio-environmental factors — not model limitations.

## Theoretical Significance
- Provides empirical grounding for the [[AI Ground Truth]] problem in a deployed setting
- Confirms [[Human-AI Synergy]] finding: combining AI and humans does not automatically improve outcomes
- Strongest real-world counterexample to benchmark-only AI evaluation

## Cross-references
- [[Emma Beede]]
- [[Human-Centered AI Evaluation]]
- [[AI Ground Truth]]
- [[Human-AI Synergy]]
- [[AI vs. Clinicians — Nagendran et al. 2020]]
- [[Deep Learning in Medical Imaging]]
