# BasicPythonStockPricePredictor
Starter MLRM model using python. Sample stock price dataset from Nishanth Shetty on Kaggle.

# Stock Price Prediction using Linear Regression

## Project Overview
This project aims to forecast the future closing price of a stock using a Multiple Linear Regression model. The analysis is based on historical price data and technical indicators like moving averages. This project serves as a practical application of time-series analysis, feature engineering, and machine learning for financial data.

## Dataset
The dataset used is the historical daily price data for the stock `EW-MAX.csv`. It contains `Date`, `Open`, `High`, `Low`, `Close`, `Adj_Close`, and `Volume` columns, spanning over 4000 trading days.

## Methodology
1.  **Data Cleaning:** The raw data was loaded, dates were converted to the correct datetime format, and the Date column was set as the index.
2.  **Feature Engineering:** Two key features were created to capture market trends: the 7-day Moving Average (MA_7) and the 30-day Moving Average (MA_30).
3.  **Model Training:** A Multiple Linear Regression model was trained on the first 80% of the historical data. The features used were `Adj_Close`, `MA_7`, and `MA_30`, with the target being the next day's closing price.
4.  **Evaluation:** The model's performance was evaluated on the remaining 20% of the data (the test set). The Root Mean Squared Error (RMSE) was the primary metric.

## Results
The model achieved an RMSE of **1.60** on the test set, which was significantly lower than the stock's standard deviation of **30.0**, indicating a strong predictive performance for a baseline model.

## How to Run
1.  Ensure you have Python and Jupyter Notebook installed.
2.  Install the required libraries: `pip install pandas scikit-learn matplotlib statsmodels`
3.  Clone this repository.
4.  Open and run the `PriceProjection.ipynb` notebook.
