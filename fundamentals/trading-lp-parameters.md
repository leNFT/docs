# Trading LP Parameters

When providing liquidity to trading pools, there are multiple parameters that need to be set:

**Price Curve** **-** Controls how the LP's price changes after each trade. There are two options: linear and exponential.\
Exponential:

$$
nextPrice = price * (1 + \delta)
$$

Linear:

$$
nextPrice = price  + \delta
$$

**Delta -** The parameter that controls the shape of the price curve. It is represented as a percentage for the exponential curve and a value in ETH for the linear curve. (e.g. 20% for the exponential curve and 0.1 ETH for the linear curve).

**Initial Price -** The initial price at which the LP will provide liquidity. It is advisable to keep this value close to the market price of the underlying NFTs in order to optimize the utilization of the liquidity.

**ETH Amount -** The amount of ETH that will be supplied to the LP.

**Fee -** The percentage fee that the LP will take on each trade it participates in. (e.g. 0.5%).

**NFTs -** The NFTs that will be supplied to the LP.
