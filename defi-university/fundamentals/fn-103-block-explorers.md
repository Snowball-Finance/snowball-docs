# FN 103 - Block Explorers

Block explorers are an essential tool for DeFi users that are present on every blockchain. This course will cover the following:

* Defining Block Explorers
* Listing Popular Block Explorers
* Block Explorer Functionality

#### Suggested Prior Reading:

{% content-ref url="fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](fn-101-decentralized-finance.md)
{% endcontent-ref %}

{% content-ref url="fn-102-wallets.md" %}
[fn-102-wallets.md](fn-102-wallets.md)
{% endcontent-ref %}

## Introduction

Block explorers provide a way to view information on the blockchain in a simple and efficient manner. This information includes wallet balances, transaction history, smart contract information and much more. When first starting to use a chain, it is essential to find a block explorer to keep track of your transactions and interact with smart contracts if necessary.

## Block Explorers

The Avalanche C-Chain has two main block explorers:

* **SnowTrace** - [**https://snowtrace.io/**](https://snowtrace.io)****
* **AvaScan** - [**https://avascan.info/blockchain/c/txs**](https://avascan.info/blockchain/c/txs)

{% hint style="info" %}
All smart contract / DeFi-related transactions take place on Avalanche's C-Chain (Contract Chain). The links above are for this chain. The X-Chain and P-Chain have their own explorers.
{% endhint %}

Both explorers provide the same type of information, but have differing visuals and sometimes have more or less information regarding any specific smart contract. SnowTrace is the newest addition to the Avalanche ecosystem, made by the same creators of EtherScan and it's other chain alternatives (BscScan, PolygonScan, FtmScan, etc.).

![Snowtrace - Avalanche C-Chain's Main Block Explorer](<../../.gitbook/assets/image (12).png>)

Other blockchains also have their own block explorers. The most popular ones are linked below:

* **Ethereum** - [**https://etherscan.io/**](https://etherscan.io)
* **Binance Smart Chain** - [**https://bscscan.com/**](https://bscscan.com)
* **Polygon** - [**https://polygonscan.com/**](https://polygonscan.com)
* **Fantom** - [**https://ftmscan.com/**](https://ftmscan.com)
* **Harmony** - [**https://explorer.harmony.one/**](https://explorer.harmony.one)

## Block Explorer Utilities

The primary and probably most important utility of a block explorer is the ability to see your transaction history. Let's take a look at a random wallet address on Avalanche for example:

![Random Wallet on Avalanche](<../../.gitbook/assets/image (9).png>)

If we search for this wallet address on the block explorer, it gives us a lot of information regarding its balance and transaction history. It seems to have been transacting some DAI.e, USDT.e and JOE lately. If you're wondering how it's possible to access anyone's transaction history through a block explorer, it's because everything on a blockchain is public. This is why blockchains are often referred to as public ledgers.

Other than viewing wallet addresses, we can also see even more information regarding smart contracts on a block explorer. Let's take a look at Snowball's main governance contract for example:

![Snowball's Governance Contract on Avalanche](<../../.gitbook/assets/image (11).png>)

We can see the entire source code for any smart contract on the block explorer unless the contract has not been verified yet. This allows for a lot more transparency and makes it easier for legitimate projects to stand out amongst the crowd of smart contracts by using well-written, safe and robust code.

Through a block explorer you can also read, and most importantly write, to any verified smart contract.

![Writing to Snowball's Governance Contract on Avalanche](<../../.gitbook/assets/image (7).png>)

When writing to a smart contract you can connect your wallet to the page much like any decentralized application, and interact with the smart contract directly. This is important since websites may have unforeseen downtime. If this happens you will always have access to your funds through the contract itself, on the blockchain.

{% hint style="info" %}
Guides for how to interact with Snowball's smart contracts through a block explorer can be found [**here**](../../resources/guides/manual-contract-interaction.md).
{% endhint %}

## Closing Thoughts

Block explorers are an amazing tool to have at your disposal. Always make sure to familiarize yourself with the block explorer on whatever chain you are using, and use it to make sure all the contracts you are interacting with are legitimate. As always, don't trust; verify.
