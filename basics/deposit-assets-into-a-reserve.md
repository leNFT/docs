# Deposit assets into a reserve

Liquidity suppliers take a major role in leNFT. Their assets are used by the protocol to provide loans to NFT holders while also accruing fees by doing so.

When depositing assets into leNFT users receive reserve tokens, a representation of their share in the reserve. These tokens will accrue value whenever a loan is paid and its corresponding interest is deposited in the underlying supply of the reserve.

The liquidation rewards mechanism provides some protection against bad debt by increasing the range in which a liquidation price range in which liquidation is profitable. It does not guarantee that bad debt is not possible and losses originating from those defaults will be taken by the reserve.

#### How to?

To deposit assets in a reserve simply go to the "Supply" page on the leNFT interface and choose the reserve you want to the deposit into, at the moment only WETH is supported. You will then be prompted to approve, and then deposit your tokens.
