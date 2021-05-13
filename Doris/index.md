## Welcome to Doris's Page

### About This Page

***What Is Bitcoin*** 

Bitcoin is a cryptocurrency developed in 2009 by Satoshi Nakamoto. Unlike investing in traditional currencies, bitcoin is not issued by a central bank or backed by a government. And buying a bitcoin is different than purchasing a stock or bond because bitcoin is not a corporation. Therefore, the monetary policy, inflation rates, and economic growth measurements that typically influence the value of currency do not apply to bitcoin.

If you are interesting about the bitcoin price, here is an article discuss the [Bitcoin price](https://www.thebalance.com/who-sets-bitcoin-s-price-391278).

---

***My Project*** 
In this page, I want to visualize the bitcoin historical price trends. You can also see the correlation between bitcoin and the stock price of large companies that accept bitcoin as payment method, correlation between bitcoin and other currency 

Machine learning (ML) has significant applications in the stock price prediction, and I compare two ML model that predicted the bitcoin price. One is [Prophet model](https://towardsdatascience.com/time-series-forecasting-predicting-stock-prices-using-facebooks-prophet-model-9ee1657132b5) developed by Facebook based on additive model; another is [Long Short-Term memory (LSTM) neural network model](https://towardsdatascience.com/lstm-time-series-forecasting-predicting-stock-prices-using-an-lstm-model-6223e9644a2f). 

PS. The code and models are well developed, and I only compare them. All the sources are available and open online.  

---

**Data Source**

All the data are from [Yahoo Finance](https://finance.yahoo.com/), it contains the Open, Close, High and Low price of bitcoin price, stocks price, and currency price. For Pearson correlation coefficient calculation, the Tech companies stocks prices is in recent one year by daily; and the currency and metal data is in last five years by monthly. 


### Bitcoin Price Trends


The Visualization of all available Bitcoin historical price in USD from Sep 15, 2014 until Today. In the black square is the bitcoin price trends after pandemic. After pandemic began, the bitcoin price is constantly increase and increase curve is became steep after Oct 2020. 
{% include_relative Visualization/BTC_USD.html %}
For bitcoin historical data table, click [here](trends.md).

****

### Bitcoin Trends Visualization

**Bitcoin Trends with Google Search Trends**
The Visualization of Bitcoin Trends and Google Search Trends of ‘Bitcoin. 
{% include_relative Visualization/BTC_Google.html %}

The trends between bitcoin research trends and bitcoin price flow are very similar in last year. When the bitcoin price increased, the search is increased. Seem like people loss the interest between Feb and March 2021 even the bitcoin price is increasing. But the recently rising interested on bitcoin topic. 

---

**Bitcoin Trends with Stock Price of tech Companies that Allow Bitcoin as Payment**

*Nasdaq stock market and stock prices of [companies](https://www.insidermonkey.com/blog/5-biggest-companies-that-accept-bitcoin-915752/3/) that accepted bitcoin as payment method: [BMW](https://finance.yahoo.com/quote/BMW.DE/history?p=BMW.DE), [Tesla](https://finance.yahoo.com/quote/TSLA?p=TSLA&.tsrc=fin-srch), [Microsoft](https://finance.yahoo.com/quote/MSFT?p=MSFT&.tsrc=fin-srch), and [AT&T](https://finance.yahoo.com/quote/T?p=T&.tsrc=fin-srch).*

{% include_relative Visualization/Bitcoin_Stocks_Trends.html %}
Through the line graph, is hard to know their price is correlate or not, but the BMW, Microsoft and Bitcoin have a little similarity after 2021. Therefore, I calculate the Pearson correlation coefficient between each stock price. 

### Bitcoin Correlation with Other Stocks and Currency

For create correlation matrix, you need to import all the stock/currency/mental historical price dataset and merge them by date. So you have a new dataset with all historical stocks price that you want to including in correlation test. Then call the DataFrame.corre(method = 'pearson). *Notice: there are three method {‘pearson’, ‘kendall’, ‘spearman’}, Pearson is the one that measure of linear correlation between two sets of data*

---

**Correlation Matrix between Tech Companies Stock Prices and Bitcoin Prices**

{% include_relative Visualization/Bitcoin_Currency_Matrix.html %} 

None of the correlation is significant (r >.95). But the correlation coefficient between BMW and bitcoin is 0.79; correlation coefficient between Microsoft and bitcoin is 0.8. Their prices are relatively correlate to bitcoin price. Noticeable, correlation is not mean causal relationship between two variables. There are some unknow internal factors that make the stock prices of BMW, Microsoft, and bitcoin price trends is very similar in last year. 

---

**Correlation Matrix between Currency, Mental Prices, and Bitcoin Price**

*The correlation matrix between [EUR](https://finance.yahoo.com/quote/EURUSD=X?p=EURUSD=X&.tsrc=fin-srch), [CNY](https://finance.yahoo.com/quote/CNY=X?p=CNY=X&.tsrc=fin-srch), [gold](https://finance.yahoo.com/quote/GOLD?p=GOLD&.tsrc=fin-srch), [silver](https://finance.yahoo.com/quote/SI=F?p=SI=F&.tsrc=fin-srch), [palladium](https://finance.yahoo.com/quote/PA=F?p=PA=F&.tsrc=fin-srch), and [platinum](https://finance.yahoo.com/quote/PL=F?p=PL=F&.tsrc=fin-srch) monthly prices in last five years*

{% include_relative Visualization/Bitcoin_Stock_Matrix.html %}

The correlation coefficient between Euro, Chinese yuan, gold, silver, palladium, and platinum is very week(r<0.6). The price of bitcoin almost not correlate with other currency and metal price. Because all of prices is measured in USD, so the USD not including in the correlation test. 

---

### Bitcoin Price Prediction

I did some research about popular stocks and bitcoin price prediction model. One is base on stock-to flow model. The 'Stock-to-flow' is a number that shows how many years, at the current production rate, are required to achieve the current stock. I didn't including in my visualization, but if you interest in this model, click [here](https://medium.com/@100trillionUSD/modeling-bitcoins-value-with-scarcity-91fa0fc03e25) for more detail information.

Other two are machine learning (ML) models that I apply on bitcoin dataset I have. One is Prophet model developed by Facebook based on [additive model](https://en.wikipedia.org/wiki/Additive_model);another is [Long Short-Term memory (LSTM) neural network model](https://en.wikipedia.org/wiki/Long_short-term_memory). 

The Prophet model’s [Github page](https://github.com/facebook/prophet);The [LSTM model's page](https://towardsdatascience.com/lstm-time-series-forecasting-predicting-stock-prices-using-an-lstm-model-6223e9644a2f). All codes I used in this visualization also from this page. If you want to build a stock price prediction by you self, all the resources in this page are free and open to public. 
For those two model, I both use data before Jan 2019 as training, and predicted price from Jan 2019 until now.
 
---

**LSTM Model, Prophet Model, and Real Bitcoin Price**

{% include_relative Visualization/Bitcoin_Pediction_Model.html %} 
*There are some data are missing and repeated between 2020-04-10 to 2020-12-13 with some unknown reason that I didn't figured out* 

I did do a statistic test to test the validity and accuracy of those two mode, but the line graph shown that the tendency of the prediction model is highly consistent with real bitcoin price. The Prophet prediction give a range of price, but I only present the upper price of the model. [Here](model.md) is the table of the bitcoin price, and model prediction price.

### Conclusion 

Bitcoin is a cryptocurrency that very popular in recent year, and more and more companies accept it as payment method. However, it work is an individual system that may different from other currency. The flow price of bitcoin are similar to flow of tech companies stock in recent year. 
Some of the machine learning model that work well on predict stock price also works on predict bitcoin price.  

### Jupyter Notebook

This is the [Jupyter Notebooks](Bitcoin.ipynb) for Bitcoin Trends Visualization and correlation matrix.
This is the [Jupyter Notebooks](Bitcoin_Prediction_Model.ipynb) for prediction model. 

 
