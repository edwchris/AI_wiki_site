---
title: "Key Challenges for Clinical AI — Kelly et al. 2019"
aliases: ["Key Challenges for Clinical AI — Kelly et al. 2019"]
type: source
tags: [clinical-ai, implementation, generalization, dataset-shift, algorithmic-bias, explainability, ai-translation, validation]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-kelly-clinical-ai-challenges]
---

# Key Challenges for Clinical AI — Kelly et al. 2019

**Full citation:** Kelly CJ, Karthikesalingam A, Suleyman M, Corrado G, King D. Key challenges for delivering clinical impact with artificial intelligence. *BMC Med*. 2019;17:195.

**DOI:** 10.1186/s12916-019-1426-2

> [!warning] All five authors are employees of Google LLC (stated in competing interests). This does not invalidate the analysis but contextualises the framing and emphasis.

---

## What it is

A comprehensive narrative review of the practical, scientific, and ethical barriers preventing AI algorithms from achieving clinical impact, despite impressive performance metrics. Published in *BMC Medicine*. Widely cited as a balanced account of the gap between algorithmic performance and real-world clinical utility.

## The AI Chasm (framing)

Similar to [[High-Performance Medicine — Topol 2019]], Kelly et al. note that:
- Many AI studies report impressive AUC/accuracy figures
- Only ~6% of 516 eligible AI imaging studies performed external validation
- Prospective trials and randomised controlled trials are nearly absent
- Algorithm performance ≠ patient outcome improvement

## Scientific/technical challenges

### Retrospective study design
- Most studies train and evaluate on retrospective data from single institutions
- Fails to account for distribution shift, changing practice, equipment variation
- Gold standard: prospective RCTs; no AI study had published one at time of writing

### Dataset shift
- The statistical properties of clinical data change over time (new scanners, protocols, population demographics)
- A model trained on 2015 data may underperform on 2020 data even without any change in the model
- Requires continuous monitoring and revalidation

### Accidentally fitting confounders
- Algorithms may learn to predict labels from spurious features (artifacts, scanner ID, patient position, patient demographics embedded in DICOM metadata)
- Classic example: skin lesion AI that learned to detect lesions near surgical skin markers — because high-risk lesions are more likely to be photographed in clinical contexts with markers
- Cabitza's asthma example ([[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]]) is the canonical clinical case

### Generalization challenges
- Training hospital ≠ deployment hospital (equipment, protocols, patient mix, labelling culture)
- Federated learning and domain adaptation proposed but not proven at scale
- External validation on independent datasets is essential but rarely reported

### Algorithmic bias
Three-source model of bias:
1. **Model bias** — underfitting, systematic errors that affect all groups
2. **Model variance** — overfitting, poor generalisation, instability across random restarts
3. **Outcome noise** — ground truth labels are themselves noisy (inter-rater disagreement, proxy measures)

Plus structural bias in training data (mirrors historical inequalities — see [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]])

### Adversarial attacks
- Small, imperceptible pixel-level perturbations can cause misclassification (e.g., stop sign to 45 mph sign)
- Medical AI could potentially be manipulated by adversarial imaging artifacts
- No documented clinical adversarial attacks but theoretical risk

## Logistical and implementation challenges

- **Data silos**: hospital EHR systems use incompatible formats; sharing data across sites is legally and technically complex
- **Regulatory frameworks**: FDA cleared 14 AI/ML-based medical devices (as of 2019); 69 granted 510(k) clearance; most pathways rely on equivalence to existing devices rather than prospective clinical validation
- **Standardisation**: no agreed benchmark datasets, no agreed evaluation metrics, no agreed reporting standards

## Human factors challenges

- **Alert fatigue**: parallel to existing clinical decision support literature — binary alerts are largely ignored; clinicians override 91–96% of medication alerts
- **Automation bias**: clinicians may over-rely on AI recommendations even when they are wrong
- **Skills decay**: reduced interpretation practice when AI takes over detection tasks (see [[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]])

## Interpretability

Kelly et al. note an accuracy-explainability trade-off (more interpretable models are generally less accurate) — this position contrasts with [[Stop Explaining Black Box ML — Rudin 2019]], who argues the trade-off is largely a myth.

> [!warning] Contradiction: Kelly et al. state an accuracy-interpretability trade-off exists; Rudin (2019) argues this is a myth for structured data with good features. Both may be correct in different regimes: the trade-off is real for complex perceptual tasks (imaging) but not for tabular/clinical data.

## Connections

- [[Automation Bias]] — cited; key concern in human factors section
- [[Deep Learning in Medical Imaging]] — addresses the same literature base
- [[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]] — confounder-fitting and deskilling examples
- [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]] — structural bias mechanism
- [[Stop Explaining Black Box ML — Rudin 2019]] — contrasting view on interpretability trade-off
- [[High-Performance Medicine — Topol 2019]] — same "AI chasm" framing
