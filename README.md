# Electricity-Market-Price-Time-Series-Analysis

# Project Overview
This project aims to forecast hourly electricity market prices for the next six months using a machine learning approach, specifically the XGBoost Regressor. The forecast accounts for short-term fluctuations in market data by leveraging advanced feature engineering techniques (e.g., lag features) and hyperparameter optimization. To quantify uncertainty in the predictions, confidence intervals are computed. Additionally, exploratory data analysis (EDA) is conducted to uncover patterns and insights in electricity market prices, including trends, seasonality, and dependencies on external and temporal factors.

# Table of Contents
1. Features
2. Pipeline Overview
3. Setup and Installation
4.  Future Improvements

# Pipeline Overview
1. **Data Preparation**
- Feature Engineering: Adds temporal and lag features to capture short-term and seasonal patterns.
- Data Normalization: Scales numerical features using StandardScaler.
2. **Model Training and Hyperparameter Optimization**
- Uses Optuna for hyperparameter tuning to minimize RMSE.
- Time-based cross-validation (TimeSeriesSplit) is applied to avoid data leakage.
3. **Forecasting**
- Retrain the model on the entire dataset to capture all patterns.
- Generate 6 months' worth of hourly timestamps for future predictions.
Preprocess the generated data and make predictions.
4. **Confidence Intervals**
- Bootstrap resampling is used to compute confidence intervals for predictions.
5. **Visualization**
- Historical data and future predictions are plotted with confidence intervals.

# Setup and Installation
**Requirements**
- Python 3.8 or higher
- Libraries:
- xgboost
- optuna
- pandas
- numpy
- matplotlib
- scikit-learn

**Installation**
Install the required libraries using:

```
- pip install xgboost optuna pandas numpy matplotlib scikit-learn
```

# Future Improvements
1. **Feature Enhancements:**
- Incorporate external data like weather, holidays, or events to improve predictions.
2. **Alternative Models:**
- Experiment with other models like LightGBM or neural networks (e.g., LSTMs).
3. **Data Resampling and Exploration:**
- Resample the hourly data into different timeframes, such as daily or weekly, to explore broader trends and enhance the understanding of long-term patterns.

# Conclusion

This project provides an end-to-end solution for forecasting hourly electricity market prices over the next six months using XGBoost. The exploratory data analysis highlights key trends, including daily and weekly seasonality, mid-month price increases, and dependencies on previous prices, which inform the forecasting approach. By incorporating confidence intervals, the model offers not only predictions but also an understanding of their reliability. The modular structure allows for easy customization and scalability, making it adaptable to various scenarios in the electricity market.
