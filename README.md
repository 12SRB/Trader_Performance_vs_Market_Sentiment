# Trader Performance vs Market Sentiment

## Overview
This project analyzes how market sentiment (Fear vs Greed)
impacts trader performance and trading behavior using historical
transaction-level data combined with sentiment indicators.

The objective is not only to measure performance differences,
but also to understand how trader behavior adapts under
different emotional market regimes.


## Problem Statement
Financial markets are strongly influenced by collective
sentiment such as fear and greed. Traders often adjust
their risk-taking behavior, trade frequency, and position
direction based on prevailing market emotions.

This project aims to answer:
- Does trader performance change across Fear and Greed periods?
- Do traders behave differently under different sentiment regimes?
- Can sentiment be used to guide better risk management strategies?


## Dataset Description
The analysis uses two datasets:

### 1. Trader Transaction Data
Contains detailed trade-level information including:
- Account identifier
- Trade size (USD)
- Buy / Sell direction
- Closed PnL
- Timestamps

### 2. Market Sentiment Data
Contains daily market sentiment indicators including:
- Timestamp / date
- Fear & Greed value
- Sentiment classification (Fear, Extreme Fear, Greed, etc.)


## Repository Structure
Trader_Performance_vs_Market_Sentiment
│
├── analysis.ipynb # Complete analysis notebook
├── README.md # Project documentation
│
├── data/
│ ├── historical_data.csv # Trader transaction data
│ └── sentiment.csv # Market sentiment data
│
└── outputs/
├── avg_pnl_by_sentiment.png
├── winrate_by_sentiment.png
└── long_short_bias.png


## Setup & How to Run

### Requirements
- Python 3.x
- Jupyter Notebook or Google Colab

### Steps to Run
1. Open `analysis.ipynb` using Google Colab or Jupyter Notebook.
2. Upload the CSV files from the `data/` folder when prompted.
3. Run all cells sequentially from top to bottom.
4. Generated charts will be automatically saved in the `outputs/` folder.

No additional environment setup or package installation is required.


## Methodology

### Data Preparation
- Loaded and inspected both datasets.
- Documented dataset dimensions, missing values, and duplicates.
- Converted timestamps and aligned both datasets at daily granularity.
- Merged trading data with sentiment data based on date.

### Feature Engineering
Created key metrics including:
- Daily PnL
- Win rate
- Trade frequency
- Average trade size
- Long / short position ratios
- PnL volatility as a risk proxy

### Analysis
- Compared trader performance across Fear and Greed periods.
- Examined behavioral changes such as trade frequency and direction bias.
- Segmented traders based on activity and consistency.
- Visualized findings using charts and summary tables.


## Key Insights

- Trader performance differs significantly across market sentiment regimes.
- Greed periods are associated with higher average PnL and win rates.
- Fear periods show increased volatility and downside risk.
- Traders tend to reduce activity and take more defensive positions during Fear.
- Consistent traders outperform aggressive but volatile traders across all conditions.

---

## Strategy Recommendations

- Implement sentiment-aware risk controls, especially during Fear periods.
- Reduce leverage and position sizes when volatility risk is elevated.
- Encourage disciplined trading behavior over aggressive strategies.
- Use trader segmentation to tailor exposure limits and platform policies.


## Bonus Analysis

- Trader Clustering:  
  Traders were grouped into behavioral archetypes using clustering techniques
  based on trade size, frequency, win rate, and PnL volatility.

- Predictive Modeling:
  A lightweight predictive model was implemented to demonstrate how
  sentiment can be used to estimate short-term volatility risk.
  The model is presented as an illustrative example due to data limitations.

## Final Takeaway
Market sentiment plays a critical role in shaping both trader performance
and behavior. Incorporating sentiment-aware analytics can significantly
improve risk management, decision-making, and overall trading outcomes.

This project demonstrates a structured, data-driven approach to
analyzing behavioral finance effects in real-world trading data.
