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
1. **Data Ingestion & Cleaning:** Loaded independent datasets, standardized timestamps, forward-filled limited missing weather observations, and dropped rows with missing PM2.5 values.
2. **Temporal Alignment:** Aggregated hourly weather data into daily averages to match the daily air-quality records.
3. **Exploratory Data Analysis (EDA):** Generated correlation heatmaps and seasonal plots to examine patterns consistent with winter smog conditions.
4. **Feature Engineering:** Created contextual time-series features including lagged PM2.5, temperature change, and a rolling PM2.5 average based only on past observations.
5. **Predictive Modeling:** Split data chronologically to prevent leakage and trained Random Forest models on weather-only and weather-plus-history feature sets.
6. **Mathematical Evaluation:** Evaluated all models against a persistence baseline using MAE, RMSE, and R².

## Repository Structure
- `data/` — Contains the original independent datasets.
- `notebooks/` - Contains the main Jupyter Notebook (`delhi_air_quality_analysis.ipynb`).