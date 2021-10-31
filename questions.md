# Questions we need answered

Q: Which exchange should we use? (Coinbase Pro, Binance US, KuCoin)  
A: Coinbase pro (assuming they have volume profile)

Q: Which trading pairs will we be focusing on?  
A: Track the top 100 on CBP, exclude things on a blacklist

Q: How many active trades at once?  
A: 2 trades at once, 25% of portfolio at once

Q: When do we take profit? When do we cut losses?  
A: See below

Q: How often will the algorithm need to be run? (daily, hourly, every 5 minutes)  
A: Trade based off 15-minute candles, so run algo every 15 min

Q: Are there any prior values or calculations that would need to be stored in a database?
Or can we compute everything we need on the fly?  
A: Store volume profile

Q: How can we mathematically define and determine what a point of support or resistance is?  
A: Use volume profile

- Keep a list of low volume ranges
- If price is 2% above the top point of the low volume area,
  - then, put a limit buy order in the middle of range
  - put a stop loss order in the middle of the high volume area directly below the current low volume area
  - put a limit sell of 50% at a 10% gain
  - put a limit sell of 50% at a 25% gain
