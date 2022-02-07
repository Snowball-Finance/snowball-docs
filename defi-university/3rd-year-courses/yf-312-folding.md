# YF 312 - Folding

Folding is a relatively safe investment strategy that can be profitable under certain conditions. This course will cover the following aspects of folding:

* Defining Folding
* Exploring Profitable Conditions
* Folding Risks

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/yf-111-lending-markets.md" %}
[yf-111-lending-markets.md](../1st-year-courses/yf-111-lending-markets.md)
{% endcontent-ref %}

## Introduction

To understand the concept of folding, let's take a look at one of Avalanche's lending markets:

![Trader Joe Lending Market - Screenshot taken on 20/10/2021](<../../.gitbook/assets/image (8) (1) (1) (1).png>)

The above is the lending market of Trader Joe, sometimes referred to as 'Banker Joe'. Other lending markets such as Aave, BenQi or Cream have a similar layout. The important data to keep an eye on is the market size (how much is being lent and/or borrowed) alongside the rates being offered. For the purposes of exploring folding strategies, we will focus on the rates available.

A quick summary of each rate being displayed is as follows:

* **Deposit APY** - Compounded interest rate on the token being deposited / lent out.
* **Deposit Rewards APR** - Rate for token incentives when lending.
* **Borrowing APY** - Compounded interest rate on any borrowed tokens.
* **Borrowing Rewards APR** - Rate for token incentives when borrowing.

In the case of Trader Joe, the deposit and borrowing rewards are currently paid out in JOE tokens. Other lending markets may choose to pay out these incentives in the form of their own token or sometimes in the form of the network's wrapped native token, like WAVAX.

**A folding strategy is one where assets can be repeatedly lent and borrowed in order to multiply the rewards received from token incentives.** While this can always be done, it is only profitable in some scenarios. Let's look at how folding works in more detail:

## How Folding Works

While the basic concept of folding is easy enough to comprehend, there are many factors to consider when deciding whether it would be an appropriate strategy to follow through with. The first is to consider the interest rates and incentives you are exposing yourself to. **If the interest rate for lending plus incentives is not higher than the borrowing rate, the strategy will not be profitable.**

$$
\text{Lending Rate} + \text{Lending Rewards} - \text{Borrowing Rate} + \text{Borrowing Rewards}
$$

In order for folding to be profitable, the equation above must result in a positive number. Let's take a look at an example from the last screenshot:

![](<../../.gitbook/assets/image (12) (1) (1).png>)

For the AVAX token, we can grab the current interest rates and incentives and check if it would be profitable to perform a folding strategy on such an asset at this time:

$$
10.57 + 5.94 - 18.18 + 8.17 = 6.5
$$

Since the resulting value is positive in this example, folding can be a profitable strategy. However, you must also take transaction fees into account. Every time you fold, you will be transacting twice, once for borrowing, and once for lending the borrowed assets. The more funds invested, the shorter the time it will take to recoup the losses of these transactions.

In practice, a 3x folding strategy using an 80% borrowing threshold would look like so:

1. You lend 100 AVAX
2. You borrow 80 AVAX
3. You lend 80 AVAX
4. You borrow 64 AVAX
5. You lend 64 AVAX
6. You borrow 51.2 AVAX
7. You lend 51.2 AVAX

Of course you can continue folding many more times, but with diminishing returns. This is because the 6.5% extra APY being gained on each fold is relative to the amount of capital invested, which grows smaller on each fold. To visualize this diminishing return, let's look at the returns on this strategy given 0, 1, 2 and 3 folds:

* 0 Folds (Only lending) = 16.51% APY
* 1 Fold = 21.71% APY
* 2 Folds = 25.87% APY
* 3 Folds = 29.2% APY

A more aggressive folding strategy using more folds and a 90% borrowing threshold, for example, can get even better rates, but will require more transactions and carry more risk.

## The Risks

As with any leveraged or margin trading strategy, the most important risk to keep in mind when folding is liquidations. **In contrast to most leveraged strategies, however, folding carries no liquidation risk on price movements.** This is because you are borrowing the same asset you are lending, meaning the price ratio of your borrowed assets to your collateral will always remain the same.

There is still risk of liquidation, but one entirely under your control. This is because while the benefits of folding dramatically increase the amount of incentive rewards you are accumulating, you are still losing funds due to the borrowing interest rate you are exposed to. In practice, this means you are losing token A while gaining even more of token B. Your collateral is token A, and the platform incentives you are receiving is token B.

If you borrow at a threshold of 90% against your collateral, for example, because of the borrowing interest rate, as time goes on that number will rise to 91%, 92% and so on. If your collateral is no longer enough to cover the amount you have borrowed (exceeded 100%), a portion of your funds may be liquidated. This is completely avoidable if you increase your collateral or pay back your loan using the rewards in token B you've gained throughout this time period.

**By using an auto-compounder like Snowball, this liquidation risk is also completely mitigated.** This is because our strategies automatically harvest your rewards to re-invest them, meaning they are converted back into token A periodically. Not to mention that you would also be gaining better rates since you are consistently increasing your invested amounts by the rewards harvested.

## Closing Thoughts

Folding can be a very profitable strategy, and knowing the risks and how to mitigate them can help you decide if it's a strategy worth pursuing. It can involve a lot of math, transactions and constant monitoring though to avoid liquidation and ensure the strategy remains profitable, which leads many to use auto-compounding contracts with all that logic already programmed in as an easy and safe solution to their folding needs.
