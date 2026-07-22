<div align="center">

<img src="assets/banner.png" alt="Bike Dekho — Who Actually Buys the Bike?" width="100%">

# 🚲 Bike Dekho — Bike Sales Analysis

**A data-storytelling deep dive into 1,000 customers, uncovering who actually buys a bike — and why.**

![Status](https://img.shields.io/badge/status-complete-brightgreen)
![Python](https://img.shields.io/badge/python-pandas%20%7C%20matplotlib-3776AB?logo=python&logoColor=white)
![Records](https://img.shields.io/badge/records-1%2C000-blue)
![Conversion](https://img.shields.io/badge/conversion%20rate-48.1%25-E8704A)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

[Report](Bike_Dekho_Sales_Analysis_Report.pdf) ·
[Video](Bike_Dekho_Story_Slideshow.mp4) ·
[Script](Bike_Dekho_Video_Script_Storyboard.md) ·
[Dataset](1784647314056_Bike_Dekho___Bike_Sales_Analysis.xlsx)

</div>

---

> 💡 **TL;DR** — 48.1% of customers bought a bike overall. That average hides two very different
> personas: one converting at **60–75%**, the other at **22–30%** — driven far more by geography,
> life stage, and commute patterns than by income.

## 📑 Contents

- [Repository Contents](#-repository-contents)
- [Dataset](#-dataset)
- [Key Findings](#-key-findings)
- [Meet the Personas](#-meet-the-personas)
- [Methodology](#️-methodology)
- [Video](#-video)
- [Limitations](#️-limitations)
- [Author](#️-author)

---

## 📁 Repository Contents

| File | Description |
|---|---|
| `Bike_Dekho_Sales_Analysis_Report.pdf` | 7-page narrative report with charts, personas, and recommendations |
| `Bike_Dekho_Story_Slideshow.mp4` | 145-second narrated video walkthrough of the analysis |
| `Bike_Dekho_Video_Script_Storyboard.md` | Scene-by-scene script/storyboard used to produce the video |
| `1784647314056_Bike_Dekho___Bike_Sales_Analysis.xlsx` | Source workbook (raw data, cleaned data, pivot tables, dashboard) |
| `assets/` | Charts and images used in this README |

---

## 📊 Dataset

The source workbook contains four sheets:

| Sheet | Contents |
|---|---|
| `bike_buyers-RAW` | Original, unprocessed customer records (1,026 rows) |
| `bike_buyers-clean_formula` | Cleaned dataset used for analysis (1,000 rows × 16 columns) |
| `PIVOT TABLE` | Pre-built pivot summaries by region and other cuts |
| `Dashboard` | Existing Excel dashboard/chart view |

**Columns:** Marital Status, Gender, Income, Children, Education, Occupation, Home Owner, Cars,
Commute Distance, Region, Age, Purchased Bike, Age Band, Income Band, Bought flag

---

## 🔑 Key Findings

<div align="center">
<img src="assets/donut.png" alt="48.1% overall conversion" width="260">
</div>

<table>
<tr>
<td width="50%" valign="top">

<img src="assets/region.png" alt="Purchase rate by region" width="100%">

**Geography sets the baseline** — the Pacific region converts at **58.9%**, while North America
(the largest market, 508 customers) trails at just **43.3%**.

</td>
<td width="50%" valign="top">

<img src="assets/age.png" alt="Purchase rate by age band" width="100%">

**Life stage matters most** — purchase interest peaks at ages **36–45 (58%)** and declines
steadily afterward, falling to less than half that by age 65+.

</td>
</tr>
</table>

<div align="center">
<img src="assets/income.png" alt="Purchase rate by income band" width="60%">
</div>

**Income is not the driver you'd expect** — the mid-tier **30–50K band converts best (56.7%)**,
outperforming every bracket above it. Higher income correlates with more car ownership, which
*suppresses* bike purchases rather than boosting them.

| Insight | Detail |
|---|---|
| 🎯 Overall conversion | 48.1% (481 / 1,000 customers) |
| 🌏 Best-converting region | Pacific — 58.9% |
| 🌎 Weakest-converting region | North America — 43.3% |
| 🎂 Age effect | Peaks at 36–45 (58%), declines steadily after |
| 🚗 Household effect | 0–1 car + <5 mile commute → 55–61%; 2+ cars → ~35% |
| 💰 Income effect | 30–50K band converts best — *not* the top bracket |

---

## 👥 Meet the Personas

| | 🟢 The Independent Professional | 🟠 The Settled Commuter |
|---|---|---|
| **Profile** | Single, mid-30s to mid-40s, Pacific region, 30–50K income, Bachelor's degree, 0–1 cars, short commute | Married, 4–5 children, 56+, North America, 3–4 cars, top-bracket income, long commute |
| **Conversion rate** | **60–75%** | **22–30%** |

> **Bottom line:** Bike Dekho doesn't have a demand problem — it has a targeting problem.

---

## 🛠️ Methodology

```
1. Data cleaning       →  standardized bike_buyers-RAW into bike_buyers-clean_formula
2. Exploratory analysis →  pandas group-by / cross-tab purchase-rate calculations
                           across every customer attribute
3. Visualization        →  matplotlib charts, consistent brand palette
4. Reporting             →  HTML → PDF via wkhtmltopdf
5. Video production      →  10-scene storyboard → animated slideshow via ffmpeg
```

Cross-referencing attributes (e.g. income × car ownership × purchase rate) surfaced compounding
patterns that single-variable analysis missed — this is what revealed the income/car-ownership
relationship above.

---

## 🎥 Video

`Bike_Dekho_Story_Slideshow.mp4` — a silent, fully-timed 1080p video (self-intro + 9 data-story
scenes, 145 seconds total). Pair it with `Bike_Dekho_Video_Script_Storyboard.md` for narration,
add a light music bed, burn in captions, and it's ready to publish.

---

## ⚠️ Limitations

- All findings are **correlational**, drawn from a single cross-sectional dataset — no causal
  claims are implied.
- Region labels (Europe, North America, Pacific) are as provided in the source data.
- Some cross-tab segments (e.g. 5-children households) have small sample sizes and should be
  read as directional, not statistically robust.

---

<div align="center">

## ✍️ Author

**Santanu Pathak** · Intern

*Feedback and suggestions welcome — feel free to open an issue or reach out.*

</div>
