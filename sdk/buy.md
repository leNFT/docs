---
description: Function to buy NFTs from a pool
---

# Buy

```javascript
buy(pool, nftIds, maximumPrice)
```

Buy `nftIds`, from a certain `pool`, limiting the price at `maximumPrice`.\
\
This function is usually combined with some of following query functions:

* [`getPool`](query-functions.md#getpool) - In order to get the `pool` from the collection's address and pool token.
* [`getPoolNFTs`](query-functions.md#getpoolnfts) - In order to get the ALL the available `nftIds` to buy.
* [`getBuyExactQuote`](query-functions.md#getbuyexactquote) - In order to get the `maximumPrice` for a certain set of NFTs.
* [`getBuyQuote`](query-functions.md#getbuyquote) - In order to get the `maximumPrice` and a list of cheapest `nftIds`.

Returns the `finalPrice` for the buy operation.
