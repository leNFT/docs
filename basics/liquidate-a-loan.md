# Liquidate a loan

Loans can be liquidated by anyone through a call to the Market contract, the contract that serves as an entrypoint for the protocol. Though the web interface supports this behaviour it is expected it will soon became automated by the use of liquidation bots.

#### Liquidation requirements

A loan is available for liquidation whenever its maximum collateral is smaller than the sum of the debt and the interest.\
The liquidation price, which needs to be smaller than the balance in the liquidator's wallet, is marked at **82%** of the collateral's price.
