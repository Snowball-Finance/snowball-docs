# StableVault

StableVault is an [_**automated market maker (AMM)**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#automated-market-maker-amm) that allows you to exchange [_**stablecoins**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#stablecoin) and other [_**pegged tokens**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#pegged-tokens). The benefit of using StableVault over other exchanges is that StableVault offers low fees and low [_**slippage**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#slippage).

## Swapping with StableVault

You can swap stablecoins with StableVault and get better exchange rates than traditional exchanges. This is because StableVault uses a different underlying model for swapping. 

In this model, trades experience lower slippage. This is due to StableVault having more than two tokens as well as a different underlying formula. 

To keep StableVault balanced, a discount is given to swaps that balance the pool. Any swaps that imbalance the pool pay a slight premium. This creates [_**arbitrage**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#arbitrage) opportunities and brings the pool to equilibrium. 

## Adding liquidity to StableVault

There are three things to know when depositing or withdrawing [_**liquidity**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#liquidity) in StableVault. 

1\) You can deposit or withdraw any combination of tokens. 

_Example: in the DAI.e, FRAX, TUSD and USDT.e pool you can deposit all four tokens or just one token._

2\) Depositing or withdrawing a token that helps balance the pool gives you a discount. Similarly, deposits or withdrawals that imbalance the pool pay a premium.

_Example: in the DAI.e, FRAX, TUSD and USDT.e pool, if there is a surplus of DAI.e, then you will get more DAI.e by withdrawing in DAI.e. You will get a smaller share of the pool by depositing in DAI.e. The reverse is true if there is a shortage of DAI.e._

3\) Depositing gives you a receipt token called s4D. This token represents your underlying deposit. 

## Why add liquidity to StableVault?

Adding liquidity to StableVault gives you a cut of the swap fees. Additionally, you earn SNOB token rewards by depositing your StableVault receipt token into the [**Compound & Earn**](https://app.snowball.network/compound-and-earn) page of our website. 

In the future, StableVault will integrate with lending strategies across Avalanche and give an opportunity for higher [_**APRs**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#annual-percentage-rate-apr).

## Active StableVaults

[**s4D StableVault**](https://app.snowball.network/s4d-vault) - a 4 token pool between DAI.e, FRAX, TUSD and USDT.e

## Deprecated StableVaults

_These vaults are in the process of being deprecated._

[**s3D StableVault**](https://app.snowball.network/s3d-vault) - a 3 token pool between USDT, DAI, and BUSD

[**s3F StableVault**](https://app.snowball.network/s3f-vault) - a 3 token pool between USDT, FRAX, and TUSD

## StableVault Resources

{% content-ref url="../resources/frequently-asked-questions/stablevault-faq.md" %}
[stablevault-faq.md](../resources/frequently-asked-questions/stablevault-faq.md)
{% endcontent-ref %}

{% content-ref url="../resources/guides/depositing-into-stablevault.md" %}
[depositing-into-stablevault.md](../resources/guides/depositing-into-stablevault.md)
{% endcontent-ref %}

{% content-ref url="../resources/smart-contracts/stablevault-contracts.md" %}
[stablevault-contracts.md](../resources/smart-contracts/stablevault-contracts.md)
{% endcontent-ref %}
