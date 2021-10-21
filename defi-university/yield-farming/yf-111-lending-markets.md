# YF 111 - Lending Markets

Lending markets allow for the safe lending and borrowing of tokens in DeFi, similarly to traditional markets but without a centralized party managing the funds. This course will cover the following:

* Basics of Lending Markets
* Collateralization Principles
* Examples of Avalanche's Lending Markets
* Exploring Investment Strategies

#### Suggested Prior Reading:

None.

## Introduction

Lending and borrowing are essential functions of any fully fledged financial ecosystems, and in DeFi these are offered by what we call lending markets. In the surface, these markets provide very simple mechanisms to lend and borrow; you can lend your tokens in order to gain some percentage in interest, or you can borrow tokens and pay some percentage in interest.

It is important, however, to note that there is no centralized entity controlling your credit score, for example. There is no entity to come running after you if you don't pay back your loans. All lending market functionality is governed autonomously by its smart contracts. This is usually accomplished through the concept of over-collateralization.

## Over-Collateralization

By ensuring that all debt taken on the platform is over-collateralized, the value of assets being lent and borrowed against can fluctuate, without ever leaving anyone's funds behind. In practice, this looks something like the following:

1. Bob deposits 1000 USDC into the lending market, and enables it as collateral.
2. Bob can now borrow against the 1000 USDC they deposited as collateral.
3. Bob borrows 900 DAI from the lending market.

We're using stablecoins both worth $1 for simplicity's sake, and a 90% threshold on borrowing. The idea is that the value of USDC could drop by 10% and all funds borrowed would still be fully covered by the provided collateral.

What if the value of the collateral drops by more than 10% in this scenario? Well, liquidations would come into play. These can vary in functionality between lending markets, but one way or another your collateral would be at least partially liquidated. This means that part of your collateral would be used to pay back what you owe, automatically.

Of course the tokens being lent and borrowed don't have to be stablecoins; one could lend ETH and borrow AVAX for example, or any combination of tokens at all, as long as the value of the collateral is larger than the value of the tokens being borrowed.

## Avalanche Ecosystem

In Avalanche, there are currently 3 main lending markets:

* [**Aave**](https://aave.com) - The largest lending market from Ethereum, now on Polygon and Avalanche.
* [**Trader Joe**](https://www.traderjoexyz.com/#/lending) - Avalanche's largest DEX, which recently added lending functionality.
* [**BenQi**](https://benqi.fi) - Lending market native to the Avalanche chain.

Each platform have different approaches to collateralization ratios and interest rates, but what all have in common are token incentives for those lending and borrowing on their platform. Currently Aave provides incentives in WAVAX tokens, while BenQi uses QI, their own governance token. Trader Joe uses a mix of both, their JOE token and AVAX tokens.

![Aave's Interface](<../../.gitbook/assets/image (10).png>)

Lending markets will commonly display, as seen above, the total market size of each token, the amount being borrowed, and the rates for both lending and borrowing each asset. In this case the platform incentives are shown under the deposit and borrow APYs. Other lending markets will share a similar interface, but may or may not already include the incentives when displaying their rates.

## Investment Strategies

"If you can only borrow up to a certain ratio of your collateral, what is the point of borrowing? Why not just use the assets you lent instead?" - A common question to pop up when it comes to lending markets. The answer comes in the form of many strategies that take these lending markets into account.

The simplest that comes to mind is a scenario where borrow incentives are so high that it makes sense to borrow against your assets to make more over time. That is, when the incentives are higher than the cost to borrow. This scenario sometimes happens when an asset is not being borrowed against very often, and platform incentives are increased for some reason.

The second reason to borrow would be to leverage your position on the same or a different asset. If you are extremely bullish on AVAX, for example, you could lend your AVAX, borrow some stablecoins by using your AVAX as collateral, and buy more AVAX. The same can be said for if you want to buy another token but don't have the assets on hand to do so. You could lend out your AVAX, borrow stablecoins and buy SNOB tokens, for example.

{% hint style="danger" %}
As always, strategies that involve leverage are risky and increase your exposure to volatile assets. Do your own research and invest carefully.
{% endhint %}

If the platform incentives are high enough so that you are gaining more for lending than borrowing, you can also implement folding strategies. These involve lending and borrowing repeatedly until it is no longer profitable due to diminishing returns. Snowball implements many folding strategies on all the lending markets on Avalanche alongside our auto-compounding strategies, so you don't have to do the math yourself.

{% hint style="info" %}
Want to learn more about folding strategies? Check out our YF 312 course on 'Folding'.
{% endhint %}

## Closing Thoughts

Making use of lending markets, either through Snowball or otherwise, can net you a lot of interesting opportunities, and if you know what you are doing when it comes to borrowing can  be some of the safest ways to invest due to the low or zero risk of liquidations when folding or simply lending an asset.
