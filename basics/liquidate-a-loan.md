# Liquidate a loan

Loans can be liquidated by anyone through a call to the Market contract, the contract that serves as the on-chain entry point for the protocol. Though the web interface supports this behaviour it is expected it will soon become automated through the use of liquidation bots.

#### Liquidation requirements

A loan is available for liquidation whenever the sum of the principal and the interest exceeds the maximum collateral value.\
The liquidation price, which needs to be smaller than the balance of the liquidator's wallet, is marked at **82%** of the collateral's price.
