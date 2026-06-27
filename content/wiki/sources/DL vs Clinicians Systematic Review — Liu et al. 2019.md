---
title: "DL vs Clinicians Systematic Review — Liu et al. 2019"
aliases: ["DL vs Clinicians Systematic Review — Liu et al. 2019"]
type: source
tags: [deep-learning, systematic-review, meta-analysis, medical-imaging, benchmark, clinician-comparison, lancet]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-liu-dl-vs-clinicians-systematic-review]
---

**Citation:** Liu, X., Faes, L., Kale, A. U., Wagner, S. K., Fu, D. J., Bruynseels, A., Mahendiran, T., Moraes, G., Shamdas, M., Kern, C., Ledsam, J. R., Schmid, M. K., Balaskas, K., Topol, E. J., Bachmann, L. M., Keane, P. A., & Denniston, A. K. (2019). A comparison of deep learning performance against health-care professionals in detecting diseases from medical imaging: a systematic review and meta-analysis. *The Lancet Digital Health*, 1(6), e271–e297. DOI: 10.1016/S2589-7500(19)30123-2

**Raw file:** `Liu et al. - 2019 - A comparison of deep learn.pdf`

## Summary
The first systematic review and meta-analysis directly comparing DL performance with health-care professionals for medical image-based disease detection. Provides the evidence base (and its limitations) for claims that AI matches or exceeds clinician performance.

## Scope
- Database search: Jan 2012–Jun 2019 (Ovid-MEDLINE, Embase, Science Citation Index, Conference Proceedings Citation Index)
- Initial hits: 19,897
- Final included: 14 studies with direct head-to-head comparisons in the same sample

## Key Findings

| Metric | Deep Learning | Health-care professionals |
|--------|--------------|--------------------------|
| Sensitivity (pooled) | 87.0% | 86.4% |
| Specificity (pooled) | 92.5% | 90.5% |

**Headline**: DL and clinicians perform approximately equivalently on narrow, well-defined imaging classification tasks.

> [!warning]
> Only 14 studies out of ~20,000 met criteria for direct, same-sample comparison. The vast majority of DL studies compare to separate test sets or historical benchmarks — not head-to-head. This is consistent with the critique in [[AI vs. Clinicians — Nagendran et al. 2020]] (BMJ).

## Methodological Findings
- Included studies had **high heterogeneity** (I² high) — pooled estimates should be interpreted cautiously
- Most studies did not pre-register their design
- Disease scope: predominantly ophthalmology (diabetic retinopathy, age-related macular degeneration) and radiology
- Few included real-world workflow conditions

## Implications
- Headline numbers ("AI = clinician") come from a very thin evidentiary base
- The gap between benchmark performance and clinical performance documented by [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]] and [[AI vs. Clinicians — Nagendran et al. 2020]] reflects the limitations of this type of comparison
- Real-world deployment is a separate research question from benchmark comparison

## Cross-references
- [[Deep Learning in Medical Imaging]]
- [[AI vs. Clinicians — Nagendran et al. 2020]]
- [[Human-Centered AI Evaluation]]
- [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]]
- [[Changing Forms and Expectations of Peer Review — Horbach and Halffman 2018]] — provides structural explanation for why peer review failed to catch the methodological problems documented here
- [[Eric Topol]]
