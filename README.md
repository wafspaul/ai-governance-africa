# AI Governance Africa

**A focused research project exploring AI-driven job displacement as a systemic risk in African economies.**

---

## What this project is

This is an independent research initiative investigating one specific question:

> *If AI automation displaces large numbers of workers in African economies — particularly in sectors like BPO, manufacturing, and informal trade — what are the downstream systemic risks, and what governance responses could prevent catastrophic outcomes?*

This project sits at the intersection of **AI safety**, **labour economics**, and **African political economy**. It is not a general survey of "AI in Africa." It is a focused attempt to understand a specific risk pathway and what can be done about it.

---

## Why this matters

Most AI safety research focuses on technical alignment: ensuring AI systems do what their designers intend. That is critical work. But there is a parallel risk that receives far less attention:

**What happens to societies when AI disrupts labour markets faster than institutions can adapt?**

In Kenya, 15.9 million people aged 15–64 are employed (ILO, 2022). A significant share work in sectors highly exposed to automation — data entry, customer service, routine manufacturing, and informal trade. Youth unemployment is already high. If AI accelerates job displacement without adequate governance responses, the social and political consequences could be severe and irreversible.

This is not a distant hypothetical. It is happening now, and it demands serious analysis.

---

## Focus area: Kenya (with broader Africa implications)

Kenya is the starting point because:
- It has a large and growing BPO sector directly exposed to AI automation
- It has reliable ILO and World Bank employment data available
- It exemplifies dynamics common across Sub-Saharan Africa: young population, high informality, rapid tech adoption alongside weak social safety nets
- What happens here has implications for Ethiopia, Nigeria, Ghana, Rwanda, and beyond

---

## Project structure

```
ai-governance-africa/
│
├── core-question.md                        ← The central research question (start here)
├── PLAN.md                                 ← Execution roadmap
├── CLAUDE.md                               ← Research context and working memory
├── requirements.txt                        ← Python dependencies
│
├── kenya_labour_analysis.ipynb             ← Main analysis notebook (74 cells, 8 parts)
├── automation_risk_analysis_notebook.ipynb ← Automation vulnerability analysis
│
├── essay-1/                                ← Main analytical essay
│   ├── draft.md                            ← Sections 1–3 complete (~1,200 words)
│   └── outline.md                          ← Essay scaffold and section prompts
│
├── notes/                                  ← Raw thinking, reflections, open questions
│   ├── data-observations.md
│   ├── questions-im-exploring.md
│   └── ai-safety-atlas-reflections.md
│
├── automation-vulnerability-kenya/         ← Sub-project: occupation exposure analysis
├── ai-bias-education-kenya/                ← Sub-project: gender bias in AI training data
├── ai-bias-kenyan-names/                   ← Sub-project: naming bias in AI systems
│
├── data_raw/                               ← Source data (not committed — see DATA_SOURCES.md)
│   ├── DATA_SOURCES.md                     ← Download instructions for all datasets
│   ├── ilo/                                ← ILO ILOSTAT files by category
│   └── world_bank/                         ← World Bank WDI files by indicator
│
└── outputs/                                ← Generated charts and reports
    ├── figures/
    └── reports/
```

## Reproducing the analysis

```bash
git clone https://github.com/wafspaul/ai-governance-africa.git
cd ai-governance-africa
pip install -r requirements.txt
# Download data files per data_raw/DATA_SOURCES.md
jupyter notebook kenya_labour_analysis.ipynb
```

---

## Current status

🟢 **Active research** — April 2026

| Component | Status |
|---|---|
| ILO + World Bank data analysis | ✅ Complete — 74-cell guided notebook, 8 analytical sections |
| Automation vulnerability sub-project | ✅ Complete |
| AI bias in education (gender) | ✅ Complete |
| AI bias in Kenyan names | ✅ Complete |
| Essay — Introduction + Sections 1–3 | ✅ ~1,200 words written |
| Essay — Section 4 + Conclusion | 🟡 In progress — target May 2026 |
| References | ⬜ Week 5 |
| Public release | ⬜ Target: 12 May 2026 |

Data sourced from ILO ILOSTAT (Kenya Continuous Household Survey 2022) and World Bank WDI. All analysis is original. Raw data files are not committed — see [`data_raw/DATA_SOURCES.md`](data_raw/DATA_SOURCES.md) for download instructions.

---

## About this project

This is independent research by Paul Wafula, exploring AI governance and safety from an African perspective. It is part of a broader effort to ensure that AI safety discourse includes the specific vulnerabilities and risks faced by developing economies in the Global South.

Questions, feedback, and collaboration welcome.
