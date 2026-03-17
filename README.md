# 💹 Pro-Quant AI Terminal

**Next-Hour Stock Movement Prediction using XGBoost & Streamlit**

[](https://www.python.org/downloads/)
[](https://streamlit.io)
[](https://opensource.org/licenses/MIT)

Pro-Quant is a sophisticated financial dashboard that bridges the gap between raw market data and machine learning. By leveraging **XGBoost**, the terminal analyzes historical price action and technical indicators to forecast the probability of the next hourly candle's direction.

## ✨ Key Features

  * **Real-time Data:** Live market fetching via `yfinance` (Yahoo Finance).
  * **Machine Learning Engine:** Powered by **XGBoost** for high-performance classification.
  * **Technical Alpha:** Automatically generates **RSI**, **Volatility**, and **SMA** features.
  * **Strategy Backtesting:** Real-time comparison between AI strategy returns vs. traditional "Buy & Hold."
  * **Interactive UI:** High-fidelity candlestick charts and probability gauges using **Plotly**.
  * **Adjustable Risk:** Custom confidence thresholds to filter out low-probability signals.

## 🛠️ Tech Stack

  * **Frontend:** [Streamlit](https://streamlit.io/)
  * **Data Science:** [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/)
  * **Machine Learning:** [XGBoost](https://xgboost.readthedocs.io/)
  * **Visualization:** [Plotly](https://plotly.com/)
  * **Finance API:** [yfinance](https://github.com/ranaroussi/yfinance)

## 🚀 Getting Started

### 1\. Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/your-username/pro-quant-terminal.git
cd pro-quant-terminal
pip install -r requirements.txt
```

*Note: If you don't have a `requirements.txt`, install manually:*

```bash
pip install streamlit yfinance pandas numpy xgboost plotly
```

### 2\. Launch the Terminal

```bash
streamlit run stock_app.py
```

## 📊 How It Works

1.  **Ingestion:** The app pulls the last $N$ days of hourly data for a selected ticker.
2.  **Transformation:** It calculates momentum (RSI) and trend (SMA) to create a feature matrix.
3.  **Training:** An XGBoost model is trained on 80% of the data to recognize patterns preceding a price increase.
4.  **Inference:** The model analyzes the *current* candle and provides a probability score for the next movement.

## ⚠️ Disclaimer

**This software is for educational purposes only.** Trading stocks involves significant risk of loss. The authors do not guarantee any financial gain, and this tool should not be used as the sole basis for investment decisions. **Always consult with a certified financial advisor.**

