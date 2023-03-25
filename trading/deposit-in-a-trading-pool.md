# Deposit in a trading pool

To deposit in a trading pool, users can navigate to the desired trading pool on the leNFT interface and follow the prompts to provide their desired combination of NFTs and ETH. Help with LP parametrization can be found [here](../protocol/trading-lp-parameters.md). After the deposit is completed, users will receive an NFT tokens in representing their LP, much like an Uniswap V3 position.

These liquidity pool tokens can then be staked in the gauge to earn LE rewards, which are distributed to stakers through the gauge system. The gauge incentivizes users to provide liquidity and participate in the ecosystem, making it a sustainable way to earn passive income.

### How are LP tokens valued?

LP tokens are valued according to the following formula:

$$
\min\left(LP\_PRICE \cdot NFT\_AMOUNT, TOKEN\_AMOUNT\right)
$$
