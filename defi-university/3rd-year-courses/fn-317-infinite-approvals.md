# FN 317 - Infinite Approvals

Most decentralized applications utilize infinite token approvals for everyday user transactions. This course will cover everything you need to know about these:

* Defining Token Approvals
* Evaluating The Risks of Infinite Approvals
* Managing Token Approvals

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/fn-101-decentralized-finance.md" %}
[fn-101-decentralized-finance.md](../1st-year-courses/fn-101-decentralized-finance.md)
{% endcontent-ref %}

{% content-ref url="../1st-year-courses/fn-104-tokens.md" %}
[fn-104-tokens.md](../1st-year-courses/fn-104-tokens.md)
{% endcontent-ref %}

{% content-ref url="../1st-year-courses/fn-106-gas-fees.md" %}
[fn-106-gas-fees.md](../1st-year-courses/fn-106-gas-fees.md)
{% endcontent-ref %}

## Introduction

The method with which decentralized applications (dapps) can transfer tokens from your wallet is through approvals - a permission you are personally granting to the application's smart contract. When calling the 'approve' function of a token, you are allowing another smart contract to transfer X amount of tokens from your wallet. When a transfer takes place, the amount of tokens transferred is subtracted from the amount you allowed the contract to transfer on your behalf.

For example, if you allow a decentralized exchange to spend 10 AVAX tokens, and you trade 6 AVAX for SNOB, you will still have an allowance of 4 AVAX on the exchange's smart contract.

There are currently two popular methods of requesting user approval prior to making transactions - either requesting the exact amount the user plans to transfer, or an infinite amount.

{% hint style="info" %}
Snowball offers both approval methods - not selecting infinite approvals by default.
{% endhint %}

## Infinite Approvals

In practice, requesting an infinite amount of tokens involves simply asking the user to approve an extremely large number of tokens to the dapp's smart contract. While these approvals have been used in scams, they are most commonly used in large, real and trusted applications, mostly for one simple reason:

**With infinite approvals, you will only need to approve a token's expenditure once.** This means significantly less transactions and gas fees for a dapp that you might utilize on a consistent basis.

The issue behind this feature is that it is a significant trade-off between convenience/cost and security. It is given that smart contracts are immutable and can only act according to their code, hopefully transparent and verified on a block explorer. Regardless, there are instances where bugs and found and exploited. An example of such can be found [**here**](https://cointelegraph.com/news/multichain-asks-users-to-revoke-approvals-amid-critical-vulnerability).

## Managing Approvals

Given the presented trade-off, there are many ways of managing your finances appropriately with a risk level that is comfortable to you. A wallet with a small amount of funds can be used with infinite approvals with little risk, thus potentially avoiding a large amount in transaction fees, and being a little easier to use in day-to-day activities.

However, if you have a wallet address with a large percentage of your assets, it is likely you'll want to simply approve exactly what you are transacting at any given time. This means that once you have transacted your tokens, your approval amount for any given contract will be of 0.

Similarly, for infinite approvals you have granted previously, you can manually assign those approval amounts to 0. This can be done on Avalanche through [**SnowTrace**](https://snowtrace.io/tokenapprovalchecker), which is also covered in our guide [**here**](https://docs.snowball.network/resources/guides/metamask-security-measures). Other block explorers from other chains also offer this functionality, and there are also some third-party apps that may accomplish this.

## Closing Thoughts

Token approvals can present an unexpected risk factor to your funds, thus keeping them in check is highly advisable. Decentralized apps should take user safety extremely seriously, and it is a good sign that more dapps are opting for limited approvals by default over time. Stay safe out there!
