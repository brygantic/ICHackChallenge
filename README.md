G-Research Mini Coding Challenge
================================

What's the challenge?
---------------------
We're going to provide the (fake) prices of some stocks during the course of one day -
you need to write a program that will work out the best trades to make over
the course of the day to *make the most money*.

Setup
-----
We'll provide you with some CSV files that contain a day's-worth of prices.
Your program will take all of these as input and produce another file listing the trades that
you would make over the course of the day. See the 'Specs' section below for
detailed information on the file format.

You send that output (trades file) to us and we'll validate it and see how much money you've made!

Winning
-------
### Enough, enough. Is there a prize?!
Yes -- the winner will receive a £100 Amazon voucher!

### Winning Criteria
1. Whoever's trades make the most money wins (cash left + value of the portfolio)
2. If that's a tie, the winner who performed the fewest trades will win
3. If THAT's a tie, we'll produce some more sample data and see whose program performs the best

The 'value of the portfolio' is defined as (quantity of stock held * price of stock at the end of the day for each stock).

You can hold as many or as few stocks as you want by the end of the day. However,
remember that if you're tied for first place, the competitor with the fewest trades will win.

Timing
------
### Starting
If you're reading this, then you can start! You'll find examples of some stock prices under `prices/`.
Don't spend a crazy amount of time on this though - your actual hacks should take priority!

### 23:30
At half eleven on Saturday, we will release a new set of prices - these are the ones that you will have to run your program against.

### Midnight
We want your trades.csv submission by midnight so that we can announce the winner during our mass pizza giveaway!

Specs
-----
### Prices Files
We will provide you with some prices files. They will be in a csv format like so:

`Time,Price`

e.g.

```
09:00:00,100
09:00:30,101
09:01:05,103
```

Times will be in `HH:mm:ss` format, and will all be between 09:00:00 and 17:00:00.

The name of the file will be the identifier for the stock - so Vodafone.csv will be for "Vodafone".

### Trades File
You should produce us a file that contains your trades for the day - call it `trades.csv`.
The format of this is:

`Time,Buy/Sell,StockIdentifier,Quantity`

e.g.

```
09:00:33,Buy,Three,5
09:01:10,Sell,Three,5
09:01:10,Buy,Vodafone,6
```

Trades should be in time order - our validator will cry otherwise.
It's fine to have two trades at the same time - the first in the file will be executed first.

### Extra Bits
- You start with 1000 in 'cash' (think of this as pence - so you start with £10!)
- All of the prices in the prices files are also stated in pence (so 100 = £1)
- You can only trade in integer quantities
- You can't "short" a stock - you must always have >= 0 quantity for each stock
- You can only use the money you currently have - money must always be >= 0

FAQs
----
### What's this got to do with G Research?
At G-Research we research markets and investment strategies that can make money.
We also develop platforms through which to simulate trading and execute trades in the market.
This challenge is a simplification of that, but should provide at least a little context to what we do day-to-day.

### I don't understand x, y or z
Come and talk to us! One of the developers here created the challenge, and all of us are more than happy to offer advice or clarify things.
Feel free to also ask questions in the Slack channel - we'll be monitoring it throughout the day.

### You told her the answer but not me!
We'll add any questions we're asked to this FAQ throughout the day

### Can we work in teams?
Sure - just remember that if you win you'll have to split the £100 of vouchers between you! 
