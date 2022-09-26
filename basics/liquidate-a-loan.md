# Liquidate a loan

Loans can be liquidated by anyone through a call on the Market contract, the on-chain entry point for the leNFT protocol.

#### Liquidation mechanics

A loan is available for liquidation whenever the sum of the debt (principal + interest) exceeds the maximum collateral value.\
When the The liquidation price, is marked at **82%** of the collateral's valuation.

#### LE Rewards

In order to incentivize liquidators, LE Rewards are distributed whenever you liquidate a loan. The amount of tokens to be distributed with each liquidation is calculated through the expressions seen  [here](../le-token-mechanics/liquidation-rewards.md).
