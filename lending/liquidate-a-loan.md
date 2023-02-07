# Liquidate a loan

Loans can be liquidated by anyone through a call on the Market contract, the on-chain entry point for the leNFT protocol.

#### Liquidation mechanics

A loan is available for liquidation whenever the sum of the debt (principal + interest) exceeds the maximum collateral value.\
When the debt is smaller than **82%** of the collateral's valuation the liquidation price will be:

$$
liquidationPrice = collateralValuation \cdot 0.82
$$

If the debt is higher than or equal to **82%** of the collateral's valuation then liquidation price will be set at:

$$
liquidationPrice = principal + interest
$$

