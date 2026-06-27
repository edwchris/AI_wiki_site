---
title: "High-Performance Medicine — Topol 2019"
aliases: ["High-Performance Medicine — Topol 2019"]
type: source
tags: [ai-medicine, deep-learning, medical-imaging, clinical-ai, radiology, overview, high-performance-medicine]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-topol-high-performance-medicine]
---

# High-Performance Medicine — Topol 2019

**Full citation:** Topol EJ. High-performance medicine: the convergence of human and artificial intelligence. *Nat Med*. 2019;25:44–56.

**DOI:** 10.1038/s41591-018-0300-7

---

## What it is

A major review of the state of AI in medicine as of 2018–19 by Eric Topol. Comprehensive survey of published AI studies across clinical specialties; defines the opportunity, the evidence base, and the barriers. Coined or popularised the concept of "AI chasm."

## Three levels of impact

Topol frames AI impacts at three levels:

1. **Clinicians** — primarily rapid, accurate image interpretation
   - Radiology: chest X-ray, CT, MRI, mammography, fracture detection
   - Pathology: WSI breast/lung cancer, tumour classification
   - Dermatology: melanoma/carcinoma classification (AUC ~0.94–0.96)
   - Ophthalmology: diabetic retinopathy (AUC 0.99), AMD, OCT (AUC 0.999)
   - Cardiology: arrhythmia, echocardiogram view/classification
   - Gastroenterology: real-time polyp detection (94% accuracy)

2. **Health systems** — workflow, efficiency, prediction
   - EHR-based outcome prediction: readmission, mortality, AKI, sepsis
   - Machine vision for handwashing monitoring, fall risk, ICU weaning
   - "Digital twins" concept: aggregate biologic data to inform individual decisions

3. **Patients** — direct-to-consumer, self-monitoring
   - FDA-approved smartwatch algorithm for atrial fibrillation
   - Smartphone-based diagnosis (skin lesions, retinal disease)
   - Continuous glucose monitoring + AI dietary guidance

## The AI Chasm

> [!important] An algorithm with an AUC of 0.99 is not worth very much if it is not proven to improve clinical outcomes.

Topol and Keane introduced "AI chasm" — the gap between demonstrating algorithmic accuracy and demonstrating clinical utility/improved outcomes. Almost no prospective real-world studies existed at time of writing.

## Limitations acknowledged

- **Bias**: training sets lack minority representation (e.g., dermatology lacks dark skin tones)
- **Privacy and security**: hacking risk, identity reconstruction from genomic/retinal data
- **Black box**: opacity demands → EU GDPR "right to explanation" requirement
- **Hype**: IBM Watson for Oncology recommended dangerous treatment combinations
- **Validation gap**: most studies retrospective; very few prospective real-world trials

## Autonomy analogy

Topol uses the SAE autonomous vehicle scale (Levels 0–5) as an analogy:
- Medicine unlikely to exceed **Level 3** (conditional automation requiring human oversight)
- Full autonomy in medicine seems "especially far-fetched" for complex clinical decisions

## Key quote

> "The current limitations... along with the future directions of these applications will be discussed in this article. Over time, marked improvements in accuracy, productivity, and workflow will likely be actualized, but whether that will be used to improve the patient–doctor relationship or facilitate its erosion remains to be seen."

## Connections

- [[Deep Learning in Medical Imaging]] — direct overlap; Topol surveys the evidence base
- [[AI in Sonography]] — sonography applications appear in radiology/cardiology sections
- [[Automation Bias]] — not discussed explicitly, but implicit in the autonomy-level framing
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — companion paper by Google team addressing the same translation challenges
- [[Stop Explaining Black Box ML — Rudin 2019]] — counterpoint on black-box models specifically
- [[AI Chasm]] — concept referenced; no dedicated page yet

## Significance

Widely cited as foundational overview of clinical AI; frequently referenced as evidence that AI can match clinicians in image interpretation tasks. Also notable for the honest appraisal of what remains unproven, and for framing AI as a convergence with (not replacement of) human intelligence.
