# Energy Forecasting and Peak Consumption Detection

This project contains two main notebook workflows:

- **Regression Modeling (Ireland)** – Energy production forecasting  
- **Classification Modeling (Portugal)** – Peak consumption detection

The workflows are implemented in the provided Jupyter notebooks.

## Table of Contents
1. Overview
2. Prerequisites
3. Installation and Setup

## 1. Overview

### Classification Modeling (Portugal)

**Purpose:**  
Use two machine learning models (**XGBoost** and **Random Forest + Logistic Regression**) to predict peak energy consumption based on weather and time variables. The models are tuned using **RandomizedSearchCV** and evaluated with standard classification metrics, including:  

- **Confusion Matrix**  
- **Accuracy**  
- **Precision and Recall**  
- **F1-score**  
- **AU-ROC**  

- **Target:** `peak_energy_consumption`  
- **Data format:** CSV  
- **Data collection:** Measurements from multiple smart meter devices collected every 15 minutes between 05/05/2022 and 02/09/2023 from 172 houses in Loureiro, Oliveira de Azeméis, Portugal. All data is included without pre-processing.  
- **Direct URL to data:** [Mendeley Dataset](https://data.mendeley.com/datasets/vryvyfz2tj/1)


### Regression Modeling (Ireland)

**Purpose:**  
Predict total energy production based on weather variables using regression models, including **Decision Tree** and **K-Nearest Neighbors (KNN)**. The models are tuned using **RandomizedSearchCV** and evaluated with **R², MAE, and RMSE** metrics.  

- **Target:** `Total Production (Wh)`  
- **Data format:** CSV  
- **Data collection:** Data from the StoreNet project, organized into three folders: `energy`, `power`, and `weather`. Energy data is in Wh, power data in W. Weather data was added from [Met Éireann historical data](https://www.met.ie/climate/available-data/historical-data) and processed into one file per year.  
- **Direct URL to data:** [Nature Article Dataset](https://www.nature.com/articles/s41597-024-03454-2/tables/7)

## 2. Prerequisites
Ensure the following are installed before running the notebooks:

- Python 3.8+  
- Jupyter Notebook (via Anaconda or Visual Studio Code)  
- NumPy  
- Pandas  
- scikit-learn  
- XGBoost  

## 3. Installation and Setup
1. Install dependencies:

```bash
pip install numpy pandas scikit-learn xgboost jupyter
