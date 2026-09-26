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

## Statistical Models

When it comes to time series forecasting using statistical models, there are quite a few popular and well-accepted algorithms. Each of them has different mathematical modalities and they come with a different set of assumptions that must be satisfied. This tutorial will not go in-depth on the mathematical concepts, rather will just give an intuition that you will hopefully find helpful.

### ARIMA

ARIMA is one of the most popular classical methods for time series forecasting. It stands for autoregressive integrated moving average and is a type of model that forecasts given time series based on its own past values, that is, its own lags and the lagged forecast errors. ARIMA consists of three components:

  - Autoregression (AR): refers to a model that shows a changing variable that regresses on its own lagged, or prior, values.
  - Integrated (I): represents the differencing of raw observations to allow for the time series to become stationary (i.e., data values are
    replaced by the difference between the data values and the previous values).
  - Moving average (MA): incorporates the dependency between an observation and a residual error from a moving average model applied to
    lagged observations.

The "AR" part of ARIMA indicates that the evolving variable of interest is regressed on its own lagged (i.e., prior observed) values. The "MA" part indicates that the regression error is actually a linear combination of error terms whose values occurred contemporaneously and at various times in the past. The "I" (for "integrated") indicates that the data values have been replaced with the difference between their values and the previous values (and this differencing process may have been performed more than once). The purpose of each of these features is to make the model fit the data as well as possible.  

### SARIMA

An extension to ARIMA that supports the direct modeling of the seasonal component of the series is called SARIMA. A problem with the ARIMA model is that it does not support seasonal data. That is a time series with a repeating cycle. ARIMA expects data that is either not seasonal or has the seasonal component removed, e.g. seasonally adjusted via methods such as seasonal differencing. SARIMA adds three new hyperparameters to specify the autoregression (AR), differencing (I), and moving average (MA) for the seasonal component of the series.  

<img width="427" height="293" alt="image" src="https://github.com/user-attachments/assets/34dc4f55-9eb0-4314-8e8b-09f69ce08c9c" />


### Exponential Smoothing

Exponential smoothing is a time series forecasting method for univariate data. It can be extended to support data with a trend or seasonal component. It can be used as an alternative to the popular ARIMA family of models.

Exponential smoothing of time series data assigns exponentially decreasing weights for newest to oldest observations. The older the data, the less weight the data is given, whereas newer data is given more weight.  

  - vSimple (single) exponential smoothing uses a weighted moving average with exponentially decreasing weights.
  - Holt's exponential smoothing is usually more reliable for handling data that shows trends.
  - Triple exponential smoothing (also called the Multiplicative Holt-Winters) is more reliable for parabolic trends or data that shows
    trends and seasonality.

    <img width="728" height="421" alt="image" src="https://github.com/user-attachments/assets/e965e46c-900c-409e-a6e3-c76df6a95142" />

                comparisons results between a single exponential smoothing (ES), double ES, and two-stage EWMA

### TBATS

TBATS models are for time series data with multiple seasonality. For example, retail sales data may have a daily pattern and weekly pattern, as well as an annual pattern.

In TBATS, a Box-Cox transformation is applied to the original time series, and then this is modeled as a linear combination of an exponentially smoothed trend, a seasonal component, and an ARMA component.  

<img width="751" height="417" alt="image" src="https://github.com/user-attachments/assets/4052d7db-121a-41b8-9971-5d5ccd69c9f0" />

**What TBATS Stands For?** 

T – Trigonometric seasonality: Uses Fourier series to model seasonal patterns using sine and cosine waves, which allows it to handle complex and high-frequency cycles efficiently.  
B – Box-Cox transformation: Stabilizes the variance in the data to make predictions more resilient against outliers and fluctuations.  
A – ARMA errors: Models the residuals (errors) using an Autoregressive Moving Average process to capture short-term dynamic patterns.  
T – Trend: Captures both linear and exponential trends, and supports trend damping for long-term forecasts.  
S – Seasonal components: Accommodates multiple overlapping seasonal periods at once (such as daily, weekly, and yearly cycles combined).  

**Why Use TBATS?** 

Multiple Seasonality: Traditional models like standard ARIMA or ETS struggle when data has more than one seasonal cycle. TBATS excels at handling combinations like hourly data that cycles every 24 hours and every 7 days.  

Flexible Seasonality: Unlike rigid dummy-variable seasonal models, seasonal patterns in TBATS can change slowly over time.  

Fully Automated: The algorithm automatically tunes parameters and selects optimal components based on the Akaike Information Criterion (AIC).  

## Machine Learning

If you don't want to use statistical models or they are not performing well, you can try this method. Machine learning is an alternative way of modeling time-series data for forecasting. In this method, we extract features from the date to add to our "X variable" and the value of the time-series is "y variable". Let's see an example:

For the purpose of this tutorial, I have used the US airline passengers dataset available to download from Kaggle.

<img width="283" height="264" alt="image" src="https://github.com/user-attachments/assets/66c18f6d-65e5-49a0-9e0c-943c316c5b29" />  

We can extract features from the "Date" column such as a month, year, week of the year, etc. See example:

      # extract month and year from dates
      data['Month'] = [i.month for i in data['Date']]
      data['Year'] = [i.year for i in data['Date']]
      
      # create a sequence of numbers
      data['Series'] = np.arange(1,len(data)+1)
      
      # drop unnecessary columns and re-arrange
      data.drop(['Date', 'MA12'], axis=1, inplace=True)
      data = data[['Series', 'Year', 'Month', 'Passengers']]
      
      # check the head of the dataset
      data.head()

<img width="389" height="280" alt="image" src="https://github.com/user-attachments/assets/95a294c1-8908-4997-b467-9dfe0874e5cb" />  


