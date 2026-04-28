# Taller 2: Anomaly Detection on Wind Turbine Power Curve

## Objective

Apply unsupervised anomaly detection techniques (DBSCAN) to real wind turbine SCADA data to identify anomalous operating points on the power curve.

## Context

This work was developed as a guided workshop activity where the professor provided the base code and walked through the DBSCAN implementation step by step. The final notebook structure, explanations, hyperparameter tuning decisions, analysis, and conclusions are my own work, built upon the workshop foundation to create a complete and well-documented anomaly detection pipeline.

## Dataset Description

The dataset contains SCADA (Supervisory Control and Data Acquisition) records from a wind turbine over approximately three years (2016-2019), with readings every 10 minutes. The dataset includes:

- 157,824 records with 4 columns: timestamp, active power (kW), wind speed (m/s), and turbine identifier
- Some records contain error messages (`[-11059] No Good Data For Calculation`) that required cleaning
- Physical constraints: power should be zero or positive, and there is a well-defined relationship between wind speed and power

The expected power curve follows three regimes:
- Below cut-in speed (≈3-4 m/s): power near zero
- Partial load region (≈4-12 m/s): power increases with wind speed
- Rated power region (≈12-25 m/s): power stabilizes near maximum (≈2000 kW)
- Above cut-out (25 m/s): turbine shuts down for safety

## Exercises

The activity is developed in a Jupyter notebook and consists of the following steps:

1. **Initial Setup** - Import libraries, load data, inspect structure and data types
2. **Data Cleaning** - Parse numeric columns, handle error messages, convert dates, remove nulls and inconsistent data
3. **Exploratory Data Analysis (EDA)** - Visualize distributions and the power-wind speed relationship
4. **Feature Scaling and Sampling for DBSCAN** - Apply MinMaxScaler and stratified sampling for hyperparameter tuning
5. **Hyperparameter Tuning for DBSCAN** - Select `minPts`, generate k-distance plot, and determine `eps` automatically using the 95th percentile
6. **Applying DBSCAN and Analyzing Results** - Train the model, filter small clusters, visualize results, and separate normal data from anomalies
7. **Conclusions** - Summarize findings, discuss effectiveness and limitations

## Key Results

- DBSCAN successfully identified a dense cluster (Cluster 0) representing normal turbine operation
- Anomalies (other clusters and noise) include points with negative or low power at moderate-to-high wind speeds
- The 95th percentile method for `eps` selection proved practical when no clear elbow was visible in the k-distance graph

## Files

- `taller2-dbscan-anomaly-detection.ipynb` - Main Jupyter notebook (in English)

## Usage

This code is for educational purposes as part of the Machine Learning course. Feel free to explore, learn, and adapt it for similar anomaly detection tasks.