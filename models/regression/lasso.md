# Lasso Regression

**ID:** `lasso`

## Summary
Linear regression with L1 regularization. The penalty can drive coefficients to zero, providing embedded feature selection.

## Tags
- problem: `regression`, `prediction`, `feature_selection`
- task: `prediction`, `feature_selection`
- data: `tabular`, `structured`, `continuous`
- pattern: `linear`, `sparse_signal`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`, `high_dimensional`, `p_greater_than_n`
- mathematics: `linear`, `regularized`, `convex`, `sparse`
- philosophy: `statistical`, `data_driven`
- output: `continuous_prediction`, `sparse_coefficients`
- competition: `common`, `formula_friendly`, `feature_analysis`

## Applicability
**Hard match:** continuous target with a linear predictor representation.

**Soft match:** many predictors, suspected sparse signal, need for variable selection.

**Negative match:** groups of highly correlated predictors where selecting one arbitrarily is undesirable; strong nonlinear structure without feature engineering.

## Parameters
- `alpha`: L1 regularization strength; select using validation or cross-validation.

## Validation
RMSE, MAE, R², cross-validation, selected-feature stability.

## Strengths
- performs prediction and feature selection in one model
- useful for high-dimensional tabular competition problems
- coefficients remain easy to communicate

## Limitations / Risks
- correlated predictors can lead to unstable selection
- linear functional form remains a constraint

## Relations
- `extension_of`: `linear-regression`
- `alternative_to`: `ridge`, `elastic-net`
- `complementary_to`: `pca`

## References
- scikit-learn Linear Models documentation: https://scikit-learn.org/stable/modules/linear_model.html
