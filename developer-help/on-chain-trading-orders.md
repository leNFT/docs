# On-chain Trading Orders

To facilitate seamless integration by other systems, leNFT provides helper functions. These tools, available for invocation via the [TradingPoolHelpers](../protocol/contract-addresses.md) contract, can assist third parties in building trading venues on top of leNFT. The helper functions are the following:

### Simulate Buy

{% code fullWidth="false" %}
```solidity
function simulateBuy(
    address tradingPool,
    uint256[] calldata nftIds
) external view returns (uint256 finalPrice)
```
{% endcode %}

Simulates a buy transaction within a given trading pool for a specified number of NFT IDs. The result is the final buy price. Please remember, it's crucial that the pool holds all the indicated NFT IDs at the time of invoking this function.

### Simulate Sell

```solidity
function simulateSell(
    address tradingPool,
    uint256[] calldata nftIds,
    uint256[] calldata liquidityPairs
) external view returns (uint256 finalPrice)
```

Simulates a sell transaction within a designated trading pool for a specific set of NFT IDs, operating against the specified liquidity pairs. The number of NFT IDs should be the same as the number of liquidity pairs (which can be repeated). The outcome is the final sell price.

### Get Sell Liquididity Pairs

```solidity
function getSellLiquidityPairs(
    address pool,
    uint256 amount
) external view returns (uint256[] memory sellLiquidityPairs)
```

Gets the liquidity pairs in a certain pool which would yield the highest sell price for a certain amount of NFTs.
