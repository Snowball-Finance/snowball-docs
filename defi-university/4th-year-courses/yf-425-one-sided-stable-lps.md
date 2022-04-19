# YF 425 - One-Sided Stable LPs

Liquidity pools consisting of one volatile asset and a stablecoin have been around for a while, but have received significantly less attention than other alternatives due to their seemingly unavoidable levels of impermanent loss. This course will cover the following:

* Defining One-Sided Stable LPs
* Exploring Obvious Downsides
* Analyzing Not-So-Obvious Opportunities

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/yf-122-liquidity-pools.md" %}
[yf-122-liquidity-pools.md](../1st-year-courses/yf-122-liquidity-pools.md)
{% endcontent-ref %}

{% content-ref url="../3rd-year-courses/yf-323-impermanent-loss.md" %}
[yf-323-impermanent-loss.md](../3rd-year-courses/yf-323-impermanent-loss.md)
{% endcontent-ref %}

## Introduction

The majority of liquidity pools are of two assets, and a majority of those include pairing a network's native token to any other token. See AVAX-SNOB on Avalanche for example, or AVAX-PNG, AVAX-JOE, etc. Why? Well, the native token of any given network is by definition needed by the network's users, and thus has great liquidity, volume and use cases. It is also generally extremely easy to wrap that token to use in liquidity pools.

By creating a liquidity pool of any token and the network's native token, you're also allowing for easy routing between your pair and all other pairs on the DEX of your choosing, which may generate more swap volume through your pool.

Another asset that is generally used by the majority of a network's users, regardless of what protocols/dapps they enjoy interacting with, are stablecoins. These also share many pools with other assets, making them ideal as far as routing is concerned.

One-sided stable LPs - the focus of this course - refer to pairs that include one stablecoin and another volatile asset. See USDC-ETH, USDC-AVAX or UST-BTC, for example. Despite being composed of mostly common tokens with large marketcaps, having incredibly large amounts of liquidity, these are mostly ignored when considering investment opportunities. Let's look at why:

## Impermanent Loss

In the [**YF 323**](../3rd-year-courses/yf-323-impermanent-loss.md) course on impermanent loss, we recommend utilizing highly correlated assets or stablecoin pairs (two stablecoins paired with each other). Such advice is quite grounded in the reality of wanting to avoid impermanent loss, and in most cases is likely the safest approach to liquidity pools in general. After all, we can clearly see that avoiding impermanent loss in such one-sided stable LPs is quite difficult.

If the price of any asset in a liquidity pool changes after your deposit, the only way to mitigate impermanent loss in that position would be if the price of the second asset in that pool has also changed by the same amount, in the same direction. If your pool consists of one volatile asset and one stablecoin, that clearly cannot take place (at least not without destructive consequences to the stablecoin).

Unless the price of the volatile asset reverts back to its value during your initial deposit, you will have incurred impermanent loss in that position, relative to how far from that original price value the token is.

