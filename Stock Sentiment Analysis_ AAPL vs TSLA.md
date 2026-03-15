# README Stock Sentiment Analysis: AAPL vs TSLA

A comprehensive Python project analyzing how news sentiment influences stock price movements for Apple (AAPL) and Tesla (TSLA).

**Author:** Student Project for AI Mentorship Course  
**Grade Level:** IBDP Grade 11  
**Date:** January 2026

---

## 📊 Project Overview

This project investigates the relationship between news sentiment and stock price movements using natural language processing (NLP) and algorithmic trading concepts. The analysis compares two major tech stocks to determine if sentiment-based trading strategies can outperform a simple buy-and-hold approach.

### Key Questions
- Can news sentiment predict stock price movements?
- Do different stocks respond differently to the same sentiment signals?
- What are the limitations of simple rule-based trading strategies?

---

## 🎯 Methodology

### 1. **Data Collection**
- Downloaded 6 months of historical stock data (Jan 1 - Jun 30, 2024)
- Fetched recent news headlines for both AAPL and TSLA
- Used the `yfinance` library for reliable financial data

### 2. **Sentiment Analysis**
- Implemented **VADER** (Valence Aware Dictionary and sEntiment Reasoner)
- VADER is specifically tuned for social media and news sentiment
- Calculated sentiment scores ranging from -1 (very negative) to +1 (very positive)

### 3. **Trading Strategy**
- **Buy Signal:** When average daily sentiment > 0.1 (threshold)
- **Sell/Hold Cash:** When sentiment ≤ 0.1
- **Backtested** the strategy against a buy-and-hold benchmark

### 4. **Performance Evaluation**
- Compared strategy returns vs. buy-and-hold returns
- Analyzed sentiment distribution across news articles
- Identified key insights and limitations

---

## 📈 Results

### AAPL (Apple)
| Metric | Value |
|--------|-------|
| Average Sentiment | 0.022 (Neutral) |
| Positive News | 4 articles (40%) |
| Negative News | 2 articles (20%) |
| Neutral News | 4 articles (40%) |
| **Strategy Return** | **0.00%** |
| **Buy & Hold Return** | **13.76%** |
| **Outperformance** | **-13.76%** ❌ |

### TSLA (Tesla)
| Metric | Value |
|--------|-------|
| Average Sentiment | 0.150 (Slightly Positive) |
| Positive News | 4 articles (40%) |
| Negative News | 2 articles (20%) |
| Neutral News | 4 articles (40%) |
| **Strategy Return** | **-20.34%** |
| **Buy & Hold Return** | **-20.34%** |
| **Outperformance** | **0.00%** ➖ |

---

## 🔍 Key Findings

1. **Sentiment alone is insufficient** for profitable trading
   - AAPL: Strategy stayed in cash (0% return) while stock gained 13.76%
   - TSLA: Strategy was fully invested but stock declined 20.34%

2. **Different stocks respond differently to sentiment**
   - AAPL had neutral sentiment (0.022) → No buy signals
   - TSLA had slightly positive sentiment (0.150) → 100% invested
   - Same strategy, different outcomes

3. **Threshold optimization matters**
   - A 0.1 threshold may be too conservative for this dataset
   - Lower thresholds might generate more signals

4. **Market conditions matter more than sentiment**
   - Both stocks declined or stagnated during this period
   - Positive news couldn't overcome broader market headwinds

---

## 📁 Project Structure

```
stock-sentiment-analysis/
├── stock_sentiment_dual_analysis.py    # Main analysis script
├── stock_sentiment_complete.py         # Single-stock version (AAPL)
├── stock_sentiment_comparison.png      # Comparison charts
├── sentiment_distribution_comparison.png # Sentiment distributions
├── analysis_results.json               # Data export
├── README.md                           # This file
└── requirements.txt                    # Python dependencies
```

---

## 🛠️ Installation & Usage

### Prerequisites
- Python 3.8+
- pip or conda

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/stock-sentiment-analysis.git
   cd stock-sentiment-analysis
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the analysis**
   ```bash
   python stock_sentiment_dual_analysis.py
   ```

### Output
The script generates:
- `stock_sentiment_comparison.png` - Price charts with trading signals
- `sentiment_distribution_comparison.png` - Sentiment histograms
- Console output with detailed statistics

---

## 📚 Libraries Used

| Library | Purpose |
|---------|---------|
| `yfinance` | Download stock data and news headlines |
| `vaderSentiment` | Natural Language Processing for sentiment analysis |
| `pandas` | Data manipulation and analysis |
| `numpy` | Numerical computations |
| `matplotlib` | Data visualization |

---

## 🧠 Technical Concepts

### VADER Sentiment Analysis
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that:
- Works well with social media and news text
- Provides a compound score (-1 to +1)
- Considers punctuation, capitalization, and emoticons
- Doesn't require training data

### Backtesting
Backtesting evaluates a trading strategy using historical data:
- Simulates trades based on signals
- Calculates returns and performance metrics
- Compares against a benchmark (buy-and-hold)

### Algorithmic Trading
Using computer programs to execute trades based on predefined rules:
- Removes emotional decision-making
- Can process large volumes of data instantly
- Requires rigorous testing and risk management

---

## ⚠️ Limitations

1. **Limited Data**
   - Only 10 recent news articles per stock
   - 6-month analysis period
   - No historical news for each trading day

2. **Simple Strategy**
   - Rule-based approach (threshold > 0.1)
   - No machine learning optimization
   - Doesn't account for transaction costs

3. **Market Factors**
   - Ignores technical indicators (RSI, MACD, etc.)
   - Doesn't consider macroeconomic factors
   - No risk management or position sizing

4. **Sentiment Analysis**
   - VADER is keyword-based, not deep learning
   - May miss context or sarcasm
   - Limited to English text

---

## 🚀 Future Improvements

### Short-term
1. **Lower the threshold** to 0.05 or 0.0 to generate more signals
2. **Add technical indicators** (RSI, Bollinger Bands, MACD)
3. **Include more stocks** (Microsoft, Google, Amazon)

### Medium-term
1. **Collect historical news** for each trading day
2. **Implement machine learning** (Random Forest, Neural Networks)
3. **Use advanced NLP models** (BERT, FinBERT for financial sentiment)
4. **Add risk management** (stop-loss, position sizing)

### Long-term
1. **Real-time trading system** with live news feeds
2. **Multi-factor analysis** combining sentiment, technicals, and fundamentals
3. **Portfolio optimization** across multiple stocks
4. **Risk-adjusted returns** (Sharpe ratio, Sortino ratio)

---

## 📖 Learning Outcomes

This project demonstrates:
- ✅ Python programming fundamentals (loops, functions, data structures)
- ✅ Data analysis with pandas and numpy
- ✅ Natural Language Processing (NLP) basics
- ✅ Financial data analysis and backtesting
- ✅ Data visualization with matplotlib
- ✅ Algorithmic thinking and problem-solving
- ✅ Understanding of market dynamics and trading concepts

---

## 📝 References

- [VADER Sentiment Analysis](https://github.com/cjhutto/vaderSentiment)
- [yfinance Documentation](https://github.com/ranaroussi/yfinance)
- [Pandas Documentation](https://pandas.pydata.org/)
- [Algorithmic Trading Basics](https://en.wikipedia.org/wiki/Algorithmic_trading)

---

## 📧 Contact

For questions or feedback about this project, please reach out through GitHub Issues.

---

## 📄 License

This project is provided as-is for educational purposes. Feel free to use, modify, and distribute for learning.

---

**Last Updated:** January 7, 2026  
**Status:** ✅ Complete and Tested
