# Electricity-Market-Price-Time-Series-Analysis

# Project Overview
- This project aims to forecast hourly values for the next six months using a machine learning approach, specifically the XGBoost Regressor. The forecast accounts for short-term fluctuations in market data by leveraging advanced feature engineering techniques (e.g., lag features) and hyperparameter optimization. To quantify uncertainty in the predictions, confidence intervals are computed.

# Table of Contents
1. Features
2. Pipeline Overview
3. Setup and Installation
4. Results and Visualization
5. Future Improvements

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
- pip install xgboost optuna pandas numpy matplotlib scikit-learn

# Future Improvements
1. **Feature Enhancements:**
- Incorporate external data like weather, holidays, or events to improve predictions.
2. **Alternative Models:**
- Experiment with other models like LightGBM or neural networks (e.g., LSTMs).
3. **Real-Time Forecasting:**
- Implement a real-time pipeline for continuous model updates and predictions.

# Conclusion

This project provides an end-to-end solution for forecasting hourly data over the next six months using XGBoost. By incorporating confidence intervals, the model offers not only predictions but also an understanding of their reliability. The modular structure allows for easy customization and scalability.
