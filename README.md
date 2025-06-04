# 🏁 F1 Pit Stop Predictor

A machine learning project that predicts the number of pit stops in a Formula 1 race based on race performance, driver attributes, and weather conditions. This model is trained using a **Random Forest Regressor** on cleaned historical F1 race data.



## 🚀 Project Overview

Pit stops are a strategic element in Formula 1 racing, often determining race outcomes. This project builds a machine learning model to estimate how many pit stops a driver is likely to take in a race based on both performance and environmental parameters.



## 📌 Project Metadata

- **Year**: 2023  
- **Model**: Random Forest Regressor  
- **Goal**: Predict number of pit stops (`num_pit_stops`)  
- **Notebook**: `F1_Pit_Stop.ipynb`  
- **Data Source**: `cleaned_data (2).csv`



## 📊 Features Used

| Feature             | Description                                      |
|---------------------|--------------------------------------------------|
| `driverId`          | Unique identifier for each driver                |
| `constructorId`     | ID representing the constructor/team             |
| `grid`              | Starting grid position                           |
| `positionOrder`     | Current position in the race                     |
| `laps`              | Total number of laps in the race                 |
| `AirTemp`           | Ambient air temperature (°C)                     |
| `Humidity`          | Relative humidity (%)                            |
| `Pressure`          | Atmospheric pressure (hPa)                       |
| `Rainfall`          | Rainfall indicator/measurement                   |
| `TrackTemp`         | Track surface temperature (°C)                   |

> 🎯 **Target Variable**: `num_pit_stops`


## 🔧 Model Description

The model uses **RandomForestRegressor** from `scikit-learn`. It was trained on race data using the above features to predict the number of pit stops.  
The performance is evaluated using metrics like **R² Score** and **Mean Squared Error (MSE)**.
)

Requirements
Python 3.8+
streamlit
scikit-learn
pandas
numpy
matplotlib
seaborn




## 📉 Visualization

The graph below illustrates actual vs. predicted pit stops on the training set:

- **Blue Dots**: Predicted vs Actual points  
- **Red Dashed Line**: Ideal predictions line (perfect match)


![image](https://github.com/user-attachments/assets/56fbbad5-1143-4106-83bf-8cc3b99edfd1)


## 🧪 Sample Input Format

```json
{
  "driverId": 1,
  "constructorId": 2,
  "grid": 3,
  "positionOrder": 5,
  "laps": 50,
  "AirTemp": 28.0,
  "Humidity": 45.0,
  "Pressure": 1010.5,
  "Rainfall": 0.0,
  "TrackTemp": 36.5
}
