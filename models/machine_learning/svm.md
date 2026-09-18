# Support Vector Machine / Support Vector Regression

**ID:** `svm`

## Summary
Margin-based supervised learning with optional kernels. Classification uses separating hyperplanes; SVR provides regression with an epsilon-insensitive loss.

## Tags
- problem: `classification`, `regression`, `prediction`
- task: `classification`, `prediction`, `nonlinear_modeling`
- data: `tabular`, `structured`, `continuous`, `mixed_features`
- pattern: `linear`, `nonlinear`, `complex_boundary`
- structure: `independent_observations`
- scale: `small_sample`, `medium_sample`, `high_dimensional`
- mathematics: `kernel_based`, `convex`, `margin_based`, `optimization_based`
- philosophy: `statistical`, `data_driven`, `geometric`
- output: `class_label`, `continuous_prediction`, `decision_score`
- competition: `common`, `prediction`, `formula_friendly`

## Applicability
**Hard match:** supervised classification or regression.

**Soft match:** small/medium sample, high-dimensional features, nonlinear structure suitable for a kernel.

**Negative match:** extremely large sample sizes with expensive nonlinear kernels; unscaled features when scale strongly affects geometry.

## Parameters
- `C`: penalty/regularization control.
- `kernel`: linear, polynomial, RBF, etc.
- `gamma`: kernel scale for supported kernels.
- `epsilon`: SVR epsilon tube width.

## Validation
Task-specific cross-validation; scale features inside the validation pipeline to avoid leakage.

## Strengths
- strong performance on small/medium datasets
- kernels provide nonlinear decision boundaries
- mathematically well-defined convex optimization

## Limitations / Risks
- sensitive to scaling and hyperparameters
- nonlinear kernels can be computationally expensive
- direct feature interpretation is limited

## Relations
- `alternative_to`: `logistic-regression`, `random-forest`, `xgboost`

## References
- scikit-learn Support Vector Machines documentation: https://scikit-learn.org/stable/modules/svm.html
