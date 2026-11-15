---
section: projects
issue: "No. 03"
---
# Projects

<!-- Featured projects: each gets a homepage carousel slot + its own page.
     Assets go in assets/projects/<slug>/ : cover.jpg, loop.mp4 (≤ a few MB), screenshots. -->

## Knowledge-Guided World Models for Irrigation Control
- **Slug:** irrigation-world-models
- **Year:** 2026
- **Role:** Researcher
- **Tags:** Model-based RL, World models, MPC, Agriculture
- **One-liner:** Teaching a planner to water crops with a world model that respects physics.
- **Links:** TODO

### Story
Long-horizon irrigation planning is costly to simulate and hard to learn from scratch. I built a model-based reinforcement-learning framework that pairs the DNDC process-based crop simulator with a learned, differentiable world model. I compared a black-box RNN dynamics model against a knowledge-guided surrogate with mechanistic inductive biases and soft physical constraints, then planned in closed loop with CEM-based Model Predictive Control. DNDC served as a high-fidelity oracle to evaluate multi-step rollout stability and the trade-off between yield and water use.
<!-- TODO: add headline result once available. -->

## Self-Supervised Vision (DINOv2-style)
- **Slug:** ssl-vision
- **Year:** 2025
- **Role:** Researcher
- **Tags:** Self-supervised learning, ViT, Computer vision
- **One-liner:** Learning to see from 860K images — no labels.
- **Links:** TODO

### Story
The goal: learn transferable image representations without any labeled pretraining data. I implemented a DINOv2-style teacher–student Vision Transformer with masked patch prediction and representation regularization, and pretrained it on 860K+ unlabeled images under architectural constraints. The learned features were evaluated by frozen linear probing across several classification benchmarks, showing stable, consistent transfer.

## Recalled Experiences of Death — NYU Langone Capstone
- **Slug:** red-classification
- **Year:** 2025
- **Role:** Capstone team member
- **Tags:** NLP, LLMs, Hierarchical classification, Healthcare
- **One-liner:** Mapping near-death narratives into 6 themes and 52 subthemes.
- **Links:** TODO

### Story
With NYU Langone, we built a hierarchical NLP framework that classifies near-death experience narratives into 6 primary themes and 52 fine-grained subthemes, using GPT-API annotation validated by domain experts. I curated and denoised 8,620 sentence-level annotations — standardizing the multi-label taxonomy and removing low-signal categories — which lifted baseline accuracy from 0.42 to 0.85. The next stage is a supervised fine-tuning pipeline with OpenAI and open-source LLMs that produces structured thematic output from multi-sentence narratives while keeping context intact.

## Dissecting RWKV-7
- **Slug:** rwkv-dissection
- **Year:** 2025
- **Role:** Co-author
- **Tags:** Interpretability, Long context, RNN-LLMs
- **One-liner:** How a recurrent LLM remembers long contexts, layer by layer.
- **Links:** TODO (blog post)

### Story
We evaluated RWKV-7 models from 0.1B to 2.9B parameters on long-context benchmarks (QuALITY, MuSiQue), measuring accuracy, robustness to distractors, and sensitivity to few-shot ordering. I helped build the analysis pipeline — activation-distribution shifts, sparsity and entropy diagnostics, token attribution with Integrated Gradients and Transformer-LRP — and studied per-layer decay divergence, temporal expressivity, and memory-persistence curves to understand how RWKV-7 encodes long context. I co-wrote the accompanying blog on RWKV's evolution.

## Mitigating Anchoring Bias in LLMs
- **Slug:** anchoring-bias
- **Year:** 2025
- **Role:** Researcher
- **Tags:** LLMs, Bias, LoRA, Prompting
- **One-liner:** Prompting plus LoRA to un-anchor language models.
- **Links:** TODO

### Story
Large language models, like people, get pulled toward the first number they see. I combined prompt techniques (Chain-of-Thought, few-shot) with LoRA fine-tuning to reduce anchoring bias, built an expanded set of 30,000 test cases, and evaluated mitigation strategies across Llama 3.2 1B and Llama 3.1 8B using established benchmarks and treatment–control comparisons.

---

## Archive
<!-- Smaller projects: shown as a compact list, no dedicated page. -->
- **Assessing Professor Effectiveness** (2024) — Regression and significance testing on student ratings; examined gender bias with Welch t-tests and bootstrapping.
- **News Category Classification: Random Forest vs. DistilBERT** (2023) — 210K+ HuffPost headlines; inspired by manual news tagging at Deloitte.
- **Movie Recommender Optimization** (2023) — Regularized matrix factorization plus user clustering for targeted campaigns.
- **World Happiness Analysis** (2023) — Linear-kernel SVR on 2008–2023 Life Ladder data, R² 0.89.
- **Interactive ML Exhibit** (2023) — Explaining recommender systems to kids, freshmen, and Spanish-speaking parents.
- **Melbourne Temperature Forecasting** (2023) — SARIMA(0,1,2)×(0,1,1)₁₂ on ten years of daily data.
- **Gaucho AI Alignment** (2024) — Reading group; rebuilt GPT-2 in PyTorch.
