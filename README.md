Earthquake Severity and Regional Risk Analysis
Overview

This project applies machine learning techniques to historical earthquake event data to analyze earthquake severity and long-term regional seismic risk. Instead of attempting to predict the exact timing of earthquakes, which is not feasible with event-based datasets, the project focuses on two realistic and valuable objectives:

Earthquake severity prediction

Regional earthquake risk classification

The analysis uses historical seismic records from 2000 to 2024 and demonstrates how machine learning can support risk assessment and disaster preparedness without overclaiming predictive capability.

Dataset

The data was obtained from the United States Geological Survey and consists of historical earthquake events with recorded magnitudes, locations, depths, and timestamps.

Two original datasets were used:

Earthquakes with magnitude greater than or equal to 2.5

Earthquakes with magnitude greater than or equal to 4.5

Each row represents a single earthquake event. The data is event-based and does not include continuous seismic signals prior to earthquakes.

Sampling Strategy

Due to repository size limitations, a representative sampled dataset is included in this repository. The sample was generated using stratified temporal sampling based on:

Year of occurrence

Earthquake severity class

This approach preserves temporal trends, class balance, and spatial diversity, ensuring that the sampled dataset remains statistically representative of the full dataset.

The sampled file used by the application and analysis is:

earthquake_sample_2000_2024.csv

Machine Learning Approach
Preprocessing and Feature Engineering

Column selection and data cleaning

Timestamp conversion to datetime format

Extraction of temporal features such as year, month, hour, and day of week

Binary severity label creation, where magnitude greater than or equal to 4.5 is classified as high severity

Models and Techniques

Logistic Regression as a baseline model for earthquake severity classification

Random Forest to capture nonlinear relationships between depth, location, and temporal features

K-Means clustering to group earthquake events into geographic regions

Evaluation

Train test split

Precision, recall, and F1 score

Confusion matrices

Qualitative error analysis

Streamlit Prototype

An interactive Streamlit dashboard was developed as a prototype decision support tool. The application allows users to:

Filter earthquake events by year range and minimum magnitude

Visualize earthquake locations by severity on an interactive map

View summary statistics for selected filters

Classify geographic regions into low, medium, or high risk categories based on historical severity ratios

The prototype uses the sampled dataset and mirrors the preprocessing steps used in the analysis notebook.

How to Run the Application

Install required dependencies:

pip install streamlit pandas scikit-learn pydeck


Ensure the following files are in the same directory:

app.py

earthquake_sample_2000_2024.csv

Run the application:

streamlit run app.py

Project Structure

notebooks/
Contains the data loading, preprocessing, modeling, and analysis notebooks

app.py
Streamlit dashboard prototype

earthquake_sample_2000_2024.csv
Representative sampled dataset used for analysis and visualization

README.md
Project documentation

Limitations

The project does not attempt to predict earthquake occurrence times

Results are based solely on historical event data

Tectonic plate boundaries and real time seismic signals are not included

Future work could integrate additional geophysical datasets to improve regional risk modeling.

Disclaimer

This project is for academic and analytical purposes only. It does not provide real time earthquake prediction, early warning, or evacuation guidance.
