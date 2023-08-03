# Buy/Sell

When buying an NFT from a leNFT pool, the user is interacting with the pool's liquidity pairs (LPs) that independently hold this asset. There's no concept of 'price' at the pool level; the buy price for an NFT is the price set by the LP holding that specific NFT.

When selling an NFT, the user is incentivized to interact with the LP that values the collection's price the highest. An off-chain trade router feeds this information to the user, who then uses it to get the highest possible price for the assets.

{% hint style="info" %}
Liquidity Pairs consider all the token within a collection to have the same price.
{% endhint %}
