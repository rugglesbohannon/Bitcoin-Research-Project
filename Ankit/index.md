## Diversification of Investment Portfolio

![](images/bitcoin.jpg)


### Focus of this page

**Founding father of Cryptocurrency: Bitcoin**

Bitcoin is a cryptocurrency that got the popularity in recent years due to much price increase. The value of bitcoin has increased by **685%** in a span of year.
Bitcoin is the largest cryptocurrency based on the market cap and makes over 50% of the entire cryptocurrency world. It would be fair to say that the entire 
cryptocurrency market is highly correlated to Bitcoin’s price movements. And we know that price movement of bitcoin is very volatile, visually we can see that on 
the graph of bullish and bearish bitcoin price below. 

In the volatile world of cryptocurrency, it is very important to implement some strategies to manage your cryptocurrency investments. Managing your investment 
well means that your portfolio is managed against risk. Keeping these things in mind, I am considering continuing my project on **Diversification of cryptocurrencies
in Investment Portfolio.** This means I will be analyzing what other cyptocurrencies you can hold along with bitcoin for less risk and good profit. For this, I will 
be analyzing the correlation matrix of different types of crypto currencies with bitcoin.

- [x] Want to know more about investment portfolio? [Click here](investment.md)

---

### Data Description

The dataset I am working will be from Yahoo finance and you can access it from here: [Bitcoin data](https://finance.yahoo.com/quote/BTC-USD/history/?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAE1iTQEM3gqle4ifIZ0FxmNSrO2jLU8jHDLYEnM4DGZk4dCEd-VhKRedEtXl6B3t2wj_eoseVG3MVLDWtXR5JAlz3aI6aQAheKcsaQTuFuWYKJvZPD2RdG3mC41_VtyVCE2slSvx_iqysSqDrh8KBvPb6GpvOmdGVTfFMCBkWE0E)
,[Ethereum data](https://finance.yahoo.com/quote/ETH-USD/history/),[NEO data](https://finance.yahoo.com/quote/NEO-USD/) and [USDC data](https://finance.yahoo.com/quote/USDC-USD/).These datasets have different columns of data like high, low, open and close price. They have also got the volumes of Bitcoin,Ethereum,NEO and USDC sold in the market which can be of particular importance
when analyzing the price and quantity of bitcoin sold. I am planning to merge bitcoin dataset with dataset of other cryptos to make a correlation matrix and then decide
what coins to hold in the portfolio.

### Data Wrangling

* Merging: Since my research was to check the correlation of bitcoin price with other cryptos, I started looking for the cryptos which have positive and negative 
correlation with the bitcoin price. I found the data of three other cryptos: NEO, USDC and Ethereum. The next step was to merge all the datasets in order to build 
a correlation heatmap. Ethereum had strong positive correlation with the Bitcoin price, NEO had moderate positive correlation with the Bitcoin price and USDC had 
weak negative correlation with the Bitcoin price. Some of the problems encountered during merging are explained below:
  * DataSets: Since all the datasets that I used were from Yahoo Finance, the column of datasets had the same name(Date,Open,High,Low,Close,Adj Close,Volume), 
              while merging I received something like x_value for the first dataset and y_value for the second dataset. This was not a helpful name to analyze 
              the correlation heatmap so before merging, I changed the name of each column with the acronym of currency name, something like High_BTC for 
              high bitcoin price.
  * Selection of Relevant Columns: Since I was only analyzing the correlation effect of prices of these crypto currencies, I dropped columns except Date and High. 
                                   The column Date was the key to merge the columns of the dataset.

*Below you can see plotly graph object visualization where different bearish and bullish movement caused bitcoin price to rise to its current level. Feel free to make use of slider to see the dates that you are interested.*

{% include_relative Visualizations/bitcoin.html %}

**Different univariate and bivariate plots**

I have chosen univariate plot to visualize both ethereum and bitcoin price. Both the prices have fluctuated a lot in a span of a year. These fluctuations are again
a reminder that our portfolio should be diverse and not just include cryptos that has got strong positive correlation.

{% include_relative Visualizations/boxplot.html %}

{% include_relative Visualizations/box.html %}


To clearly see the positive correlation between bitcoin and ethereum price, I made bivariate scatter plot.This hints on how our portfolio should look: 
it's sure that we don't want our crypto portfolio to contain only bitcoin and ethereum.

{% include_relative Visualizations/ethereum.html %}

**Coming Soon**

I am finding datasets of other cryptos that have moderate relation with the price of Bitcoin. After finding the correlation matrix of all those cryptos with that of 
Bitcoin, I can explain what coins to hold in our portfolio. The visualization might include correlation heatmap which is very important in the field of finance and 
investment.

Cryptos   |High_BTC | High_ETH | High_NEO | High_USDC
----------|---------|----------|----------|----------
High_BTC  | 1.00    | 0.98     |  0.82    | -0.42 
High_ETH  | 0.98    | 1.00     |  0.86    | -0.41   
High_NEO  | 0.83    | 0.86     |  1.00    | -0.20 
High_USDC |-0.43    |-0.42     | -0.20    |  1.00







