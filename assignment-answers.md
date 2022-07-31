## Questions

### How does the Prophet Algorithm differ from an LSTM?

LSTM is a type of recurrent neural network, whereas Prophet is an additive model of the form $y_t = g(t) + s(t) + h(t) + \epsilon_t$, where:

|Term|Description|
|----|-----------|
|$y_t$|Current period value.|
|$g(t)|Trend.|
|$s(t)|Seasonality.|
|$h(t)|Holidays.|
|$\epsilon_t|Error term with mean equal to zero and an unknown variance.|

### Why does an LSTM have poor performance against ARIMA and Prophet for Time Series

LSTM requires large datasets to prevent overfitting. Most time series datasets are not very large, therefore simpler methods such as ARIMA and Prophet preform better.

### What is exponential smoothing and why is it used in Time Series Forecasting?

Exponential smoothing is an alternative to ARIMA models, that instead of estimating auto-regressive and/or moving-average terms creates set of exponentially decreasing weights for the lags. These weights are controlled by a smoothing parameter, often called $\alpha$. In addition to the univariate version just described, there are also versions of exponential smoothing that account for trends and seasonality.

One popular version of exponential smoothing is called Holt-Winters, or Triple Exponential Smoothing. It uses equations for smoothing the level (or mean), trend and seasonality.

Exponential smoothing is used in time series, because it is simpler to estimate than ARIMA models and provides forecasts that are similar in quality to ARIMA methods.

### What is stationarity? What is seasonality? Why Is Stationarity Important in Time Series Forecasting?

A stationary time series is one in which the observations are only dependent on the lag values, not on the time period. For example, if a time series has a trend, then the values depend on the time period, $t$.  Other examples, would be changes in variance of the error term over time, or parameter instability of ARMA terms.

Seasonality is changes in the time series that are regular and (roughly) predictable, such as an increase in sun screen sales in the summer.

Most, if not all, time series estimation and forecasting methods require the data to be stationary to be valid.

### How is seasonality different from cyclicality? Fill in the blanks:

Seasonality is predictable, whereas cyclicality is not. Seasonal changes are expected and repeatable. For example, increase in beer sales in the summer due to warmer weather. Cyclical changes are due to changes that do not have a regular cycle. For example, housing sales my increase or decrease due to interest rate changes by the Federal Reserve.
