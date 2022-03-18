# FN 308 - Consensus Mechanisms

![](../../.gitbook/assets/IMG\_0630.png)

Different blockchains make use of different consensus mechanisms to ensure their decentralized nature and the safety of their network, while still remaining as scalable as possible. While software architecture is a large part of this, this course will specifically focus on how blockchains achieve consensus from their enormous number of participants; covering aspects as the following:

* Defining Consensus Mechanisms
* Understanding the Blockchain Trilemma
* Exploring Different Consensus Mechanisms

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](../1st-year-courses/fn-101-decentralized-finance.md)
{% endcontent-ref %}

## Introduction

Consensus mechanisms refer to the manner with which blockchains can achieve consensus; meaning the majority of the network agree that data or transactions made are valid. This is a fundamental aspect of any blockchain and necessary for their efficient functionality.

Different consensus mechanisms have been developed and explored in the recent years, with many different ways of addressing the many problems existing in achieving consensus efficiently. These problems have generally been referred to as the 'blockchain trilemma', including the three most important problems faced upon any blockchain design.

## The Blockchain Trilemma

![](<../../.gitbook/assets/image (9).png>)

The problems to solve within the blockchain trilemma are not exclusively related to consensus mechanisms, as major factors also include the blockchain's underlying software architecture, how data is stored, how nodes are engineered, etc. That being said, the consensus mechanism utilized on any given blockchain is integral to all its functionality, and needs to attend to these three problems accordingly:

### Security

Any blockchain needs to be secure. This means not allowing a malicious actor from manipulating any data existing on-chain, or adding any invalid or malicious data to any new block.

The toughest security risk to defend from is a an extreme form of Sybil attack often referred to as a 51% attack. This is particularly difficult since the purpose of a consensus mechanism is to infer consensus from the majority of participants in a network. If the majority of the network (51%) is malicious, well, that's tough to deal with.

This is why most networks' consensus mechanisms create/use scarce resources in order to represent a user in the network along with incentives to remain fair and to not attempt to harm the network.

### Decentralization

While using scarcity as a mechanism to halt malicious actors from taking part of a network is great from a security standpoint, it may cause issues regarding to the network's decentralization.

If the consensus mechanism makes it too difficult for any given user to take part in the network, logically less users will be able to take part in the network. As there are less users validating the network, it becomes less decentralized and could even make it easier to perform a 51% attack.

### Scalability

Scalability refers to many aspects of a blockchain as it scales. This includes the speed at which any given transaction achieves finality, the security and decentralization of the chain as well as any unintended outcomes such as significant environmental impact, etc.

As a blockchain scales, scarce resources may become too expensive resulting in lesser decentralization, or perhaps compromises on security may be made by not utilizing the entire network when achieving consensus, allowing for more efficient consensus to be reached.

## Consensus Mechanisms

### Proof of Work

This consensus mechanism was the first to be used in the blockchain space, still being used to this day when it comes to Bitcoin and Ethereum. The latter has plans to move to Proof of Stake sometime soon, however.

Through proof of work, a user (miner, in this case) needs to solve a complex algorithmic/mathematical problem in order to add new data to the blockchain. This is usually done through expensive graphics cards and/or dedicated mining hardware, which may consume a large amount of electricity and generate much heat. This mining is the activity through which scarcity is introduced to the consensus mechanism. In order to mine, you would need to have a lot of potentially expensive hardware for a single purpose, meaning a significant monetary loss for anyone planning to attack the network.

The incentive for users to mine new blocks and in turn help secure the network in this case is the mining rewards, usually through minting more of the network's native token and/or through a portion of transaction fees contained within blocks mined. The more mining capability a user has (more or more powerful hardware), the more likely it is that they will be picked to be the one mining  any given new block.

The mining of any given block of data is difficult to accomplish, but once the work has been done, it is extremely easy to be validated by other nodes in the network. In short, this is how the consensus mechanism functions. If the majority of nodes in the network agree to the previously mined blocks, they will keep adding new blocks on top of the old ones, forming a longer chain over time. The longer the chain, or in other words, the more validations previous blocks have, the safer any given block is to be truly valid.

### Proof of Stake

This consensus mechanism is the most utilized in many blockchains currently, with many chains opting for a slight variation of the original alternative to proof of work. In short, this consensus mechanism requires users to stake (deposit/lock) the network's native token for a period of time in order to participate. The more tokens you have staked, the more likely it is you will be selected to validate any given new block.

Similarly to proof of work, incentives are given out in various forms to network validators. In contrast, however, many blockchains have implemented slashing; the act of actively removing tokens from a users' stake if they attempt to harm the network in any way.

The act of validating data is a lot more efficient in proof of stake, since it does not involve any complex problem to solve, thus eliminating any potentially harmful environmental concerns as the network scales.

Many blockchains opt for this basic consensus mechanism for its simplicity and efficiency, while still creating an effective alignment between economic incentives and network security. There are, however, many changes that can be made to how a network reaches consensus other than its base scarcity/accessibility model. Let's look at how some chains approach this:

#### Ethereum 2.0

As Ethereum 2.0 is focusing more on its sharding infrastructure for scalability, the chain introduced a 128 validator 'committee' which checks the work done by any validator. These validators are chosen randomly among the validator pool, and this lower count makes it possible to accomplish efficient validation and reach consensus faster even on smaller shards. Read more about how proof of stake works on Ethereum 2.0 [**here**](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/).

#### Solana

Solana chose to adopt what is referred to as 'proof of history', a version of proof of stake where the truthfulness/validity of any block is determined by how long it has been stored on-chain. The longer that time is, the more effort it takes (a higher number of validators is needed) to classify it as invalid and roll it back. Read more about how proof of stake works on Solana [**here**](https://solana.com/news/proof-of-history).

#### Avalanche

Avalanche uses the [**Snowball Algorithm**](https://www.youtube.com/watch?v=AXrrqtFlGow\&t=357s) to achieve incredibly quick transaction finality, through clever use of probability. In a nutshell, it involves many rounds of validation where nodes query other nodes' responses to continuously learn more about the network's opinion on any given block of data. This means that not every node will have to check every other nodes' work, increasing efficiency with no compromise on security. Read more about how this algorithm works [**here**](https://docs.avax.network/learn/platform-overview/avalanche-consensus), or learn more about how proof of stake in general works on Avalanche [**here**](https://docs.avax.network/learn/platform-overview/staking).

## Closing Thoughts

There are many different ways of approaching consensus in a massively decentralized network, many of which have been extremely successful to this day. As blockchain technology and DeFi is increasingly adopted around the world we will likely see many struggle to meet the demands of the blockchain trilemma, especially at scale.
