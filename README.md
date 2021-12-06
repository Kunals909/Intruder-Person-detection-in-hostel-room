
# Stock Portfolio Optimisation 
- ## Terms 
Clustering (K-means, Hierarchical), Unsupervised Machine Learning, Portfolio Diversification, Sharpe Ratio, Volatility, Python.

- ## Aim 
We employ clustering algorithms in this project to generate a diversified portfolio that reduces volatility and total risk of an investment portfolio. 

---
- ## Libraries
     - Numpy
     - Pandas
     - matplotlib
     - glob
     - os 
     - Agglomerative Clustering

- ## Summary 
The purpose of this research is to use clustering to create a well-diversified portfolio.  

 We worked with four different models:

 (1) k-means clustering with daily log returns as features.

 (2) agglomerative (hierarchical) clustering algorithms with single linkage.

 (3) complete linkage.

 (4) and average linkage based on correlation distances. For more information, see the project notebook/report/slides. 

---
![](https://github.com/jiyoungsim/Portfolio-Diversification-Based-on-Clustering-Analysis/blob/master/figs/portfolio_consturction.png?raw=true) 
 
Four equally weighted portfolios of 30 equities are created by selecting the stock with the highest Sharpe ratio from each cluster. The final model is agglomerative clustering with average linkage trained on the last one year of data, based on silhouette scores and Sharpe ratio. 

![](https://github.com/jiyoungsim/Portfolio-Diversification-Based-on-Clustering-Analysis/raw/master/figs/results.png) 


![](https://github.com/jiyoungsim/Portfolio-Diversification-Based-on-Clustering-Analysis/raw/master/figs/silhouette.png) 

![](https://github.com/jiyoungsim/Portfolio-Diversification-Based-on-Clustering-Analysis/raw/master/figs/volatility.png)

 - In terms of Sharpe ratio, the selected portfolio outperformed random selection but fell short of the DJIA over the test period. The selected portfolio had an annualised volatility that was lower than random selection as well as the average volatility of all clusters, and was quite close to that of an equally weighted portfolio consisting of all 470 stocks in the data. In addition, only one of the 30 clusters had a lower volatility than the chosen portfolio. The following suggestions for improvements and more research are made: 

-  Sharpe Ratio can be replaced with the following metrics: Value-at-Risk, Sortino Ratio, and so forth. 

-  Change the number of clusters and the length of the training period. 

-  Change/expand the stock pool 

-  Set up distance thresholds. 

-  To maximise the Sharpe ratio, assign weights to each stock in the portfolio based on an optimization problem. 

-  Add/use information about each company's industry sector. 

-  To describe the changes in stock prices over time, use time series analysis.