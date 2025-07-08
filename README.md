# 🇬🇷 Greek Stock Portfolio Optimization & Backtesting

This project applies Modern Portfolio Theory (MPT) to a diversified selection of 10 Greek equities listed on the Athens Stock Exchange (ATHEX). Using historical price data from Yahoo Finance, we calculate performance metrics, construct optimized portfolios, and evaluate their out-of-sample performance through backtesting.

---

## 📈 Objectives

- Retrieve historical price data for 10 major Greek stocks using `yfinance`
- Calculate key financial and risk metrics: Sharpe Ratio, Sortino Ratio, Max Drawdown, VaR, CVaR
- Construct:
  - **Minimum Variance Portfolio** (lowest risk under constraints)
  - **F Portfolio** (target 20% annual return)
- Visualize:
  - Portfolio allocations (pie charts)
  - Efficient frontier of 10,000 random portfolios
  - Cumulative performance during backtest (2023–2024)
- Backtest both portfolios using a train/test split
- Compare risk-return tradeoffs out-of-sample

---

## 💼 Assets Used

All assets are traded on the Athens Stock Exchange:

```
['HTO.AT', 'EUROB.AT', 'ETE.AT', 'TPEIR.AT', 
 'MOH.AT', 'ELPE.AT', 'BELA.AT', 'OPAP.AT', 
 'MYTIL.AT', 'GEKTERNA.AT']
```

---

## 🧪 Methodology

1. **Data Source**: Daily adjusted close prices from 2019–2024 via Yahoo Finance
2. **Metrics**: Returns, volatility, Sharpe/Sortino ratios, drawdowns, VaR/CVaR
3. **Optimization**:
   - No short-selling (weights ≥ 0)
   - Fully invested (weights sum to 1)
   - Target return constraint (for F portfolio)
4. **Backtesting**:
   - Train on 2019–2022, test on 2023–2024
   - Evaluate real-world performance of both strategies

---

## 📊 Key Visualizations

- Normalized price chart
- Efficient frontier
- Pie charts of portfolio weights
- Cumulative return plots during backtest

---

## 🛠️ Tools Used

- Python (Colab)
- `pandas`, `numpy`, `matplotlib`
- `yfinance` for data
- `scipy.optimize` for portfolio optimization

---

## 🚀 How to Run

1. Clone the repository or open the notebook directly in Google Colab
2. Run all cells top-to-bottom
3. Adjust tickers, time frames, or constraints as needed

---

## 📁 File Structure

```
greek_portfolio_optimization_backtest.ipynb   # Main notebook
README.md                                     # Project description
```

---

## 📌 Possible Extensions

- Add ETFs or international assets for diversification
- Introduce rolling window rebalancing
- Use machine learning for factor-based selection
- Deploy as a Streamlit dashboard

---

## 📄 License

This project is for educational and academic use only.
