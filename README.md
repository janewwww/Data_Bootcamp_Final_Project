# Data_Bootcamp_Final_Project

## 1. Data Sources
### Source 1: Kenneth French Data Library

a. _factors.csv_
- Historical monthly return from 1926/7 to 2021/2
- Fama French Three Factors: MKT, SMB, HML
- RF

b. _portfolio.csv_
- 5*5 Portfolios Sorted on Size and Value
- Different degrees of Size (measured by ME) and Value (measured by BM)
- Historical monthly return from 1926/7 to 2021/2

### Source 2: WRDS Compustat US Mutual Fund Dataset

_mutual_fund_data.csv_

Monthly Scale and return data of all U.S. Mutual Fund
- mret: Return per Share
- mnav: Net Asset Value per Share
- mtna: Total Net Asset Value 

## 2. Data Cleaning

Mainly for _mutual_fund_data.csv_:
- Drop rows with NAN or non-numeric values in mret column
- Drop funds with less than 60 (5 years) number of observations

## 3. Models
### a. Regression on 25 Portfolios from K.F. Data Library
Compare value of betas and correlation with Size & Value factors

### b. Regression on U.S. Mutual Funds
Compare and categorize mutual funds based on value of betas and r-squared ("scores")

### c. k-means
Clustering over mutual funds using regression parameters as features

## 4. Methodology
Given that our factors are constructed based on historical data of US stocks, they construct a model that better explains the return of mutual funds whose major asset allocation is stocks. The fixed-income mutual funds, on the other hand, follows the money market movement and are explained by different factors. Therefore, we reversely extrapolate the main target asset class of the funds from the regression model goodness of fit.
Furthermore, we can also infer the investment style of the funds. A positive and significant beta on a certain factor implies that the return can be contributed to this risk factor exposure. For instance, the positive coefficient on SMB factor implies the fund’s leveraging on small capitalization stocks more than big capitalization stocks, while the negative coefficient on HML factor implies the fund’s leveraging on growth stocks more than value stocks.


## 5. Key visualizations
### Figure 1, 2: 
Heatmap of size and value sorted portfolio returns’ regression coefficients on SMB and HML

### Figure 3:
Scatter plot of size and value coefficients, with color indicating the fitness of regression model

### Figure 4:
Pie chart of different size and value categories of mutual funds, estimated based on the regression coefficients

### Figure 5, 6:
Elbow curve for selecting k of k-means model;
3D scatter plot of size, value coefficients and r-squared, with color indicating the cluster labeled by the model
