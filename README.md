# cricket_ML_internship

An interpretable machine learning pipeline specifically designed to forecast outcomes in Test Cricket (multi-day format) using historical international data spanning from 2000 to 2025. This project implements, evaluates, and compares an optimized Logistic Regression classifier (featuring a dynamic ELO rating algorithm and interaction terms) against a baseline Random Forest classifier.

📌 Project Overview & Key Research Objectives
Predicting Test Cricket outcomes presents distinct challenges compared to shorter formats (T20, ODIs). Spanning up to five days, match dynamics shift significantly due to pitch degradation, changing weather, player fatigue, and complex declarations.

This repository implements the machine learning framework designed to solve three primary research targets:

Dynamic Metric Evaluation (RQ1): Measuring how effectively an adapted ELO rating system can capture shifting team strengths over multi-decade scopes compared to traditional static metrics.

Model Trade-Offs (RQ2): Evaluating the balance between predictive power and direct transparency/interpretability when comparing linear models against ensemble architectures.

Feature Impact (RQ3): Quantifying the exact weight of venue advantage, short-term momentum (recent form), and long-term team capability (ELO gap) on modern match results.

🛠️ Key Methodological Contributions
Unlike typical sports analytics architectures that rely on static aggregations, this pipeline introduces:

Binary Classification for Long Format: Explicit filtering pipelines that remove drawn matches to isolate clear victory/defeat behaviors post-2000.

Dynamic ELO with Experience-Based K-Factor: A customized ELO engine featuring a sliding K-factor that scales responsively using a combination of the team's total games played (experience baseline) and a recent-form multiplier.

Non-Linear Interaction Modeling: Explicit generation of cross-feature terms (e.g., ELO_diff_x_home_form) to provide linear classifiers with geometric awareness of momentum disparities.

Granular Team Bias Controls: One-hot encoding parameters applied to team structures to handle country-specific historic baselines seamlessly during inference scaling.
