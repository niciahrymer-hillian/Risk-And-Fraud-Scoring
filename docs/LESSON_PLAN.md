# 📖 Lesson Plan — Risk-And-Fraud-Scoring

> **Chain S — FinTech Engineering** | Score transactions for fraud risk: features, rules vs models, class imbalance, and the precision/recall tradeoff that decides who gets blocked.

## What This Project Is

Build a fraud model on heavily imbalanced data and confront the fact that the decision threshold is a business and ethical choice, not a modeling one.

## Learning Objectives

By the end I can:

1. Explain why **accuracy** is meaningless under severe class imbalance.
2. Engineer velocity, geography, device, and deviation features.
3. Compare a rules engine with a learned model, and know when each wins.
4. Evaluate with **precision/recall and PR curves** rather than ROC alone.
5. Choose a threshold from the cost of each error type.
6. Check whether false positives fall unevenly across groups.

## Software You Will Use

- Python, pandas, scikit-learn.
- XGBoost or LightGBM.
- imbalanced-learn for resampling.
- A public fraud dataset.

## Build Order

1. Explore the data; quantify the imbalance.
2. Build a naive baseline and show its high accuracy is worthless.
3. Engineer behavioural features.
4. Train a model with class weighting; evaluate with PR curves.
5. Price false positives and false negatives; choose a threshold from that.
6. Audit error rates across subgroups.

## Common Mistakes to Avoid

- Reporting accuracy on a 1000:1 imbalance.
- Using ROC-AUC alone when the positive class is tiny.
- Leaking future information (e.g. a chargeback flag) into features.
- Setting a threshold at 0.5 by default with no business reasoning.
- Never checking who the false positives land on.

## Check Your Understanding

The quiz covers class imbalance, PR vs ROC curves, threshold selection by cost, and leakage in fraud features.

## Why This Matters (Industry Application)

Every bank, payment processor, marketplace, and insurer runs risk scoring, and it's a well-paid
specialization. The transferable lesson — imbalanced classification, threshold selection, precision/recall
under real business costs — shows up in medical screening, content moderation, and anywhere a rare event
matters more than overall accuracy.

## Reflection Questions

- What is the human cost of a false positive here, and does your threshold reflect it?
- How would you explain a declined transaction to the customer it wrongly blocked?
