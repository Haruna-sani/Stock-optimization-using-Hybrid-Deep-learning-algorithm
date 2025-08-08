# 🧠📈 Forecast First, Optimize Next: Deep Learning + Portfolio Strategy

This project explores the integration of **deep learning** and **portfolio optimization** to not only forecast stock prices but also derive actionable investment strategies.

## 📌 Project Overview

Can deep learning do more than just predict stock prices — can it guide **smarter investment decisions**?

This end-to-end project combines a **hybrid CNN + Bi-LSTM model** for stock price forecasting with **mean-variance portfolio optimization** to answer that question.

## 📊 Stocks Analyzed

Forecasts were made for the adjusted close prices of six major tech stocks using data from **2018 to 2025** via [yfinance](https://pypi.org/project/yfinance/):

- AAPL
- AMZN
- META
- MSFT
- GOOGL
- NVDA

---

## 🔍 Part 1: Deep Learning Forecasting

Each stock was modeled independently using a **CNN + Bi-LSTM hybrid architecture**:

- CNN captures local patterns in the time series
- Bi-LSTM captures long-term temporal dependencies

### 📈 Model Results (Test Set)

| Ticker | R² Score | MAE    |
|--------|----------|--------|
| AAPL   | 0.985    | 4.52   |
| AMZN   | 0.977    | 4.28   |
| META   | 0.989    | 10.85  |
| MSFT   | 0.990    | 7.36   |
| GOOGL  | 0.978    | 4.49   |
| NVDA   | 0.986    | 3.52   |

✅ All models achieved **R² > 0.97**  
✅ MAE remained within acceptable bounds despite volatility  
✅ Forecasts closely followed actual stock trends

---

## 💼 Part 2: Portfolio Optimization

Using the **forecasted prices**, two types of portfolios were constructed via **mean-variance optimization**:

### 🏆 Maximum Sharpe Ratio Portfolio

| Stock  | Weight (%) |
|--------|------------|
| AAPL   | 58.44      |
| MSFT   | 30.77      |
| GOOGL  | 8.47       |
| AMZN   | 1.74       |
| META   | 0.50       |
| NVDA   | 0.07       |

📈 **Expected Return**: 28.79%

### 🛡️ Minimum Variance Portfolio

| Stock  | Weight (%) |
|--------|------------|
| AMZN   | 75.69      |
| META   | 7.13       |
| GOOGL  | 7.42       |
| NVDA   | 2.36       |
| AAPL   | 4.02       |
| MSFT   | 3.38       |

📈 **Expected Return**: 27.40%

### 📉 Benchmark

- **NASDAQ-100 Return**: 25.70%

> 📌 Assumptions: No short-selling, full capital allocation, based on forecasted return and covariance matrix.

---

## ✨ Key Insights

- Hybrid **CNN + Bi-LSTM models** offer high-accuracy stock forecasts
- Pairing forecasts with **portfolio optimization** transforms predictions into **investment decisions**
- This approach is applicable to **quantitative finance**, **AI in investing**, and **risk-managed strategies**

---

## 🧪 Tech Stack

- Python (Pandas, NumPy, Matplotlib, Scikit-learn)
- TensorFlow/Keras (CNN + Bi-LSTM Modeling)
- YFinance (Data Sourcing)
- PyPortfolioOpt (Portfolio Optimization)

---

