# Boost

Users can increase the maximum LTV of future loans in a certain collection by voting in that same collection with their LE tokens. In order to vote the tokens need to be deposited into the LE token vault available through the "Stake" tab in the [web app](https://lenft.fi/).

The following formula relates the increase in maximum LTV with the number of votes in the collection of the loan's collateral:

$$boost = \frac{voteCount \cdot TokenPrice}{collectionLoansCount \cdot boostFactor}$$%
