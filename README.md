**Stock Sentiment Analysis and Prediction Project**:

---

# Stock Sentiment Analysis and Prediction

## Overview

This project is aimed at providing a comprehensive analysis of stock price movements by combining **news sentiment analysis** with **technical indicators** and **machine learning models**. It uses sentiment data from news headlines related to a specific stock ticker and predicts future stock prices using technical indicators such as **Moving Averages**, **RSI**, and **MACD**.

## Features

1. **News Scraping & Sentiment Analysis**:
   - Scrapes recent news headlines for a given stock ticker from Google News.
   - Analyzes the sentiment (polarity and subjectivity) of the news using `TextBlob`.
   - Provides investment suggestions based on the analyzed sentiment.

2. **Stock Data Analysis**:
   - Fetches historical stock data from Yahoo Finance.
   - Calculates technical indicators such as Moving Averages (20-day, 50-day), **RSI**, and **MACD**.
   - Identifies **Buy** and **Sell** signals based on RSI and MACD crossovers.

3. **Machine Learning-based Stock Price Prediction**:
   - Uses **Linear Regression** to predict future stock prices based on historical data.
   - Implements **AutoML** through **TPOT** to find the best regression model for stock price forecasting.
   - Evaluates the performance using **MSE**, **MAE**, **RMSE**, **R² Score**, and **MAPE**.

4. **Future Stock Price Forecasting**:
   - Predicts future stock prices for a specific number of days ahead using the trained model.
   - Plots both historical and predicted future prices for visual comparison.

## Prerequisites

To run the project, the following Python libraries need to be installed:

```bash
!pip install beautifulsoup4
!pip install lxml
!pip install html5lib
!pip install textblob
!pip install yfinance
!pip install scikit-learn
!pip install tpot
!pip install ta
```

## Project Structure

- **`scrape_news()`**: Scrapes the latest news headlines for a given stock ticker.
- **`analyze_sentiment()`**: Analyzes the sentiment of the news headlines using `TextBlob`.
- **`fetch_stock_data()`**: Fetches historical stock price data from Yahoo Finance.
- **`plot_sentiment()`**: Plots the sentiment scores (polarity, subjectivity) as a bar chart.
- **`investment_suggestion()`**: Provides investment suggestions based on the sentiment polarity.
- **Technical Analysis**:
  - **Moving Averages (SMA_20, SMA_50)**: Computed for analyzing the trend.
  - **RSI & MACD**: Indicators used to generate buy/sell signals.
- **Stock Price Prediction**:
  - **Linear Regression**: Basic prediction model.
  - **TPOTRegressor**: AutoML for finding the best model for stock price prediction.
- **Model Evaluation**: Calculates performance metrics such as **MSE**, **MAE**, **RMSE**, and **R²**.
- **Future Prediction**: Forecasts stock price for a number of days ahead using the trained TPOT model.

## Usage

1. **Sentiment Analysis and Investment Suggestion**:
   - Enter a stock ticker symbol when prompted.
   - The script scrapes recent news, analyzes sentiment, and provides an investment suggestion based on the polarity score.
   - Example output:
     ```
     Sentiment Polarity: 0.15
     Investment Suggestion: Positive sentiment detected. Consider investing.
     ```

2. **Stock Data and Technical Indicators**:
   - The script fetches stock data from Yahoo Finance, computes technical indicators (RSI, MACD), and displays buy/sell signals.
   - It also plots the stock prices and technical indicators.

3. **Stock Price Prediction**:
   - The project predicts stock prices using linear regression and AutoML (TPOT).
   - The model is evaluated using R² score, MSE, and other metrics.
   - Future stock prices are forecasted and plotted.

## Model Performance Evaluation

- **MSE**: Mean Squared Error
- **MAE**: Mean Absolute Error
- **RMSE**: Root Mean Squared Error
- **R² Score**: Coefficient of determination
- **MAPE**: Mean Absolute Percentage Error

## Example Output

1. **Sentiment Analysis**:
   - Polarity: 0.18 (Positive)
   - Subjectivity: 0.45 (Moderately subjective)

2. **Stock Price Prediction**:
   ```
   MSE: 1.23
   MAE: 0.85
   R² Score: 0.92
   RMSE: 1.11
   MAPE: 2.5%
   ```

3. **Predicted Stock Price for Next Day**:
   ```
   Current Stock Price: 140.25
   Predicted Stock Price for Day 1: 142.58
   ```

## Future Work

- **Incorporate More Sentiment Data**: Expand the news sources for better sentiment analysis.
- **Additional Technical Indicators**: Add more indicators like Bollinger Bands, Stochastic Oscillator, etc.
- **Deep Learning Models**: Experiment with deep learning models such as LSTM for time series forecasting.

## License

This project is licensed under the MIT License.

## Contact

For any queries, please reach out to vishalratnakar453@gmail.com.

---
