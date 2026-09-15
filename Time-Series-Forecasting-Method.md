There are two types of time series forecasting based on variables involved. Which one you should use depends on the type of data you are dealing with and the use-case in hand:

## Univariate Forecast

A univariate time series, as the name suggests, is a series with a single time-dependent variable. For example, if you are tracking hourly temperature values for a given region and want to forecast the future temperature using historical temperatures, this is univariate time series forecasting. Your data may look like this:

<img width="231" height="280" alt="image" src="https://github.com/user-attachments/assets/441c49c9-4f44-447c-9d3b-a15d221b2507" />


## Multivariate Forecast

On the other hand, a Multivariate time series has more than one time-dependent variable. Each variable depends not only on its past values but also has some dependency on other variables. This dependency is used for forecasting future values.

Consider the above example and suppose that our dataset includes other weather-related attributes over the same time period, such as perspiration percent, dew point, wind speed, etc., along with the temperature values. In this case, there are multiple variables to be considered to optimally predict temperature. A series like this would fall under the category of multivariate time series. Your dataset will look like this now:

<img width="691" height="330" alt="image" src="https://github.com/user-attachments/assets/0e05a028-3d77-41db-8361-5e3ea34a4dd4" />

You are still forecasting temperature values for the future but now you can use other available information in your forecast as we assume temperature values will be dependent on these factors as well.
