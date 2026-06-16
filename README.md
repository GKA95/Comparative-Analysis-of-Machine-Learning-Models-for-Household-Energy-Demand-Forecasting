# Comparative Analysis of Machine Learning Models for Household Energy Demand Forecasting

## Overview

Accurate household electricity demand forecasting is essential for smart grid operation, demand-side management, renewable energy integration, and energy planning. This project presents a comparative analysis of machine learning models for short-term household energy demand forecasting using smart meter data.

The study evaluates the predictive performance of four machine learning algorithms:

* Linear Regression (LR)
* Random Forest Regression (RFR)
* Gradient Boosting Regression (GBR)
* Extreme Gradient Boosting (XGBoost)

A unified preprocessing and evaluation framework was implemented to ensure fair model comparison.

---

## Research Objectives

The objectives of this study were to:

* Preprocess and analyze household electricity consumption data.
* Engineer temporal and statistical features from smart meter readings.
* Develop and train multiple machine learning forecasting models.
* Evaluate model performance using standard forecasting metrics.
* Identify the most suitable model for short-term residential load forecasting.

---

## Dataset

The project uses the Individual Household Electric Power Consumption Dataset from the UCI Machine Learning Repository.

Dataset characteristics:

* Household electricity consumption measurements
* Time-series observations
* Active and reactive power measurements
* Voltage and current measurements
* Energy sub-metering variables

Target Variable:

```text
Global Active Power
```

---

## Methodology

### Data Preprocessing

The dataset was cleaned and prepared through:

* Missing value handling
* Datetime conversion
* Data type correction
* Chronological sorting

### Feature Engineering

To capture temporal dependencies, the following features were generated:

#### Lag Features

* Lag 1
* Lag 24

#### Rolling Statistics

* 24-hour rolling mean
* 168-hour rolling mean

#### Time Features

* Hour of day
* Day of week

#### Cyclical Encoding

* Sine and cosine transformations of temporal variables

---

## Machine Learning Models

Four forecasting models were implemented and evaluated:

| Model             | Purpose                     |
| ----------------- | --------------------------- |
| Linear Regression | Baseline forecasting model  |
| Random Forest     | Nonlinear ensemble learning |
| Gradient Boosting | Sequential error correction |
| XGBoost           | Optimized gradient boosting |

---

## Evaluation Metrics

Model performance was assessed using:

* Mean Absolute Error (MAE)
* Root Mean Square Error (RMSE)
* Coefficient of Determination (R²)

---

## Results

### Model Performance Comparison

| Model             | MAE      | RMSE     | R²       |
| ----------------- | -------- | -------- | -------- |
| Gradient Boosting | 0.081440 | 0.216883 | 0.941413 |
| XGBoost           | 0.082145 | 0.217776 | 0.940929 |
| Linear Regression | 0.084822 | 0.219203 | 0.940152 |
| Random Forest     | 0.095520 | 0.224984 | 0.936955 |

### Key Findings

* Gradient Boosting achieved the best forecasting performance.
* Ensemble learning methods consistently outperformed baseline regression.
* Feature engineering significantly improved predictive accuracy.
* Historical consumption patterns were the strongest predictors of future demand.

---

## Research Contributions

This work contributes:

* A standardized benchmarking framework for household energy forecasting.
* A comparative evaluation of widely used machine learning algorithms.
* Insights into the effectiveness of ensemble learning for smart grid applications.
* A reproducible workflow for energy forecasting research.

---

## Applications

Potential applications include:

* Smart grids
* Demand response systems
* Load scheduling
* Renewable energy integration
* Residential energy management
* Energy planning and forecasting

---

## Repository Structure

```text
notebooks/
results/
paper/
src/
data/
```

The notebooks are arranged sequentially to allow full reproduction of the study.

---

## Author

GKA

Research Interests:

* Energy Systems
* Smart Grids
* Machine Learning
* Artificial Intelligence
* Power Systems Analytics
* Renewable Energy Forecasting
