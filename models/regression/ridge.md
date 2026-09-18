# Ridge Regression

**ID:** `ridge`

## Summary
Linear regression with L2 regularization, useful when predictors are correlated or coefficient variance needs to be controlled.

## Tags
- problem: `regression`, `prediction`
- task: `prediction`, `feature_shrinkage`
- data: `tabular`, `structured`, `continuous`
- pattern: `linear`, `multicollinearity`
- structure: `independent_observations`
- scale: `medium_sample`, `large_sample`, `high_dimensional`
- mathematics: `linear`, `regularized`, `convex`
- philosophy: `statistical`, `data_driven`
- output: `continuous_prediction`, `coefficients`
- competition: `common`, `formula_friendly`, `interpretation_friendly`

## Applicability
**Hard match:** continuous target and linear predictor representation.

**Soft match:** correlated predictors, p relatively large, prediction more important than exact sparse variable selection.

**Negative match:** requirement for exact sparse feature selection; severe nonlinear structure without feature engineering.

## Parameters
- `alpha`: L2 regularization strength; select by validation or cross-validation.

## Validation
RMSE, MAE, R², cross-validation, coefficient stability.

## Strengths
- stabilizes correlated regression coefficients
- convex optimization
- useful as a strong interpretable baseline

## Limitations / Risks
- does not perform exact feature selection
- remains linear in the supplied features

## Relations
- `extension_of`: `linear-regression`
- `alternative_to`: `lasso`, `elastic-net`
- `complementary_to`: `polynomial-features`

## References
- scikit-learn Ridge documentation: https://scikit-learn.org/stable/modules/linear_model.html
