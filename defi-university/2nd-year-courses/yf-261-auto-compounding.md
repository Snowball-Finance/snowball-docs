# YF 261 - Auto-Compounding

Auto-Compounding services allow users to maximize the rates on their investments through utilizing extra platform rewards as efficiently as possible. This course will cover the following:

* Defining Auto-Compounding
* Exploring Parameters and Fees
* Snowball's Strategies

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/yf-111-lending-markets.md" %}
[yf-111-lending-markets.md](../1st-year-courses/yf-111-lending-markets.md)
{% endcontent-ref %}

{% content-ref url="../1st-year-courses/yf-122-liquidity-pools.md" %}
[yf-122-liquidity-pools.md](../1st-year-courses/yf-122-liquidity-pools.md)
{% endcontent-ref %}

## Introduction

When providing liquidity, either through a lending contract on a lending market or a liquidity pool on a decentralized exchange, you will likely be gaining some extra token rewards as a platform incentive. An auto-compounder would sell those extra token rewards for whatever token you initially invested, and add them to your investment.

With this compounding effect, your investment's returns would increase exponentially as time goes on. This is something that you could to manually, however. You would simply need to spend some more assets on transaction fees, and compound your earnings every day or every week. Auto-compounders do that for you, however. Not only would you not be paying transaction fees every time you compound, but the auto-compounding contract will likely have a strategy to compound as efficiently as possible; maximizing your returns.

## Auto-Compounding Parameters

In order to compound efficiently, the contract's strategy should take many parameters into account:

* Transaction fees
* Any platform-specific deposit/withdrawal fees
* Incentive rewards rate

With these in mind, an auto-compounder should calculate how often it should harvest rewards and re-invest them to earn the most over time. Along with these, it should also calculate how much of a performance fee it should charge in order to cover the costs of these transactions.

If a strategy can gain a lot more by compounding multiple times a day, for example, it may be worth it to spend more in transactions and charge a higher performance fee to do so. At the end of the day, the user would see higher returns. If transactions costs rise, however, it might not be profitable to maintain a high rate of harvests. These are all calculations done by a well-written auto-compounding smart contract.

## Snowball's Strategies

Snowball provides auto-compounding strategies for liquidity pools on popular decentralized exchanges, compounding 2-3 times per day and drastically increasing the rates earned for any given token pair. Alongside our strategies, we also offer extra SNOB rewards allocated based on our community's voting. The performance fee on our auto-compounding strategies is of 10%, and there is no deposit or withdrawal fees on any of Snowball's strategies.

There are also Snowball strategies on single-asset deposits, usually through lending markets. Alongside the usual 2-3 harvests per day, the single-asset strategies also involve folding, where you repeatedly lend and borrow the same asset in order to make the most of the incentives provided in any given platform. These usually greatly multiply earnings compared to simply depositing into a lending market.

{% hint style="info" %}
To learn more about Snowball's compounding strategies, check out our [**Compounding page**](../../our-products/compounding.md) or our FAQ [**here**](../../faq/compounding-faq.md).
{% endhint %}

## Closing Thoughts

Auto-compounding can not only take a lot off your plate, but also allow you to gain a much better rate on your investment than you otherwise would have. Be sure to check out all the auto-compounding opportunities out there prior to investing into any liquidity pool or lending market!
