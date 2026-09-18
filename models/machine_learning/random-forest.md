# Random Forest

**ID:** `random-forest`

## Summary
An ensemble of randomized decision trees using aggregation to improve predictive stability and reduce variance. It supports both classification and regression.

## Tags
- problem: `regression`, `classification`, `prediction`
- task: `prediction`, `feature_analysis`, `nonlinear_modeling`
- data: `tabular`, `structured`, `mixed_features`
- pattern: `nonlinear`, `interaction`, `threshold_effects`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`, `high_dimensional`
- mathematics: `tree_based`, `ensemble`, `nonparametric`
- philosophy: `data_driven`, `ensemble_learning`
- output: `continuous_prediction`, `class_label`, `feature_importance`
- competition: `very_common`, `prediction`, `feature_analysis`, `visualization_friendly`

## Applicability
**Hard match:** supervised tabular prediction with labeled targets.

**Soft match:** nonlinear effects, interactions, mixed feature types, limited desire for feature scaling.

**Negative match:** strict extrapolation beyond the training response range; problems whose primary requirement is a compact explicit mathematical equation.

## Parameters
- `n_estimators`: number of trees.
- `max_depth`: tree depth control.
- `max_features`: feature subsampling strategy.
- `min_samples_leaf`: leaf regularization.

## Validation
Use task-appropriate holdout or cross-validation; regression metrics include RMSE/MAE/R², classification metrics include F1/ROC-AUC/PR-AUC.

## Strengths
- captures nonlinearities and interactions
- comparatively little preprocessing
- useful benchmark and feature-analysis model

## Limitations / Risks
- less transparent than parametric models
- extrapolation is limited
- impurity-based feature importance can be misleading with correlated features

## Relations
- `alternative_to`: `xgboost`, `svm`, `linear-regression`
- `ensemble_with`: `linear-regression`, `arima`

## References
- scikit-learn ensemble documentation: https://scikit-learn.org/stable/user_guide.html
