# sector_ETFs_screener
This script perform a screening and selection of the best ETF for each of the 11 industrial sectors using multiple metrics and ETFs made available by Fidelity. Historical data are retrieved from Yahoo finance using its API.

The user first has to download from Fidelity (https://screener.fidelity.com/ftgw/etf/evaluator/gotoBL/research#/home) the Excel files contaning the ETFs information, one file for each sector.
The script  integrates this dataset with historical prices and enrich the metrics using market data, then some criteria are defined to attribute a weighted score to each ETF and perfom the selection. Finally, some portfolio construction techniques are applied to perform the portfolio selection.

The basic ETFs info are integrated with the following measure computed on the historical prices.
1. closing price change
2. volume change
3. inception date (how long the data is present from)
4. Regression Alpha
5. Regression CAPM Beta (vs mkt)
6. regression R2
7. regression market timing beta
8. return volatility 
9. volume volatility 
10. avg volume 
11. last 30 weeks max ret
12. last 30 weeks max ret

Both Sharpe-ratio and mean-variance optimal portfolios are calculated and the results presented and plotted. The portfolio optimizations are realized using the library pypfopt.
