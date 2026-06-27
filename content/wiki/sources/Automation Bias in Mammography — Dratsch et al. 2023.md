---
title: "Automation Bias in Mammography — Dratsch et al. 2023"
aliases: ["Automation Bias in Mammography — Dratsch et al. 2023"]
type: source
tags: [automation-bias, mammography, radiology, RCT, BI-RADS, reader-performance]
created: 2026-06-27
updated: 2026-06-27
sources: [2023-dratsch-automation-bias-mammography]
---

**Citation:** Dratsch, T., Chen, X., Feyer, D., Morelli, J. N., Schöneck, M., Dratsch, C., Siedek, F., Krug, K. B., Persigehl, T., & Borggrefe, J. (2023). Automation bias in mammography: The impact of artificial intelligence BI-RADS suggestions on reader performance. *Radiology*, 307(5), e222176. DOI: 10.1148/radiol.222176

**Raw file:** `Dratsch-2023-Automation-bias-in-mammography-th.pdf` (also: `dratsch-et-al-2023-automation-bias-in-mammogra.pdf` — duplicate)

## Summary
Prospective RCT directly measuring automation bias in radiologist mammography reading when an AI system provides BI-RADS category suggestions. Provides empirical evidence of automation bias in a real clinical imaging context — the clearest in-vivo demonstration in this wiki's literature.

## Study Design
- Design: RCT, crossover
- Participants: 24 radiologists (varying experience)
- Task: Mammography reading — assign BI-RADS category
- Condition 1: Without AI suggestion
- Condition 2: With AI suggestion (AI assigned a BI-RADS category before radiologist read)
- Outcome: Agreement with AI; change in reading from correct to incorrect (commission errors); detection rates

## Key Findings

| Outcome | With AI | Without AI |
|---------|---------|------------|
| Cases where correct radiologist decision changed to follow wrong AI | Significantly higher | Baseline |
| Sensitivity | Modified by AI suggestion direction | Baseline |
| Specificity | Modified by AI suggestion direction | Baseline |

**Headline**: When AI provided an incorrect BI-RADS suggestion, radiologists significantly increased their rate of following the incorrect suggestion (commission errors). This is the direct manifestation of automation bias predicted by [[Automation Bias Systematic Review — Goddard et al. 2012]].

> [!important]
> Both junior and senior radiologists showed the effect. Experience did not protect against automation bias in this task.

## Implication
- Merely adding AI suggestions to a radiologist's workflow creates automation bias risk, even when the radiologist is nominally "in control"
- This is a strong argument for [[AI-Human Role Separation]]: if AI and radiologist operate on the same task, bias is almost certain
- Design implications: consider showing AI outputs only after radiologist makes independent assessment (AI as check, not first input)

## Cross-references
- [[Automation Bias]]
- [[Automation Bias Systematic Review — Goddard et al. 2012]]
- [[AI-Human Role Separation]]
- [[Trust in Automation]]
- [[Deep Learning in Medical Imaging]]
- [[Human-Centered AI Evaluation]]
