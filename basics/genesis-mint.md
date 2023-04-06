# Genesis Mint

## How does it work?

The Genesis Mint is an exclusive collection of non-fungible tokens (NFTs) that commemorates the launch of the Genesis NFT protocol. Limited to just 4,999 tokens, each NFT can be minted for a price of 0.3 ETH.

When a user mints a Genesis NFT, they have the option to choose a locktime duration between 14 and 180 days. The protocol then pairs 0.2 ETH with 1000 LE tokens and deposits all the tokens  into a LE/ETH trading pool. After the lockup period, the Genesis NFT can be burned and the liquidity position withdrawn. If the withdrawal amount is higher than 1000 LE the user will receive WITHDRAWAL\_AMOUNT - 1000 LE tokens, if the withdrawal amount is smaller than 1000 LE the burn won't yield any LE.\
The remaining 0.1 ETH is reserved for protocol development costs. \
The Genesis NFT itself is always transferable between different users.

Additionally, users who mint a Genesis NFT are also rewarded with LE tokens, which are given in the form of veLE tokens locked for the chosen locktime. These tokens represent a share of protocol revenue and can also be used to vote for gauges that distribute inflation within the ecosystem. LE tokens are distributed according to the following formula:

$$
reward= \frac{locktime * (4999 - \frac{minted}{2})}{30000000}\hspace{2mm}LE
$$



The locktime is in seconds and 'minted' is the number of Genesis NFTs already minted.

Users can only have one active lock at a time, meaning they won't be able to mint a Genesis NFT again until their lock is over. If a user wishes to participate in the minting process but has an active lock period, they can still do so using a different address.

## What can I do with my Genesis NFT?

There are 3 things you can currently do with your Genesis NFT:

* Increase the LTV of your next loan by 5%.
* Pair it with ETH and provide liquidity in the Genesis NFT / ETH trading pool. Then stake the LP token you received in the pool's gauge.
* Use it to join the exclusive areas of our Discord.
