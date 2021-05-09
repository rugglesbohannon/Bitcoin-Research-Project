## Diversification of Investment Portfolio

![](images/bitcoin.jpg)


### Focus of this page

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

The dataset I am working is from Yahoo finance and you can access it from here: [Bitcoin data](https://finance.yahoo.com/quote/BTC-USD/history/?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAE1iTQEM3gqle4ifIZ0FxmNSrO2jLU8jHDLYEnM4DGZk4dCEd-VhKRedEtXl6B3t2wj_eoseVG3MVLDWtXR5JAlz3aI6aQAheKcsaQTuFuWYKJvZPD2RdG3mC41_VtyVCE2slSvx_iqysSqDrh8KBvPb6GpvOmdGVTfFMCBkWE0E)
,[Ethereum data](https://finance.yahoo.com/quote/ETH-USD/history/),[NEO data](https://finance.yahoo.com/quote/NEO-USD/) and [USDC data](https://finance.yahoo.com/quote/USDC-USD/).These datasets have different columns of data like high, low, open and close price. They have also got the volumes of Bitcoin,Ethereum,NEO and USDC sold in the market which can be of particular importance
when analyzing the price and quantity of bitcoin sold. I am planning to merge bitcoin dataset with dataset of other cryptos to make a correlation matrix and then decide
what coins to hold in the portfolio.

---

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

* Missing values: During my initial inspection of the dataset, I found that the weekend datas were missing from the dataset.Later on I realized that during 
these times the stock market is closed. Although the stock market is closed, trading apps like Robinhood, Coinbase allow you to trade these cryptos during the weekend. 
I tried to find these datas and wanted to fill in the missing days but it seems like these apps don’t provide their data publicly. In future, if this is available 
you can easily use pandas data analysis tool to add those data values. 

* Correlation Matrix: For this part of data analysis, I used pearson coefficient correlation method and received the following data:

Cryptos   |High_BTC | High_ETH | High_NEO | High_USDC
----------|---------|----------|----------|----------
High_BTC  | 1.00    | 0.98     |  0.82    | -0.42 
High_ETH  | 0.98    | 1.00     |  0.86    | -0.41   
High_NEO  | 0.83    | 0.86     |  1.00    | -0.20 
High_USDC |-0.43    |-0.42     | -0.20    |  1.00

---

*Below you can see plotly graph object visualization where different bearish and bullish movement caused bitcoin price to rise to its current level. Feel free to make use of slider to see the dates that you are interested.*

{% include_relative Visualizations/bitcoin.html %}

---

**Different bivariate plots**

There are different biavariate scatter plots that are useful to visualize how these cryptocurrencies are correlated.

{% include_relative Visualizations/ethereum.html %}


From the above scatter plot, we can see that there is a strong positive correlation between the ethereum and the bitcoin price.

{% include_relative Visualizations/NEO.html %}

From the above scatter plot, we can see that there is moderate positive correlation between the NEO and the bitcoin price.

{% include_relative Visualizations/USDC.html %}

Finally from the above scatter plot, we can see that there is a weak negative correlation between the USDC and the bitcoin price.

---

### Correlation HeatMap

*Below you can see the correlation heatmap of all the prices of cryptocurrencies that I am working in this project. Feel free to hover your mouse on different blocks
to see the correlation between the prices of different currencies.* 

{% include_relative Visualizations/correlation.html %}

---

This is a link to Jupyter notebook which has got the code for data wrangling and analysis. [Jupyter Notebook](Project.ipynb)









