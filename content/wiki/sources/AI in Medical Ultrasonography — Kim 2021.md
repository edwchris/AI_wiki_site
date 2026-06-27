---
title: "AI in Medical Ultrasonography — Kim 2021"
aliases: ["AI in Medical Ultrasonography — Kim 2021"]
type: source
tags: [AI-in-ultrasound, operator-dependency, standardisation, implementation-challenges, editorial]
created: 2026-06-27
updated: 2026-06-27
sources: [2021-kim-ai-medical-ultrasonography]
---

**Citation:** Kim, Y. H. (2021). Artificial intelligence in medical ultrasonography: driving on an unpaved road. *Ultrasonography*, 40(3), 313–317. DOI: 10.14366/usg.21031

**Raw files:** `Kim - 2021 - Artificial intelligence in medica.pdf` and `usg-21031.pdf` (same paper — two copies; `usg.21031` is the DOI suffix for the Ultrasonography journal)

**Type:** Perspective/editorial

## Core Argument
Ultrasonography is uniquely difficult for AI compared to CT and MRI because **image quality depends heavily on operator skill and patient factors** — creating acquisition variability that is absent in other modalities. This "unpaved road" must be graded before AI can reliably navigate it.

## Why Ultrasound AI Is Harder
- No standardised acquisition protocol → different operators produce different images of the same patient
- Operator qualification varies widely, especially with POCUS diffusion into non-radiology settings
- Patient factors (body habitus, cooperation, acoustic window) add noise absent in other modalities
- Without controlling for input variability, AI algorithms trained on expert images fail with novice acquisitions

## Key Prerequisites Identified
1. **Standardised examination protocols** — specifying probe position, angle, and labelling conventions
2. **Operator qualification frameworks** — regulating who performs ultrasound and to what standard
3. **Clinical data integration** — combining imaging with demographics, history to improve diagnostic performance
4. **Performance feedback loops** — AI systems that tell operators when image quality is insufficient for analysis

## Applications Cited
| Domain | AI application noted |
|--------|---------------------|
| Echocardiography | Novice guidance for loop acquisition; LV ejection fraction estimation |
| Obstetrics/Gynaecology | AI introduction across fetal and pelvic imaging |
| Thyroid | Computer-aided diagnosis for nodule characterisation |
| Breast | Color Doppler + ML for cancer diagnosis |

## Risk Warning
Without standardisation and qualification frameworks first:
> "widespread AI implementation risks wasted resources, malpractice caused by misdiagnoses, and institutional burden"

## Significance
Useful as a **cautionary editorial framing** that counterbalances optimistic AI adoption narratives. Published in *Ultrasonography* (journal of Korean Society of Ultrasound in Medicine) — a practitioner-facing perspective, not a research study.

## Cross-references
- [[AI in Sonography]]
- [[Sonographer Professional Role]]
- [[Whither the Ultrasound Specialist — Finberg 2004]]
- [[AI in Obstetric Ultrasound — Drukker et al. 2020]]
- [[Survey of Deep Learning in Ultrasound — Akkus et al. 2019]]
- [[Deliberate Practice]]
- [[AI Implementation in Radiology]]
