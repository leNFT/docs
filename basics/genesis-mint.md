# Genesis Mint

The Genesis Mint is the an NFT collection that celebrates the birth of the Genesis NFT protocol. \
There are 9999 Genesis NFT tokens with each token is being sold for 0.3 ETH.

When minting an NFT the user chooses a locktime duration between 14 and 120 days. After the locktime is over the NFT can be burned and 0.2 ETH redeemed.

On mint, 0.1 ETH is sent to the developer address and reserved for protocol funding.

Users are awarded LE tokens for locking their Genesis NFT according to the following formula:

$$
reward= \frac{locktime * (9999 - mintedCount)}{50000000}*10^{18}
$$

The locktime is in seconds and the minted count is the number of Genesis NFTs already minted.
