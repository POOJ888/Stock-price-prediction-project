# 📈 Stock Price Prediction with Linear Regression

A lightweight baseline project that **downloads daily stock data, engineers simple lag features, trains a Linear Regression model, and forecasts the next-day closing price.**  
Perfect as a starter template before moving to more advanced models (XGBoost, LSTM, Prophet, etc.).

---

## 🧩 Key Features

| Feature                         | Details |
|---------------------------------|---------|
| **Auto-download data**          | Fetches OHLCV via **[yfinance](https://pypi.org/project/yfinance/)** (`--ticker`, `--period`). |
| **Time-series-aware split**     | Keeps chronological order (no shuffling) for train/test. |
| **Lag-based features**          | Uses previous 1-, 2-, and 3-day closes + a numeric day index. |
| **Simple baseline model**       | `StandardScaler ➜ LinearRegression` (scikit-learn). |
| **Metrics**                     | Mean Absolute Error (MAE) and R² on a held-out test set. |
| **Visualization**               | Saves PNG comparing *actual vs predicted* prices. |
| **Model persistence**           | Saves trained model (`joblib`) and allows one-off inference via `--predict`. |

---

## 📁 Project Structure


---

## ⚙️ Installation

```bash
git clone https://github.com/yourname/stock-price-lr.git
cd stock-price-lr
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install yfinance pandas numpy scikit-learn matplotlib joblib
