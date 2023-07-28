---
description: Functions that return information about a trading pool's state.
---

# Query Functions

### getPool

```
getPool(nft, token)
```

Returns the trading pool associated with a certain `nft` and `token`.\
Most of the time you will want to use the WETH address for the token parameter.



### getPoolNFTs

```javascript
getPoolNFTs(pool)
```

Returns the NFTs deposited in certain `pool`.



### getNFTLP

```javascript
getNFTLP(pool, nftId)
```

Returns the LP ID associated with a certain `nftId` in the `pool`.



### getPrice

```javascript
getPrice(pool)
```

Returns the buy and sell price for a certain pool.



### getBuyQuote

```javascript
getBuyQuote(amount, pool)
```

Returns a pool's buy quote for an amount of NFTs.

###

### getBuyExactQuote

```javascript
getBuyExactQuote(nfts, pool)
```

###

###

### getSellQuote

```javascript
getSellQuote(amount, pool)
```

