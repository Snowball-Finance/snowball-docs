# EX 281 - DeFi Composability

![](<../../.gitbook/assets/DeFi Composability.png>)

The composability of smart contracts in decentralized finance brings immense possibilities to the space, but also with it brings the possibility of new bugs, exploits and attack vectors. This course will cover the basic concepts of composability in DeFi, such as:

* Defining Composability
* Exploring Composability Benefits
* Analyzing the Negative Aspects of Composability

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](../1st-year-courses/fn-101-decentralized-finance.md)
{% endcontent-ref %}

## Introduction

The composability of a system refers to the inter-connectivity potential of its components. The world of decentralized finance is entirely built through smart contracts which interact with each other, meaning it is inherently a system of incredible composability.

This inter-connectivity allows smart contracts to build on top of other smart contracts, which can then be built upon further, and so on... Let's look at some examples of this building in practice:

## Building With Money Legos

The simplest building block in DeFi could likely be considered the tokens themselves. An ERC-20 token is just that, a token that exists on the blockchain. Without anything else they aren't very useful. With other smart contracts to govern their minting, however, a lot more can be done.

On Snowball, for example, the minting of SNOB tokens is governed by Snowball's Treasury, which in turn is controlled by Snowball's Governance contract as well as Snowball's Council contract. At this point, this is already 3 or 4 levels of legos piling on top of each other, and we've barely covered a fraction of one protocol built on the Avalanche blockchain.

Things get even more complex when you build smart contracts on top of another protocol's smart contracts, as Snowball does quite often. Here's another example, this time of a series of actions a user could take utilizing many protocols interacting with each other:

* Deposit AVAX on Teddy.
* Mint TSD on Teddy by using your AVAX as collateral.
* Mint LP tokens on Trader Joe by depositing AVAX and the TSD minted on a liquidity pool.
* Deposit the LP tokens on Snowball in order to auto-compound your rewards.
* Deposit the receipt token received into Snowball's gauge contract to earn SNOB.

Obviously these platforms will try and abstract as much of this functionality out as possible, but the underlying building blocks of all these actions are even more complex that the list above. Constant work is always being put into making even the most complex smart contract interactions as easy as possible for the end user.

## Why Is Composability Desirable?

The composable nature of smart contracts allows development of extremely complex financial tools to be much more efficient. It is incredibly difficult to build an all-encompassing financial tooling system in any scenario. By building on top of protocols and smart contracts that have achieved excellency in their particular space, you can increase the complexity of such system and offer more services in a much smaller timeframe.

In an ecosystem like DeFi that moves so fast, the speed at which tooling and services are built is critical. The faster we can develop solutions to our problems in DeFi, the more streamlined adoption will become, and the clearer its position will be in replacing the traditional financial systems.

## Composability Downsides

This efficiency of development and ease of which increased complexity can be achieved is all well and good, but it does come with some negative aspects. More specifically, these include increased risk of bugs and exploits, as well as generally creating fragmented liquidity in any given ecosystem.

#### Smart Contract Risks

By building smart contracts on top of other smart contracts, the risk of bugs and exploits increase since there are more contracts being used. Not only that, but the impact of any one contract being exploited or having a bug is largely amplified. If a token contract is exploited, all protocols in the ecosystem that leverage that token for any of their activity will have issues, for example.

#### Fragmented Liquidity

Due to the fact that DeFi is built in such a composable manner, there will likely always be different implementations of similar technologies. As more money legos are added to the pile, developers can create many more different products, but it does mean that token liquidity will be fragmented between all these great products. A lack of deep liquidity in any given asset is detrimental to users in the ecosystem, as it becomes more difficult to gauge value and swap between assets.

## Closing Thoughts

Smart contracts are the building blocks of this new financial ecosystem being created. As time progresses, even more of these blocks will be available to build with, meaning even more and better tools for the space. In the near future we could even see cross-chain composability become a reality. We should all look forward to what is being developed, or be a part of its creation!
