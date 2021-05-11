## Welcome to Ruggles's Bitcoin Page

### Welcome to my page

**Leading Question:**

Has media attention, adoption, and rejection of Bitcoin had an affect on Bitcoins market price?
 
**Main Data Sorces:**

- [Yahoo Finance](https://finance.yahoo.com/quote/BTC-USD/history/?guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAE1iTQEM3gqle4ifIZ0FxmNSrO2jLU8jHDLYEnM4DGZk4dCEd-VhKRedEtXl6B3t2wj_eoseVG3MVLDWtXR5JAlz3aI6aQAheKcsaQTuFuWYKJvZPD2RdG3mC41_VtyVCE2slSvx_iqysSqDrh8KBvPb6GpvOmdGVTfFMCBkWE0E&guccounter=2)
- [MarketWatch](https://www.marketwatch.com/story/bitcoin-price-hits-new-record-clears-60-000-milestone-11615648314)
- [Statista](https://www.statista.com/statistics/864738/leading-cryptocurrency-exchanges-traders/)
- [Tesla 2021 Q1 Report](https://www.sec.gov/Archives/edgar/data/1318605/000095017021000046/tsla-20210331.htm)
- [Twitter](https://twitter.com/elonmusk)

Some of Yahoo Finance's data has missing values on 2020-10-09, 2020-10-12, and 2020-10-13. 
My research does not suggest that the market was under any unusual distress during these dates. These missing values were reported months after the market crash in March of 2020. Reports from the [Yahoo Finance](https://finance.yahoo.com/news/stock-market-news-oct-9-134301485.html) and [The New York Times](https://www.nytimes.com/issue/todaysheadlines/2020/10/09/todays-headlines) corroborate that there was no unusual market activity that would have caused missing data.

I validated the Yahoo Finance data by looking at [MarketWatch's](https://www.marketwatch.com/story/bitcoin-price-hits-new-record-clears-60-000-milestone-11615648314) list of major market events and comparing specific dates and prices from each source. Below I have included two bar graphs comparing major price milestones from Jan 2nd, Jan 7th, Feb 16th, Mar 13th of 2021.

Yahoo Finance Data Line Graph
{% include relative Visualizations/ww-bitcoinfull.html %}

Yahoo Finance Data Bar Graph
{% include relative Visualizations/ww-bitcoinfullbar.html %}

Yahoo Finance Major Milestones
{% include relative Visualizations/ww-yahoomilestone.html %}

Market Watch Major Milestones
{% include relative Visualizations/ww-marketwatchmilestone.html %}

Yahoo Finance Data 3D
{% include relative Visualizations/ww-bitthreed.html %}


**Project Concept & Methodology**

Cryptocurrencies have recently been receiving a lot of attention. Being highly volatile, hard to understand, created through mining, and apparently holding the opportunity for massive financial gains, these currencies are hard to not consider when thinking about the future of money. 

I will be focusing my project around Bitcoin. Bitcoin is one of the more popular Cryptocurrencies. Bitcoin is a decentralized global cryptocurrency created by [Satoshi Nakamoto](https://en.wikipedia.org/wiki/Satoshi_Nakamoto#:~:text=Satoshi%20Nakamoto%20is%20the%20name,devised%20the%20first%20blockchain%20database) in 2009.

To give some perspective surrounding why Bitcoin specifically may be the focus of so much media and financial buzz, consider the following. In 2013, only a few years after bitcoins creation, a single bitcoin was worth ~$100. In today's crypto market, a single bitcoin is estimated to be worth ~50,000. 

I decided to use various types of data to delineate any connections between Bitcoins stock price and the media attention it receives. I decided to use various types of data to delineate any connections between Bitcoins stock price and the media attention it receives. I decided I would first look at Coinbase, a cryptocurrency marketplace. Their IPO occurred on April 14, 2021 (Wednesday). This IPO gained a ton of attention after their market valuation was released at $85 Billion. Because Coinbase is a market on which Bitcoin can be purchased and sold, I hypothesized that this valuation would have increased the stock value of Bitcoin. 

Below I have included a Plotly visualization showing how large this IPO valuation was in comparison to other crypto exchanges, along with two visualizations showing what Bitcoins stock price looked like when Coinbase’s IPO was released. 

{% include relative Visualizations/ww-exch13.html %}

{% include relative Visualizations/ww-coinbaseipo.html %}

{% include relative Visualizations/ww-coinbaseipo3d.html %}

The decline in stock value is evident after the IPO date. This finding did not support my hypothesis about Coinbase’s IPO lifting the stock value. This could be because stockholders believed that Coinbase’s valuation was overvalued. It is interesting as to why the stock peaked when it did. There may have been some anticipation for Coinbase to go public, and that anticipation caused stock to be purchased before the IPO was released.

I then decided to continue my exploration by looking into if the adoption of Bitcoin gave it more value in the market. I did this by looking at Tesla Motors. Tesla has been at the forefront of engaging in cryptocurrencies, even accepting Bitcoin as a form of payment for their vehicles. Tesla's well known founder, Elon Musk, engages with his social media frequently, posting on Twitter and on other platforms. I was curious if there were any specific Tweets or comments from him that could have influenced the price of Bitcoins market value. I isolated one Tweet from March of 2021 that seemed especially pro-Bitcoin.

![ElonTweet](https://user-images.githubusercontent.com/82183767/117762764-983e2e00-b1de-11eb-8b30-4b1c19ce932d.png)

I checked to see if this social media activity had any effect on the stock value of Bitcoin by isolating the original Yahoo data during the month when the Tweet was made, and then checked to see if the stock had any major movements following the comment. 

{% include relative Visualizations/ww-musktweet.html %}

As seen in the plot, the stock fell significantly the day after the tweet, but then rose again in the following days. It is hard to say with certainty that the Tweet is related to the stocks eventual rise, although it could be a factor. 

Finally, I decided to again use Tesla as an example to see if the rejection of Bitcoin had any affect on its market value. During the first quarter of 2021, Tesla purchased and sold a significant amount of Bitcoin. On February 8th of 2021, Tesla purchased $1.5B worth of Bitcoin. This comes out to be aproxomatly 43,000 Bitcoin. During the same quarter, due to the volatility and instability of the cryptocurrency, decided to sell off some of their Bitcoin. After selling, Tesla ended the first quarter with ~ 38,300 Bitcoin that cost $1.329B. 

{% include relative Visualizations/ww-buysell.html %}

This action of their Bitcoin has received a lot of attention. I again isolated the month where this event occurred by locating the day on which Teslas Q1 report was published, and plotted the Yahoo Finance data to see if there was a correlation.

{% include relative Visualizations/ww-teslaqone.html %}

As seen in this plot, there seems to be a slight bump in the stock price after the report was released. Although, it is hard to draw a definite conclusion that this increase in stock value has been caused by the publication. 

**Sorces**

- [CNBC](https://www.cnbc.com/2021/04/15/coinbase-coin-climbs-11percent-in-premarket-after-nasdaq-debut.html#:~:text=Coinbase%20employees%20spray%20champagne%20during,Wednesday%2C%20April%2014%2C%202021.&text=Bloomberg%20%7C%20Getty%20Images-,Coinbase%20shares%20whipsawed%20Thursday%2C%20a%20day%20after%20the%20cryptocurrency%20exchange,in%20a%20blockbuster%20direct%20listing)

- [WSJ 1](https://www.wsj.com/articles/coinbase-stock-price-valuation-and-everything-else-you-need-to-know-11618413312) [WSJ 2](https://www.wsj.com/articles/coinbase-shares-surge-in-trading-debut-11618421619?mod=article_inline)

- [Buy Bitcoin Worldwide](https://www.buybitcoinworldwide.com/who-accepts-bitcoin/)

- [Forbes](https://www.forbes.com/sites/clareoconnor/2014/02/17/how-to-use-bitcoin-to-shop-at-amazon-home-depot-cvs-and-more/?sh=56495c5d2de2)

- [Business Insider](https://www.businessinsider.com/more-companies-accepting-bitcoin-cryptocurrency-paypal-starbucks-2021-4)

- [CNBC](https://www.cnbc.com/2021/03/24/elon-musk-says-people-can-now-buy-a-tesla-with-bitcoin.html)

- [MIT Technology Review](https://www.technologyreview.com/2019/05/14/135388/you-can-now-pay-with-cryptocurrency-at-whole-foods/)

- [Yahoo Life](https://www.cnbc.com/2021/02/08/tesla-buys-1point5-billion-in-bitcoin.html)

- [CNBC](https://www.cnbc.com/2021/02/08/tesla-buys-1point5-billion-in-bitcoin.html)

- [The Street](https://www.thestreet.com/crypto/bitcoin/why-did-tesla-sell-some-of-its-bitcoin)

- [Fortune 1](https://fortune.com/2021/04/27/tesla-tsla-bitcoin-btc-bet-how-much-has-it-made-elon-musk-profits/#:~:text=Ever%20since%20Tesla%20announced%20its,made%20on%20its%20big%20wager) [Fortune 2](https://fortune.com/2021/04/27/tesla-tsla-bitcoin-btc-bet-how-much-has-it-made-elon-musk-profits/#:~:text=Result%3A%20Tesla%20still%20holds%20around%2038%2C300%20Bitcoin%20that%20cost%20%241.329%20billion)

- [Twitter](https://twitter.com/elonmusk)

- [Coindesk](https://www.coindesk.com/tesla-sold-bitcoin-in-q1-for-proceeds-of-272m)

- Tesla [Press Release info](https://ir.tesla.com/press-release/tesla-announces-date-first-quarter-2021-financial-results-and-webcast#:~:text=PALO%20ALTO%2C%20Calif.%2C%20April,Monday%2C%20April%2026%2C%202021), [Quarterly & Annual Summaries](https://ir.tesla.com/), [Q1 2021 Report](https://www.sec.gov/Archives/edgar/data/1318605/000095017021000046/tsla-20210331.htm), [Q1 2021 Report Slides](https://tesla-cdn.thron.com/static/R3GJMT_TSLA_Q1_2021_Update_5KJWZA.pdf?xseo=&response-content-disposition=inline%3Bfilename%3D%22TSLA-Q1-2021-Update.pdf%22)

- [Statista](https://www.statista.com/statistics/864738/leading-cryptocurrency-exchanges-traders/)

**Aditinal Questions to Consider:**

1. What has caused some companies to adopt or reject Bitcoin as payment at their private business? 
2. Why did they make their decision when they did? 
3. How does Bitcoin adjust for inflation?
4. How will the addition of more Bitcoin (as it is mined more frequently) change the price of one Bitcoin?


