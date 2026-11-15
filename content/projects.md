---
section: projects
issue: "No. 03"
---
# Projects

<!-- Each project gets a homepage carousel slot + its own page.
     Assets go in assets/projects/<slug>/ : cover.jpg, loop.mp4 (≤ a few MB), screenshots. -->

## SKU Demand Forecasting & Replenishment
- **Slug:** replenishment-tool
- **Year:** 2025
- **Role:** Sole builder (at Buzzdglobal)
- **Tags:** Forecasting, Supply chain, Python
- **One-liner:** Weekly reorders for 35 SKUs across a 72-day ocean lead time.
- **Links:** none (internal tool)

### Story
Ordering from China means committing 72 days before stock lands. I built a Python tool that reconciles warehouse inventory with orders from several stores, forecasts demand per SKU with a growth-rate model, and sets reorder points for weekly replenishment of 35 SKUs (30,000+ units). A days-of-stock model with in-transit ETAs and tiered safety stock replaced gut-feel reorders, and along the way it surfaced a data error: sample shipments were being counted as sales during promotions.
<!-- Showcase idea: anonymized dashboard screenshots / a stock-curve animation for the loop video. -->

## Continual Policy Adaptation for Language Agents
- **Slug:** clin-scienceworld
- **Year:** 2026
- **Role:** Researcher (NYU)
- **Tags:** LLM agents, Continual learning, Ablation study
- **One-liner:** 4,800 runs to find what makes an agent learn from its own memory.
- **Links:** TODO

### Story
CLIN is a continual-learning agent that improves from persistent text memory rather than gradient updates. I reproduced it on the ScienceWorld benchmark and ran a 12-configuration ablation (400 episodes each, 4,800 runs) to find which components drive cross-episode learning. The best configuration (Q2 + Failure Abstraction) raised the average score by 9.4 points, cut the fatal-error rate from 24.4% to 11.3%, and lifted the gold-trace rate from 43% to 60%.

## Recalled Experiences of Death: NYU Langone Capstone
- **Slug:** red-classification
- **Year:** 2025
- **Role:** Capstone team member
- **Tags:** NLP, LLMs, Hierarchical classification, Healthcare
- **One-liner:** Sorting clinical narratives into 6 themes and 52 subthemes.
- **Links:** TODO

### Story
With NYU Langone, we built a hierarchical NLP framework that classifies clinical narratives into 6 themes and 52 subthemes, using GPT-API annotation checked by clinicians. I curated 8,620 sentence-level labels, which raised accuracy from a 0.42 baseline to 0.85.

## Rating Bias & Drivers: 52K RateMyProfessors Records
- **Slug:** rating-bias
- **Year:** 2024
- **Role:** Analyst (NYU)
- **Tags:** Statistics, Hypothesis testing, Regression
- **One-liner:** Significant, but negligible: what 52K ratings say about gender bias.
- **Links:** TODO

### Story
Using Welch t-tests and 10,000-iteration bootstrap confidence intervals (α = 0.005), I tested 52K professor ratings for gender bias. The gap was statistically significant (p ≈ 4e-12) but negligible in practice: 0.067 stars, Cohen's d 0.06. To model what drives ratings, I used Linear, Ridge and Lasso regression, required at least 6 ratings per professor to reduce small-sample noise, and imputed a feature missing 86% of its values, raising test R² from 0.50 to 0.65.
