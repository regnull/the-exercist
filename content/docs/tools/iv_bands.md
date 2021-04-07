---
title: IV Bands
---

# IV Bands

Many people are familiar with [Bollinger bands](https://en.wikipedia.org/wiki/Bollinger_Bands), which are drawn two standard deviations from simple moving average on a stock price chart. Statistically, stock price would be between bands 95% of the time if the price movement were to be random. Therefore, if the stock price crosses one of the bands, it might indicate that the movement is not random, and it can be used to predict price trend.

Bollinger bands are useful because they show price relative to the range defined using historical data, based on past price movements. What if we were to define the range using implied volatility instead? This would show us where the stock price is relative to where the market thought it would be, based on the implied volatility.

The range we draw is based on the probability, which roughly translates into option delta. So here is the way to interpret the chart:

![Example image](/aapl_iv_bands.png)

Assume we draw IV bands using time shift of 20 days and delta of 30%. The bands show us where the market thought the price of the stock today would be, as of 20 days ago, vs. where the stock really is.

Let's say you sold a 20 DTE call at 0.3 delta. This rougly translates into 30% probability of the call being ITM at expiration. Because the top IV bands is based on 30% delta, if the stock price is above this line at expiration date, the call would be assigned.

If stock movements were purely random, we would expect price to be above the top band roughly 30% of the time, below the bottom band 30% of the time, and between bands the remaining 40%. In reality the picture is quite different for trending stocks. Many of them spend most of the time above the 30% delta line, meaning that someone selling OTM calls at 30% delta would have a really bad time.