# FN 221 - DEXs

Decentralized Exchanges (DEXs) are another essential functionality in DeFi. They allow you to trade any token without the relying on centralized companies and services. This course will cover the following:

* Defining Decentralized Exchanges
* Listing Popular DEXs
* DEX Functionality

#### Suggested Prior Reading:

{% content-ref url="fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](fn-101-decentralized-finance.md)
{% endcontent-ref %}

{% content-ref url="fn-102-wallets.md" %}
[fn-102-wallets.md](fn-102-wallets.md)
{% endcontent-ref %}

{% content-ref url="fn-104-tokens.md" %}
[fn-104-tokens.md](fn-104-tokens.md)
{% endcontent-ref %}

## Introduction

Decentralized exchanges are an alternative to centralized exchanges such as Binance, Gemini, Coinbase, etc. Having to send your tokens to a centralized exchange, trade them for another token and then bring them back into DeFi would be a somewhat cumbersome, if not excessively inefficient process. Being able to make that swap without leaving your favorite chain is ideal, and is exactly what DEXs allow you to do.

## DEXs

The Avalanche Chain's main DEXs are [**Trader Joe**](https://www.traderjoexyz.com/#/trade) and [**Pangolin**](https://app.pangolin.exchange/#/swap), since they currently have the most liquidity and trading volume in the ecosystem. There are however, many other projects that provide swapping services. As a user, you are looking for platforms with a lot of liquidity, low [_**slippage**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#slippage) and low fees per swap.

{% hint style="info" %}
Snowball has launched Axial, a decentralized exchange for swapping between value-pegged assets such as stablecoins and other wrapped or synthetic assets. It offers much lower fees and slippage than traditional DEXs. Check it out [**here**](https://axial.exchange) or learn about it [**here**](https://docs.axial.exchange).
{% endhint %}

Other chains also have their own DEXs. The following are a few with decent functionality in each of the most popular chains:

* **Ethereum** - [**UniSwap**](https://app.uniswap.org/#/swap), [**Curve**](https://curve.fi), [**1Inch**](https://app.1inch.io/#/1/swap), [**SushiSwap**](https://app.sushi.com/swap)
* **Binance Smart Chain** - [**PancakeSwap**](https://pancakeswap.finance/swap), [**1Inch**](https://app.1inch.io/#/56/swap), [**SushiSwap**](https://app.sushi.com/swap)
* **Polygon** - [**QuickSwap**](https://quickswap.exchange/#/swap), [**Curve**](https://polygon.curve.fi), [**1Inch**](https://app.1inch.io/#/137/swap), [**SushiSwap**](https://app.sushi.com/swap)
* **Fantom** - [**SpookySwap**](https://spookyswap.finance/swap), [**Curve**](https://ftm.curve.fi)
* **Harmony** - [**Curve**](https://harmony.curve.fi), [**SushiSwap**](https://app.sushi.com/swap), [**ViperSwap**](https://viperswap.one/#/swap)

## DEX Utilities

Swapping tokens through a DEX is simple, and in most cases follows the following three steps:

1. Connecting your wallet to the dapp.
2. Signing an 'approval' transaction through your wallet for the token you want to trade.
3. Signing the 'swap' transaction through your wallet.

![Trading 1 AVAX for SNOB on Pangolin](<../../.gitbook/assets/image (11).png>)

Once you input both the token you want to swap and the token you want to swap for, the dapp should show you the estimated slippage (displayed as 'price impact' above), and any fees associated with your transaction. Large transactions may have higher slippage and fees depending on where you are trading, so make sure you watch out for those and pick your DEX accordingly.

![Trading 100 DAI.e for USDT.e on Snowball's StableVault](<../../.gitbook/assets/image (15).png>)

As you can see, swap interfaces are relatively similar and should always follow the same transaction process. If you have already traded a token using a specific DEX before, you will not need to approve its spending again, meaning the process is now reduced to 2 simple steps. Furthermore, most dapps automatically connect to your wallet if you've done so previously, which means exchanging tokens through a DEX is as easy as selecting the tokens you want to trade and clicking on 'Swap'. You'll have to sign the transaction, of course.

## Closing Thoughts

Some decentralized exchanges may provide extra functionality, while others focus on simply providing the lowest fees and/or slippage. Whatever it is you are looking for in a DEX, finding it and familiarizing yourself with its functionality is a must whenever transacting in DeFi.
