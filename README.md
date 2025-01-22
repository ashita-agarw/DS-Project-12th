# Temperature Forecasting Project (Independent Project)

## Project Overview
This project focuses on forecasting temperature data for Salt Lake City collected from an online data source. The goal is to analyze the seasonal patterns in the temperature data and build an accurate predictive model using statistical and machine learning techniques. The primary tool employed for the analysis is the **SARIMAX** model, which accounts for both seasonal and non-seasonal components in the time series data.

---

## Objectives
1. **Data Collection:** Gather temperature data (including associated parameters like pressure and height) for Salt Lake City over a specified timeframe.
2. **Data Analysis:** 
   - Visualize the temperature trends.
   - Check for seasonality and stationarity in the data.
3. **Model Development:** Use SARIMAX to forecast temperature based on identified patterns.
4. **Performance Evaluation:** Compare predicted values against real data using metrics like Root Mean Squared Error (RMSE).

---

## Methodology
### 1. **Data Preprocessing**
   - Imported raw data in CSV format using `pandas`.
   - Parsed and set date information as the index.
   - Cleaned and formatted the data for time series analysis.
   - Visualized the raw temperature data to observe trends and anomalies.

### 2. **Stationarity Check**
   - Conducted an **Augmented Dickey-Fuller (ADF)** test to verify stationarity.
   - Applied seasonal differencing to handle non-stationary trends.

### 3. **Model Selection**
   - Used **Auto-ARIMA** to automate the determination of optimal p, d, q (non-seasonal parameters) and P, D, Q, S (seasonal parameters).
   - Chose SARIMAX as the primary forecasting model.

### 4. **Training and Testing**
   - Split the data into training and testing sets.
   - Trained the SARIMAX model on the training data and validated performance on testing data.
   - Generated predictions for:
     - Training data (in-sample accuracy).
     - Testing data (out-of-sample performance).

### 5. **Performance Metrics**
   - Calculated **RMSE** to quantify the accuracy of predictions.

### 6. **Visualization**
   - Plotted recorded and predicted temperature values for training and testing sets.
   - Created visualizations for 7-day ahead forecasts and combined predictions.

---

## Key Observations
- The data exhibited **strong seasonality** with periodic peaks and troughs.
- Seasonal differencing improved stationarity, enhancing model accuracy.
- SARIMAX delivered reliable forecasts for short- and long-term periods.

---

## Tools and Libraries Used
- **Data Analysis:** `pandas`, `numpy`
- **Visualization:** `matplotlib`
- **Statistical Modeling:** `statsmodels`, `auto_arima`
- **Performance Metrics:** `mean_squared_error`

---

## Results and Conclusion
- SARIMAX effectively captured seasonal patterns, enabling accurate temperature forecasts.
- Auto-ARIMA streamlined parameter selection, ensuring optimal configurations.
- Predictions closely aligned with real data in both training and testing phases.

---

## Future Enhancements
- Incorporate additional external factors (e.g., pressure, humidity) to improve forecast accuracy.
- Experiment with machine learning methods such as LSTMs for time series forecasting.

---

## Visualization Samples
- Training vs. Predicted Data Plot
- Testing vs. Predicted Data Plot
- 7-Day Ahead Forecast

These visualizations illustrate the effectiveness of SARIMAX in modeling seasonal temperature data and its potential for practical forecasting applications.
