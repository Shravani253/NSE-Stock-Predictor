# NSE-Stock-Predictor
Stock market up/down predictor trained on NSE data with yfinance API.

Introduction:

This project is a stock market prediction model built using NSE historical stock data and machine learning. The goal is to predict whether the stock price will move up or down the next day by analyzing past price movements and trends.

Objective:

To use historical NSE data and apply data cleaning, feature engineering, and machine learning for stock movement prediction.

To test if a RandomForestClassifier can capture patterns in stock trends.

To evaluate the predictive ability of the model using backtesting techniques.

⚙️Methodology:

Data Collection
Data fetched via yfinance API (NSE stock values).
Although NSE data is available since 1927, effective values are considered from 1990 onwards for analysis.

Data Cleaning & Feature Engineering
Added a new column Tomorrow = shifted Close (-1).

Created a Target column:
+1 → if Tomorrow price > Close (price goes up).
0 → otherwise (price goes down).

Model Training

Applied RandomForestClassifier to predict next-day price direction (up/down).
Initial evaluation done on the training data.

Backtesting

Performed rolling backtest to evaluate predictive performance across time.
Added features like close ratio and trend indicators to improve accuracy.

Evaluation

Compared model predictions with actual outcomes to measure how often the stock was predicted correctly up or down.

Conclusion:

The RandomForest model captures certain short-term patterns in NSE stock price movement.
Feature engineering (close ratio, trend) improves performance, but prediction accuracy is still limited by market randomness.
The project demonstrates a baseline ML approach for stock prediction, which can be further enhanced with more features, advanced models, or sentiment data.
