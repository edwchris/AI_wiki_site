---
title: "Algorithm Aversion"
aliases: ["Algorithm Aversion"]
type: concept
tags: [algorithm-aversion, trust-in-automation, disuse, human-ai-interaction, forecasting, behavioral-science]
created: 2026-06-27
updated: 2026-06-27
sources: [2015-dietvorst-algorithm-aversion, 1997-parasuraman-riley-humans-automation]
---

# Algorithm Aversion

The tendency of people to irrationally abandon or reject algorithmic recommendations after witnessing a single error, even when the algorithm continues to outperform human alternatives. Coined by Dietvorst, Simmons & Massey (2015) as the opposite failure mode to [[Automation Bias]].

## Core finding

People hold algorithms to a higher standard than humans. A human forecaster and an algorithm making the same errors at the same rate are judged differently: the human is forgiven, the algorithm is abandoned.

In [[Algorithm Aversion — Dietvorst et al. 2015]]: participants who saw an algorithm err once were 74% likely to switch to a human advisor on subsequent trials; those who hadn't seen the algorithm err were 47% likely to switch. The algorithm outperformed humans throughout.

## Mechanism

- Algorithms are expected to be more reliable than humans — they violate expectations more when they fail
- Algorithm errors feel systematic (will repeat), whereas human errors feel situational (won't repeat)
- This asymmetry in attribution causes abandonment that is not warranted by the error rate

## Relationship to Automation Bias

| | Algorithm Aversion | Automation Bias |
|-|-------------------|-----------------|
| Direction | Under-reliance / disuse | Over-reliance / misuse |
| Trigger | Single witnessed error | Consistent reliability + low vigilance |
| Result | Ignoring better-performing AI | Accepting wrong AI recommendation |
| Parasuraman term | Disuse | Misuse |

Both represent miscalibrated trust — see [[Trust in Automation]].

## The agency remedy

When participants could modify algorithm outputs (even minimally), algorithm aversion reversed — they used the algorithm more. **Agency and sense of control** mediate the effect.

**Design implication:** Clinical AI tools that allow clinicians to adjust outputs before finalising decisions may achieve better adoption than tools that present outputs as binary accept/reject choices.

## Clinical relevance

- Clinicians may abandon AI systems after a single witnessed misdiagnosis, even when the system's overall accuracy remains superior to unaided judgment
- This creates an adoption paradox: transparent AI (visible errors) may be rejected; opaque AI (hidden errors) may be used uncritically
- Training programs that set realistic error-rate expectations before deployment may reduce aversion
- Participatory interface design (override/adjust options) is supported by evidence

## Connections

- [[Algorithm Aversion — Dietvorst et al. 2015]] — foundational source
- [[Berkeley Dietvorst]] — lead author; coined the term
- [[Automation Bias]] — the opposite failure mode
- [[Humans and Automation — Parasuraman and Riley 1997]] — "disuse" category in the four-outcome taxonomy
- [[Trust in Automation]] — calibration is the solution to both problems
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — algorithm aversion implicit in human factors challenges section
- [[Human-AI Synergy]] — miscalibrated trust (either direction) degrades collaborative performance
