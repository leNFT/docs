# Auction a loan

Loans can be liquidated by anyone through a call on the Market contract, the on-chain entry point for the leNFT protocol.

#### Liquidation mechanics

A loan is available for liquidation whenever the sum of the debt (principal + interest) exceeds the value of the collateral multiplied by the collection's liquidation threshold.

