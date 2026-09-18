# Linear Regression

**ID:** `linear-regression`

## Summary
Ordinary least squares regression for estimating a linear relationship between a continuous response and predictors.

## Tags
- problem: `regression`, `prediction`, `relationship_analysis`
- task: `prediction`, `parameter_estimation`, `feature_analysis`
- data: `tabular`, `structured`, `continuous`
- pattern: `linear`, `additive`
- structure: `independent_observations`
- scale: `small_sample`, `medium_sample`, `large_sample`
- mathematics: `linear`, `statistical`, `parametric`
- philosophy: `statistical`, `data_driven`
- output: `continuous_prediction`, `coefficients`
- competition: `very_common`, `formula_friendly`, `interpretation_friendly`

## Applicability
**Hard match:** continuous target, meaningful predictor-response relationship.

**Soft match:** approximately linear effects, moderate sample size, need for coefficient interpretation.

**Negative match:** strong nonlinear structure without useful transformations; severe multicollinearity; strong heteroscedasticity left untreated.

## Prerequisites
- residual diagnostics
- multicollinearity check
- heteroscedasticity check
- influential-point analysis when appropriate

## Validation
RMSE, MAE, R², adjusted R², residual plots, coefficient significance when inferential assumptions are justified.

## Strengths
- simple mathematical expression
- highly interpretable coefficients
- strong baseline for competition model comparison

## Limitations / Risks
- linear functional form can be too restrictive
- coefficients can be unstable under multicollinearity
- extrapolation can be unreliable

## Interpretation
- overall: `very_high`
- formula: `very_high`
- parameter: `very_high`
- feature: `high`

## Relations
- `alternative_to`: `ridge`, `lasso`, `elastic-net`, `random-forest`, `xgboost`
- `predecessor_of`: `polynomial-regression`
- `baseline_for`: `many_regression_models`

## References
- scikit-learn Linear Models documentation: https://scikit-learn.org/stable/modules/linear_model.html
