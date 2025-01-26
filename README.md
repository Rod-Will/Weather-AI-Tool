# Weather-AI-Tool
# Weather Forecasting and Time Series Analysis Using LSTM

This repository contains an end-to-end pipeline for weather forecasting using Long Short-Term Memory (LSTM) neural networks. The project involves data preprocessing, exploratory analysis, model training, cross-validation, and generating future forecasts.

## Table of Contents
- [Project Overview](#project-overview)
- [Folder Structure](#folder-structure)
- [Requirements](#requirements)
- [Pipeline Steps](#pipeline-steps)
- [How to Use](#how-to-use)
- [Results](#results)
- [Acknowledgment](#acknowledgment)
- [License](#license)
- [Contact](#contact)

---

## Project Overview
The objective of this project is to leverage LSTM models for forecasting weather parameters, including:
- Specific Humidity
- Relative Humidity
- Temperature
- Precipitation

The pipeline includes data preprocessing, feature engineering, hyperparameter optimization, and long-term forecasting of future values.

---

## Folder Structure
```
Output_02/
├── models/               # Saved LSTM models for each feature
├── plots/                # Visualizations for exploratory analysis and forecast results
├── results/              # Final CSV files containing forecasted values
```

---

## Requirements
This project requires the following Python libraries:
- `tensorflow`
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `statsmodels`
- `scikit-learn`

Install the required packages with:
```bash
pip install -r requirements.txt
```

---

## Pipeline Steps

### 1. **Data Preprocessing**
- Missing values are imputed with column means.
- Data is normalized using MinMaxScaler for stability in LSTM training.
- Lagged datasets are created to incorporate temporal dependencies.

### 2. **Exploratory Data Analysis**
- Correlation heatmaps and pairwise plots are generated to identify relationships between features.
- Dual-axis plots are used to compare precipitation with other weather parameters.

### 3. **Model Training**
- LSTM models are trained on time-lagged datasets for each feature.
- Cross-validation is performed using `TimeSeriesSplit`.

### 4. **Forecasting**
- Future values are predicted for 5 years (60 months) using the trained LSTM models.
- Forecasted values are rescaled to their original range for interpretation.

![Specific Humidity_5year_forecast](https://github.com/user-attachments/assets/a97e9c43-ccdf-4fa0-a2da-ed9203143415)

### 5. **Results**
- Forecasted data and historical trends are plotted and saved as PNG files.
- A combined CSV file containing 5-year forecasts for all features is saved for further analysis.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/weather-lstm-forecast.git
   cd weather-lstm-forecast
   ```

2. Place your dataset (`Weather_Data.csv`) in the root directory.

3. Run the main script:
   ```bash
   python main.py
   ```

4. Results will be saved in the `Output_02` folder:
   - Models (`.keras` files) in `models/`
   - Plots in `plots/`
   - Forecasted data in `results/`

---

## Results
- Forecast plots for each feature (e.g., `Temperature_5year_forecast.png`) show historical trends and future predictions.
- A combined CSV (`5year_forecast_combined.csv`) includes all forecasted values.

---

## Acknowledgment
- The LSTM models were implemented using [TensorFlow](https://www.tensorflow.org/).
- Data preprocessing and visualization were performed using [pandas](https://pandas.pydata.org/), [matplotlib](https://matplotlib.org/), and [seaborn](https://seaborn.pydata.org/).

---

## License
This project is licensed under the Creative Commons Zero v1.0 Universal (CC0 1.0).  
You are free to use, modify, and distribute this work without any restrictions.

---

## Contact
For questions, feedback, or contributions, contact:  
[https://github.com/Rod-Will]  
[rhudwill@gmail.com]

---

## References
1. Chollet, François. *Deep Learning with Python*. Manning Publications, 2017.
2. TensorFlow Documentation: [https://www.tensorflow.org/](https://www.tensorflow.org/)
3. Scikit-learn Documentation: [https://scikit-learn.org/](https://scikit-learn.org/)

--- 
