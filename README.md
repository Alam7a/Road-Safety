# Chicago Crash Frequency Analysis – NB-GLM, Empirical Bayes, and Machine Learning
Complete crash-frequency analysis pipeline for Chicago (2017–2024). Includes data cleaning, spatial grid creation, NB-GLM modeling, Empirical Bayes PSI ranking, severity and regional models, statistical tests, and ML validation (XGBoost, RF, LightGBM). Generates maps and reports.
Chicago Crash Frequency Modeling and Network Screening

This repository presents a comprehensive crash-frequency modeling framework for the City of Chicago (2017–2024). The workflow integrates spatial processing, statistical modeling, empirical Bayes estimation, machine-learning validation, and network screening, following established road safety analysis practices.

Overview

The project develops a spatially resolved crash dataset using a 50 m × 50 m grid, assigns exposure measures through nearest-neighbor AADT matching, incorporates environmental and roadway attributes, and evaluates crash risk using multiple modeling strategies. The analysis produces Potential for Safety Improvement (PSI) estimates, priority rankings, and visualization products that support engineering decision-making.

Methodology
Data Preparation

Spatial grid construction and site-level aggregation

AADT assignment using KD-Tree matching

Derivation of weather, lighting, and camera indicators

Filtering of low-exposure or incomplete sites

Statistical Modeling

Negative Binomial Generalized Linear Models (NB-GLM)

Empirical Bayes (EB) adjustment for stabilized crash estimates

Severity-specific models (Fatal, Injury, PDO)

Regional NB models for spatial subgroups

Machine Learning Validation

XGBoost (Poisson objective)

LightGBM

Random Forest

Feed-forward Neural Network (optional)

Network Screening

PSI estimation using EB-adjusted frequencies

Ranking of sites into Critical, High, Moderate, and Normal priority classes

Export of top-ranked locations for intervention planning

Statistical Tests

Chi-Square tests for categorical associations

One-way ANOVA and Tukey HSD for regional differences

Variance Inflation Factor (VIF) for multicollinearity diagnostics

Outputs

The workflow generates:

Model coefficients and diagnostics

EB-adjusted predictions and PSI values

Feature importance from machine-learning models

Hotspot and severity-based maps

Regional and severity comparison tables

Presentation-ready Excel files

Dependencies

Python 3.9+ with:
pandas, numpy, scipy, statsmodels,
xgboost, lightgbm, scikit-learn,
matplotlib, seaborn, tensorflow (optional).

Execution

Run the full analysis using:

python road_safety_glm_nb_eb_xgboost_v11.py


Outputs will be saved to the configured directory structure.

Author

Mahin Alam
University of Windsor
MASc Thesis Research in Road Safety & Transportation Systems
