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

| Contract               | Optimism Contract Address                  |
| ---------------------- | ------------------------------------------ |
| Ricochet DAO Multisig  | 0x8e38Be5c136B3f7f05aD570c2996e43733418C4a |
| Ricochet (RIC) Token   | 0x7abd51A15668308D3b42Cc1F6148Be8bdE939568 |
| rexSHIRT Token         | 0x0942570634A80bcd096873afC9b112A900492fd7 |
| rexHAT Token           | 0xBaB5fF73925a1C205F8b2565B225AbF55c5D68a9 |
| RIC Launchpad          | 0x5c2e1a331678e1a9c6f8c156b5d48a5cc7e50cda |
| REX Referral           | 0xC79255821DA1edf8E1a8870ED5cED9099bf2eAAA |
| REX Market: USDC>>DAI  | 0xd16DAc3C32498D231eA80a1D93Aea7A016762b91 |
| REX Market: DAI>>USDC  | 0x5f4919B2ed93b7d0Ae686d42AA8A94d372640F78 |
| REX Market: USDC>>OP   | 0x9e5d41aab1Db526eBb74e393A0D3bEa25E7583ed |
| REX Market: DAI>>OP    | 0x6Cdd465096dC77E4184003c44b727877Db224a9D |
| REX Market: OP>>USDC   | 0xD139afb20e3c98472C82a992B6B1548280C41d3b |
| REX Market: OP>>DAI    | 0xD245e7D9301D73247939baF954A17fDf49d0D7ff |
| REX Market: USDC>>ETH  | 0xbabc9f466f87e1957b6732d333da2209ed80ef79 |
| REX Market: DAI>>ETH   | 0x091196943555d3e1513F7775ffA6b5779d3DefE9 |
| REX Market: USDC>>WBTC | 0x51b398BCe9d0D6619a2c9CFb4C6BbBB97A76eD49 |
| REX Market: DAI>>WBTC  | 0x91562e9163Da2a33241f4d6e2D5924a73D9dB24e |
| REX Market: WBTC>>USDC | 0x151F234140Ca257d3F8751D8982792c0A1576361 |
| REX Market: WBTC>>DAI  | 0xBd858C9e3a264a66609a7726A87A1DaFA4D4628D |

## Super Tokens

Superfluid curates tokens on Mumbai for testing. Ricochet needs to make a Uniswap Liquidity Pool with these tokens so that the REX Market contracts have a pool to use. This table explains what tokens are available:

| Token | Optimism Address                           |
| ----- | ------------------------------------------ |
| USDC  | 0x7F5c764cBc14f9669B88837ca1490cCa17c31607 |
| USDCx | 0x8430f084b939208e2eded1584889c9a66b90562f |
| DAI   | 0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1 |
| DAIx  | 0x7d342726b69c28d942ad8bfe6ac81b972349d524 |
| WBTC  | 0x68f180fcCe6836688e9084f035309E29Bf0A2095 |
| WBTCx | 0x9638EC1D29dfA9835fdb7fa74B5B77B14d6Ac77e |
| ETH   | Native Network Token                       |
| ETHx  | 0x4ac8bd1bdae47beef2d1c6aa62229509b962aa0d |

{% hint style="info" %}
A full list of Supertoken contract addresses can be found here: [Supertoken Contract Addresses](https://docs.superfluid.finance/superfluid/developers/networks#test-networks)
{% endhint %}
