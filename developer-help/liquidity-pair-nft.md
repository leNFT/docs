---
description: Integrate leNFT's liquidity pair tokens into your DeFi protocol
---

# Liquidity Pair NFT

When a user deposits into a leNFT trading liquidity pool, they will obtain a liquidity pair (LP) NFT. This LP NFT is a dynamic NFT (dNFT), characterized by its evolving metadata as the liquidity pool changes over time. This adaptability makes it ideally suited for integration with other protocols in a composable manner.

Below is an example of the dynamic metadata found in an LP NFT:

{% code title="Trading LP NFT Metadata" overflow="wrap" lineNumbers="true" %}
```json
{
   "name":"Liquidity Pair TNFTWETH #0",
   "description":"leNFT trading liquidity pair.",
   "image":"data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0MDAgNDAwIiBzdHlsZT0id2lkdGg6MTAwJTtiYWNrZ3JvdW5kOiNlYWVhZWE7ZmlsbDpibGFjaztmb250LWZhbWlseTptb25vc3BhY2UiPjx0ZXh0IHg9IjUwJSIgeT0iMjRweCIgZm9udC1zaXplPSIxMiIgdGV4dC1hbmNob3I9Im1pZGRsZSI+bGVORlQgVHJhZGluZyBQYWlyIFRORlRXRVRIICMwPC90ZXh0Pjx0ZXh0IHg9IjI0cHgiIHk9IjcycHgiIGZvbnQtc2l6ZT0iOCI+VHJhZGluZyBwb29sOiAweDU2ZDkxZmYxODdmOTQ4NGY2N2QwNmY0ODlhM2NhNzg5MzAzMWYyN2Y8L3RleHQ+PHRleHQgeD0iMjRweCIgeT0iOTBweCIgZm9udC1zaXplPSI4Ij5ORlQ6IFRlc3QgTkZUPC90ZXh0Pjx0ZXh0IHg9IjI0cHgiIHk9IjEwOHB4IiBmb250LXNpemU9IjgiPlRva2VuOiBXcmFwcGVkIEV0aGVyPC90ZXh0Pjx0ZXh0IHg9IjI0cHgiIHk9IjEyNnB4IiBmb250LXNpemU9IjgiPk5GVCBCYWxhbmNlOiAxPC90ZXh0Pjx0ZXh0IHg9IjI0cHgiIHk9IjE0NHB4IiBmb250LXNpemU9IjgiPlRva2VuIEJhbGFuY2U6IDEwMDAwMDAwMDAwMDAwMTwvdGV4dD48dGV4dCB4PSIyNHB4IiB5PSIxNjJweCIgZm9udC1zaXplPSI4Ij5GZWU6IDEwMDwvdGV4dD48dGV4dCB4PSIyNHB4IiB5PSIxODBweCIgZm9udC1zaXplPSI4Ij5DdXJ2ZTogMHg5MTU1NDk3ZWFlMzFkNDMyYzBiMTNkYmNjMDYxNWEzN2Y1NWEyYzg3PC90ZXh0Pjx0ZXh0IHg9IjI0cHgiIHk9IjE5OHB4IiBmb250LXNpemU9IjgiPkRlbHRhOiAwPC90ZXh0Pjwvc3ZnPg==",
   "attributes":[
      {
         "trait_type":"Pool address",
         "value":"0x56d91ff187f9484f67d06f489a3ca7893031f27f"
      },
      {
         "trait_type":"Token",
         "value":"0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2"
      },
      {
         "trait_type":"NFT",
         "value":"0x4ea0be853219be8c9ce27200bdeee36881612ff2"
      },
      {
         "trait_type":"Price",
         "value":"100000000000000"
      },
      {
         "trait_type":"Token balance",
         "value":"100000000000001"
      },
      {
         "trait_type":"NFT balance",
         "value":"1"
      },
      {
         "trait_type":"Curve",
         "value":"0x9155497eae31d432c0b13dbcc0615a37f55a2c87"
      },
      {
         "trait_type":"Delta",
         "value":"10"
      },
      {
         "trait_type":"Fee",
         "value":"100"
      }
   ]
}
```
{% endcode %}

