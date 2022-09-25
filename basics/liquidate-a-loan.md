# Liquidate a loan

Loans can be liquidated by anyone through a call on the Market contract, the on-chain entry point for the leNFT protocol.

#### Liquidation requirements

A loan is available for liquidation whenever the sum of the principal and the interest exceeds the maximum collateral value.\
The liquidation price, is marked at **82%** of the collateral's valuation.

#### LE Rewards

LE token liquidation rewards are given in accordance to the expressions below:\


When collateral price > liquidation price:

$$reward = \frac{assetPrice}{liquidationRewardFactor \cdot reserveTokenPrice \cdot nativeTokenPrice \cdot (2 \cdot liquidationPrice  - assetPrice))}$$\


When collateral price <= liquidation price:

​$$reward = \frac{liquidationPrice}{liquidationRewardFactor \cdot reserveTokenPrice \cdot nativeTokenPrice \cdot (2 \cdot liquidationPrice  - assetPrice))}$$​

​
