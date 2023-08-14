# Install

The leNFT SDK is a way to directly integrate leNFT liquidity into your NFT project.

Install using npm:

```bash
npm i lenft-sdk
```

Import:

```javascript
import leNFT from "lenft-sdk";	
```

To initialize the SDK you will need to provide an ethers [provider](https://docs.ethers.org/v6/getting-started/#starting-connecting):

```javascript
let provider;
if (window.ethereum == null) {
    console.log("MetaMask not installed; using read-only defaults")
    provider = ethers.getDefaultProvider()
} else {
    provider = new ethers.BrowserProvider(window.ethereum)
}

const lenft = new leNFT(provider);
```

[Github repository](https://github.com/leNFT/sdk).
