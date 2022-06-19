# Compounding FAQ

### Where can I find the current list of compounding strategies?

All our compounding strategies can be found on the [**Compound & Earn**](https://app.snowball.network/compound-and-earn) page of our website. You can also find a list of all strategies under the [**Compounding Contracts**](../smart-contracts/compounding-contracts.md) page of our documentation.

### What fees does Snowball charge for auto-compounding?

Snowball takes a 10% performance fee on all profits made through auto-compounding. This happens once every harvest. There are no deposit or withdrawal fees.

### Are Snowball’s compounding strategies safe?

Snowball’s compounding strategies use code that has been forked from [**Pickle Finance**](https://www.pickle.finance), which has been audited. However, we still recommend using the protocol with caution as any new code may not have been fully audited. You can review our code on the [**Snowball GitHub**](https://github.com/Snowball-Finance).

### How does auto-compounding work with Snowball?

To learn about how auto-compounding works with Snowball, visit the [**Compounding**](../our-products/compounding.md) page of our documentation. For a step by step guide on how to use Snowball’s auto-compounding page, view our [**compounding guides**](../resources/guides/).

### How do I earn SNOB rewards while compounding?

Once you’ve deposited tokens into a compounding strategy on Snowball, you will automatically start to earn SNOB rewards if the pool you deposited into has been voted on to receive rewards. SNOB rewards are determined by each pool's [**gauges**](../governance/xsnob/gauges.md).

### How often are rewards compounded?

Rewards from our compounding strategies are compounded / re-invested 2-3 times a day. Feel free to check the #harvests channel on our [**Discord Server**](https://discord.gg/BPnBYDSqcb) to see updates each time this takes place.

### Does the APY on pools take fees into account?

All APR and APY values displayed on Snowball have already taken into account our performance fee. What you see is what you get, always.

### I don't see my pool on Snowball anymore. Are my funds safe?

If a pool you've deposited into is deprecated (no longer in use) it will not be displayed on our website. But do not worry, your funds are safe. Check out our guides [**here**](../resources/guides/) on how to withdraw them.

### Can I get liquidated when depositing in any of Snowball's single-asset auto-compounding strategies?

There is no liquidation risk for any of Snowball's strategies. This is because on our folding strategies, you are borrowing the same token you are providing as collateral, and Snowball is constantly re-investing your rewards, so your borrowed amount will never surpass 100% of your collateral's value.

### My single-asset strategy balance is slowly decreasing over time. What is going on?

If the single-asset strategy you are deposited into involves folding, your balance will slowly decrease due to borrowing costs until a harvest occurs. When this takes place, Snowball is selling the rewards you've accumulated for your original underlying asset, and your balance will increase by a value much higher than what it decreased by previously. At the moment, these harvests take place 2-3 times a day and can be tracked through the #harvests channel on our Discord server.

### When are strategy APRs updated?

The APRs displayed on each strategy on our site are updated every 10 minutes.

### How is Snowball getting such high rates from lending platforms?

When possible, Snowball's strategies employ folding strategies. These allow us to achieve much higher rates on single-asset strategies that just lending your assets normally. To learn more about folding, check out our explanation [**here**](../our-products/compounding.md#lending-+-folding-strategies) or head to our [**DeFi University**](../defi-university/introduction.md).

### What happens when SNOB emissions end?

Once SNOB emissions end, rewards will continue to be rolled out through buyback functionalities similar to proposal 14’s. Of course, there can be any change to the systems behind SNOB rewards if the community deems it necessary, in which case a proposal will be put in place for us all to vote on together.

### I haven't seen any harvests taking place in a little while, is everything OK?

Harvest may not occur in certain circumstances, such as during rapid spikes in gas prices. Since we compound so often though, any changes to strategy profitability should be negligible.

### How can I calculate how much I've earned through compounding?

While these stats are currently not displayed on Snowball's dashboard - they will be in the near future. Until then, keeping track of how much you've deposited initially is the easiest way to calculate this. Simply subtract that amount from what you currently have on Snowball, regardless of what type of token it is.

If you haven't kept track, you can check your transaction history through a [**block explorer**](https://snowtrace.io) by inputting your wallet address. Some tools are available to help in that regard, so don't hesitate to reach out to us on [**Discord**](https://discord.gg/BPnBYDSqcb) if you need help.

### I've withdrawn my funds but don't see the tokens in my wallet, what happened?

The most likely scenario is that you've withdrawn your LP tokens to your wallet - these are Liquidity Provider tokens from platforms such as Trader Joe or Pangolin, where you initially made your deposit. In order to convert those into your original tokens you'll have to go to their platforms and withdraw your liquidity. You should be able to see and withdraw your liquidity on the 'Pools' tab of either one.

### How do Zappers work?

Zappers work through automatically making most of the transactions needed for depositing into our many compounding strategies. These are the same transactions you would be making manually otherwise, but faster and more gas-efficient. All tokens received through such transactions go to your wallet or our strategy on your behalf. No protocol fee is taken for this service. Read more about this functionality in our article [**here**](https://medium.com/snowball-finance/a-look-at-snowballs-new-zapper-functionality-a7ddabae483).

### How do Optimized Pools work?

Optimized Pools work by daily re-allocating funds to whichever platform has the best yield at the time. Of course this means only utilizing the best battle-tested dapps on Avalanche, to ensure users' safety. Learn more about these pools in our article [**here**](https://medium.com/snowball-finance/introducing-snowballs-optimized-pools-ebba8dca34d9).
