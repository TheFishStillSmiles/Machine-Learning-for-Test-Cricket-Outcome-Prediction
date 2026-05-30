# cricket_ML_internship

An interpretable machine learning pipeline specifically designed to forecast outcomes in Test Cricket (multi-day format) using historical international data spanning from 2000 to 2025. This project implements, evaluates, and compares an optimized Logistic Regression classifier (featuring a dynamic ELO rating algorithm and interaction terms) against a baseline Random Forest classifier.

📌 Project Overview & Key Research Objectives
Predicting Test Cricket outcomes presents distinct challenges compared to shorter formats (T20, ODIs). Spanning up to five days, match dynamics shift significantly due to pitch degradation, changing weather, player fatigue, and complex declarations.

This repository implements the machine learning framework designed to solve three primary research targets:

Dynamic Metric Evaluation (RQ1): Measuring how effectively an adapted ELO rating system can capture shifting team strengths over multi-decade scopes compared to traditional static metrics.

Model Trade-Offs (RQ2): Evaluating the balance between predictive power and direct transparency/interpretability when comparing linear models against ensemble architectures.

Feature Impact (RQ3): Quantifying the exact weight of venue advantage, short-term momentum (recent form), and long-term team capability (ELO gap) on modern match results.

🛠️ Key Methodological Contributions

While conventional sports analytics literature heavily skews toward shorter, limited-overs formats (T20s and ODIs) due to their uniform game states, this framework explicitly addresses the complex, multi-day landscape of international Test cricket. The repository introduces several specialized architectural syntheses and feature engineering optimizations designed to capture long-format variance:

* **Long-Format Domain Optimization:** Establishes a targeted predictive baseline engineered for five-day matches. By isolating decisive win/loss scenarios from exogenous environmental interruptions (such as persistent weather draws), the pipeline builds a clean framework optimized for analyzing structural team superiority over extended temporal horizons.
* **Bifurcated Dynamic Elo Synthesis:** Implements a customized dynamic $K$-factor ranking system tailored to international sport scheduling. Moving beyond static or volume-based updates, the engine scales rating volatility by cross-referencing an *institutional tenure decay factor* with a *localized micro-momentum coefficient* (derived from a 5-match rolling causal lag window), adapting rapidly to sudden squad transitions.
* **Synergistic Interaction Modeling:** Bridges the interpretability gap between linear models and tree-based ensembles. By introducing specialized cross-product interaction terms—such as structural ELO power differentials multiplied by temporal form momentum—the pipeline allows a highly regularized $L_2$ Logistic Regression classifier to capture non-linear, multi-variable dependencies without sacrificing exact parametric transparency.
* **Empirical Calibration of Baseline Intercepts:** Couples standardized historical metrics with full-rank team indicator vectors. The pipeline mathematically isolates and quantifies the exact structural, geographic baseline home-field advantage across Test-playing nations, providing an uncertainty-aware framework for predictive match forecasting.

---

## 📊 Model Performance & Insights

The framework evaluates and contrasts a highly optimized regularized Logistic Regression classifier against a structural Random Forest baseline across all modern Test matches from 2000 to early 2025:

| Model Architecture | Features Utilized | Prediction Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | One-Hot Encoding, Dynamic Elo ($K$-factor), Multiplicative Interaction Terms | **73.3%** |
| **Random Forest** | Nominal Metadata, Head-to-Head Records, Toss/Match Choices | **67.0%** |
