# Liquidation Rewards

In order to avoid bad debt due to adverse market conditions and sudden collateral pricing changes liquidations in leNFT are incentivized through the use of the leNFT native protocol token.

LE token liquidation rewards are given in accordance to the expressions below:

**When collateral price > liquidation price:**

$$
\frac{assetPrice}{rewardFactor\cdot underlyingTokenPrice\cdot LEPrice\cdot(2 \cdot assetPrice - liquidationPrice)}
$$

**When collateral price <= liquidation price:**

$$
\frac{liquidationPrice}{rewardFactor\cdot underlyingTokenPrice\cdot LEPrice\cdot(2 \cdot liquidationPrice - assetPrice)}
$$
