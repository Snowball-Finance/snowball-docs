# FN 205 - Bridges

Bridges are fundamental services for being able to move tokens between different blockchains and thus keeping our decentralized finance ecosystem as well-connected as possible. This course will cover the following regarding these:

* Defining Bridges
* Exploring Different Bridge Types
* Listing Popular Bridges

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](../1st-year-courses/fn-101-decentralized-finance.md)
{% endcontent-ref %}

{% content-ref url="../1st-year-courses/fn-104-tokens.md" %}
[fn-104-tokens.md](../1st-year-courses/fn-104-tokens.md)
{% endcontent-ref %}

## Introduction

Let's say you have some tokens on Ethereum or some other blockchain, and you would like to use them on some exciting new decentralized apps on Avalanche. How would you make this move? In some cases, you might have to rely on a centralized exchange somewhere, deposit your tokens there, and hope they have support for Avalanche's C-Chain. Bridges introduce a solution to this problem.

Through a bridge, you are able to transfer tokens on Ethereum to the same equivalent token on Avalanche, for example. Some bridges even allow swapping for a different token on another chain, which can be useful if you planned to make the swap on the other end anyways. Let's get into how these work:

## Bridge Functionality

While they are most commonly referred to as bridges, there are technically two distinct types of services that function entirely differently from one another; bridges and routers.

**Bridges function by locking a token on the original chain, and minting a new token on the destination chain.** This means the new token is backed 1:1 by the locked token. As an example, this would be like bridging USDC from Ethereum to Avalanche, where you would receive USDC.e tokens. Bridging the other way (from Avalanche to Ethereum) would result in the new token being burned, and the original token being sent to your wallet.

**Routers function by having liquidity for a token in both chains, receiving it through a user in one chain and delivering it to such user in another chain.** This means no tokens are locked or minted in the process. Following the previous example, it would mean the protocol would have USDC tokens on Ethereum and USDC.e tokens on Avalanche. As long as there is enough liquidity, one can swap between them.

Due to each of these methodologies requiring smart contracts to operate on both the origin and destination chain, there needs to be some system connecting the two. Most bridges opt for a centralized approach, since it is the easiest to implement and guarantees control over the transactions taking place. There are, however, ways of achieving this functionality in a decentralized manner, and those do opt for these are called trustless bridges. These usually involve validating transactions in the same way a blockchain does - through miners or validators.

## Bridges Available

There are many bridges available on every chain, meaning they are are more inter-connected than ever before. When choosing between bridges, it important to take into account a number of factors:

* If a bridge is trustless or centralized.
* The fees charged to bridge your tokens.
* Any bridge-specific liquidity issues on routing.
* The chain and/or token coverage of the bridge.
* How long a transaction takes to complete.

To that end, let's look at some of the best bridges available on Avalanche (most of which are also available in a handful of other chains):

### Avalanche Bridge&#x20;

{% embed url="https://bridge.avax.network" %}

The Avalanche Bridge is the native bridge of the Avalanche C-Chain, and can be used to bridge the most popular tokens between Ethereum and Avalanche.

It is a simple bridge that functions extremely well, and also awards any transaction of over $75 to Avalanche with a generous AVAX airdrop. The fee associated with such transaction will be a flat fee of $3 for Ethereum to Avalanche transactions, or $15 for Avalanche to Ethereum transactions.

### AnySwap V3

{% embed url="https://stable.anyswap.exchange/#/swap" %}

AnySwap V3 is a trustless bridge that functions as a router. It has fees of only $0.9, unless you are bridging to Ethereum, in which case a 0.1% fee is charged. Transactions can take over 10+ minutes, and even larger amounts of time on large transactions. This bridge covers 8 different chains, but only a handful of stablecoins and WETH can be bridged.

This version is a big improvement in terms of usability when it comes to [**AnySwap V2**](https://anyswap.exchange), but if you'd like to bridge other tokens not supported by V3, V2 is your best bet. It comes with similar fee structures, a lot more chain and token support, but much less pleasant of a user experience. When using their router, you would have to ensure a token has enough liquidity on destination chain, lest your tokens won't be fully routed (you'll have to wait for someone to add liquidity before being able to withdraw).

### cBridge

{% embed url="https://cbridge.celer.network/#/transfer" %}

cBridge is another trustless bridge that offers a very simple user experience. Transactions take about 5-10 minutes, and it covers 8 of the most popular chains. The bridge covers only some of the most popular stablecoins along with WETH.

A bridging transaction has a base fee that usually ranged between $2-$3, and a 0.04% fee based on the amount transferred. If you are transferring between L2s on Ethereum such as Arbitrum or Optimism, this fee is increased to 0.1-0.2% depending on the transaction's direction.

### Synapse Bridge

{% embed url="https://synapseprotocol.com" %}

The Synapse Bridge offers trustless bridging between 10 different chains, and many of the same tokens offered by other bridges. Due to the nature of their protocol, you can even swap one token for another in some cases, such as USDC on Avalanche for DAI on Ethereum, for example. Bridging also provides some small amount of native tokens on the destination chain for future transactions, which is a great addition.

Their fees are a little more complex, since they depend on liquidity of each of their pools. In practice, these are usually a flat fee of $1-$3 on most chains ($200 on Ethereum), and a certain percentage on top of that based on pool composition and liquidity. This percentage could even be negative!

### ElkNet

{% embed url="https://app.elk.finance/#/elknet" %}

ElkNet is a bridge that provides functionality for bridging the ELK token to other chains. While in Beta, there are no fees associated with the bridge other than what a user would pay for gas fees. Transactions take at least 2+ minutes to complete, and there is an option to convert 1 ELK to the destination chain's native token for future gas fees.

This simple bridge can be a great choice if the fees on other bridges are too high - as long as buying and selling the ELK token on any given chain would not generate too much loss to compensate for that.

## Closing Thoughts

There are a lot of great bridges to choose from, and as the ecosystem evolves, there'll be even more popping up. You should always check the rates and fees offered by each bridge before committing to a transaction, since even your favorite bridge may not be the best for the particular transaction you want to make. Have a safe and great time with your swaps, and good bridging!
