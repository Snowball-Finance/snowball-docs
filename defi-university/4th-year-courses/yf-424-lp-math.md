# YF 424 - LP Math

The math around liquidity pools can be a bit confusing, but nonetheless very insightful. This course will shed a light on the equations that govern these pools and will cover the following:

* Constant Product Formula
* Calculating Fee Revenue
* Calculating Impermanent Loss

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/yf-122-liquidity-pools.md" %}
[yf-122-liquidity-pools.md](../1st-year-courses/yf-122-liquidity-pools.md)
{% endcontent-ref %}

{% content-ref url="../3rd-year-courses/yf-323-impermanent-loss.md" %}
[yf-323-impermanent-loss.md](../3rd-year-courses/yf-323-impermanent-loss.md)
{% endcontent-ref %}

## Introduction

There are many different types of liquidity pools, but by far the most common are pools with two tokens, of a 1:1 ratio (50/50) in total pool value. This course will explore these pools. The equations demonstrated in this course are applicable to other types of pools, but would require some modifications.

## Constant Product

The main equation that governs the balancing of tokens in a liquidity pool is the constant product formula:

$$
x * y = k
$$

Simple enough. In this equation, `x` refers to the amount of the first token in the pool, and `y` refers to the amount of the other token in pool. Finally, `k` is the pool's constant product. Let's use the AVAX-SNOB pool on Pangolin as an example:

![Pangolin's AVAX-SNOB Liquidity Pool Contract](<../../.gitbook/assets/image (11).png>)

As can be seen on the pool's [**contract**](https://snowtrace.io/address/0xa1C2c3B6b120cBd4Cec7D2371FFd4a931A134A32), there are approximately 1,089 AVAX tokens and 623,500 SNOB tokens in it. This means we can calculate the pool's current `k` value:

$$
\text{1,089} * \text{623,500} = \text{678,911,50}0
$$

This value, while not very useful on its own, can help calculate the pool's balances based on certain events. The relevant events that can take place in a liquidity pool are the following:

* Others deposit into the liquidity pool
* Fees are collected from swaps
* A change in price of one of the tokens in the pool

When others deposit into the pool, the value of `k` would increase since there are more tokens in the pool, but your percentage share of the pool would decrease proportionally. Therefore, other than receiving a smaller percentage of trading fees over time, your LP position would not be majorly affected.

In the case of trading fees being collected into the pool, since there are also more tokens in the pool, the value of `k` would increase. However, since there are still the same amount of LP tokens in circulation, your share of the pool is unaffected. This means your LP tokens are now worth more. For example, if you owned 0.5% of the pool:

$$
\frac{\text{1,089}} {100} * 0.5 = \text{5.445} \text{ AVAX} \text{, } \frac{\text{623,500}} {100} * 0.5 = \text{3,117.5} \text{ SNOB}
$$

However, let's say over the span of a week 10 AVAX and 5,725 SNOB were collected as fees into the pool:

$$
\frac{\text{1,099}} {100} * 0.5 = \text{5.495} \text{ AVAX} \text{, } \frac{\text{629,225}} {100} * 0.5 = \text{3,146.125} \text{ SNOB}
$$

This would result in a profit of 0.05 AVAX and 28.625 SNOB for you. This is assuming there were no deposits into or withdrawals from the pool in terms of liquidity, or any asset price changes.

These first two events are quite self-explanatory, and do not require a lot of calculations. Where it does start getting a little messy is when price changes come into play.

## Price Changes

The important value to keep in mind when considering asset price changes is the ratio between the two tokens in the pool. In our starting example:

$$
\frac{\text{623,500}} {\text{1,089}} \approx 572.54
$$

In practice, this means 1 AVAX is equal to 572.54 SNOB. As calculated beforehand, if you owned 0.5% of the pool, you have 5.445 AVAX and 3,117.5 SNOB.

However, let's say that the price of SNOB tokens doubles by next week. AVAX prices remain the same. 1 AVAX would be equal to 286.27 SNOB. In order to calculate the new pool balances based on this price change, we need a few new equations:

$$
x_t = \sqrt{\frac{k} {r_t}}, y_t = \sqrt{{k * r_t}}
$$

In the equations above, `x` and `y` are the token balances at any given time. `k` is the product constant that we calculated beforehand. `r` refers to the ratio of tokens at any given time. We can test these equations with our original values prior to the price change:

$$
x_t = \sqrt{\frac{\text{678,911,500}} {572.54}} \approx \text{1,089}, y_t = \sqrt{{\text{678,911,500} * 572.54}} \approx \text{623,461}
$$

And similarly, calculate the new balances after the price change using the new ratio:

$$
x_t = \sqrt{\frac{\text{678,911,500}} {286.27}} \approx \text{1,540}, y_t = \sqrt{{\text{678,911,500} * 286.27}} \approx \text{440,854}
$$

If you owned 0.5% of the pool, previously you would have had 5.445 AVAX and 3,117.5 SNOB. After the price change, you would now have:

$$
\frac{\text{1,540}} {100} * 0.5 = \text{7.7} \text{ AVAX} \text{, } \frac{\text{440,854}} {100} * 0.5 = \text{2,204.27} \text{ SNOB}
$$

## Impermanent Loss

Since we have the pool's token balances at any given time based on it's token ratio, we can also calculate the impermanent loss for any price change. We can convert the token balances to one token for easier calculations. For example, prior to the price change:

$$
\text{1,089} + \frac{\text{623,461}} {572.54} = \text{2,178 AVAX}
$$

And similarly, after the SNOB token's price change:

$$
\text{1,540} + \frac{\text{440,854}} {286.27} = \text{3,080 AVAX}
$$

If you owned 0.5% of the pool, you would have gone from having the equivalent of 10.89 AVAX to having the equivalent of 15.4 AVAX. That is a 41.41% increase in value, or a profit of 4.51 AVAX. Since the value of SNOB doubled, wouldn't you expect a 50% increase in value? The value of your original deposit, if you hadn't provided liquidity, would now be the following:

$$
5.445 + \frac{3,117.5} {286.27} \approx 16.335 \text{ AVAX}
$$

This would be a 50% increase in value, as expected. To calculate the impermanent loss of such an event, we can use the following equation:

$$
\text{IL} = \frac{value_{lp}} {value_{hold}} - 1
$$

$$
\text{IL} = \frac{15.4} {16.335} - 1 \approx -0.057 = \text{-5.7%}
$$

**This means that a 100% change in price of one token in comparison to the other paired token will result in an impermanent loss of approximately -5.7%.** Of course, if AVAX prices in this example also climb in at the same rate, impermanent loss will be null. The same is true for the same percentages to the downside, as well.

## Closing Thoughts

With these equations, you can more accurately predict the impact of trading fee revenue, price changes and impermanent loss on your LP positions. With this information you can hopefully make better decisions as to what pools you would like to invest in, and what risks you are willing to take in your positions.
