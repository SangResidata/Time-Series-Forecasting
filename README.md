# Time-Series-Forecasting  

This is Repository about Statistical Forecasting Time Series analysis for predicting the future data.

## What is Time Series Data Analysis?

Time series analysis is a statistical technique used to analyze data points recorded at regular time intervals. It can help identify patterns, trends, and seasonal variations, making it useful for forecasting results over time.  

Engineers and scientists working with time series data can use time series analysis to monitor, model, and predict system behaviors, which optimizes systems and improves forecasting accuracy.

Financial analysts use time series data such as stock price movements, or a company’s sales over time, to analyze a company’s performance.  

<img width="1024" height="729" alt="image" src="https://github.com/user-attachments/assets/91e9b610-732c-4fbd-aa9b-772f3c80839a" />


```

Repository ini didedikasikan sebagai jurnal belajar mandiri (*learning in public*) untuk menguasai konsep, metodologi, dan implementasi **Time Series Forecasting** (Peramalan Deret Waktu).

---

## 🗺️ Peta Jalan Belajar & Kurikulum

### 🛑 Fase 1: Time-Series Data Wrangling & EDA
- [ ] Pengaturan `DatetimeIndex` dan manipulasi frekuensi data (`resample()`).
- [ ] Penanganan data hilang (*Forward Fill, Backward Fill, Linear Interpolation*).
- [ ] *Exploratory Data Analysis* (EDA): Visualisasi dekomposisi musiman.

### 📊 Fase 2: Metode Statistik Klasik
- [ ] Uji Stasioneritas Data (Augmented Dickey-Fuller Test).
- [ ] Analisis Plot ACF (Autocorrelation) dan PACF (Partial Autocorrelation).
- [ ] Membangun dan tuning model **ARIMA / SARIMA**.

### 🤖 Fase 3: Pendekatan Machine Learning (Supervised Learning)
- [ ] Transformasi deret waktu menjadi tabular (*Supervised Learning Matrix*).
- [ ] *Feature Engineering*: Pembuatan *Lag Features* ($t-1, t-2$) dan *Rolling Window Metrics*.
- [ ] Implementasi Model: **Random Forest, XGBoost,** dan **LightGBM**.


```

## How Time Series Analysis Works?  

Time series analysis involves working with time series data to analyze the data systematically.  
Time series data is a sequence of data points collected or recorded at specific points in time such that each data point is associated with a particular timestamp, enabling analysis of how the data changes relative to time.

## Components of Time Series Data

Time series data can be broken down into several fundamental components to help understand underlying patterns and forecast  

## Characteristics of Time Series Data Components  

Time series data consists of observations recorded over regular time intervals. It is primarily analyzed by breaking it down into four fundamental components: trend, seasonality, cyclicality, and irregular variations.

<img width="651" height="448" alt="image" src="https://github.com/user-attachments/assets/5a2a850e-6e08-4cf1-ac0d-864b43814c33" />


## Time Series Analysis Steps  

<img width="671" height="141" alt="image" src="https://github.com/user-attachments/assets/cc730678-4c45-4e83-a0ca-7677c209b637" />


Analyzing time series data involves a systematic approach that integrates various techniques for understanding, modeling, and forecasting data points collected over time.  


## Exploratory Data Analysis  

Exploratory data analysis (EDA) involves collecting raw data and then preprocessing and visualizing the data for further analysis. It includes:

- Data collection: Gathering observations over a specified period and ensuring the quality and accuracy of the data set.
- Data preprocessing and data visualization: Understanding and preparing the data set for analysis and modeling. Data preprocessing includes data cleaning, data transformation, and structural operations.


## Decomposition

Decomposition is a technique used to break down time series data into its fundamental components—trends, seasonal, cyclic, and remainder—making it easier to analyze the underlying patterns and interpret data.  

<img width="482" height="386" alt="image" src="https://github.com/user-attachments/assets/cae5b042-d3e5-452c-b564-9366d22fa72c" />  


## Model Selection and Fitting

Model selection finds the most suitable model to capture the underlying data patterns based on characteristics such as seasonality, trend, and stationarity. Model fitting focuses on training the selected model to minimize the difference between observed data and predictions, ensuring it generalizes well to new data  


## Model Prediction and Forecasting

In model prediction and forecasting, the model trained in the previous step is applied to new data to generate future data points based on historical patterns



## Model Evaluation

Model evaluation involves assessing how well a model performs and the accuracy of its predictions. It comprises of three key components:

-  Performance metrics: Metrics such as root mean squared error (RMSE) calculate the differences between predicted and actual values, providing a measure of the accuracy of a model.  
-  Validation techniques: Cross-validation, backtesting, and other techniques assess the reliability of a model by evaluating its performance in making predictions on new data sets.
-  Interpretability methods: Techniques such as local interpretable model-agnostic explanations (LIME) and Shapley additive explanations (SHAP) help with understanding model predictions, making the model’s decisions more transparent.

