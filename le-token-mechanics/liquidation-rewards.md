# Liquidation Rewards

In order to avoid bad debt due to adverse market conditions and sudden collateral pricing changes liquidations in leNFT are incentized through the use of the leNFT native protocol token.

LE token liquidation rewards are given in accordance to the expressions below:

When collateral price > liquidation price:

$$
reward = \frac{assetPrice}{liquidationRewardFactor \cdot reserveTokenPrice \cdot nativeTokenPrice \cdot (2 \cdot liquidationPrice  - assetPrice))}
$$

When collateral price <= liquidation price:

$$
reward = \frac{liquidationPrice}{liquidationRewardFactor  \cdot reserveTokenPrice \cdot nativeTokenPrice \cdot (2 \cdot liqudationPrice - assetPrice))}
$$

