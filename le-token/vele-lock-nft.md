---
description: Integrate veLE Lock NFTs in your DeFi protocol
---

# veLE Lock NFT

veLE lock NFTs act as a receipt for when a user locks LE tokens into the VotingEscrow contract. These are dynamic NFT (dNFT)  characterized by its evolving metadata as the weight of the lock changes over time. This adaptability makes it ideally suited for integration with other protocols in a composable manner.

Below is an example of the dynamic metadata found in an veLE lock NFT:

{% code title="veLock NFT Metadata" overflow="wrap" lineNumbers="true" %}
```json
{
   "name":"veLE Lock #0",
   "description":"Vote Escrowed LE Lock",
         "image":"data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0MDAgNDAwIiBzdHlsZT0id2lkdGg6MTAwJTtiYWNrZ3JvdW5kOiNlYWVhZWE7ZmlsbDpibGFjaztmb250LWZhbWlseTptb25vc3BhY2UiPjx0ZXh0IHg9IjUwJSIgeT0iMzAlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjE4Ij52ZUxFIExvY2sgIzA8L3RleHQ+PHRleHQgeD0iNTAlIiB5PSI1MCUiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZvbnQtc2l6ZT0iMTQiPjEwMDAwMDAwMDAwMDAwMDAwMDAwIExFPC90ZXh0Pjwvc3ZnPg==",
   "attributes":[
      {
         "trait_type":"end",
         "value":"1691100000"
      },
      {
         "trait_type":"weight",
         "value":"684912956617449594"
      },
      {
         "trait_type":"amount",
         "value":"10000000000000000000"
      }
   ]
}
```
{% endcode %}
