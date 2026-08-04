# Risk-And-Fraud-Scoring

### Score transactions for fraud risk: features, rules vs models, class imbalance, and the precision/recall tradeoff that decides who gets blocked.

![Chain S](https://img.shields.io/badge/Chain%20S-0F766E?style=for-the-badge) [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge)](LICENSE-GPL) [![License: AGPL v3](https://img.shields.io/badge/License-AGPLv3-blue?style=for-the-badge)](LICENSE-AGPL)

[📖 Lesson Plan](docs/LESSON_PLAN.md) · [🎮 Interactive Tour](docs/interactive/index.html)

<!-- SCREENSHOT PLACEHOLDER: docs/screenshots/overview.png -->

> ⬜ **Scaffold pending.** Directory created to portfolio standard; full content (README, lesson plan, tour + quiz, skeleton code) still to be built. Part of **Chain S — FinTech Engineering**.

## Why This Was Built

Fraud detection is a genuinely hard modeling problem because the classes are wildly imbalanced — maybe one
transaction in a thousand is fraudulent — so a model that predicts "not fraud" every time scores 99.9%
accurate and is completely worthless. That single fact reframes how you evaluate everything.

The other half is that the threshold is a **business decision, not a modeling one**. Block too aggressively
and you punish legitimate customers; block too little and you eat losses. I want to build the model and then
sit with that tradeoff honestly, including who gets hurt by a false positive.

## Why This Matters (Industry Application)

Every bank, payment processor, marketplace, and insurer runs risk scoring, and it's a well-paid
specialization. The transferable lesson — imbalanced classification, threshold selection, precision/recall
under real business costs — shows up in medical screening, content moderation, and anywhere a rare event
matters more than overall accuracy.

## Topics Covered

| Area | What this project covers |
|------|--------------------------|
| Class imbalance | Why accuracy lies, and resampling / class-weight approaches |
| Features | Velocity, geography, device, amount deviation, and account age |
| Rules vs models | When a simple rule beats a model — and when it stops |
| Thresholds | Precision/recall tradeoffs priced in real dollars |
| Evaluation | PR curves, AUC-PR, and cost-weighted metrics |
| Fairness | False positives fall unevenly — checking who bears them |

## How This Connects

Chain S (FinTech Engineering). Applies **ML-Modeling-Classic** and **Model-Evaluation-And-Experimentation** to a high-stakes domain; related to the screening logic in my Chain G work.

---
Dual licensed — [GPL v3](LICENSE-GPL) and [AGPL v3](LICENSE-AGPL).