<img width="334" height="286" alt="gambar" src="https://github.com/user-attachments/assets/a0f83979-f829-4639-a999-b89ecda49570" />  

<img width="304" height="303" alt="gambar" src="https://github.com/user-attachments/assets/e47e96fb-e1d8-4d69-8962-50fcd46284fa" />  

## Common Approaches to Time Series Modeling  

Three common approaches to modeling time series data are traditional forecasting models, machine learning models, and deep learning models.

### 1. Traditional Forecasting Models

Traditional forecasting models use statistical techniques to identify and model underlying data patterns and trends.  

**The auto regressive integrated moving average (ARIMA)** statistical model predicts future values by analyzing historical data. It captures trends and seasonality, making it applicable for both stationary and nonstationary data sets and suitable for short- to medium-term forecasting, such as stock prices and sales.  

<img width="924" height="333" alt="gambar" src="https://github.com/user-attachments/assets/ba1ce1df-4e45-499f-8e5e-40e630c92051" />


Estimating an ARIMA model using System Identification Toolbox for time series forecasting. (See MATLAB code.)  


The exponential smoothing model applies exponentially decreasing weights to past observations, prioritizing more recent data. This method effectively smooths short-term fluctuations while capturing underlying trends and patterns in time series data. It is particularly useful for data with trends or seasonality.  

### 2. Machine Learning Models

Machine learning models can capture the complex patterns in data that traditional models might miss. 

**Random forest models** build multiple decision trees and combine their outputs to improve prediction accuracy in time series analysis. They handle large, high-dimensional data sets and are robust to overfitting. By using past data as predictors, they capture nonlinear relationships and interactions, making them well-suited for modeling irregular patterns.

**Support vector machines (SVMs)** are supervised learning models used for classification and regression. In time series analysis, they can model nonlinear relationships and handle high-dimensional data, especially with small, complex data sets. For example, SVMs can forecast energy demand by capturing nonlinear interactions between historical consumption, weather, and economic indicators. 

<img width="567" height="427" alt="gambar" src="https://github.com/user-attachments/assets/ae44cf4c-4fac-4c9d-b3ba-8918d74fd1d5" />


Plot showing classification of ECG signals using signal processing, wavelet-based feature extraction, and a support vector machine (SVM) classifier to distinguish between arrhythmia (ARR), congestive heart failure (CHF), and normal sinus rhythm (NSR). (See MATLAB code.)  

## Deep Learning Models
Deep learning enhances time series analysis by automatically learning patterns and dependencies directly from data. These models capture both short-term fluctuations and long-term trends, making them ideal for forecasting and anomaly detection.  

**Long short-term memory (LSTM)** models are a specialized type of recurrent neural network (RNN) designed to overcome the limitations of traditional RNNs by using memory cells and gating mechanisms. This design enables them to capture long-term dependencies effectively, making LSTMs particularly useful for time series analysis tasks such as forecasting and sequence prediction.  

<img width="621" height="218" alt="gambar" src="https://github.com/user-attachments/assets/8547b0ae-f9d2-458f-b0ba-805540362e30" />  

**Convolutional neural networks (CNNs)** are used in time series analysis as they can automatically extract features from data using convolutional layers. They identify local patterns and hierarchies, making them effective for identifying short-term dependencies for tasks such as multivariate time series classification.  

<img width="857" height="413" alt="image" src="https://github.com/user-attachments/assets/b7b7ec9c-1451-4574-8df1-95f42f75d17f" /> 


## Types of Time Series Analysis

Time series analyses can be classified into categories that describe, explain, forecast, and optimize data trends and patterns effectively:
 - **Descriptive analysis** summarizes the key features of a data set. It helps in understanding the underlying patterns, trends, and seasonal variations in the data.
 - **Explanatory analysis** aims to understand the relationships and causal effects within the data. It seeks to explain why certain patterns or trends occur by 
      examining the underlying factors and correlations.
 - **Predictive analysis** uses historical data, statistical models, and machine learning algorithms to predict future trends and patterns.
 - **Prescriptive analysis** provides recommendations and actions based on predictive insights. It suggests optimal decisions by evaluating different scenarios and their potential outcomes.

## Challenges in Time Series Analysis

Certain types of obstacles are typical of time series analysis. During data acquisition, it’s common for sensors or instruments to record data at inconsistent intervals, a problem for many time series models designed to handle monotonically increasing data. Preparing the data may include handling missing data, outliers, noise, and other irregularities as well as resampling the data to create uniform intervals. Exploratory data analysis techniques discussed above can help in mitigating these issues.

















