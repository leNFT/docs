# Unity Integration

Some developers might want to integrate leNFT's SDK directly into their Unity games. This can be achieved by adding as described in the [Unity documentation](https://docs.unity3d.com/Manual/webgl-interactingwithbrowserscripting.html).\
\
Start by creating a `lenft.jslib` file in your project's `Assets/Plugins` path, this file will be responsible for interacting with the functions in your browser's javascript:

{% code title="lenft.jslib" %}
```javascript
mergeInto(LibraryManager.library, {
  ConnectWallet: function () {
    window.connectWallet();
  },
  
  Buy: function () {
    window.buy(1, "150000000000000000");
  },
});
```
{% endcode %}

In the this example we integrate two functions, one to connect the user's wallet and the other to perform a buy operation.\
\
You can then create a `lenft.cs` file which should include a C# class that imports the javascript functions:

```csharp
using UnityEngine;
using UnityEngine.UI;
using System.Runtime.InteropServices;

public class LeNFT : MonoBehaviour
{
    [DllImport("__Internal")]
    private static extern void ConnectWallet();

    [DllImport("__Internal")]
    private static extern void Buy();

    public void ConnectWalletFunction()
    {
        ConnectWallet();
    }

    public void BuyFunction()
    {
        Buy();
    }
}
```

These functions can then be called directly from your C# script.



Don't forget to expose the functions called in `lenft.jslib`  in your browser javascript:

```javascript
"use client";
import { Unity, useUnityContext } from "react-unity-webgl";
import React from "react";
import leNFT from "lenft-sdk";
import { ethers } from "ethers";

export default function GamePage() {
  const genesisNFTPool = "0xb2FD99528Ce8f7a6AecFC24c286e63E9D19f06F1";
  const { unityProvider } = useUnityContext({
    loaderUrl: "/Build/build.loader.js",
    dataUrl: "/Build/build.data.unityweb",
    frameworkUrl: "/Build/build.framework.js.unityweb",
    codeUrl: "/Build/build.wasm.unityweb",
  });

  var lenft;
  async function connectWallet() {
    var provider;
    if (window.ethereum == null) {
      console.log("MetaMask not installed; using read-only defaults");
      provider = ethers.getDefaultProvider("mainnet");
    } else {
      console.log("MetaMask installed; using MetaMask provider");
      provider = new ethers.BrowserProvider(window.ethereum);

      // Print wallet information address
      console.log("Signer address: " + (await provider.getSigner()).address);
    }
    lenft = new leNFT(provider);
  }

  async function buy(amount, maximumPrice) {
    console.log("Buying " + amount + " NFTs for " + maximumPrice + " ETH");
    const nfts = (await lenft.getBuyQuote(amount, genesisNFTPool)).exampleNFTs;
    console.log("NFTs: " + nfts);

    const finalPrice = await lenft.buy(genesisNFTPool, nfts, maximumPrice);
    console.log("Final price: " + finalPrice);
  }

  window.connectWallet = connectWallet;
  window.buy = buy;

  return (
    <div>
      <p>leNFT Game</p>
      <Unity
        unityProvider={unityProvider}
        style={{ width: 800, height: 600, border: "solid black 1px" }}
      />
    </div>
  );
}
```
