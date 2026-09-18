# SARIMAX

**ID:** `sarimax`

## Summary
Seasonal ARIMA with exogenous regressors. It models temporal dependence, differencing, seasonal structure, and external predictors in a unified time-series framework.

## Tags
- problem: `forecasting`, `time_series`, `multivariate_regression`
- task: `forecasting`, `model_fitting`, `exogenous_effect_analysis`
- data: `time_series`, `exogenous_variables`, `ordered`, `numeric`
- pattern: `trend`, `seasonality`, `autocorrelation`, `nonstationarity`
- structure: `temporal`, `sequential`
- scale: `small_sample`, `medium_sample`
- mathematics: `statistical`, `stochastic`, `autoregressive`, `moving_average`, `state_space`
- philosophy: `statistical`
- output: `time_series_forecast`, `prediction_interval`, `regression_effects`
- competition: `very_common`, `formula_friendly`, `interpretation_friendly`

## Applicability
**Hard match:** time-ordered target plus aligned exogenous variables when external drivers are part of the problem.

**Soft match:** seasonal behavior, autocorrelation, trend, and plausible external predictors.

**Negative match:** no temporal structure; exogenous predictors unavailable for the forecast horizon; extremely nonlinear dynamics not captured by the specified structure.

## Parameters
- `order=(p,d,q)`
- `seasonal_order=(P,D,Q,s)`
- exogenous-variable specification
- trend specification

## Prerequisites
- verify temporal alignment of exogenous variables
- inspect stationarity and seasonality
- avoid future-information leakage
- use rolling/expanding temporal validation

## Validation
Rolling-origin forecasting; MAE/RMSE and task-appropriate percentage metrics; residual autocorrelation checks; prediction-interval coverage.

## Strengths
- combines time dependence, seasonality, and external drivers
- highly suitable for explanatory competition narratives
- supports explicit comparison with machine-learning predictors

## Limitations / Risks
- exogenous variables must be known or forecast at prediction time
- parameter selection can become complex
- nonlinear interactions may be under-modeled

## Relations
- `extension_of`: `arima`, `sarima`
- `alternative_to`: `xgboost`, `random-forest`, `exponential-smoothing`
- `hybrid_with`: `xgboost`

## References
- statsmodels ARIMA/SARIMAX documentation: https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html
