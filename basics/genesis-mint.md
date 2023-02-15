# Genesis Mint

The Genesis Mint is the an NFT collection that celebrates the birth of the Genesis NFT protocol. \
There are 4999 Genesis NFT tokens with a mint price of 0.3 ETH.

When minting an NFT the user chooses a locktime duration between 14 and 120 days. The protocol uses 0.2 ETH and pairs it with $LE tokens, depositing the all the tokens in a LE/ETH trading pool. After the locktime is over the Genesis NFT can be burned and half of the pool liquidity position withdrawn.&#x20;

0.1 ETH is reserved for protocol development costs.

Users are awarded LE tokens for locking their Genesis NFT according to the following formula:

$$
reward= \frac{locktime * (4999 - \frac{minted}{2})}{50000000}*10^{18}
$$

The locktime is in seconds and 'minted' is the number of Genesis NFTs already minted.
