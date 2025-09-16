# diabetes-risk-analysis

## Week 2 Project: Diabetes Risk Analysis

This notebook provides an end-to-end Exploratory Data Analysis (EDA) and baseline modeling on the PIMA Indians Diabetes dataset.

### Objectives

- Understand the dataset and feature distributions
- Handle missing/invalid values (e.g., zeros in medical measurements)
- Visualize correlations and class balance
- Build baseline models (Logistic Regression, Random Forest)
- Evaluate with accuracy, precision, recall, F1, ROC-AUC

### Methods

- Data loaded from a public GitHub CSV (Plotly datasets mirror)
- Biologically-impossible zeros in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` treated as missing and imputed with medians
- Exploratory visuals: distributions, boxplots, correlation heatmaps
- Train/test split with scaling for Logistic Regression
- Baseline models: Logistic Regression (scaled), Random Forest (unscaled)
- Metrics: accuracy, precision, recall, F1, ROC-AUC, confusion matrix, classification report, ROC curves
- Feature importance analysis for Random Forest

### Key Findings

- Elevated glucose and higher BMI are key risk indicators; age and pregnancy count add predictive signal
- Baseline models achieve reasonable performance; ROC-AUC and recall are important for risk screening
- False negatives in the confusion matrix should be carefully inspected

### Recommended Next Steps

- Hyperparameter tuning with cross-validation (GridSearchCV/RandomizedSearchCV)
- Address class imbalance using `class_weight='balanced'` or SMOTE; review PR curves
- Decision threshold tuning to optimize for recall or F1
- Probability calibration for better risk scoring
- Interpretability via SHAP or permutation importance

See `week2project.ipynb` for full code, analysis, and visualizations.
