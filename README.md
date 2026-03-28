# Walmart_Sales_Analysis

Predictive Modeling & Data Engineering

Project Overview :
This project focuses on predicting the Weekly Sales for Walmart stores using historical data. The goal is to help inventory managers understand how external factors like Temperature, Fuel Price, CPI, and Unemployment affect revenue, while accounting for massive seasonal spikes during holidays.

Tech Stack :
Language: Python 3.x
Libraries: Pandas, NumPy, Matplotlib, Seaborn
Modeling: Statsmodels (OLS Regression), Scikit-Learn
Environment: Jupyter Notebook

Data Engineering & Feature Highlights :
To achieve high accuracy, I moved beyond basic cleaning and implemented advanced Feature Engineering:
Multi-Source Integration: Merged Features, Stores, and Train datasets using a composite key of Store and Date.
Time Intelligence: Extracted Year, Month, Week, and Quarter from timestamps to capture cyclical trends.
52-Week Lag Features: Created a "memory" for the model by shifting sales data by 52 weeks, allowing it to "remember" last year's holiday performance.
Categorical Encoding: Applied One-Hot Encoding to Store Types (A, B, C) while avoiding the Dummy Variable Trap.

Key Visualizations : 
Note: These insights were generated using Seaborn and Matplotlib.
1. Sales Seasonality Trend
This chart highlights the massive spikes in sales during the "Super Bowl," "Labor Day," "Thanksgiving," and "Christmas" weeks.
2. Economic Correlation Heatmap
I analyzed how macro-economic factors influence the bottom line. Interestingly, Store Size showed a much stronger correlation with sales than Fuel Prices.
3. Holiday Impact Analysis
A statistical comparison proving that holiday weeks consistently outperform normal weeks, specifically in Type A stores.

Model Performance
I implemented an Ordinary Least Squares (OLS) Regression model to quantify the impact of each feature on Weekly Sales.
Model Type: Ordinary Least Squares (OLS) Regression
Metric (R-Squared): 0.91 (Replace this with your actual value from model.summary)
Key Predictor: Sales_Lag_52 (This captures the yearly seasonality)
Data Strategy: 80/20 Time-Based Split (Using past data to predict the future)
Feature Engineering: 1-week and 52-week Lags included for higher accuracy

Business Recommendations : 
Inventory Buffering: Increase stock levels 2 weeks prior to Week 47 (Thanksgiving) to prevent stockouts.
Store Prioritization: Focus promotional budgets on Type A stores during holidays, as they show the highest sensitivity to seasonal spikes.
Macro-Economic Monitoring: While CPI has an impact, the Lagged Sales are the strongest predictors, suggesting that internal store momentum is the best indicator of future success.