There is, however, great study into concepts such as [**mean reversion**](https://www.investopedia.com/terms/m/meanreversion.asp), where assets trend towards their mean average over any given period of time. By timing your entry into a liquidity pool where your entry price is as close to the volatile asset's mean price, you have a greater chance of essentially 'absorbing' potential price changes and more opportunity to liquidate your position with diminished impermanent loss. This is particularly applicable to assets commonly trading within a distinguished [**range**](https://www.investopedia.com/terms/r/range.asp).

## The Probabilistic Approach

Among the many interesting arguments for the profitability of a one-sided stable LP, one is approaching the issue of impermanent loss and upside potential through the lens of simple probability. For a simple liquidity pool, there are nine possible outcomes when it comes to the price action of its underlying assets:

1. <mark style="color:green;">Asset A has no change in price. Asset B has no change in price.</mark>
2. <mark style="color:orange;">Asset A has no change in price. Asset B's price increases.</mark>
3. <mark style="color:orange;">Asset A has no change in price. Asset B's price decreases.</mark>
4. <mark style="color:orange;">Asset A's price increases. Asset B has no change in price.</mark>
5. <mark style="color:green;">Asset A's price increases. Asset B's price increases.</mark>
6. <mark style="color:red;">Asset A's price increases. Asset B's price decreases.</mark>
7. <mark style="color:orange;">Asset A's price decreases. Asset B has no change in price.</mark>
8. <mark style="color:red;">Asset A's price decreases. Asset B's price increases.</mark>
9. <mark style="color:green;">Asset A's price decreases. Asset B's price decreases.</mark>

Obviously in reality there is a lot more granularity to how each outcome affects a pool's position, but we can simplify each outcome by how likely it is to generate a large amount of impermanent loss.

Highlighted in green above, for example, are the scenarios where impermanent loss is somewhat mitigated, even though outcomes 5 and 9 could see impermanent loss if one asset's price movement is much larger than the other.

Highlighted in orange are scenarios where impermanent loss is caused by one asset's price movement, and thus would require a large percentage change in order to cause a large amount of impermanent loss.

Highlighted in red are outcomes where due to assets' prices moving in different directions, a smaller percentage change in each asset's price would be required to affect the pool's ratio enough and cause significant impermanent loss.

The following would be a similar list of possible outcomes, but for a one-sided stable LP:

1. <mark style="color:green;">Asset A has no change in price. Asset B has no change in price.</mark>
2. <mark style="color:orange;">Asset A has no change in price. Asset B's price increases.</mark>
3. <mark style="color:orange;">Asset A has no change in price. Asset B's price decreases.</mark>

In this case we maintain the 1/3 chance of generating no impermanent loss, either the same as a traditional liquidity pool or drastically better if you'd argue against the classification of previous outcomes 5 and 9. More importantly, you are no longer exposed to the scenarios most likely to generate large amounts of impermanent loss. This is quite intuitive when you consider you are only exposed to the price movements of one token rather than two.

## The Automation Approach

The strategy of buying an asset when it's price is low and selling it when it is high is the most basic strategy in investing, regardless of the type of market. Many investors seeking exposure in DeFi may opt to have a significant amount of their assets in stablecoins, use them to buy a token when its price is low and other conditions have been met, and sell the token back to stablecoins when the price is high enough, or a downwards move is to be expected.

By instead allocating a token's position into a one-sided stable LP, you are essentially automating this strategy. Due to the way liquidity pools operate, as a token's price decreases there will be more of that token in the liquidity pool. Similarly, as a token's price increases there will be less of that token in the liquidity pool. If you have deposited liquidity into such pool, the ratio of your owned liquidity will be changing accordingly.

Take a USDC-AVAX liquidity pool, for example. As the price of AVAX decreases, your share of the liquidity pool will contain less USDC, and more AVAX. You are essentially spending USDC to purchase more AVAX as its price decreases. Similarly, as the price of AVAX increases, you will essentially be selling AVAX for USDC.

In practice, this functions as a somewhat unconventional [**hedge**](https://www.investopedia.com/terms/h/hedge.asp), where you are automatically taking profits off of a performing asset with the downside of limiting your exposure to that asset's potential upside. Of course these profits would only be truly realized when exiting the position. You could even consider exiting the position after a large upwards price change of an asset, accepting the impermanent loss that comes from such a move, if you expect the asset to quickly reverse towards its mean.

## The Yield Approach

At the end of the day, if a strategy's yield is not there, it is not worth much regardless of its safety factor or probability of impermanent loss. It is relevant that, as discussed prior, stablecoins are some of the assets with the most liquidity and volume of most ecosystems.

![Top 10 Trader Joe Liquidity Pools Sorted By 7-Day Volume (https://analytics.traderjoexyz.com/)](<../../.gitbook/assets/image (5).png>)

Above we can see the ten largest liquidity pools sorted by weekly volume, on Avalanche's largest decentralized exchange, Trader Joe. All of them include WAVAX, the wrapped form of Avalanche's native token; AVAX. Interestingly, six of them are also one-sided stable LPs, including the two largest pools, with over $100M in weekly volume each. Keep in mind this is only one decentralized exchange; similar results can be seen on Pangolin, for example:

![Top 10 Pangolin Liquidity Pools Sorted By 7-Day Volume (https://info.pangolin.exchange/)](<../../.gitbook/assets/image (11).png>)

Considering even the worst Trader Joe one-sided stable LP has a yield of 11.55% APR, one could argue that exposure to impermanent loss is but a small inconvenience. At these rates, the price of the volatile asset in such a pool would have to almost triple in order to engulf the yield received. This is, of course, completely plausible in DeFi during the timespan of a year, but nonetheless, if an asset you are holding triples in value, I'd say you are well off regardless.

Keep in mind the above rates are demonstrative of yield received through swap fees when providing liquidity, and not encompassing of any additional yield platforms such as Trader Joe or Pangolin may use as incentives to attract liquidity.

## A Personal Experiment

In an attempt to prove to myself the efficacy of these pools, I embarked in an almost 2-month long experiment in one of Trader Joe's pools; not one of their top pools in terms of liquidity or volume, but one with popular assets that I thought would enable me to gain some insights:

![WETH.e - USDC.e Trader Joe Liquidity Pool Stats](<../../.gitbook/assets/image (14).png>)

I entered the pool on the near the end of January, when the price of WETH.e was at approximately $2,396. During the time I had liquidity deposited in such pool, the price of ETH (and subsequently WETH.e) increased by 23.33%, to a value of approximately $2,955. Despite the large price increase, due to no downwards (or upwards) movement from the the stable asset in the pool, the impermanent loss caused was considerably low.

Even though I was only in the pool until the second half of March (approximately 50 days after depositing liquidity), the yield generated from swap fees more than covered the impermanent losses caused by the price jump. After all, the impermanent loss caused by such a move would only be approximately 0.55%.

By holding USDC and ETH, I would have a profit of 11.67% solely due to the price change of one of the tokens. By comparison, I withdrew my liquidity from the pool after the 50 days with a total profit of 14.12%, including any impermanent loss generated from price movements.

## Closing Thoughts

There are many strategies to consider when providing liquidity, and even more when considering the entirety of DeFi, nevertheless I hope these one-sided stable LPs are no longer dismissed as a simple guarantee of impermanent loss, and contribute to anyone's arsenal of investment tools. Be safe, informed, and happy farming!
