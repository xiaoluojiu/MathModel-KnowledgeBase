# Logistic Regression

**ID:** `logistic-regression`

## Summary
A generalized linear model for classification that models class probabilities through a logistic link. It is a useful interpretable classification baseline.

## Tags
- problem: `classification`, `probability_prediction`
- task: `classification`, `probability_estimation`
- data: `tabular`, `structured`, `continuous`, `categorical`
- pattern: `linear_decision_boundary`, `additive`
- structure: `independent_observations`
- scale: `small_sample`, `medium_sample`, `large_sample`, `high_dimensional`
- mathematics: `linear`, `probabilistic`, `statistical`, `convex`
- philosophy: `statistical`, `data_driven`
- output: `class_label`, `class_probability`
- competition: `common`, `formula_friendly`, `interpretation_friendly`

## Applicability
**Hard match:** categorical target; binary logistic regression is the basic case.

**Soft match:** approximately linear log-odds relationship and need for probability estimates or coefficient interpretation.

**Negative match:** strongly nonlinear class boundaries without useful feature transformations; severe class overlap where linear separation is inadequate.

## Parameters
- `C` or equivalent inverse regularization strength.
- regularization choice and class weighting when required.

## Validation
Accuracy, precision, recall, F1, ROC-AUC, PR-AUC, log loss; calibration when probabilities are used.

## Strengths
- interpretable coefficients and probabilities
- strong baseline for classification
- efficient and easy to validate

## Limitations / Risks
- linear decision boundary in feature space
- probability calibration can degrade under misspecification

## Relations
- `alternative_to`: `svm`, `random-forest`, `xgboost`
- `extension_of`: `linear-models`

## References
- scikit-learn classification and linear model documentation: https://scikit-learn.org/stable/user_guide.html
