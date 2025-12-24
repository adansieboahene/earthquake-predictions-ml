# Earthquake Severity and Regional Risk Analysis

## Overview
This project explores machine learning techniques for analyzing historical earthquake data.
Rather than attempting to predict the exact timing of earthquakes, the study focuses on two
realistic and feasible tasks:

1. Earthquake severity prediction
2. Regional earthquake risk classification

The project uses historical seismic event data from 2000 to 2024 and demonstrates how
machine learning can support long-term risk assessment and preparedness.

---

## Dataset
The data was obtained from the United States Geological Survey (USGS) and includes:
- Earthquake time
- Latitude and longitude
- Depth
- Magnitude

Two datasets were used:
- Earthquakes with magnitude ≥ 2.5
- Earthquakes with magnitude ≥ 4.5

Each record represents a single earthquake event.

---

## Machine Learning Approach

### Preprocessing
- Column selection and cleaning
- Timestamp conversion and feature extraction
- Label engineering for earthquake severity
- Spatial clustering to define regions
- Aggregation of event-level data into regional profiles

### Models
- Logistic Regression for baseline severity prediction
- Random Forest for nonlinear classification
- K-Means clustering for regional grouping

### Evaluation
- Train-test split
- Precision, recall, and F1-score
- Confusion matrices
- Error analysis

---

## Streamlit Prototype

An interactive Streamlit dashboard was developed to visualize:
- Earthquake locations by severity
- Summary statistics
- Regional earthquake risk levels
- Temporal and magnitude-based filters

The prototype demonstrates how the analysis results could be used in a decision-support
context. It does not provide real-time prediction or early warning functionality.

---

## How to Run the App

1. Install dependencies:
   pip install streamlit pandas scikit-learn pydeck

2. Place the following files in the same folder:
   - apps.py
   - query_M2.5+_2000-2024.csv
   - query_M4.5+_2000-2024.csv

3. Run the app:
   streamlit run app.py

---

## Disclaimer
This project is for academic and analytical purposes only. It does not attempt to predict
earthquake occurrence times or provide evacuation guidance.
