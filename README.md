# Data_Bootcamp_Final_Project

# 1. Data Sources
## Source 1: Kenneth French Data Library

a. _factors.csv_
- Historical monthly return from 1926/7 to 2021/2
- Fama French Three Factors: MKT, SMB, HML
- RF

b. _portfolio.csv_
- 5*5 Portfolios Sorted on Size and Value
- Different degrees of Size (measured by ME) and Value (measured by BM)
- Historical monthly return from 1926/7 to 2021/2

## Source 2: WRDS Compustat US Mutual Fund Dataset

_mutual_fund_data.csv_

Monthly Scale and return data of all U.S. Mutual Fund
- mret: Return per Share
- mnav: Net Asset Value per Share
- mtna: Total Net Asset Value 

# 2. Data Cleaning

Mainly for _mutual_fund_data.csv_:
- Drop rows with NAN or non-numeric values in mret column
- Drop funds with less than 60 (5 years) number of observations

# 3. Models
## a. Regression on 25 Portfolios from K.F. Data Library
Compare value of betas and correlation with Size & Value factors
## b. Regression on U.S. Mutual Funds
Compare and categorize mutual funds based on value of betas and r-squared ("scores")
## c. k-means
Clustering over mutual funds using regression parameters as features

# 4. Methodology

# 5. Key visualizations:
## Figure 1,2: 
Heatmap of size and value sorted portfolio returns’ regression coefficients on SMB and HML

## Figure 3:
Scatter plot of size and value coefficients, with color indicating the fitness of regression model

## Figure 4:
Pie chart of different size and value categories of mutual funds, estimated based on the regression coefficients
