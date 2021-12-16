# StableVault FAQ

### Where can I find the StableVault?

The StableVault can be found on the [**StableVault**](https://app.snowball.network/s4d-vault) page of our website.

### Is StableVault safe?

StableVault uses code that has been forked from [**Saddle Finance**](https://saddle.finance), which has been audited. However, we still recommend using the protocol with caution as any new code may not have been fully audited. You can review our code on the [**Snowball GitHub**](https://github.com/Snowball-Finance).

### Are there any deposit or withdrawal fees on the StableVault?

None. There are however incentives and disincentives to deposit or withdraw tokens that would balance or imbalance the pool. See more details [**here**](../our-products/stablevault.md).

### Do I need to deposit all the tokens listed in the vault?

No, you can deposit any combination of tokens into StableVault. This is possible because the tokens in the pool are all [_**stablecoins**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#stablecoin) pegged to the U.S. dollar. To keep the balance of the pool stable, we give incentives to anyone who deposits a token that has a lower supply in the pool.

### Why did I receive less tokens than I put into the pool?

If you deposit a token that is high in supply, relative to other tokens in the pool, you will pay a small premium for depositing. Similarly, if you deposit a token with a low supply, relative to the other tokens in the pool, you will be given a discount.

For example, if there are 300 DAI.e, 500 FRAX, 400 TUSD and 700 USDT.e in the s4D pool, you will need to pay a fee to deposit USDT.e and you will be given a reward to deposit DAI.e. The exact same mechanism is also applicable when withdrawing from the pool. Given the above example, you would pay a fee to withdraw in DAI.e and be rewarded for withdrawing in USDT.e.

### Where can I get the tokens to deposit into the s4D pool?

DAI.e, FRAX, TUSD and USDT.e can be found on most Avalanche exchanges. In case they are not listed by default, their addresses are the following:

* DAI.e - [**0xd586E7F844cEa2F87f50152665BCbc2C279D8d70**](https://snowtrace.io/token/0xd586E7F844cEa2F87f50152665BCbc2C279D8d70)****
* FRAX - [**0xDC42728B0eA910349ed3c6e1c9Dc06b5FB591f98**](https://snowtrace.io/token/0xDC42728B0eA910349ed3c6e1c9Dc06b5FB591f98)****
* TUSD - [**0x1C20E891Bab6b1727d14Da358FAe2984Ed9B59EB**](https://snowtrace.io/token/0x1C20E891Bab6b1727d14Da358FAe2984Ed9B59EB)****
* USDT.e - [**0xc7198437980c041c805A1EDcbA50c1Ce5db95118**](https://snowtrace.io/token/0xc7198437980c041c805A1EDcbA50c1Ce5db95118)****

Always double-check the token's contract address before making a swap.

### What are the fees to swap using the StableVault?

All swaps through the StableVault have a 0.04% fee. 75% of these fees (0.03%) are shared amongst the pool's liquidity providers. The other 25% of the fees (0.01%) is sent to Snowball.

### Why use StableVault instead of an exchange like Pangolin?

Most [_**decentralized exchanges**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#decentralized-exchange-dex) are modeled after Uniswap V2. They are excellent models for swapping most cryptocurrencies; however, they are not great for swapping [_**stablecoins**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#stablecoin) or other [_**value-pegged assets**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#pegged-tokens). This is because the model allows for lots of [_**slippage**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#slippage) on the tokens being swapped.

If a stablecoin pool undergoes a large transaction in this traditional model, then the two coins may be taken off peg. For example, one may trade slightly lower than $1, around $0.95, while the other may trade slightly higher, around $1.05. With StableVault, this risk is mostly mitigated. In this scenario, the coins would still be relatively close to their $1 peg, closer to $0.99 and $1.01.
