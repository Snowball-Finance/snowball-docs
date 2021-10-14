# Security

## **Smart Contract Audits** <a href="smart-contract-audits" id="smart-contract-audits"></a>

Snowball originated as a fork of Pickle Finance and Saddle Finance, both of which have been thoroughly audited. Their audits can be found [**here**](https://github.com/pickle-finance/protocol/tree/master/audits) and [**here**](https://github.com/saddle-finance/saddle-audits), respectively. However, the Snowball protocol itself has not been audited yet.

## Timelock

All Snowball contracts have a 24 hour timelock for any upgrades, updates or changes. Furthermore, all key admin functions on contracts, including any SNOB token emissions, are also subjected to a 24 hour timelock.

## **Multisig** <a href="timelocks-and-multisig" id="timelocks-and-multisig"></a>

To further increase the decentralization of the Snowball protocol, we have implemented 3 separate [_**multisig**_](https://snowballs.gitbook.io/snowball-docs/resources/defi-glossary#multisig) contracts. They are the following:

### 1) Treasury

This contract is owned and controlled by on-chain governance and our Council. It is the owner of almost all other Snowball smart contracts.

**Treasury Address:** [0x294aB3200ef36200db84C4128b7f1b4eec71E38a](https://cchain.explorer.avax.network/address/0x294aB3200ef36200db84C4128b7f1b4eec71E38a/transactions)

| Signer         | Address                                                                                                                                            |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Governance** | [0xfdCcf6D49A29f435E509DFFAAFDecB0ADD93f8C0](https://cchain.explorer.avax.network/address/0xfdCcf6D49A29f435E509DFFAAFDecB0ADD93f8C0/transactions) |
| **Council**    | [0x028933a66DD0cCC239a3d5c2243b2d96672f11F5](https://cchain.explorer.avax.network/address/0x028933a66DD0cCC239a3d5c2243b2d96672f11F5/transactions) |

### 2) Council

This contract is owned and controlled by a small group of trusted Snowball members. It is the owner of any incoming revenue and is a signer to the Treasury multisig contract.

**Council Address:** [0x028933a66DD0cCC239a3d5c2243b2d96672f11F5](https://cchain.explorer.avax.network/address/0x028933a66DD0cCC239a3d5c2243b2d96672f11F5/transactions)

| Signer                                                 | Address                                                                                                                                            |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| ****[**Big Wampa**](https://twitter.com/big_wampa)**** | [0xDFCCF13C19BfC6eD87FA238FF92236f86baA3F4a](https://cchain.explorer.avax.network/address/0xDFCCF13C19BfC6eD87FA238FF92236f86baA3F4a/transactions) |
| ****[**Leo**](https://twitter.com/Best_coder_NA)****   | [0x3B7631F8E3428dEaB77634BF799b622ce412e9Ea](https://cchain.explorer.avax.network/address/0x3B7631F8E3428dEaB77634BF799b622ce412e9Ea/transactions) |
| ****[**Brandon**](https://github.com/bmino)****        | [0xFd7b8597cF8eE5317439B0B5C55a111F6Eec449D](https://cchain.explorer.avax.network/address/0xFd7b8597cF8eE5317439B0B5C55a111F6Eec449D/transactions) |
| ****[**Bloomie**](https://twitter.com/BloomieBTC)****  | [0xA60c6091F06925DBd8344634806918D207d5F5c1](https://cchain.explorer.avax.network/address/0xA60c6091F06925DBd8344634806918D207d5F5c1/transactions) |
| ****[**Jonas**](https://twitter.com/cyberjenos)****    | [0xC99Ee029ebaeaf473eF69Aef6633489d9aE53385](https://cchain.explorer.avax.network/address/0xC99Ee029ebaeaf473eF69Aef6633489d9aE53385/transactions) |
| ****[**Jomari**](https://twitter.com/Jomari_P)****     | [0xF5f08Ba7F46e2a86b5ef3BFD56c2097C9f4276D7](https://cchain.explorer.avax.network/address/0xF5f08Ba7F46e2a86b5ef3BFD56c2097C9f4276D7/transactions) |

### 3) Payroll

This contract is owned and controlled by the founders of Snowball and is used for sending payments to other members of the Snowball team.

**Payroll Address:** [0x05faF04e3416e40Af70ecA1deEfe2E8B6feC3703](https://cchain.explorer.avax.network/address/0x05faF04e3416e40Af70ecA1deEfe2E8B6feC3703/transactions)

| Signer                                                                | Address                                                                                                                                            |
| --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**Big Wampa**](https://twitter.com/big_wampa)****                    | [0xdbc195a0ED72c0B059f8906e97a90636d2B6409F](https://cchain.explorer.avax.network/address/0xdbc195a0ED72c0B059f8906e97a90636d2B6409F/transactions) |
| ****[**Abominable Sasquatch**](https://twitter.com/abominablesas)**** | [0x6f6fA54d4c680Aa40077608592d59Dc1A306Baf6](https://cchain.explorer.avax.network/address/0x6f6fA54d4c680Aa40077608592d59Dc1A306Baf6/transactions) |
| ****[**8-Bit Giraffe**](https://twitter.com/8bitgiraffe\_)****        | [0x12e63004E314313607797e702C24491507329886](https://cchain.explorer.avax.network/address/0x12e63004E314313607797e702C24491507329886/transactions) |
