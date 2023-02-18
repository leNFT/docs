# Genesis Mint

The Genesis Mint is an exclusive collection of non-fungible tokens (NFTs) that commemorates the launch of the Genesis NFT protocol. Limited to just 4,999 tokens, each NFT can be minted for a price of 0.3 ETH.

When a user mints a Genesis NFT, they have the option to choose a locktime duration between 14 and 120 days. The protocol then pairs 0.2 ETH with LE tokens and deposits both into a LE/ETH trading pool. After the lockup period, the Genesis NFT can be burned and half of the pool's liquidity position can be withdrawn. The remaining 0.1 ETH is reserved for protocol development costs.

Additionally, users who buy a Genesis NFT duration are also rewarded with LE tokens, which are given in the form of veLE tokens locked for the chosen locktime. These tokens represent a share of protocol revenue and can be used to vote for gauges that distribute inflation within the ecosystem. LE tokens are distributed according to the following formula:

$$
reward= \frac{locktime * (4999 - \frac{minted}{2})}{50000000}*10^{18}
$$

The locktime is in seconds and 'minted' is the number of Genesis NFTs already minted.
