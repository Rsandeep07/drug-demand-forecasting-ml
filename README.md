# Drug Demand Forecasting for Pharmaceutical Inventory Optimization

##  Project Overview

This repository is part of a **Machine Learning Capstone Project** focused on building an **end-to-end ML solution** for forecasting pharmaceutical drug demand.

The project is structured into **three phases**, following an industry-style ML workflow.
Currently, this repository contains **Phase 1: Problem & Data Foundations**.

---

##  Project Phases

### **Phase 1: Problem & Data Foundations**  *(Completed)*

* Problem statement formulation
* Dataset selection and justification
* Exploratory Data Analysis (EDA)
* Target variable creation
* Evaluation metric definition

### **Phase 2: Modeling & Explainability** *(Upcoming)*

* Feature engineering
* Multiple ML model implementations
* Hyperparameter tuning
* Model interpretability

### **Phase 3: Deployment & MLOps** *(Upcoming)*

* Streamlit application
* Deployment on Hugging Face
* Experiment tracking using MLflow
* Workflow orchestration using Prefect

---

##  Problem Statement

Pharmaceutical companies face challenges in maintaining optimal inventory levels due to fluctuating demand and seasonal patterns. Overstocking increases holding costs and drug wastage, while understocking can lead to shortages that impact patient care.

The objective of this project is to **forecast daily pharmaceutical drug demand** using historical sales data to support **inventory planning and supply chain optimization**.

---

##  Dataset Description

* **Source:** Public pharmaceutical sales dataset from Kaggle
* **Granularity:** Daily sales data
* Each row represents sales observed on a specific date
* Multiple drug category columns represent daily demand for different pharmaceutical groups
* Time-based features such as year, month, and weekday are included

To align with inventory-level forecasting, demand values across individual drug categories are aggregated to create a single target variable.

---

##  Target Variable

* **Target:** `total_demand`
* Defined as the sum of daily demand across all drug categories
* Represents overall pharmaceutical demand per day, which is relevant for inventory and supply chain decisions

---

##  Exploratory Data Analysis (EDA)

EDA is performed to understand:

* Overall demand trends over time
* Seasonal and monthly demand patterns
* Weekday-wise demand variations
* Distribution and outliers in daily demand
* Contribution of different drug categories

The insights obtained from EDA help guide **feature engineering and model selection** in later phases.

 Notebook:

```
notebooks/01_eda_phase1.ipynb
```

---

##  Evaluation Metrics

Since this is a **regression / forecasting problem**, the following metrics are defined:

* **RMSE (Root Mean Squared Error):** Penalizes large prediction errors, important for avoiding stock-outs and overstocking
* **MAE (Mean Absolute Error):** Provides an interpretable average error value
* **MAPE (Mean Absolute Percentage Error):** Expresses error in percentage terms for business-level understanding

These metrics will be used for model evaluation in Phase 2.

---

##  Repository Structure

```
drug-demand-forecasting-ml/
│
├── data/
│   ├── raw/
│   │   └── salesdaily.csv
│   └── processed/
│       └── processed_daily_demand.csv
│
├── notebooks/
│   └── 01_eda_phase1.ipynb
│
├── README.md
└── requirements.txt
```

---

##  Current Status

 **Phase 1 completed**
 Phase 2 and Phase 3 will be implemented next

---

##  Next Steps

* Implement multiple ML models for demand forecasting
* Perform hyperparameter tuning and model explainability
* Deploy the model using Streamlit
* Integrate MLOps practices using MLflow and Prefect

---

