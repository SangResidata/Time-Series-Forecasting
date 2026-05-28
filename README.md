# Time-Series-Forecasting
Statistical Forecasting Time Series analysis for predicting the future data.

## What is Time Series Data Analysis?

Time series data analysis is the analysis of datasets that change over a period of time. Time series datasets record observations of the same variable over various points of time. Financial analysts use time series data such as stock price movements, or a company’s sales over time, to analyze a company’s performance.

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
