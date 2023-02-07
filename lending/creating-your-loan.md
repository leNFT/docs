# Create a loan

You can create a loan by going to the [web app](https://lenft.fi/) and clicking on the NFT you want to use as collateral. The collateral has to be approved and can then be used as collateral for a new loan.\
Only [supported collections](broken-reference) NFTs' can be used as collateral for a loan.

#### Maximum borrowable amount

Let's suppose you want to take out a loan using CryptoPunk #45. Let's also suppose that:

* leNFT prices this asset at 100 ETH
* the CryptoPunks collection has a maximum [LTV](https://en.wikipedia.org/wiki/Loan-to-value\_ratio) of 60%

This means that if you create a loan using CryptoPunk #45 as collateral, your loan is not at risk of being liquidated right up until your debt (principal + interest) reaches 60 ETH.

{% hint style="info" %}
To avoid unexpected liquidations the UI only allows users to create loans worth half of the liquidation threshold (30 ETH for the aforementioned example).\
Bigger loans can be created by interaction directly with the leNFT contracts.
{% endhint %}

#### Health level

Whenever you create a loan in leNFT there is a risk you can lose your collateral. This can happen whenever the debt on loan is higher than the maximum loan-to-value permitted for your collateral.\
In order to avoid falling into liquidation territory regularly check your loan's health level. If the health level reaches 0% your loan is at risk of being liquidated.
