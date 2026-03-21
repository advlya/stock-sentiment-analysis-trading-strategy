# Stock Sentiment Analysis: Apple vs Tesla

A Python project exploring how news sentiment relates to stock price movements for Apple (AAPL) and Tesla (TSLA).

This project uses natural language processing (NLP) to analyze financial news headlines and tests a simple sentiment-based trading strategy against a traditional buy-and-hold approach.

## Project Overview

The goal of this analysis is to investigate whether positive or negative news sentiment can help predict short-term stock price behavior.

Using historical stock data and recent news headlines, sentiment scores are calculated and used to generate trading signals. The strategy is then backtested and compared with a buy-and-hold benchmark.

## Methodology

1. **Data Collection**

   * Historical stock prices downloaded using `yfinance`
   * News headlines collected for Apple and Tesla

2. **Sentiment Analysis**

   * Sentiment scores calculated using VADER
   * Scores range from **-1 (negative)** to **+1 (positive)**

3. **Trading Strategy**

   * Buy when average sentiment > 0.1
   * Hold cash otherwise

4. **Performance Evaluation**

   * Strategy returns compared with buy-and-hold returns
   * Sentiment distribution across news articles analyzed

## Key Findings

* News sentiment alone was **not sufficient to generate consistent profits**.
* Apple showed mostly neutral sentiment, resulting in **few trading signals**.
* Tesla showed slightly positive sentiment but still **underperformed buy-and-hold** during the period analyzed.
* Results highlight the **limitations of simple rule-based trading strategies**.

## Project Structure

```
stock-sentiment-analysis/
│
├── stock_sentiment_dual_analysis.py
├── stock_sentiment_complete.py
├── stock_sentiment_comparison.png
├── sentiment_distribution_comparison.png
├── analysis_results.json
├── README.md
└── requirements.txt
```

## Tools & Libraries

* Python
* pandas
* numpy
* matplotlib
* yfinance
* vaderSentiment

## Purpose

This project was created as a learning exercise under a mentorship program while exploring Python, financial data analysis, and basic quantitative finance concepts.


