# Elastic Net

**ID:** `elastic-net`

## Summary
Regularized linear regression combining L1 and L2 penalties. It is useful when feature selection and stability under correlated predictors are both desired.

## Tags
- problem: `regression`, `prediction`, `feature_selection`
- task: `prediction`, `feature_selection`
- data: `tabular`, `structured`, `continuous`
- pattern: `linear`, `sparse_signal`, `multicollinearity`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`, `high_dimensional`, `p_greater_than_n`
- mathematics: `linear`, `regularized`, `convex`, `sparse`
- philosophy: `statistical`, `data_driven`
- output: `continuous_prediction`, `sparse_coefficients`
- competition: `common`, `formula_friendly`, `feature_analysis`

## Applicability
**Hard match:** continuous target with linear predictor representation.

**Soft match:** correlated predictors plus a need for sparsity or variable selection.

**Negative match:** strongly nonlinear relationships without suitable feature construction.

## Parameters
- `alpha`: total regularization strength.
- `l1_ratio`: balance between L1 and L2 penalties.

## Validation
RMSE, MAE, R², cross-validation, coefficient stability.

## Strengths
- combines sparsity and coefficient stabilization
- often more stable than pure Lasso with correlated features

## Limitations / Risks
- requires tuning at least two regularization controls
- remains linear in the feature representation

## Relations
- `extension_of`: `ridge`, `lasso`
- `alternative_to`: `ridge`, `lasso`
- `alternative_to`: `linear-regression`

## References
- scikit-learn Linear Models documentation: https://scikit-learn.org/stable/modules/linear_model.html
