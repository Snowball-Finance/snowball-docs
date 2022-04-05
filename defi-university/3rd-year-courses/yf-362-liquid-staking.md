# YF 362 - Liquid Staking

![](../../.gitbook/assets/IMG\_0603.png)

Liquid staking brings a whole other level of flexibility when it comes to staking and securing the network. This course will cover the following regarding this awesome new way to stake:

* Defining Liquid Staking
* Exploring How Liquid Staking Works
* Pros/Cons of Liquid Staking

#### Suggested Prior Reading:

{% content-ref url="fn-308-consensus-mechanisms.md" %}
[fn-308-consensus-mechanisms.md](fn-308-consensus-mechanisms.md)
{% endcontent-ref %}

## Introduction

Liquid staking is a solution to the common problem of locking your assets long-term in any blockchain. In these stakes - usually in Proof-of-Stake blockchains - participants can gain significant yield on the chain's native asset while also helping secure the blockchain by validating blocks of transactions. The issue is that these stakes are almost always long-term commitments, where unstaking your assets before their locking period has come to an end is either impossible or not financially sound.

Liquid staking allows you to stake your assets as always, but in turn also be rewarded another liquid asset of the same or similar value to your stake when you do so. In practice, this means you can continue to utilize DeFi with that asset, as if your underlying assets were not locked.

## Advantages of Liquid Staking

#### Velocity of Money

As less assets are locked and unusable, the velocity of money in the network is increased. This does not mean there is more money in circulation, but rather that some of the value that was previously locked is now liquid again. This brings more economic activity to DeFi protocols as well as more opportunities for investors in the space.

#### Investment Flexibility

As liquid staking platforms are essentially a proxy between direct staking, they can bring many utilities to allow for more flexible staking. This is usually the case in terms of staking minimums as well as lock periods. Investors with less funds are able to stake through delegations with no minimums as enforced by most proof-of-stake blockchains, as well as stake for shorter or longer periods of time, with less restrictions and early withdrawal penalties.

## The Risks

#### Centralization

The risk of centralizing staked funds exists in most types of staking platforms, not only liquid staking ones. As a platform acts as an intermediary to facilitate such stakes, most commonly the assets are concentrated in one or a handful of validators in a network. This can be mitigated by employing a more decentralized approach to bringing in new validators to the platform, but can be a tough problem to solve.

#### Intermediary Points of Failure

Whenever there is an intermediary to any sort of transaction, there is risk. In DeFi this can be mitigated through well-tested, open-source smart contracts of course, but sometimes staking can be a little more complicated. On Avalanche, for example, since staking takes place on the P-Chain and DeFi and smart contracts take place on the C-Chain, there needs to be an intermediary to transfer funds between them.

#### Slashing

This refers to a penalty to validators that 'misbehave'; usually a loss of a certain percentage of your stake. This is not an issue on Avalanche since slashing does not occur, but in other networks since you are delegating your stake to another validator through the liquid staking protocol, you would need to trust the validator to not misbehave and lose your funds.

## Implementations

There are many ways to implement liquid staking, with each type of implementation having its own advantages and disadvantages. The following are a couple of examples to start you off on your own research:

### Lido

{% embed url="https://lido.fi" %}

**Lido** was one of the earliest liquid staking platforms available on Ethereum 2.0, and works well through issuing tokens 1:1 to your original stake. Although they have plans to decentralize their staking mechanisms in their roadmap, their current number of validators is quite low, meaning centralization is a definite concern.

### Lava

{% embed url="https://lavax.org" %}

**Lava** is another of Snowball's ventures, bringing decentralized and flexible liquid staking to Avalanche. LAVAX is issued 1:1 to your original stake, community validators mean that the protocol remains decentralized as it scales, and there are economic mechanisms in play to prevent malpractice from P-Chain/C-Chain intermediaries.

### BenQi

{% embed url="https://staking.benqi.fi/stake" %}

**BenQi**, the popular lending protocol on Avalanche, has also released their form of liquid staking. Their sAVAX token grows in value in reference to AVAX as staking rewards accrue, meaning it does not maintain a 1:1 peg to AVAX. This can be a little inconvenient for farming liquidity, but may facilitate rewards acquisitions. They also delegate stakes among public and available Avalanche validators, meaning their approach is also quite decentralized.

## Closing Thoughts

Liquid staking brings a lot of flexibility to staking, and thus becomes some of the safest and most rewarding strategies to invest in out there. Knowing how a protocol works when choosing one to stake in is extremely important, so make sure you research the ins and outs of it before investing any funds. Good luck in your liquid staking journey!
