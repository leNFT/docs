---
description: Function to sell NFTs to a pool
---

# Sell

{% code fullWidth="false" %}
```javascript
sell(pool, nftIds, liquidityPairs, minimumPrice)
```
{% endcode %}

Sells user's `nftIds` to the `liquidityPairs` belonging to a `pool`, throws an error if the `finalPrice` is lower than `minimumPrice`.\
\
This function is usually combined with some of following query functions:

* [`getPool`](query-functions.md#getpool) - In order to get the `pool` from the collection's address and pool token.
* [`getSellQuote`](query-functions.md#getsellquote) - In order to get the best (highest price) `liquidityPairs` to sell into and the `minimumPrice` for the sell operation.

Returns the `finalPrice` for the sell operation.
