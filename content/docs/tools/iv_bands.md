---
title: IV Bands
---

# IV Bands

Many people are familiar with [Bollinger bands](https://en.wikipedia.org/wiki/Bollinger_Bands), which are drawn two standard deviations from the simple moving average on a stock price chart. Assuming that the price movements are competely random, stock price would fall between the bands 95% of the time. In practice it's not quite the case, and we can assume that the things are not quite random when the price crosses the top or bottom band. This can be interpreted as a buy or a sell signal in a trading strategy.

Bollinger bands are based on the historical stock movements, so in this sense they are backward-looking. Imagine that some news announcement is expected, for example, the result of a drug trial. The market expects stock to move significantly, either in positive or negative direction. It would be great to compare the expected range with the actual stock movement after the news come out. This is what IV bands are about - they show the expected stock movement, based on implied volatility (IV) with the actual price. 

To do this comparison, we need to draw the expected range at some point in the future. Imaging that based on implied volatility we expect stock to move 0.5 in the next 20 days. We would draw IV lines on the chart 20 days in the future, $0.5 apart from the current stock price.

$0.5 price movement expectation means that the standard deviation is $0.5. Instead of the standard deviation, we could use some specific probability number, for example, draw the line so that the probability of the price being above this line would be, let's say 10%. In fact, this might be a better approach, because the probability numbers roughly translate into option delta. 

Let's say I sold an OTM call option with 0.1 delta, expiring 20 days in the future. If I were to draw lines based on 10% probability (which is roughly 0.1 delta), it would be easy to say when the option is assigned - this would happen if the price were to cross the top IV band.

The range we draw is based on the probability, which roughly translates into option delta. So here is the way to interpret the chart:

![Example image](/images/aapl_iv_bands.png)

Assume we draw IV bands using time shift of 20 days and delta of 30%. The bands show us where the market thought the price of the stock today would be, as of 20 days ago, vs. where the stock really is.

Let's say you sold a 20 DTE call at 0.3 delta. This rougly translates into 30% probability of the call being ITM at expiration. Because the top IV bands is based on 30% delta, if the stock price is above this line at expiration date, the call would be assigned.

If stock movements were purely random, we would expect price to be above the top band roughly 30% of the time, below the bottom band 30% of the time, and between bands the remaining 40%. In reality the picture is quite different for trending stocks. Many of them spend most of the time above the 30% delta line, meaning that someone selling OTM calls at 30% delta would have a really bad time.