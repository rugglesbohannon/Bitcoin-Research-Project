## Welcome to Ankit's Bitcoin Page

![](images/bitcoin.jpg)

**Broad Questions**
1. Is it safe to invest only in Bitcoin?
2. How can we maintain investment portfolio of Cryptocurrency to minimize our risk and earn smart profit?
3. Will dogecoin land on the moon and how will bitcoin help dogecoin? 
4. Which cryptos have positive correlation with bitcoin and which cryptos are unrelated to dogecoin?

**Focus of this page**

*Founding father of Cryptocurrency: Bitcoin*

Bitcoin is a cryptocurrency that got the popularity in recent years due to much price increase. The value of bitcoin has increased by **685%** in a span of year.
Bitcoin is the largest cryptocurrency based on the market cap and makes over 50% of the entire cryptocurrency world. It would be fair to say that the entire 
cryptocurrency market is highly correlated to Bitcoin’s price movements. And we know that price movement of bitcoin is very volatile, visually we can see that on 
the graph of bullish and bearish bitcoin price below. 

In the volatile world of cryptocurrency, it is very important to implement some strategies to manage your cryptocurrency investments. Managing your investment 
well means that your portfolio is managed against risk. Keeping these things in mind, I am considering continuing my project on **Diversification of cryptocurrencies
in Investment Portfolio.** This means I will be analyzing what other cyptocurrencies you can hold along with bitcoin for less risk and good profit. For this, I will 
be analyzing the correlation matrix of different types of crypto currencies with bitcoin.

- [x] Want to know more about investment portfolio? [Click here](investment.md)

**Data Description**

The dataset I am working will be from Yahoo finance and you can access it from here: [Bitcoin data](https://finance.yahoo.com/quote/BTC-USD/history/?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAE1iTQEM3gqle4ifIZ0FxmNSrO2jLU8jHDLYEnM4DGZk4dCEd-VhKRedEtXl6B3t2wj_eoseVG3MVLDWtXR5JAlz3aI6aQAheKcsaQTuFuWYKJvZPD2RdG3mC41_VtyVCE2slSvx_iqysSqDrh8KBvPb6GpvOmdGVTfFMCBkWE0E)
It has different columns of data like high, low, open and close price. It has also got the volumes of Bitcoin sold in the market which can be of particular importance
when analyzing the price and quantity of bitcoin sold. I am planning to merge bitcoin dataset with dataset of other cryptos to make a correlation matrix and then decide
what coins to hold in the portfolio.

**Issues encountered with dataset and Analyzation**

* The bitcoin and ethereum data both misses the value of Saturday and Sunday maybe because the stock market is closed during that day but I know that people do 
trade cryptocurrency when the market is closed too and apps like Coin base, Robinhood shows the data of these cryptocurrency during the weekend.
* While merging the dataset of bitcoin and ethereum, because they have the same column names, one of them gets the x_value and the other gets the y_value. Is there a better way to give names of certain coins instead of x and y values. 
I have tried giving column names after merging.
* I am having a really hard time coming up with cryptocurrency that has negative correlation with bitcoin and got higher market cap. Once I come up with that I need 
to import the dataset of that currency to find the correlation of that with bitcoin and analyze it in detail to manage our portfolio. 

*Below you can see plotly graph object visualization where different bearish and bullish movement caused bitcoin price to rise to its current level. Feel free to make use of slider to see the dates that you are interested.*

{% include_relative Visualizations/bitcoin.html %}

**Different univariate and bivariate plots**

I have chose univariate plot to visualize both ethereum and bitcoin price. Both the prices have fluctuated a lot in a span of a year. These fluctuations are again
a reminder that our portfolio should be diverse and not just include cryptos that has got strong positive correlation.

{% include_relative Visualizations/boxplot.html %}

{% include_relative Visualizations/box.html %}


To clearly see the positive correlation between bitcoin and ethereum price, I made bivariate scatter plot.This hints on how our portfolio should look: 
it's sure that we don't want our crypto portfolio to contain only bitcoin and ethereum.

{% include_relative Visualizations/ethereum.html %}













