# FN 106 - Gas Fees

![](<../../.gitbook/assets/Gas Fees.png>)

Gas/transaction fees; everyone knows of them, everyone hates them, but not everyone understands them. This course will cover the following regarding these fees:

* Defining Gas Fees
* Reasons for Gas Fees' Existence
* How Gas Fees Work

#### Suggested Prior Reading:

{% content-ref url="fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](fn-101-decentralized-finance.md)
{% endcontent-ref %}

{% content-ref url="fn-102-wallets.md" %}
[fn-102-wallets.md](fn-102-wallets.md)
{% endcontent-ref %}

## Introduction

When making a transaction on any blockchain, users will need to spend some of the blockchain's native token in order to write this new data to the chain. This amount of tokens is determined by the complexity of the transaction being made (gas amount) and the price of gas at any given time. Paying more than the actual price of gas would mean your transaction would be prioritized, and therefore is likely to be executed faster.

For this course, we'll use three EVM-compatible chains as examples; Ethereum, Polygon PoS and Avalanche C-Chain. The native token of each of these chains are ETH, MATIC and AVAX respectively.

## The Necessity of Fees

It is a simple fact that blockchains and DeFi as we know it today would not be possible in a fee-less structure. This is because the main reason they exist is to prevent network congestion and spam. Regardless of how fast, scalable or efficient blockchain technology gets, there will always be a certain limit to how many transactions can be processed per second, how much data can be written, etc.

Without fees, anyone would be able to generate an infinite amount of transactions and bring the network to a halt. By adding fees to the table, an attacker would still be able to generate these transaction, but it would cost them quite a bit. Creating necessary losses for attackers reduces the profitability of any attack, meaning the network also becomes more secure.

Polygon, for example, has some of the lowest fees around, but in 2021 have had to raise their minimum fees since they were experiencing a large amount of bots spamming the network, slowing it down.

Another reason why fees are necessary in some blockchains are to maintain the profitability of network validators. If block rewards and/or staking rewards are not sufficient to make it a profitable endeavor for validators to keep the network running, it would mean a significant drop in computing power maintaining the network. In turn, this would mean the network would become less decentralized, and likely less efficient.

## How Fees Work

Depending on the underlying blockchain, the fees spent through making a transaction are treated differently:

* **Ethereum** - Ever since the EIP-1559 upgrade, there are two types of fees to consider; the base fee and the priority fee. The base fee is burned - the tokens are gone forever. The priority fee is sent to network miners/validators.
* **Polygon PoS** - The fees paid by users are sent to network validators. However, it is likely that in the near future Polygon PoS will adopt the same system as Ethereum.
* **Avalanche C-Chain** - All transaction fees are burned - the AVAX tokens are gone forever. While some wallets such as MetaMask allow you to select a priority fee similar to how transactions are structured in Ethereum, in practice it is easier and more efficient to simply select a higher base fee. Everything is burned anyhow.

On every blockchain, the price of gas varies depending on how congested the network is. Each blockchain, however, have their own complex methodologies to analyze congestion levels and determine gas prices while keeping them somewhat predictable, avoiding huge spikes in price, etc.

Even so, price spikes may happen due to a large number of users trying to make time-sensitive transactions at any given time:

![Gas Prices on Avalanche C-Chain (23/12/2021)](<../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png>)

Charts like the one seen above can be found for Avalanche [**here**](https://ava-labs-inc.metabaseapp.com/public/dashboard/d7a03dd2-28cf-44e5-bc1d-3c9ef41e69f5#refresh=60). These spikes can happen during exciting new IDOs, token launches, NFT drops, etc. On Avalanche these usually are very short-lived and regular users can simply avoid making transactions for half an hour or so in order to avoid paying high fees for everyday transactions.

Reliable gas trackers for Ethereum and Polygon can be found [**here**](https://etherscan.io/gastracker) and [**here**](https://polygonscan.com/gastracker) respectively.

## Closing Thoughts

Now that fees make more sense, we can hopefully bypass some of the Web 2.0 mentality of fees always seemingly benefiting some large corporation or evil overlord. Gas fees are necessary in order to make our ecosystems function as they do, and even so there is always a lot of work being done in order for these to be as low and as predictable as possible.
