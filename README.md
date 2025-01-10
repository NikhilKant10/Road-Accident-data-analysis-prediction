# Road-Accident-data-analysis-prediction
Maryland Road Accident Data Analysis &amp; ML Model for predicting Crash Duration
Maryland Road Accident Data Analysis & Crash Duration Prediction

Overview

This repository contains a comprehensive analysis of road accident data in Maryland and a machine learning model for predicting crash duration. The project addresses key questions related to crash statistics, temporal distributions, and predictive modeling, leveraging both exploratory data analysis (EDA) and machine learning techniques.

Key Questions Addressed

Distribution of Crash Duration:

Calculated crash duration and visualized its distribution.

Addressed skewness using log transformation.

Temporal Distribution of Crash Counts:

Analyzed crash counts by hour, day of the week, and month.

Identified peak crash times (e.g., rush hours and weekdays).

Crash Duration vs Vehicles Involved:

Explored the relationship between crash duration and the number of vehicles involved.

Identified weak correlation.

Crash Count by Functional Road Class:

Grouped crashes by functional road classes.

Found that functional class 1 roads have the highest crash frequency.

Vehicle Miles Traveled (VMT) vs Crash Counts:

Computed VMT and analyzed its correlation with crash counts.

Observed a moderate positive correlation.

Crash Duration Prediction Models:

Built and tuned machine learning models including Linear Regression, Random Forest, XGBoost, and Decision Trees.

Achieved the best performance in terms of lowest MAE of 27.15 with Backward Elimination based Regression Model(Adjusted R² = 63%).

Speed Ratio Analysis:

Compared speed ratios during crash and non-crash intervals.

Observed distinct patterns in speed ratios.

Dataset Description

Files:

segment_info.csv:

Contains segment-level information (e.g., road class, functional class, miles).

Columns: segment_id, road, direction, miles, road_class, func_class, aadt

crash_info.csv:

Contains crash-level information (e.g., timestamps, vehicle counts, road conditions).

Columns: event_id, segment_id, start_tstamp, closed_tstamp, vehicle_count, precip_rate, etc.

speed.csv:

Contains speed data for specific segments at 5-minute intervals.

Columns: segment_id, measurement_tstamp, speed

Project Structure

Exploratory Data Analysis (EDA):

Visualized crash distributions and trends (hourly, daily, monthly).

Analyzed relationships between variables (e.g., VMT vs crash counts).

Feature Engineering:

Addressed multicollinearity using Variance Inflation Factor (VIF).

Created cyclical features for temporal variables (hour, day, month).

One-hot encoded categorical variables (e.g., road condition, event subtype).

Model Building & Evaluation:

Models: Linear Regression, Random Forest, XGBoost, and Decision Trees.

Metrics: R², RMSE, MAE.

Tuned hyperparameters for optimal performance.

Forward/Backward Selection:

Used statistical methods to identify the best subset of features.

Key Results

Crash Duration Distribution:

Highly skewed; log transformation improved model performance.

Best Model:

Decision Tree Regressor achieved the highest R² (39%) for predicting crash duration.

Speed Ratio Analysis:

Crash time speed ratios were tightly clustered around 1.0 compared to non-crash intervals.

Requirements

Libraries

Install required Python libraries using:

pip install pandas numpy matplotlib seaborn scikit-learn statsmodels xgboost

Tools

Python (>= 3.7)

Jupyter Notebook

How to Run

Clone this repository:

git clone <repository_url>

Open the notebook file in Jupyter:

jupyter notebook Maryland_Road_accident_data_analysis_&_model_for_predicting_Crash_Duration.ipynb

Upload the 3 attached data files.

Run all cells to perform the analysis and build predictive models.

Future Enhancements

Include external factors like weather data for better predictions.

Explore advanced machine learning models such as Neural Networks.

Perform cross-validation to validate model robustness.

Integrate traffic flow data for additional insights.

Contact

For any questions or suggestions, feel free to reach out at [nkant@umd.edu].

