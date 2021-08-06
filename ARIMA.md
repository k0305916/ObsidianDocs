# Background
An ARIMA model consists of coordinates (p, d, q):

-   **p** stands for the number of autoregressive terms, i.e. the number of observations from past time values used to forecast future values. e.g. if the value of p is 2, then this means that two previous time observations in the series are being used to forecast the future trend.
-   **d** denotes the number of differences needed to make the time series stationary (i.e. one with a constant mean, variance, and autocorrelation). For instance, if d = 1, then it means that a first-difference of the series must be obtained to transform it into a stationary one.
-   **q** represents the moving average of the previous forecast errors in our model, or the lagged values of the error term. As an example, if q has a value of 1, then this means that we have one lagged value of the error term in the model.
# [[Stationarity]]
When it comes to forecasting, a key assumption for time series data is that of stationarity. This is where the mean, variance, and autocorrelation of a series are constant.
However, this can formally be tested for using the [[Dickey-Fuller test]].
The test for a unit root is as follows:
$$ \Delta{y_t} = \delta{y_{t-1}} + u_t $$
# Autocorrelation
The **p** parameter in ARIMA accounts for the number of autoregressive terms in the model — which allows the model to handle autocorrelation. Autocorrelation is a situation where correlation exists between the error terms across different observations in the time series, and this can also skew forecasts.
## [[ACF(autocorrelation function) && PACF(partial autocorrelation function function)]]
# [[Auto ARIMA]]
# Model Checking
## [[White Noise Checking]]
## [[Parameter Significance Checking]]
# Conclusion
???
It may be possible that ARIMA would excel when forecasting data with a more clearly defined trend or one that does not particularly exhibit seasonality — we saw very clear signs of this for the dataset in question. However, other cases where seasonality is not present may not be suitable for use with Prophet.
???

# Reference
[ARIMA vs. Prophet: Forecasting Air Passenger Numbers](https://towardsdatascience.com/arima-vs-prophet-forecasting-air-passenger-numbers-4e01b2d93608)