---
description: Integrating leNFT's SDK into Unity Games
---

# Unity Integration

### Overview

Some developers might want to integrate leNFT's SDK directly into their Unity games. This can be achieved by adding JavaScript sources to your project, and then call those functions directly from your script code as described in the [Unity documentation](https://docs.unity3d.com/Manual/webgl-interactingwithbrowserscripting.html).\
This guide provides step-by-step instructions on how to integrate the leNFT SDK into your Unity project using Unity WebGL.

### Prerequisites

1. Unity installed with WebGL support.
2. Basic knowledge of C# and JavaScript.
3. Familiarity with React and Unity WebGL.

### **File Structure**

Ensure that the following files are placed in the appropriate locations within your Unity project:

1. **lenft.jslib:** Place this file in your project's Assets/Plugins folder. It will be responsible for interacting with the functions in your browser's JavaScript.
2. **lenft.cs:** Create a C# script with this name. It should contain a C# class that imports the JavaScript functions. Place it inside the Assets/Scripts folder.



### Step 1: Implement lenft.jslib

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

In the this example we integrate two functions, one to connect the user's wallet and the other to perform a buy operation for 1 NFT with a maximum price of 0.15 ETH.

### Step 2: Implementing lenft.cs

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

This script imports the JavaScript functions and makes them callable from C#.

### **Step 3: Expose Functions in Browser JavaScript**

To expose the functions called in lenft.jslib in your browser's JavaScript, consider using React Unity WebGL or a similar setup. Below is an example of how to do it with React Unity WebGL:

```javascript
"use client";
import { Unity, useUnityContext } from "react-unity-webgl";
import React from "react";
import leNFT from "lenft-sdk";
import { ethers } from "ethers";

export default function GamePage() {
  const liquidtyPool = "0x...";
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

In this example we wrap the leNFT SDK buy function and expose the `buy(amount, maximumPrice)` through the window object. We also expose a `connectWallet()` function responsible for connecting the user's wallet and initialize the SDK.\
You should also replace the `liquidtyPool` with the address of your NFT's liquidity pool.

### Conclusion

You can now use the functions in your C# script to directly call your browser's javascript function.
