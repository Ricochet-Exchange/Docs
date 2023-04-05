---
description: Ricochet Protocol's setup on Polygon for Protocol Developers
---

# ♾ Polygon Network

## Overview

There are contracts on Polygon set up for protocol developers to use for production applications.&#x20;

{% hint style="info" %}
**Interested in becoming a Ricochet Protocol Developer?** Try forking the ricochet-protocol repository on GitHub, clone it locally, and try to set up your environment so you can run the Hardhat tests. There's a bounty on Dework you can earn once you have gotten the tests to run successfully.&#x20;

Check it out now: [Run Protocol Tests Bounty](https://app.dework.xyz/ricochet-exchange-da/onboarding-78105?taskId=1599166b-2ad6-491f-9c50-3b665630123d)
{% endhint %}

{% embed url="https://github.com/Ricochet-Exchange/ricochet-protocol" %}
Check out the Ricochet Protocol repository on Github
{% endembed %}

## REX Contracts

| Contract                | Optimism Contract Address                  |
| ----------------------- | ------------------------------------------ |
| Ricochet DAO Multisig   | 0x9C6B5FdC145912dfe6eE13A667aF3C5Eb07CbB89 |
| Ricochet (RIC) Token    | 0x263026e7e53dbfdce5ae55ade22493f828922965 |
| rexSHIRT Token          | 0x19cA69C66768B487D28226C0a60Ab2B2aa8E5c5C |
| rexHAT Token            | 0xe91D640fCAEA9602CF94C0d48A251a7f6d946953 |
| RIC Launchpad           | 0x98d463A3F29F259E67176482eB15107F364c7E18 |
| REX Referral            | 0xA0eC9E1542485700110688b3e6FbebBDf23cd901 |
| REX Market: USDC>>DAI   | 0x8f8E389Fa66e439EE98f4f2d71104ad993190983 |
| REX Market: DAI>>USDC   | 0x21140427F2e32C801FA8AAC2A352e85a9e23847b |
| REX Market: USDC>>ETH   | 0x2D482F552eC3F770b3eF67833D61723CB2c745b3 |
| REX Market: ETH>>USDC   | :construction:                             |
| REX Market: DAI>>ETH    | :construction:                             |
| REX Market: ETH>>DAI    | :construction:                             |
| REX Market: USDC>>WBTC  | :construction:                             |
| REX Market: WBTC>>USDC  | :construction:                             |
| REX Market: DAI>>WBTC   | :construction:                             |
| REX Market: WBTC>>DAI   | :construction:                             |
| REX Market: USDC>>MATIC | :construction:                             |
| REX Market: MATIC>>USDC | :construction:                             |
| REX Market: DAI>>MATIC  | :construction:                             |
| REX Market: MATIC>>DAI  | :construction:                             |

## Super Tokens

Superfluid curates tokens on Mumbai for testing. Ricochet needs to make a Uniswap Liquidity Pool with these tokens so that the REX Market contracts have a pool to use. This table explains what tokens are available:

| Token | Optimism Address                           |
| ----- | ------------------------------------------ |
| USDC  | 0x7F5c764cBc14f9669B88837ca1490cCa17c31607 |
| USDCx | 0x8430f084b939208e2eded1584889c9a66b90562f |
| DAI   | 0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1 |
| DAIx  | 0x7d342726b69c28d942ad8bfe6ac81b972349d524 |
| ETH   | Native Network Token                       |
| ETHx  | 0x4ac8bd1bdae47beef2d1c6aa62229509b962aa0d |

{% hint style="info" %}
A full list of Supertoken contract addresses can be found here: [Supertoken Contract Addresses](https://docs.superfluid.finance/superfluid/developers/networks#test-networks)
{% endhint %}
