# Project Overview

In this project, we aim to analyze and model the demand for scooter rentals in a city using historical data that includes factors such as weather, season, time of day, and other indicators. The project focuses on two primary objectives:

### Objective Q1: Predicting the Total Number of Scooter Rentals per Hour for the Week of December 17-23, 2012
This task involves regression techniques to provide precise quantitative estimates for managers or operators of scooter rental services. The goal is to help plan scooter availability based on anticipated demand.

### Objective Q2: Predicting the Probability of High Demand Over the Next 7 Days
This objective is approached as a binary classification problem, where the model predicts whether demand will be high or low. The purpose is to anticipate periods of intense demand, allowing for additional resource allocation and reduced waiting times for users.

---

## Project Steps

To achieve these objectives, we followed these steps:

### Data Preprocessing
We began by preprocessing the input data, including transforming the `datetime` column into more interpretable components (year, month, day, hour, weekday) and handling missing values. We split the data into features (predictors) and target variables for each objective.

### Objective Q1 - Regression Modeling

- We tested several regression models, such as **Linear Regression**, **Decision Tree Regressor**, **Random Forest Regressor**, and **Gradient Boosting Regressor**, to identify the best-performing model.
- After evaluating the performance of each model using **Mean Squared Error (MSE)**, we selected the model with the lowest error and applied hyperparameter tuning to optimize the predictions.

### Objective Q2 - Classification Modeling

- We approached the high-demand prediction as a binary classification problem, creating a "high demand" and "low demand" label based on the average demand value.
- Similar to the regression approach, we tested various classification models, including **Decision Tree Classifier**, **Random Forest Classifier**, and **Gradient Boosting Classifier**.
- We used class weighting to address data imbalance and optimized hyperparameters for the best-performing model using **Grid Search**.

---

## Conclusions

### Conclusion Q1: Hourly Demand Prediction for Scooters
For the first objective, we successfully developed a regression model with good accuracy that predicted the number of scooter rentals per hour for the selected week. The model accurately estimates average demand but has some difficulty capturing peak hours (such as morning and evening times). This is a typical limitation for regression models, which tend to "linearize" data and may not fully capture extreme variations. Nonetheless, the model is highly useful for providing daily and hourly estimates, which can assist in resource allocation and inventory management for scooter rentals.

### Conclusion Q2: Classification of High vs. Low Demand
For the second objective, the classification model achieved excellent accuracy of approximately 91.68% using a Decision Tree Classifier with class weighting. This indicates that the model can successfully predict periods of high and low demand. The results show a good balance between demand classes, demonstrating that the model effectively distinguishes periods of high demand. This capability is valuable for advanced resource planning, allowing better coverage of customer needs during peak periods.

