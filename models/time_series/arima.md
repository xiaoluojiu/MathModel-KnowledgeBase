# ARIMA

**ID:** `arima`

## Summary
Autoregressive Integrated Moving Average for univariate time-series modeling and forecasting, with differencing used to represent nonstationary series through a stationary representation.

## Tags
- problem: `forecasting`, `time_series`, `prediction`
- task: `forecasting`, `model_fitting`, `residual_analysis`
- data: `time_series`, `ordered`, `numeric`
- pattern: `trend`, `autocorrelation`, `nonstationarity`, `stationarity_after_differencing`
- structure: `temporal`, `sequential`
- scale: `small_sample`, `medium_sample`
- mathematics: `statistical`, `stochastic`, `autoregressive`, `moving_average`
- philosophy: `statistical`
- output: `time_series_forecast`, `prediction_interval`
- competition: `very_common`, `formula_friendly`, `interpretation_friendly`

## Applicability
**Hard match:** ordered time-series target with a meaningful time index.

**Soft match:** autocorrelation, trend/nonstationarity that can be differenced, approximately stable dynamics after transformation.

**Negative match:** no meaningful temporal ordering; strong exogenous-driver dependence that is central to the problem; severe structural breaks without appropriate modeling.

## Parameters
- `p`: autoregressive order.
- `d`: differencing order.
- `q`: moving-average order.
- trend specification.

## Prerequisites
- inspect time ordering and frequency
- stationarity diagnostics such as ADF/KPSS where appropriate
- ACF/PACF and residual diagnostics
- time-aware validation

## Validation
Rolling-origin or expanding-window validation; MAE, RMSE, MAPE/sMAPE where appropriate, prediction-interval coverage, AIC/BIC for model comparison rather than as sole evidence of forecast quality.

## Strengths
- interpretable time-series structure
- effective classical forecasting baseline
- strong mathematical presentation for competitions

## Limitations / Risks
- univariate structure can omit important exogenous drivers
- order selection can be unstable
- ordinary random cross-validation is inappropriate for temporal forecasting

## Relations
- `extension_of`: `arma`
- `alternative_to`: `exponential-smoothing`, `prophet`, `xgboost`
- `extension_to`: `sarima`, `sarimax`
- `hybrid_with`: `xgboost`

## References
- statsmodels ARIMA documentation: https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html
