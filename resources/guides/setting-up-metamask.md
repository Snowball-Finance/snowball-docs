# Setting Up MetaMask

This guide covers how to setup MetaMask on your browser for making transactions on the Avalanche C-Chain. In order to transfer funds to your wallet, you'll need to use some exchange or fiat gateway that supports transfers/withdrawals to the Avalanche C-Chain.

1\) Install MetaMask from [**here**](https://metamask.io/download).

{% hint style="danger" %}
Always verify the URL you are downloading wallet software from. Downloading it from a third-party website may mean downloading compromised and unsafe software.
{% endhint %}

2\) Create or Import a Wallet.

If you already have an Ethereum wallet address, you can import it to MetaMask. If you do not, selecting **Create a Wallet** will allow you to make one. This process is free.

When following MetaMask's steps on creating a new wallet, make sure you take note of your password, seed phrase and private key. The password is locally stored - and is not linked to the blockchain in any way. The seed phrase is what MetaMask can use to identify your private key. Your private key is what any wallet software needs to sign your transactions on the blockchain.

Keep all three of these items somewhere safe, don't write them down online or in any cloud services or messaging apps. **If you lose all three, you will lose access to your wallet and all funds in it.**

3\) Connect to the Avalanche C-Chain.

![](<../../.gitbook/assets/image (9) (1) (1).png>)

By selecting **Add Network** on the dropdown menu, you'll be prompted to enter some data for the new network you want to connect to. Enter the following into their respective fields:

* **Network Name**: Avalanche Network
* **New RPC URL**: https://api.avax.network/ext/bc/C/rpc
* **Chain ID**: 0xa86a
* **Symbol**: AVAX
* **Block Explorer URL**: https://snowtrace.io/

Once these are setup, you should see Avalanche on the networks list to switch to anytime.

**Congratulations!** Once these settings are setup, you should see the Avalanche Network on the networks list to switch to anytime. Once you have some AVAX in this newly created wallet, you'll be ready to make some transactions.
