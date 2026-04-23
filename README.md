# Final Exam Project: The Impact of Weather on Delhi's Air Quality

## Project Topic
This project investigates the critical relationship between meteorological conditions and severe air pollution (PM2.5) in Delhi, India, utilizing time-series machine learning.

## Main Objective
To determine how weather variables (temperature, humidity, wind speed) correlate with PM2.5 spikes, and to build a predictive Random Forest Regressor to forecast pollution levels based on historical and meteorological context.

## Project Type
This project is structured as a **Technical Report and Tutorial hybrid**. It combines environmental science explanations, mathematical evaluation metrics, Python code, and predictive data modeling in a Jupyter Notebook.

## Independent Data Sources
This project successfully merges two disparate datasets:
1. **Air Quality Data:** Historical daily AQI and PM2.5 readings for Delhi (via CPCB / Kaggle).
2. **Weather Data:** Hourly historical meteorological records for New Delhi (via Kaggle).

## Workflow and Methodology
1. **Data Ingestion & Cleaning:** Loaded independent datasets and handled missing sensor data via linear interpolation.
2. **Temporal Alignment:** Aggregated hourly weather data into daily averages to match AQI granularity.
3. **Exploratory Data Analysis (EDA):** Generated correlation heatmaps and dual-axis time-series plots to prove the "Winter Smog" thermal inversion effect.
4. **Feature Engineering:** Created contextual time-series features (lagged PM2.5, temperature changes, rolling averages).
5. **Predictive Modeling:** Split data chronologically (to prevent data leakage) and trained a `RandomForestRegressor`.
6. **Mathematical Evaluation:** Evaluated the model using MAE, RMSE, and $R^2$ to assess accuracy and identify limitations regarding outlier events.

## Repository Structure
- `data/` — Contains the original independent datasets.
- `src/` — Contains the main Jupyter Notebook (`delhi_air_quality_analysis.ipynb`).