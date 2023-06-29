# Genesis Mint

## How does it work?

The Genesis Mint is an exclusive collection of non-fungible tokens (NFTs) that commemorates the launch of the Genesis NFT protocol. Limited to just 1337 tokens, each NFT can be minted for a price of 0.25 ETH. Although there is no whitelist for this mint, its announcement will be made on leNFT's [Discord](https://discord.gg/B62BgWmGQT) 48 hours before it is disclosed anywhere else."

When a user mints a Genesis NFT, they have the option to choose a locktime duration between 14 and 180 days. The protocol then pairs 0.1 ETH with 40000 LE tokens and deposits all the tokens  into a LE/ETH trading pool. After the lockup period, the Genesis NFT can be burned and the liquidity position withdrawn. If the withdrawal amount is higher than 40000 LE the user will receive WITHDRAWAL\_AMOUNT - 40000 LE tokens, if the withdrawal amount is smaller than 40000 LE the burn won't yield any LE.\
The remaining 0.15 ETH is reserved for protocol development costs. \
The Genesis NFT itself is always transferable between different users.

Additionally, users who mint a Genesis NFT are also rewarded with LE tokens, which are given in the form of veLE tokens locked for the chosen locktime. These tokens represent a share of protocol revenue and can also be used to vote for gauges that distribute inflation within the ecosystem. LE tokens are distributed according to the following formula:

$$
reward= \frac{locktime * (1337 - \frac{minted}{2})}{400000}\hspace{2mm}LE
$$

The locktime is in seconds and 'minted' is the number of Genesis NFTs already minted.

## What can I do with my Genesis NFT?

There are 3 things you can currently do with your Genesis NFT:

* Increase the LTV of your next loan by 2.5%.
* Pair it with ETH and provide liquidity in the Genesis NFT / ETH trading pool. Then stake the LP token you received in the pool's gauge for extra LE rewards.
* Use it to join the exclusive areas of our Discord.

## What will the money raised be used for?

* **Audits:** The funding will first and foremost be allocated to cover the cost of the audit that has already been conducted. This ensures our systems and operations maintain the high standard we strive for. Moving forward, we also anticipate the need for future audits to consistently maintain these standards, and we will set aside a portion of the funds for these anticipated costs.
* **New Developer Hire:** To bolster our technical prowess and enhance our product development capabilities, we plan to hire an additional software developer for a term of one year.
* **Community/Social Manager Hire:** Understanding the importance of a vibrant community and strong social media presence, we will hire a community/social manager for a one-year term to foster and strengthen these areas.
* **New Frontend:** We have already invested in designing a new user interface to provide a more seamless and user-friendly experience. The funds will be used to pay for this design and cover the cost of its implementation.
* **Treasury:** All of the remaining funds will be used to kickstart the leNFT treasury.
