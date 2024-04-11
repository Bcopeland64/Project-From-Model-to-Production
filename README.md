# Traffic Stop Data Analysis Project

## Overview
This project focuses on analyzing traffic stop data across various states and cities in the U.S. The aim is to perform profiling, classification, and evaluation of traffic stop data based on different demographic factors such as race. The project utilizes Python libraries such as Pandas, NumPy, YData Profiling, MLflow, and Pycaret for data processing, analysis, and machine learning.

## Dataset Description
The project uses two datasets:
1. **State-Level Data (`opp-stops_state.csv`)**: Contains traffic stop data on a state level, including details like state, city, geography, race, search rate, stop rate, and more.
2. **City-Level Data (`opp-stops_city.csv`)**: Contains city-specific traffic stop data with similar attributes to the state-level data.

## Key Features
- **Data Profiling**: Using YData Profiling, detailed profiling reports for both datasets are generated for initial exploration and analysis.
- **Top Stops Analysis**: The project identifies the top 10 states and cities with the highest number of traffic stops.
- **Missing Value Imputation**: Missing numerical values are imputed with mean values.
- **Classification Model**: A classification model is built to predict the subject's race based on the traffic stop data.
- **MLflow Tracking**: The project sets up an MLflow server for experiment tracking and logs various metrics and parameters.
- **Model Evaluation and Finalization**: The best-performing model is evaluated, finalized, and saved for future predictions.
- **Data Drift Detection**: A drift report is generated to monitor any significant changes in the data over time.
- **Infrastructure Monitoring**: Important IPs for Prometheus and Grafana are provided for infrastructure and data monitoring.

## Getting Started
### Prerequisites
Ensure you have Python installed with the following packages:
- `numpy`
- `pandas`
- `ydata_profiling`
- `mlflow`
- `pycaret`

### Data Import
Load the datasets using Pandas:
```python
import pandas as pd

data_state = pd.read_csv('path_to/opp-stops_state.csv')
data_city = pd.read_csv('path_to/opp-stops_city.csv')



