# Trader Behavior Insights Based on Bitcoin Market Sentiment

This project analyzes the relationship between Bitcoin market sentiment and trader performance using over 211,000 trades on the Hyperliquid exchange. The objective is to uncover patterns in trader behavior, profitability, and risk exposure under different emotional market states such as Fear, Greed, and Neutral.

---

## Objective

Can market sentiment be used as a signal to anticipate trader profitability, risk behavior, and trading volume?

We examine how traders behave under different emotional market states, utilizing sentiment data from the Fear & Greed Index and real-world execution data from Hyperliquid.

---

## Datasets Used

### 1. Bitcoin Fear & Greed Index
- Source: alternative.me
- 2,644 days of historical data
- Fields: `date`, `value` (0 to 100), `classification` (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

### 2. Hyperliquid Trade History
- 211,224 trades
- Fields include: `Execution Price`, `Size USD`, `Fee`, `Closed PnL`, `Side`, `Account`, `Timestamp IST`

---

## Data Processing

- Converted timestamps in both datasets to standard date format
- Merged datasets on `date` field
- Removed rows with missing sentiment labels
- Aggregated and grouped by sentiment classification for descriptive analysis

---

## Key Insights

- Extreme Greed periods had the highest average profits and lowest transaction fees, suggesting efficient trade execution and bullish market conviction.
- Fear and Extreme Fear days were characterized by higher volatility, higher fees, and significantly larger position sizes. These traits reflect elevated risk-taking during uncertainty.
- Neutral markets delivered the lowest average profits and smallest variance, possibly due to a lack of strong directional movement or liquidity.
- Sentiment labels can be used as input features for supervised learning models or as filters in trading strategy logic.

---

## Visualizations and Analysis

The Jupyter notebook includes:

- Average PnL per sentiment category
- Win rate comparison between sentiment states
- Distribution of transaction fees by sentiment
- Position size trends across emotional phases
- Summary table and recommendations

---

## Technology Stack

- Language: Python 3
- Libraries: pandas, numpy, matplotlib, seaborn
- Development Environment: Jupyter Notebook
- Version Control: Git & GitHub

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/trader-sentiment-analysis.git
   cd trader-sentiment-analysis

2. Install the required packages:
pip install -r requirements.txt

3. Launch the Jupyter notebook:
jupyter notebook notebooks/analysis.ipynb

