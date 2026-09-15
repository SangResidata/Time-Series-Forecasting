There are two types of time series forecasting based on variables involved. Which one you should use depends on the type of data you are dealing with and the use-case in hand:

## Univariate Forecast

A univariate time series, as the name suggests, is a series with a single time-dependent variable. For example, if you are tracking hourly temperature values for a given region and want to forecast the future temperature using historical temperatures, this is univariate time series forecasting. Your data may look like this:

<img width="231" height="280" alt="image" src="https://github.com/user-attachments/assets/441c49c9-4f44-447c-9d3b-a15d221b2507" />


## Multivariate Forecast

On the other hand, a Multivariate time series has more than one time-dependent variable. Each variable depends not only on its past values but also has some dependency on other variables. This dependency is used for forecasting future values.

Consider the above example and suppose that our dataset includes other weather-related attributes over the same time period, such as perspiration percent, dew point, wind speed, etc., along with the temperature values. In this case, there are multiple variables to be considered to optimally predict temperature. A series like this would fall under the category of multivariate time series. Your dataset will look like this now:

<img width="691" height="330" alt="image" src="https://github.com/user-attachments/assets/0e05a028-3d77-41db-8361-5e3ea34a4dd4" />

You are still forecasting temperature values for the future but now you can use other available information in your forecast as we assume temperature values will be dependent on these factors as well.  

<img width="708" height="159" alt="image" src="https://github.com/user-attachments/assets/a76d4d1d-9855-4bfc-b545-ad0986b3b36e" />  

When we are dealing with multivariate time series forecasting, the input variables can be of two types:

  1. Exogenous: Input variables that are **not influenced** by other input variables and on which the output variable depends.
  2. Endogenous: Input variables that are **influenced** by other input variables and on which the output variable depends.

# Time Series Forecasting Methods

Time series forecasting can broadly be categorized into the following categories:

    1. Classical / Statistical Models — Moving Averages, Exponential Smoothing, ARIMA, SARIMA, TBATS
    2. Machine Learning — Linear Regression, XGBoost, Random Forest, or any ML model with reduction methods
    3. Deep Learning — RNN, LSTM

