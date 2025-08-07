# 🧠 MindBridge Data Science Challenge – 3rd Place Submission 🥉

> **Top 3 Winner** of the national **MindBridge x Carleton Data Science Challenge 2025**  
> Tasked with building a **real-world financial anomaly detection system** using AI  
> Outperformed dozens of participants across Canada with a fully engineered, optimized, and explainable solution

---

## 🚨 The Problem: Detecting Anomalies in 170,000+ Credit Card Transactions

The dataset presented two real-world challenges:

1. **Fraudulent Transactions (~0.17%)**
2. **Digit Pattern Anomalies (~0.01%)**

Both anomalies are **extremely rare**, and undetectable through surface-level modeling. The challenge required not just technical implementation—but thoughtful design, responsible evaluation, and creative feature engineering.

---

## 🧠 My Solution: Precision Meets Strategy

I built an end-to-end ML pipeline focused on **maximizing fraud detection performance while integrating subtle digit anomaly signals**, without degrading reliability.

**Key Components:**

- ✅ **Baseline XGBoost model** with `aucpr` optimization  
- ✅ **Advanced Feature Generator** using KMeans, PCA, IsolationForest, and handcrafted statistical features  
- ✅ **Smart bonus-only ensemble logic** — adds digit anomaly signal *only when confident*  
- ✅ **50-trial Optuna sweep** for best fraud model performance  
- ✅ **Leakage-free design** with clean train/test splits and modular code

---

## 📈 Final Results (Verified)

| Metric                    | Score     |
|---------------------------|-----------|
| **Fraud Detection AP**    | **0.8364** (vs. 0.82 Baseline)
| **Digit Anomaly AP**      | 0.0682  
| **Improvement**           | +1.6% PR-AUC over baseline  

This improvement may seem modest—**but in high-stakes financial domains, every fractional lift in AP translates to real-world impact.**

---

## 📊 Why Precision-Recall over Accuracy?

In fraud detection, **accuracy is misleading**. A model that predicts “no fraud” 100% of the time is still ~99.8% accurate—and utterly useless.

That’s why I focused on **Precision-Recall AUC (PR-AUC)**:

- **Precision** = How often am I right when I flag fraud?  
- **Recall** = How many real frauds did I catch?  
- **PR-AUC** = A robust signal of real-world usefulness in **imbalanced data scenarios**

This is not just a model—it’s a **system designed with real business constraints in mind**.

---

## ⚙️ Highlights from the Pipeline

- 🔍 **Over 40 engineered features**: Roundness, time-of-day, behavioral clusters, V-feature stats  
- 🔒 **Leakage prevention** through clean splits and isolated transformations  
- 🧠 **Ensemble design prioritizes conservatism**: bonuses for digit anomalies only applied with high confidence  
- 📉 **Transparent metrics**: All evaluation done on unseen holdout data

---

## 💬 Lessons Learned

- Feature engineering is a *force multiplier* in fraud detection  
- Digit anomaly detection is a **needle-in-haystack** problem requiring smart targeting  
- Model interpretability and restraint matter more than leaderboard gaming  
- Grit, not perfection, drives results—I entered unsure, and placed top 3 by building, learning, and iterating fast

---

## 🙋‍♂️ About Me

**Ahmed Elnimah**  
📍 B.Comp. Honours Computer Science (Co-op), Carleton University  
🏆 3rd Place – 2025 MindBridge AI Challenge  
🔍 Interests: AI + FinTech, interpretable ML, systems that solve real-world problems  
📫 [linkedin.com/in/ahmedelnimah](https://linkedin.com/in/ahmedelnimah)

> _“I didn’t go in as an expert—I built my way into the top 3 by staying curious, intentional, and relentless.”_

---

