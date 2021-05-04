## Welcome to Doris's Page

**What Is Bitcoin** 

Bitcoin is a cryptocurrency developed in 2009 by Satoshi Nakamoto. Unlike investing in traditional currencies, bitcoin is not issued by a central bank or backed by a government. And buying a bitcoin is different than purchasing a stock or bond because bitcoin is not a corporation. Therefore, the monetary policy, inflation rates, and economic growth measurements that typically influence the value of currency do not apply to bitcoin. 

**What Determined Bitcoin Price?** 

The article about [Bitcoin price](https://www.thebalance.com/who-sets-bitcoin-s-price-391278). For this project, I want to roughly predict the bitcoin price in years based on the historical data. Additionally, detect the correlation between bitcoin and the stocks price of large companies that accept bitcoin as payment method. 

**Data Source**

All the data are from [Yahoo Finance](https://finance.yahoo.com/), it contains the Open, Close, High and Low price of bitcoin price, stocks price, and currency price. 

**Bitcoin Price Trends**


The Visualization of all available Bitcoin historical price in USD from Sep 15 2014 until Today* 
{% include_relative Visualization/BTC_USD.html %}

****

**Bitcoin Correlation with Other Stocks and Currency**

I used Pearson r correlation for all the data. The stocks prices is in recent one year by daily, and the currency data is in last five years by monthly. 

{% include_relative Visualization/Bitcoin_Currency_Matrix.html %} 

*The correlation matrix between [EUR](https://finance.yahoo.com/quote/EURUSD=X?p=EURUSD=X&.tsrc=fin-srch), [CNY](https://finance.yahoo.com/quote/CNY=X?p=CNY=X&.tsrc=fin-srch), [gold](https://finance.yahoo.com/quote/GOLD?p=GOLD&.tsrc=fin-srch), [silver](https://finance.yahoo.com/quote/SI=F?p=SI=F&.tsrc=fin-srch), [palladium](https://finance.yahoo.com/quote/PA=F?p=PA=F&.tsrc=fin-srch), and [platinum](https://finance.yahoo.com/quote/PL=F?p=PL=F&.tsrc=fin-srch) monthly prices in last five years*

{% include_relative Visualization/Bitcoin_Stock_Matrix.html %}

*The correlation matrix between Nasdaq stock market and stock prices of [companies](https://www.insidermonkey.com/blog/5-biggest-companies-that-accept-bitcoin-915752/3/) that accepted bitcoin as payment method: [BMW](https://finance.yahoo.com/quote/BMW.DE/history?p=BMW.DE), [Tesla](https://finance.yahoo.com/quote/TSLA?p=TSLA&.tsrc=fin-srch), [Microsoft](https://finance.yahoo.com/quote/MSFT?p=MSFT&.tsrc=fin-srch), and [AT&T](https://finance.yahoo.com/quote/T?p=T&.tsrc=fin-srch).*


Here is the [Trends Visualization](trends.md).

**Bitcoin Price Prediction** 

This part will predict the trends of bitcoin price based on other currency and stocks trends. Base on [stock-to flow model](https://medium.com/@100trillionUSD/modeling-bitcoins-value-with-scarcity-91fa0fc03e25)