---
description: Ricochet Protocol's setup on Optimism for Protocol Developers
---

# 🅾 Optimism Network

## Overview

There are contracts on Optimism set up for protocol developers to use for production applications.&#x20;

{% hint style="info" %}
**Interested in becoming a Ricochet Protocol Developer?** Try forking the ricochet-protocol repository on GitHub, clone it locally, and try to set up your environment so you can run the Hardhat tests. There's a bounty on Dework you can earn once you have gotten the tests to run successfully.&#x20;

Check it out now: [Run Protocol Tests Bounty](https://app.dework.xyz/ricochet-exchange-da/onboarding-78105?taskId=1599166b-2ad6-491f-9c50-3b665630123d)
{% endhint %}

{% embed url="https://github.com/Ricochet-Exchange/ricochet-protocol" %}
Check out the Ricochet Protocol repository on Github
{% endembed %}

## REX Contracts

| Contract              | Optimism Contract Address                  |
| --------------------- | ------------------------------------------ |
| Ricochet DAO Multisig | 0x8e38Be5c136B3f7f05aD570c2996e43733418C4a |
| Ricochet (RIC) Token  | 0x7abd51A15668308D3b42Cc1F6148Be8bdE939568 |
| rexSHIRT Token        | 0x0942570634A80bcd096873afC9b112A900492fd7 |
| rexHAT Token          | 0xBaB5fF73925a1C205F8b2565B225AbF55c5D68a9 |
| RIC Launchpad         | 0x5c2e1a331678e1a9c6f8c156b5d48a5cc7e50cda |
| REX Referral          | 0xC79255821DA1edf8E1a8870ED5cED9099bf2eAAA |
| REX Market: USDC>>DAI | 0x0d98B7D4f19A585296b330C538b7316351677A79 |
| REX Market: DAI>>USDC | :construction:                             |
| REX Market: DAI>>ETH  | :construction:                             |
| REX Market: USDC>>ETH | :construction:                             |

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
