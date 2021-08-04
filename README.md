# sector_ETFs_screener
This script perform a screening and selection of the best ETF for each of the 11 industrial sectors using multiple metrics and ETFs made available by Fidelity

The user first has to download from Fidelity (https://screener.fidelity.com/ftgw/etf/evaluator/gotoBL/research#/home) the Excel files contaning the ETFs information, one file for each sector.
The script  integrates this dataset with historical prices and enrich the metrics using market data, then some criteria are defined to attribute a weighted score to each ETF and perfom the selection. Finally, some portfolio construction techniques are applied to perform the portfolio selection.
