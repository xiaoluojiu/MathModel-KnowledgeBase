# XGBoost

**ID:** `xgboost`

## Summary
Gradient-boosted decision trees optimized for supervised learning. It is particularly useful for nonlinear tabular regression and classification.

## Tags
- problem: `regression`, `classification`, `prediction`
- task: `prediction`, `feature_analysis`, `nonlinear_modeling`
- data: `tabular`, `structured`, `mixed_features`
- pattern: `nonlinear`, `interaction`, `threshold_effects`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`, `high_dimensional`
- mathematics: `tree_based`, `gradient_based`, `ensemble`, `nonlinear`
- philosophy: `data_driven`, `ensemble_learning`
- output: `continuous_prediction`, `class_probability`, `feature_importance`
- competition: `very_common`, `prediction`, `feature_analysis`

## Applicability
**Hard match:** supervised prediction with a defined target.

**Soft match:** nonlinear relationships, feature interactions, tabular data, predictive accuracy as a priority.

**Negative match:** very small datasets without strong regularization/validation; strict need for a compact mechanistic equation; severe temporal leakage risk if time order is ignored.

## Parameters
- `n_estimators`: boosting rounds.
- `learning_rate`: step size.
- `max_depth`: tree complexity.
- `subsample`: row subsampling.
- column subsampling controls.
- regularization parameters.

## Validation
Use leakage-safe cross-validation or holdout design. Select metrics according to the task; inspect learning curves and feature importance carefully.

## Strengths
- strong nonlinear tabular modeling
- captures feature interactions
- flexible regularization and tuning

## Limitations / Risks
- can overfit without disciplined validation
- less directly interpretable than linear models
- time-series use requires explicit temporal feature construction and leakage control

## Relations
- `alternative_to`: `random-forest`, `svm`, `linear-regression`
- `ensemble_with`: `arima`, `linear-regression`

## References
- scikit-learn gradient boosting and model-selection documentation: https://scikit-learn.org/stable/user_guide.html
