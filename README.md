# 🌫️ Air Quality Forecasting & Analysis Using Python

## 📌 Project Overview

This project focuses on time-series analysis and forecasting of air-quality data using Python.

The dataset contains 9,357 observations covering multiple environmental and air-quality variables, including temperature, relative humidity and pollutant sensor measurements.

The main forecasting target analyzed in this project is Relative Humidity (RH).

The project focuses on:

- Time-series visualization
- Forecast analysis
- Actual vs forecast comparison
- Forecast uncertainty
- Data-quality validation
- Forecast evaluation

---

## 🎯 Objectives

The project aims to:

1. Analyze air-quality time-series data.
2. Visualize forecast values over time.
3. Compare actual Relative Humidity with forecasted values.
4. Visualize forecast uncertainty intervals.
5. Calculate key forecast statistics.
6. Identify data-quality issues.
7. Evaluate forecast performance.

---

## 📂 Dataset

The dataset contains:

- 9,357 observations
- 17 columns

Important variables include:

| Column | Description |
|---|---|
| ds | Date and Time |
| CO(GT) | Carbon Monoxide measurement |
| PT08.S1(CO) | CO sensor measurement |
| NMHC(GT) | NMHC measurement |
| C6H6(GT) | C6H6 measurement |
| NOx(GT) | NOx measurement |
| NO2(GT) | NO2 measurement |
| PT08.S5(O3) | O3 sensor measurement |
| t | Temperature |
| rh | Actual Relative Humidity |
| ah | Absolute Humidity |
| yhat | Forecasted value |
| yhat_lower | Lower forecast bound |
| yhat_upper | Upper forecast bound |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Jupyter Notebook

---

## 🔄 Workflow

### 1. Load Data

The dataset is loaded using Pandas.

### 2. Date-Time Processing

The `ds` column is converted to datetime format.

### 3. Forecast Visualization

The `yhat` values are plotted against time.

### 4. Uncertainty Visualization

The forecast is displayed together with:

- Lower bound
- Central forecast
- Upper bound

### 5. Actual vs Forecast

Actual RH (`rh`) is compared with forecasted RH (`yhat`).

### 6. Key Metrics

The project calculates:

- Average RH
- Average forecast
- Maximum upper forecast bound
- Minimum lower forecast bound

---

## 📊 Key Visualizations

### 1. Forecast Over Time

Displays the forecast value (`yhat`) against the timestamp.

### 2. Forecast with Uncertainty Range

Shows the central forecast together with the lower and upper forecast bounds.

### 3. Actual RH vs Forecasted RH

Compares actual Relative Humidity with forecasted values.

### 4. Key Metrics Dashboard

Displays summary forecast statistics in metric cards.

---

## 🔎 Key Findings

The forecast shows a clear temporal pattern across the observation period.

The forecast captures the broad trend in Relative Humidity, while actual measurements contain more short-term variation.

The original dataset also contains invalid `-200` placeholder values.

There are 366 such values in the RH column.

Therefore, data cleaning is essential before calculating meaningful statistics.

---

## 📈 Forecast Evaluation

After excluding RH values equal to `-200`:

| Metric | Value |
|---|---:|
| Valid observations | 8,991 |
| MAE | 9.42 |
| RMSE | 12.14 |
| Correlation | 0.714 |
| Interval Coverage | 81.95% |
| Average Interval Width | 30.97 |

These metrics provide a more objective evaluation of forecast performance.

---

## ⚠️ Data Quality Note

The value `-200` appears as a placeholder for missing/invalid sensor readings.

It should not be treated as a real Relative Humidity value.

Therefore, forecast evaluation should be performed after filtering or imputing these invalid observations.

---

## 💡 Key Learning Outcomes

This project strengthened my understanding of:

- Time-series data processing
- Datetime handling
- Forecast visualization
- Prediction intervals
- Data-quality validation
- Forecast evaluation
- Interactive visualization
- Python data analysis

---

## 🚀 Future Improvements

Potential improvements include:

- Train and document the forecasting model explicitly
- Add train/test time-series splitting
- Compare multiple forecasting models
- Add MAE, RMSE and MAPE directly to the notebook
- Perform residual analysis
- Analyze seasonality
- Handle all `-200` sensor placeholders systematically
- Add pollutant forecasting
- Build a Streamlit dashboard
- Deploy an interactive forecasting application

---

## 👨‍💻 Author

Durgesh Yadav

Aspiring Data Analyst / Data Scientist

Skills:
Python | SQL | Power BI | Excel | Statistics | Machine Learning | Data Visualization
