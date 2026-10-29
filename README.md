# BBIM709 – Big Data Analytics Assessment 2

# Project Overview

This project explores big data processing and machine learning using Databricks, Apache Spark and PySpark. It focuses on analysing Indian banking transactions, identifying fraudulent activity and predicting monthly transaction volumes.

# Dataset

- **Dataset:** Indian Banking Transactions
- **Records:** 550,000
- **Original columns:** 20
- **Cleaned columns:** 22
- **Storage:** Databricks Delta Lake
- **Classification target:** `is_fraud`
- **Forecasting target:** Monthly transaction count

The dataset was prepared for distributed processing, temporal analysis and predictive modelling.

## Task 1 – Big Data Framework Implementation

The dataset was imported into Databricks using PySpark. Data quality checks, missing-value handling and feature engineering were performed before storing the cleaned dataset in Delta Lake.

Delta Lake optimisation and verification operations were also implemented.

## Task 2 – MapReduce Analysis

Spark DataFrame transformations and aggregations were used to implement MapReduce-style processing.

The analysis examined monthly transaction volumes, fraudulent transaction counts and fraud rates. Spark execution plans and partitioning experiments were used to investigate processing behaviour and performance.

## Task 3 – Machine Learning Implementation

Two machine learning algorithms were implemented using PySpark MLlib.

**Random Forest Classification**

The model was trained to identify fraudulent transactions. Performance was evaluated using accuracy, precision, recall, F1-score, ROC-AUC and PR-AUC.

The final model achieved 96.43% accuracy and 11.09% fraud recall, demonstrating the challenges of highly imbalanced classification.

**Random Forest Regression**

The model was developed to predict monthly transaction counts using historical lag features and calendar information.

The optimised model achieved an MAE of 154.84, RMSE of 229.15 and MAPE of 1.74%.

## Technologies Used

- Databricks Serverless CPU
- Apache Spark 4.2.0
- Python and PySpark
- Delta Lake
- Spark MLlib
- Jupyter Notebook
- GitHub

## Project Files

**BIG data analysis.ipynb** – Jupyter notebook containing the data engineering, MapReduce and machine learning implementation, including saved outputs.

## Limitations

The fraud classification model was affected by severe class imbalance. The forecasting analysis was limited by the number of available monthly observations.

Future improvements could include alternative classification methods, additional forecasting features and more extensive model validation.

## Reproducibility

The notebook uses a Databricks Unity Catalog volume path and Delta Lake tables. To reproduce the analysis, the dataset must be made available in a compatible Databricks environment and the notebook's data paths adjusted accordingly.

## Academic Information

Course: BBIM709 – Big Data Analytics

Assessment: Assessment 2 – Portfolio

Institution: New Zealand Skills and Education (NZSE)
