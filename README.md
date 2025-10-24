# Trader Behavior Insights – Bitcoin Market Sentiment Analysis

This project explores how market sentiment (Fear/Greed) affects trader performance using real trading data from Hyperliquid and sentiment data from the Bitcoin Fear–Greed Index.

# Objective

To uncover ***patterns between trader profitability*** and ***market sentiment*** — and determine whether traders behave differently under Fear vs Greed conditions.

# Data Sources

***1. Historical Trader Data (Hyperliquid)***

    -Columns: account, execution_price, size_tokens, side, closed_pnl, timestamp, etc.
    -Used to compute daily performance metrics such as total trades, total PnL, and win rate.

***2.Bitcoin Market Sentiment (Fear/Greed Index)***

    -Columns: date, classification (Fear / Greed)
    -Used to measure the overall market psychology.

# Analysis Highlights

***Data Cleaning & Preparation***
-Normalized timestamps, merged both datasets by date.
-Handled missing and inconsistent column names (e.g. closed_pnl, timestamp_ist, etc.).

***Exploratory Data Analysis***
-Visualized PnL distributions, win rates, and trade frequency.
-Compared performance metrics between Fear and Greed periods.

***Machine Learning (Logistic Regression)***
-Built a basic classifier predicting profitable vs. unprofitable trades using:
    Leverage
    Trade size
    Side (Buy/Sell)
    Market sentiment score
-Model achieved a mean ROC-AUC ≈ 0.70, indicating moderate predictive strength.

# Key Insights

-Trader behavior shows clear bias under market sentiment:
    Average profits tend to be higher during Greed phases.
    Fear periods often see smaller positions and lower win rates.
-Leverage and trade size have strong correlation with profit probability.
-Sentiment index adds a valuable psychological dimension for risk-aware trading strategies.

# Conclusion

This analysis demonstrates that market psychology — represented by the Fear & Greed Index — significantly influences trading outcomes.
Integrating sentiment indicators into algorithmic models could improve risk management and entry/exit timing for crypto traders.

# Tools Used

Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
Google Colab
GitHub for version control
