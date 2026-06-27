---
title: "Deep Learning in Medical Imaging"
aliases: ["Deep Learning in Medical Imaging"]
type: concept
tags: [deep-learning, medical-imaging, radiology, cnn, computer-vision, clinical-ai]
created: 2026-06-27
updated: 2026-06-27
sources: [2020-nagendran-ai-vs-clinicians, 2019-geis-ethics-ai-radiology, 2023-multisociety-ai-tools-radiology, 2020-beede-human-centered-diabetic-retinopathy]
---

Application of deep learning (primarily convolutional neural networks) to diagnostic medical image analysis; the dominant paradigm for AI in radiology, pathology, and ophthalmology.

## Core Task Types
| Task | Description | Example |
|------|-------------|---------|
| Classification | Disease present vs. absent | Diabetic retinopathy grading, pneumonia detection |
| Detection | Localize findings in image | Nodule detection on CT |
| Segmentation | Delineate anatomical structures | Organ boundaries on MRI, fetal biometry |
| Measurement | Automated quantification | Fetal biometric parameters, cardiac volumes |
| Report generation | Structured auto-report from images | Chest X-ray findings |

## Common Imaging Modalities
- Chest X-ray / CT (historically most studied)
- MRI
- Ultrasound / Echocardiography → [[AI in Sonography]]
- Ophthalmology (fundus photography, OCT)
- Whole-slide pathology imaging

## Published Claims vs. Actual Evidence
- Most published studies (≥75%) claim AI performs comparably or better than clinicians — [[AI vs. Clinicians — Nagendran et al. 2020]]
- But: studies are predominantly non-prospective, retrospective, single-institution, high risk of bias
- Real-world deployment frequently underperforms benchmark → [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]]
- The [[AI Ground Truth]] problem: performance is only as valid as the labels used to define it

## Training Data Failure Modes
- **Distribution shift**: models trained at one institution fail at others (different equipment, patient demographics)
- **Label noise**: ground truth created by expert consensus may not capture tacit diagnostic reasoning
- **Demographic bias**: underrepresentation of ethnic groups, age ranges, or comorbidities in training data
- **Covariate shift**: non-clinical image features (scanner model, contrast protocol) correlate with labels

## Workflow Integration Models
1. **Assistive**: AI flags findings; radiologist reviews → risk of automation bias → [[Human-AI Synergy]]
2. **Role separation**: AI and radiologist assigned distinct non-overlapping tasks → [[AI-Human Role Separation]]
3. **Autonomous** (limited): AI acts without human review (e.g., pre-screening filter, worklist prioritization)

## Cross-references
- [[AI Ground Truth]]
- [[AI in Sonography]]
- [[AI Ethics in Radiology]]
- [[AI-Human Role Separation]]
- [[Human-Centered AI Evaluation]]
- [[AI Implementation in Radiology]]
- [[Human-AI Synergy]]
