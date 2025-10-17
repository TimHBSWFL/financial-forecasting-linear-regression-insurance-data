# Financial Forecasting with Linear Regression on Synthetic Insurance Data
## Overview

This project demonstrates a complete forecasting workflow using synthetic insurance transaction data generated with NumPy.
The objective was to predict total transaction volumes for the last quarter of 2025, applying regression modeling, hyperparameter tuning, and data visualization to evaluate regional and product-level trends.

## Data Generation

A dataset of 100,000 synthetic transactions was created to simulate real-world insurance activity from January 1, 2024, to September 30, 2025.
Each record includes:

*Product type: Renters, Homeowners, Flood
*Region: Northeast, Midwest, South, West
*Installment amount: Randomized transaction value
*Transaction date: Daily records generated using NumPy’s random and datetime functions

## Modeling and Benchmarking

The analysis began with a Linear Regression model to establish a benchmark using default parameters.
To explore potential improvements, I implemented hyperparameter tuning across multiple regression algorithms:

*Linear Regression
*Lasso Regression
*Ridge Regression
*Decision Tree Regressor
*Random Forest Regressor
*XGBoost Regressor

A parameter search loop was used to evaluate each model and record the best_params, best_score, and best_estimator.

## Results

Model performance was assessed using Root Mean Squared Error (RMSE) and R² Score.
Despite extensive tuning, none of the models significantly outperformed the baseline Linear Regression model.

*Best model: Lasso Regression
*RMSE: 19.67
*R²: 0.9185

Interestingly, the XGBoost and Random Forest models produced slightly weaker results than the benchmark.

## Forecast and Visualization

The best-performing model was applied to forecast Q4 2025 transaction totals, both at the regional level and by region-product combination.
Visualizations were created using Matplotlib to illustrate forecasted patterns.

Key insights:

*The Southern region showed the highest projected transaction amounts across all product categories.
*Forecasted distributions across other regions followed historical proportions, indicating stable regional trends in synthetic data behavior.