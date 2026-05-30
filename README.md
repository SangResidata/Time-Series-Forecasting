# Time-Series-Forecasting
Statistical Forecasting Time Series analysis for predicting the future data.

## What is Time Series Data Analysis?

Time series analysis is a statistical technique used to analyze data points recorded at regular time intervals. It can help identify patterns, trends, and seasonal variations, making it useful for forecasting results over time.  

Engineers and scientists working with time series data can use time series analysis to monitor, model, and predict system behaviors, which optimizes systems and improves forecasting accuracy.

Financial analysts use time series data such as stock price movements, or a company’s sales over time, to analyze a company’s performance.  

<img width="1024" height="729" alt="image" src="https://github.com/user-attachments/assets/91e9b610-732c-4fbd-aa9b-772f3c80839a" />


```markdown

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

...


## How Time Series Analysis Works?  

Time series analysis involves working with time series data to analyze the data systematically. Time series data is a sequence of data points collected or recorded at specific points in time such that each data point is associated with a particular timestamp, enabling analysis of how the data changes relative to time.  

