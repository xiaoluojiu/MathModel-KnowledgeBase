# Model Registry

This registry is the human-readable entry point to the model knowledge base. It is intentionally organized by modeling role rather than only by software library.

## Current catalog

| Model | Family | Primary problems | Key data patterns |
|---|---|---|---|
| Linear Regression | regression | regression, explanation | linear, continuous |
| Ridge | regression | regression, regularization | multicollinearity, high-dimensional |
| Lasso | regression | regression, feature selection | sparse effects, high-dimensional |
| Elastic Net | regression | regression, feature selection | correlated predictors, sparse effects |
| Logistic Regression | classification | binary classification | linear decision boundary, probabilities |
| Random Forest | ensemble learning | regression, classification | nonlinear, tabular |
| XGBoost | gradient boosting | regression, classification | nonlinear, interactions |
| SVM / SVR | kernel methods | classification, regression | margin structure, nonlinear kernels |
| K-Means | clustering | clustering | compact distance-based groups |
| PCA | dimensionality reduction | reduction, feature extraction | correlated features, continuous variables |
| ARIMA | time series | forecasting | autocorrelation, trend/nonstationarity |
| SARIMAX | time series | forecasting | seasonality, autocorrelation, exogenous variables |

## Planned core families

- Statistical regression and generalized linear models
- Time-series and state-space models
- Clustering and dimensionality reduction
- Evaluation and multi-criteria decision making
- Grey-system methods
- Fuzzy methods
- Linear/integer/mixed-integer optimization
- Transportation, assignment, scheduling and network optimization
- Dynamic programming
- Classical graph algorithms
- Metaheuristic and evolutionary optimization
- Stochastic simulation and Monte Carlo
- Markov and queueing models
- Differential-equation and dynamical-system models
- Ensemble and hybrid modeling pipelines

## Inclusion rule

A model is not considered complete merely because it has an implementation. A production-quality knowledge card should explain when it fits, when it does not, what evidence should be checked before use, how it should be validated, and which neighboring models should be compared.