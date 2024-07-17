# Bike Sharing Demand Prediction

## Overview
Forecasting bike demand is a common problem for bike rental companies, as accurate predictions can help optimize inventory and pricing strategies. This project aims to develop a regression-based machine learning model to predict bicycle demand over time.

The dataset includes bicycle rental data from a bike-sharing company, featuring the number of bicycles rented, rental times and dates, weather conditions, seasonal characteristics, and other factors that may influence bicycle demand, such as holidays and weekdays.

## Problem Statement
Currently, rental bikes are introduced in many urban cities to enhance mobility comfort. It is crucial to make rental bikes available and accessible to the public at the right time to minimize waiting times. Therefore, predicting the bike count required each hour is essential for ensuring a stable supply of rental bikes.

## Dataset Information
- **Date**: Year-month-day
- **Rented_Bike_Count**: Count of bikes rented each hour
- **Hour**: Hour of the day
- **Temperature**: Temperature in Celsius
- **Humidity**: Percentage humidity
- **Windspeed**: Windspeed in m/s
- **Visibility**: Visibility in 10m units
- **Dew point temperature**: Dew point temperature in Celsius
- **Solar radiation**: Solar radiation in MJ/m²
- **Rainfall**: Rainfall in mm
- **Snowfall**: Snowfall in cm
- **Seasons**: Winter, Spring, Summer, Autumn
- **Holiday**: Holiday/No holiday
- **Functional Day**: Non-functional hours (NoFunc) or functional hours (Fun)

## Methodology
1. **Data Preprocessing**:
   - Cleaned and preprocessed the data, handling null values and outliers.
   - Split the data into training and test sets.

2. **Model Training**:
   - Tried several model architectures and hyperparameter settings.
   - Chose the best-performing model based on test data results.

3. **Performance Evaluation**:
   - Used metrics like mean absolute error, squared error, and R-squared.
   - The final model achieved an R-squared value of 0.88 and an average absolute error of 2.58.

4. **Ablation Studies**:
   - Assessed the impact of individual features on model performance.
   - Found that temperature, weather, and seasonal changes significantly affect bicycle demand.

## Conclusion
- A Gradient Boosting model with GridSearchCV showed promising results with an R² score of 0.91.
- Key factors driving bike rental demand include temperature, functioning days, humidity, rainfall, and solar radiation.
- Bike demand peaks around 8-9 AM and 6-7 PM.
- Higher bike rental rates are observed in summer compared to winter.
- Clear days see more bike rentals than snowy or rainy days.
- Temperature range from 22°C to 25°C has higher bike demand.
- The dataset's time-dependent nature means factors like temperature, wind speed, and solar radiation may vary, affecting model performance. Continuous learning and adaptation to new advancements in machine learning are essential.

## Future Work
- Explore additional features and data sources to enhance model accuracy.
- Continuously update the model with new data to maintain performance.
- Investigate real-time prediction capabilities for better operational integration.
