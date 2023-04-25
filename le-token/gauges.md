# Gauges

leNFT's approach to liquidity management involves using gauges to incentivize activity in our lending and trading pools. After depositing assets in a pool, users receive an ERC721 (for trading pools) or ERC20 (for lending pools) token, which can then be staked in the pool's corresponding gauge to earn additional LE rewards.

Each pool has its own gauge, enabling the direction of LE incentives towards specific liquidity pools. Initially, the development team will create these gauges. However, this process will eventually be replaced by a DAO proposal submission and approval vote to ensure the community's input is integrated into the platform's decision-making process.

The amount of gauge rewards distributed per epoch depends on the ratio of locked/total LE and is given by the following formula:

$$
rewards(epoch) = \text{rewards_ceiling}(\text{epoch}) \times \left(\frac{\text{locked_LE}}{\text{total_LE}}\right)^3
$$
