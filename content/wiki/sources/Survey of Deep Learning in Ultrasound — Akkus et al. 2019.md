---
title: "Survey of Deep Learning in Ultrasound — Akkus et al. 2019"
aliases: ["Survey of Deep Learning in Ultrasound — Akkus et al. 2019"]
type: source
tags: [deep-learning, ultrasound, survey, JACR, clinical-workflow, AI-in-ultrasound]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-akkus-survey-dl-ultrasound]
---

**Citation:** Akkus, Z., Cai, J., Boonrod, A., Zeinoddini, A., Weston, A. D., Philbrick, K. A., & Erickson, B. J. (2019). A survey of deep-learning applications in ultrasound: Artificial intelligence–powered ultrasound for improving clinical workflow. *Journal of the American College of Radiology*, 16(9 Pt B), 1318–1328. DOI: 10.1016/j.jacr.2019.06.004

**Raw file:** `Akkus et al. - 2019 - A Survey of Deep-Learnin.pdf`

## Summary
Comprehensive survey of DL applications across all domains of clinical ultrasound at 2019 state of the art. Covers the full range from image quality enhancement to automated reporting. Published in JACR — written for a radiological/clinical audience, not a technical one.

## Application Categories Surveyed

| Category | Examples | Maturity (2019) |
|----------|---------|----------------|
| Image quality | Noise reduction, super-resolution | Research/emerging |
| Segmentation | Organ boundaries, lesion delineation | Active research, some clinical |
| Classification | Liver lesion type, thyroid nodule TIRADS | Competitive with experts in controlled studies |
| Plane detection | Standard fetal planes, cardiac views | Commercially available |
| Biometry | Fetal measurements, organ sizing | Commercially available |
| Lesion detection | Breast mass, hepatic lesion | Research |
| Report generation | Automated structured reporting | Emerging |

## Key Observations
- Ultrasound presents unique DL challenges: acoustic noise, operator dependence, real-time requirements, high site-to-site variability
- Transfer learning from natural images (ImageNet) is widely used but may not capture ultrasound-specific features
- Most validation studies use single-centre data — cross-site generalisation is a consistent weakness

## Workflow Integration Models
Three models described:
1. **AI-first**: AI processes image, presents result to clinician
2. **Real-time guidance**: AI guides acquisition, not interpretation
3. **Background quality control**: AI monitors image quality during scanning, alerts operator

[[PROMETHEUS RCT — Day et al. 2025]] implements model 2 (real-time guidance) — the most studied model by 2025.

## Cross-references
- [[AI in Sonography]]
- [[Deep Learning in Medical Imaging]]
- [[PROMETHEUS RCT — Day et al. 2025]]
- [[AI in Obstetric Ultrasound — Drukker et al. 2020]]
