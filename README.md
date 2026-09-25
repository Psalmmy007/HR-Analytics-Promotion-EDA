# Workforce Analytics: Optimizing Corporate Talent Pipelines

Exploratory Data Analysis on 54,800+ employee records to identify the real drivers behind
promotion decisions at a multinational conglomerate, and surface data-driven checkpoints
to speed up a slow, manual evaluation cycle.

*(Case study dataset via 10Alytics — Apex Global Innovations Inc. is a simulated company.)*

## Business Problem

HR currently relies on lengthy manual review to decide who gets promoted, delaying
transitions into leadership roles. This analysis looks for measurable patterns in
ratings, training, and demographics that could replace part of that manual process
with an evidence-based first pass.

## What's in this repo

- `Workforce_Analytics_EDA.ipynb` — full analysis: data cleaning, univariate/bivariate/
  multivariate profiling, and visualizations, with narrative explanation throughout.
- `employee_promotion_cleaned.csv` — the cleaned dataset used in the analysis.

## Key Findings

- **Tenure and age don't predict promotion.** Despite being correlated with each other
  (0.66), neither has a meaningful relationship with `is_promoted` (~-0.02).
- **Performance signals do.** `awards_won` (0.20), `avg_training_score` (0.18), and
  `previous_year_rating` (0.16) are the strongest correlates with promotion.
- **Awards are the single biggest differentiator**: 44% promotion rate for award
  winners vs. 7.7% for everyone else.
- **A rating of 5 behaves like a threshold**, not a point on a gradient — promotion
  rate is flat across ratings 1-4, then jumps sharply at 5.
- **Rating and training score compound**: employees strong in both were promoted at
  31%, versus near-0% for employees weak in both.
- **Missing data had a structural cause, not a random one** — every missing
  `previous_year_rating` belonged to a first-year employee with no review cycle yet.

## Tools

Python · Pandas · Matplotlib · Seaborn · Jupyter

## How to Run

```bash
pip install pandas matplotlib seaborn jupyter
jupyter notebook Workforce_Analytics_EDA.ipynb
```
