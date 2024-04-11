# Traffic Stop Data Analysis Project

## Overview
This project focuses on analyzing traffic stop data across various states and cities in the U.S. The aim is to perform profiling, classification, and evaluation of traffic stop data based on different demographic factors such as race and gender. The project utilizes Python libraries such as Pandas, NumPy, YData Profiling, MLflow, and Pycaret for data processing, analysis, and machine learning.

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
```
### Data ProfilingGenerate profiling reports:
```from ydata_profiling import ProfileReport

profile_state = ProfileReport(data_state, title="State Level Profiling Report")
profile_city = ProfileReport(data_city, title="City Level Profiling Report")
```
### Analysis and Machine Learning

1 - Identify top stops:
    Analyze and print the top 10 states and cities based on the number of stops.
    
2 - Impute missing values:
    Handle missing numerical values by imputation.
    
3 - Build and evaluate the classification model:
    Use pycaret to set up the classification model, compare different models, and finalize the best model.
    
4 - Track experiments with MLflow:
    Set up and start the MLflow server for tracking experiments.

### Monitoring and Reporting

1 - Start Grafana and Prometheus servers for data monitoring.

2 - Check for data drift to ensure the model's relevance over time.

### Additional Information

Important IPs:

    Prometheus: localhost:9090
    MLFlow: localhost:5001
    Grafana: localhost:3000
    
Generated Files:

    Model: Final Classification Model.pkl
    Drift Report: Classification_State_Metrics_1688755676_Drift_Report.html

### Conclusion

This project demonstrates a comprehensive approach to analyzing traffic stop data using data profiling, machine learning, and monitoring tools. It aids in understanding the dynamics of traffic stops across different demographics and locations.


This README provides a structured overview of your project, outlining its purpose, datasets, main features, usage instructions, and additional details for a thorough understanding.

