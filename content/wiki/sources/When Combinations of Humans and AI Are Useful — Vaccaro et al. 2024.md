---
title: "When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024"
aliases: ["When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024"]
type: source
tags: [human-ai-collaboration, meta-analysis, synergy, decision-making, generative-ai]
created: 2026-06-22
updated: 2026-06-22
sources: [2024-12-vaccaro-human-ai-meta-analysis]
---

# When Combinations of Humans and AI Are Useful: A Systematic Review and Meta-Analysis

**Authors**: [[Michelle Vaccaro]], Abdullah Almaatouq, [[Thomas Malone]]
**Published**: *Nature Human Behaviour*, Vol. 8, December 2024, pp. 2293–2303
**DOI**: 10.1038/s41562-024-02024-1
**Affiliation**: [[MIT Center for Collective Intelligence]]
**Raw file**: `raw/2024-12-vaccaro-human-ai-meta-analysis.pdf`

---

## Summary

A preregistered systematic review and meta-analysis asking: **when do human–AI combinations outperform either alone?** Analysed 106 experiments (370 effect sizes) from 74 papers published Jan 2020–Jun 2023, drawn from ACM DL, Web of Science, and AIS eLibrary.

---

## Key Definitions

- **[[Human-AI Synergy]]** (strong form): human–AI group outperforms *both* human alone *and* AI alone.
- **[[Human Augmentation]]**: human–AI group outperforms human alone (weaker baseline).

> [!important]
> Most prior work studied human augmentation. This paper insists on the stronger test — synergy — because if you just want the best outcome, you'd use whichever single agent is better.

---

## Core Findings

### 1. Overall: No Synergy on Average
- Human–AI synergy effect: **g = −0.23** (95% CI: −0.39 to −0.07; p = 0.005) — significantly *negative*
- Human augmentation effect: **g = 0.64** (95% CI: 0.53 to 0.74; p < 0.001) — significantly *positive*
- **Interpretation**: Human–AI systems were better than humans alone but worse than whichever of human/AI performed best alone.

### 2. Task Type Moderates Synergy (p = 0.006)
| Task Type | n | Synergy g | Interpretation |
|-----------|---|-----------|----------------|
| Decision tasks | 344 | −0.27 (sig.) | Performance loss |
| Creation tasks | 34 | +0.19 (not sig.) | Performance gain |

- ~85% of studied effect sizes were decision tasks; only ~10% creation tasks.
- Creation tasks (open-ended, generative) show promising gains — understudied area.

### 3. Relative Human/AI Performance Is the Strongest Moderator (p < 0.001)
| Condition | Synergy g | Interpretation |
|-----------|-----------|----------------|
| Human > AI alone | +0.46 (sig.) | Synergy exists |
| AI > Human alone | −0.54 (sig.) | Substantial loss |

**Hypothesis**: When humans are better overall, they are also better at *knowing when to trust the AI*, producing synergy. When AI is better, humans are poor judges of when to defer, creating drag.

### 4. Surprising Non-Results
The following moderators were **not statistically significant**:
- AI explanation provided (yes/no)
- AI confidence score displayed (yes/no)
- Expert vs. non-expert participants
- Division of labour structure (only 3 experiments tested this)

> [!warning]
> Much HCI research has focused on explanations and confidence displays. This meta-analysis finds neither helps on average — calls into question a major research focus.

### 5. Other Significant Moderators
- **AI type**: Deep learning vs. shallow ML vs. Wizard of Oz (p = 0.026 for synergy)
- **Year of publication**: Trend across 2020–2023 (p = 0.015)
- **Data type**: Image/text/numeric/etc. (p < 0.001 for both outcomes)

---

## Methods

- **Search period**: Jan 2020 – Jun 2023
- **Inclusion criteria**: Original experiment reporting human alone + AI alone + human–AI performance quantitatively
- **Effect size**: Hedges' g (unitless, bias-corrected standardized mean difference)
- **Model**: Three-level random-effects meta-analytic model; cluster-robust standard errors
- **Bias tests**: Funnel plots, Egger's regression, rank correlation — no evidence of publication bias for synergy; *potential bias detected for human augmentation* (towards positive results)

---

## Implications and Roadmap

1. **Prioritize creation tasks** — generative AI research should focus here; current literature is sparse
2. **Design better task allocation processes** — only 3 experiments tested predetermined subtask division; these showed positive (though non-significant) synergy
3. **Richer evaluation metrics** — single accuracy scores miss cost of rare errors; composite metrics needed
4. **Commensurability criteria** — standardized benchmarks, reporting guidelines, and open data repositories needed for the field

---

## Limitations

- Only includes studies that reported all three conditions (human alone, AI alone, human–AI) — excludes tasks impossible without one partner
- Variation in study quality, participant pools, and stimulus sets
- High residual heterogeneity (I² = 97.7%) — unexplained moderators remain
- Research topic selection bias: lab studies may not reflect real-world deployments

---

## Related Pages
- [[Human-AI Synergy]] — core concept page
- [[MIT Center for Collective Intelligence]]
