---
title: "Levels of Automation"
aliases: ["Levels of Automation"]
type: concept
tags: [levels-of-automation, human-factors, automation, supervisory-control, AI-design]
created: 2026-06-27
updated: 2026-06-27
sources: [2000-parasuraman-sheridan-wickens-levels-automation]
---

# Levels of Automation

A taxonomy of how much autonomy an automated system exercises, ranging from full human control to full machine control. Developed by Parasuraman, Sheridan, and Wickens (2000). Essential framework for AI system design and evaluation.

---

## The 10-Level Scale (Sheridan & Verplanck 1978; Parasuraman et al. 2000)

| Level | Description |
|-------|-------------|
| 1 | Computer offers no assistance; human does everything |
| 2 | Computer offers a complete set of alternatives |
| 3 | Computer narrows selection to a few alternatives |
| 4 | Computer suggests one alternative |
| **5** | **Computer executes suggestion if human approves** |
| **6** | **Computer allows human a restricted time to veto** |
| 7 | Computer executes automatically, then informs human |
| 8 | Computer informs human only if it decides to |
| 9 | Computer informs human only if asked |
| 10 | Computer acts entirely autonomously |

---

## Four Types of Automation (Parasuraman et al. 2000)

Each level applies to different cognitive functions:

| Type | Function | Example |
|------|----------|---------|
| Information acquisition | Sensing and monitoring | Auto-windowing, image reconstruction |
| Information analysis | Processing and classification | AI lesion detection |
| Decision selection | Recommending action | AI diagnosis suggestion |
| Action implementation | Executing decisions | Automated report generation |

High automation at information analysis (Level 7–8) is increasingly common; high automation at decision selection (Level 7–10) is clinically controversial.

---

## Design Implications

**Benefits of higher levels:**
- Efficiency; throughput; consistency

**Costs of higher levels:**
- [[Situation Awareness]] degradation (out-of-the-loop)
- [[Ironies of Automation]] — skill erosion; poor takeover
- [[Automation Bias]] — complacency; commission errors
- Accountability gaps

**The calibration challenge:**
The optimal level varies by task, operator expertise, time pressure, and stakes. There is no universally correct level of automation.

---

## Current AI in Medical Imaging

Most radiology AI sits at **Level 3–4** for decision selection (suggests diagnosis/triage flag); movement toward **Level 6–7** is underway (auto-flag, human can veto). Full **Level 10** is aspirational and raises fundamental accountability concerns (see [[AI Ethics in Radiology]]).

[[AI-Human Role Separation]] proposes a different architecture: rather than choosing a level for the whole task, assign specific subtasks where AI operates at **Level 9–10** (e.g., biometry) while humans operate at **Level 1** on other subtasks (diagnosis). This avoids the monitoring irony by eliminating mixed-mode operation.

---

## Related Pages
- [[A Model for Types and Levels of Human Interaction with Automation — Parasuraman et al. 2000]]
- [[Situation Awareness]]
- [[Ironies of Automation]]
- [[Trust in Automation]]
- [[Automation Bias]]
- [[AI-Human Role Separation]]
- [[AI Ethics in Radiology]]
