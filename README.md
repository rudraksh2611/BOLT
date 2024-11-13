# Electricity Meter Reading Prediction

This repository contains a project for predicting electricity meter readings using various machine learning and deep learning models. The project includes data filtering, preprocessing, and time-series forecasting techniques applied to electricity consumption data for Building ID 779.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Models Used](#models-used)
- [Evaluation Metrics](#evaluation-metrics)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

### Project Overview
This project aims to predict electricity meter readings by analyzing time-series data. It utilizes ARIMA, Random Forest, GRU, and LSTM models to compare their performance on electricity consumption forecasts. The models help in understanding seasonal trends and detecting anomalies, making it easier to manage energy consumption.

### Dataset
The dataset includes four columns:
- **building_id**: Unique identifier for each building.
- **meter**: Type of meter (only electricity meter data with `meter=0` is used in this project).
- **timestamp**: Date and time of the meter reading.
- **meter_reading**: Recorded electricity consumption.

**Data Preprocessing Steps:**
1. Filter data for electricity meter readings (`meter=0`).
2. Convert meter readings to kWh by multiplying by 0.2931.
3. Split data into training and testing sets (80-20 split) for model training and evaluation.

### Project Workflow
1. **Data Filtering and Conversion**: Filtered electricity data is saved in `filtered_electricity_data.csv`. Data for building 779 is further saved in `filtered_electricity779_data.csv` and converted to kWh in `building_779_updated_meter_reading.csv`.
2. **Data Visualization**: Plots distributions of numerical columns and uses descriptive statistics to summarize the data.
3. **Modeling**:
   - **ARIMA** for time-series forecasting.
   - **Random Forest** for regression.
   - **GRU** and **LSTM** for sequence learning.
4. **Evaluation**: Measures error metrics and compares model predictions against actual meter readings.
5. **Anomaly Detection**: Detects anomalies by analyzing residuals of model predictions.

### Models Used
- **ARIMA**: A classic time-series forecasting model, suited for data with trends and seasonality.
- **Random Forest**: An ensemble method that averages multiple decision tree predictions to improve accuracy.
- **GRU (Gated Recurrent Unit)**: A type of recurrent neural network (RNN) that captures sequential dependencies in time-series data.
- **LSTM (Long Short-Term Memory)**: Another RNN variant with memory cells, designed to handle long-term dependencies.

### Evaluation Metrics
To assess model performance, the following metrics are used:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Percentage Error (MAPE)**

### Usage
#### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/electricity-meter-reading-prediction.git
cd electricity-meter-reading-prediction
```
#### 2. Install Dependencies
Install required Python libraries:
```bash
pip install -r requirements.txt
```
#### 3. Run Data Preprocessing and Modeling
You can follow the steps in the provided code to:

1. Filter the data by running the data filtering steps.
2. Use ARIMA, Random Forest, GRU, and LSTM models to forecast meter readings.
3. Save and view the results.

#### 4. Evaluate Model Performance
Review the printed evaluation metrics to compare models.

#### 5. Anomaly Detection
Use the anomaly detection step to identify data points deviating significantly from the predicted values.

### Results
#### 1. Actual Data Analysis After Pre-Processing:
   ![Actual Data Analysis](https://github.com/user-attachments/assets/de027553-a4c3-4f08-b642-d585b8ddc016)
#### 2. Raw Data Plot for 779 Building Id:
![Actual Data Plot](https://github.com/user-attachments/assets/3dc82eb6-c8b4-426a-a5e8-f99b0f3cdfe8)
#### 3. GRU Prediction:
![GRU Prediction](https://github.com/user-attachments/assets/369db538-fb67-47ee-a3e6-2db3461c6fed)

#### 4. LSTM Prediction:
![LSTM Prediction](https://github.com/user-attachments/assets/c6608c1a-5710-4179-b0bd-68cea1ff0a35)
#### 5. Anomaly Detection:
![Anomaly Detection](https://github.com/user-attachments/assets/1f580958-051d-425c-b120-cbcc3437ffaf)
   

Results are saved and displayed in CSV files, plots, and evaluation metrics. Comparative results for MAE, MSE, RMSE, and MAPE for each model (ARIMA, Random Forest, GRU, LSTM) are provided in the output. The anomaly detection highlights unusual consumption patterns, which could help in energy optimization.

### Contributing
If you want to contribute to this project, please fork the repository and submit a pull request.

### License
This project is licensed under the MIT License.

