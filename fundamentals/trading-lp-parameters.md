# Trading LP Parameters

When creating a trading LP position there are multiple parameters that need to be set:

**Price Curve** **-** Controls how your LP's price changes after each trade. There are two price curves, linear and exponential. In the exponential curve you'll find that

$$
nextPrice = price * (1 + \delta)
$$

while in the linear curve you'll find:

$$
nextPrice = price  + \delta
$$

**Delta -** The parameterization of the price curve. (e.g. 20% for the exponential curve and 0.1 ETH for the linear curve).

**Initial Price -** The initial price your LP will be providing liquidity at. If you want you want to optimize the use of your liquidity your should keep this parameter close to the NFT's market price.

**ETH Amount -** The amount of ETH to supply to the LP.

**Fee -** The % fee your LP will take on each trade it partakes in. (e.g. 0.5%).

**NFTs -** The NFTs to be supplied to the LP.
