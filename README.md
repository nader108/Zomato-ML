# Zomato Restaurant Data Analysis & Predictive Modeling

This project explores a Zomato restaurant dataset and builds predictive models to predict restaurant ratings based on various features like location, cuisine, price, and service type. The analysis includes data cleaning, feature engineering, exploratory data analysis (EDA), and predictive modeling using linear regression and other machine learning algorithms.

Table of Contents
Project Overview
Data Cleaning & Preparation
Exploratory Data Analysis
Predictive Modeling
Evaluation Metrics
Key Insights
Project Overview
The Zomato dataset contains restaurant details such as:

Restaurant name
Location
Service types (Online ordering, Table booking, etc.)
Cuisine types
Rating and pricing information
The objective of this project is to predict restaurant ratings (rate) based on various features, using both linear regression and other advanced models like Random Forest.

Data Cleaning & Preparation
Missing Data Handling:

The dataset had several missing values, especially in columns like rate, dish_liked, and phone. These missing values were cleaned or imputed based on the analysis.
Column Transformation:

The rate column was transformed to extract the numeric value from ratings like '4.1/5' by splitting the string.
The approx_cost(for two people) column was converted to numeric by removing commas from values like '1,500' and converting them to integers.
Handling Duplicates:

Duplicate entries for restaurants were removed, keeping only the entry with the highest vote count.
Exploratory Data Analysis
Rating Distribution:

The distribution of restaurant ratings was explored, highlighting outliers using boxplots.
Service Type Analysis:

The types of services (e.g., Delivery, Dine-out, Buffets) offered by restaurants were visualized using count plots.
Online Orders and Table Bookings:

The availability of online ordering and table booking features in the dataset was visualized with pie charts to understand customer preferences.
Price Distribution:

The distribution of approx_cost(for two people) was explored using boxplots and stripplots.
Predictive Modeling
Data Preprocessing:

Categorical variables like online_order, book_table, and location were transformed using Binary Encoding to prepare the data for regression.
Linear Regression:

A Linear Regression model was used to predict restaurant ratings (rate). The model was trained on transformed features and evaluated using various metrics.

Mean Squared Error (MSE): 0.1337

R-squared: 0.3026

PCA for Dimensionality Reduction:

Principal Component Analysis (PCA) was applied to reduce the dimensionality of the feature space for visualization and modeling.
Polynomial Regression:

Polynomial features were used to fit a higher-degree regression model to improve prediction performance. The model's performance was evaluated but did not perform as well as expected.
Random Forest Regression:

A Random Forest Regressor was applied to the dataset as a more advanced model. This model showed improvement over linear regression and is explored further for feature importance and prediction.
Evaluation Metrics
The performance of the regression models was evaluated using the following metrics:

Mean Absolute Error (MAE): 0.2841
Mean Squared Error (MSE): 0.1337
Root Mean Squared Error (RMSE): 0.3656
R-squared: 0.3026 (for Linear Regression)
The polynomial regression model performed poorly with negative R-squared values, indicating overfitting or issues with the model complexity.

Key Insights
Restaurant Types: Delivery services are the most common, followed by Dine-out, Buffet, and others.
Online Ordering & Table Booking: A majority of restaurants offer online ordering, and a significant portion provides table booking services.
Price & Rating Relationship: Higher-rated restaurants tend to have higher prices, but the correlation is weak.
Best Model: The Random Forest Regressor showed better predictive power compared to the linear models.
Future Work
Improving Model Performance: Further feature engineering, hyperparameter tuning, and the use of ensemble methods could improve model performance.
Recommendation Systems: Based on the features, a recommendation engine can be built to suggest restaurants to users.
Geospatial Analysis: Given the location data, geospatial analysis could uncover interesting insights about restaurant locations and pricing.
