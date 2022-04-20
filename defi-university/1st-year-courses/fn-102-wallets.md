# FN 102 - Wallets

![](<../../.gitbook/assets/image (16) (1).png>)

To interact with any contract in DeFi, you will need a wallet to call your own. In this essential beginners course we will cover the following:

* Defining Wallets
* Wallet Providers
* Making Transactions
* Understanding Transaction Fees

#### Suggested Prior Reading:

{% content-ref url="fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](fn-101-decentralized-finance.md)
{% endcontent-ref %}

## Introduction

Your wallet is what holds your digital assets. It is similar to a bank account in the traditional sense, except for the fact that there is no personal information associated with it. The most important aspect of having your own wallet is that all the funds in it are directly controlled by you and nobody else.

A wallet from the Ethereum chain or any other EVM-compatible (Ethereum Virtual Machine) chain will have the following characteristics:

* A 42 character public key.
* A randomly generated SHA256-encrypted private key.

The Avalanche C-Chain, for example, is an EVM-compatible chain. The public key is what you would use to receive a transaction from someone else, or identify yourself in the blockchain. The private key is what you would use to make a transaction, or sign something. **This functions similarly to a username and password on any online service.** However, having to remember or walk around with your private key would be quite inconvenient, and honestly, rather unsafe. This is why there are many wallet providers out there that can help you access your wallet through a more standard interface, with a regular password, etc.

## Wallet Providers

Most wallet providers will provide you with a seed phrase, which is simply a sentence with 12 words (sometimes more) that can be used to extrapolate your private key. This is to make it easier to import and export your wallet to different platforms. **Much like your private key, you should never share your seed phrase with anyone.**

You can generally have two different types of wallets; hardware and digital. Hardware wallets are excellent for security, since they are disconnected from any computer and/or the internet, and can safely hold your private key away from any potential security risk. The two biggest providers of hardware wallets are Ledger and Trezor. Both offer integration with some digital wallets in order to interact with many of your favorite DeFi projects.

Digital wallets are the easiest to access for those that plan on making many transactions per day, without the hassle of always having your hardware wallet with you. The most popular digital wallet as of 2021 is MetaMask, due to its simplicity, multi-chain integration and dapp support. Popularity is important in this case because the more decentralized applications that support your wallet, the easier it will be to make the most of your journey into DeFi.

![Snowball's Supported Wallets](<../../.gitbook/assets/image (16) (1) (1) (1).png>)

{% hint style="info" %}
We have a guide on how to setup MetaMask for use on the Avalanche Chain [**here**](../../resources/guides/setting-up-metamask.md#1-metamask-setup).
{% endhint %}

## Transactions

When making a transaction, your private key is required in order to sign it. This is facilitated through the wallet provider of your choice - they will simply ask you to confirm the transaction.

When using a new DeFi project for the first time, you will likely need to give permission for the smart contract to spend the assets in your wallet. For example, if you want to deposit some USDC into Snowball, we will ask you for permission to spend your wallet's USDC. This can be granted by confirming the transaction when it pops up through your wallet of choice.

{% hint style="info" %}
We have many guides on how to make any transaction on Snowball [**here**](../../resources/guides/).
{% endhint %}

It is important to note that with every transaction, you will need to pay a fee to execute it on the blockchain. Depending on what chain you are transacting in, there may be different mechanisms at play when a transaction fee is paid. On Ethereum, for example, a portion of transaction fees are burned (destroyed forever) and another portion is paid to users validating the network (keeping it running). The important thing to note is that by definition, there is never a centralized party collecting these fees. On Avalanche, all transaction fees are burned.

What also varies between chains is the amount paid per transaction. This is never a fixed amount, and usually correlates with the amount of traffic on the network at any given time. Some [**tools**](https://cointool.app/gasPrice/avax) can help you track transaction fees on each chain at any given time.

{% hint style="info" %}
To learn why transaction/gas fees exist and how they work in more detail, check out the FN 106 course on 'Gas Fees'.
{% endhint %}

## Closing Thoughts

Having your own wallet and choosing how you want to access it is an important step to starting your DeFi journey. Make sure to keep your seed phrase, private key and yourself safe!
