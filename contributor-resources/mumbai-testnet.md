---
description: Ricochet Protocol's setup on Mumbai for Protocol Developers
---

# 🧪 Mumbai Testnet

## Overview

There are contracts on Mumbai Testnet set up for protocol developers to use for testing. This document explains what's available and why it's there. This document is for protocol developers.

{% hint style="info" %}
**Interested in becoming a Ricochet Protocol Developer?** Try forking the ricochet-protocol repository on GitHub, clone it locally, and try to set up your environment so you can run the Hardhat tests. There's a bounty on Dework you can earn once you have gotten the tests to run successfully.&#x20;

Check it out now: [Run Protocol Tests Bounty](https://app.dework.xyz/ricochet-exchange-da/onboarding-78105?taskId=1599166b-2ad6-491f-9c50-3b665630123d)
{% endhint %}

{% embed url="https://github.com/Ricochet-Exchange/ricochet-protocol" %}
Check out the Ricochet Protocol repository on Github
{% endembed %}

## REX Contracts

| Contract                | Mumbai Contract Address                    |
| ----------------------- | ------------------------------------------ |
| Ricochet DAO Multisig   | 0x9d7254F07b4De4643B409B5971eE2888E279417F |
| Ricochet (RIC) Token    | 0xDCf9273075A29F0070d5cB4632814367CE4350aE |
| RIC Launchpad           | 0xd6cf77c9bc69181ab859b5fc963d769cf2e2c2af |
| REX Referral            | 0x24239b083143759C8920Ba56d76Be36CD70DE490 |
| REX Market: fUSDC>>fDAI | 0x4fb7309f1e000d40c0eb074cd5579e14386c1b77 |
| REX Market: fDAI>>fUSDC | 0xd3b6767173fe6c9d60938713bb7578fbab80947e |
| rexSHIRT Token          | 0x3997918224f980FF933f8922d1aCcc26463eD702 |
| rexHAT Token            | 0xea3003b77f1c36318Ac50069Fc33D1793Ce416b9 |

## Tokens

Superfluid curates tokens on Mumbai for testing. Ricochet needs to make a Uniswap Liquidity Pool with these tokens so that the REX Market contracts have a pool to use. This table explains what tokens are available:

| Token                   | Token                                      | Supertoken                                 |
| ----------------------- | ------------------------------------------ | ------------------------------------------ |
| <p>fUSDC <br>fUSDCx</p> | 0xbe49ac1EadAc65dccf204D4Df81d650B50122aB2 | 0x42bb40bF79730451B11f6De1CbA222F17b87Afd7 |
| <p>fDAI<br>fDAIx</p>    | 0x15F0Ca26781C3852f8166eD2ebce5D18265cceb7 | 0x5D8B4C2554aeB7e86F387B4d6c00Ac33499Ed01f |

{% hint style="info" %}
You can **mint any amount of fDAI and fUSDC** using mumbai.polygonscan.com. If you need these tokens for testing, then use this method of minting by connecting to mumbai.polygonscan.com.
{% endhint %}

{% hint style="info" %}
A full list of Supertoken contract addresses can be found here: [Supertoken Contract Addresses](https://docs.superfluid.finance/superfluid/developers/networks#test-networks)
{% endhint %}

## Liquidity Pools

There is a UniswapV3 Liquidity Pool for fDAI-fUSDC for testing the REX Market's on testnet. There's also fDAI-MATIC and fUSDC-MATIC  pools to support Gelato transaction pays for itself. Use https://app.uniswap.org to access the swap, you can find contract details in the table below.&#x20;

| Uniswap V3 Pair | Pool Fee |
| --------------- | -------- |
| fUSDC-fDAI      | 0.05%    |
| fUSDC-MATIC     | 0.05%    |
| fDAI-MATIC      | 0.05%    |

<figure><img src="../.gitbook/assets/Screen Shot 2023-03-19 at 11.27.52 AM.png" alt=""><figcaption><p>The exchange rate on Mumbai Testnet will not always be 1:1 like shown above.</p></figcaption></figure>

{% hint style="warning" %}
You may need to add fDAI and fUSDC using the contract addresses in the table above. fDAI and fUSDC may or may not show up if you have them in your wallet.
{% endhint %}

{% hint style="info" %}
**Uniswap Contract Addresses:** The contract address you may need for developing with UniswapV3 can be found here: [Uniswap Deployment Addresses](https://docs.uniswap.org/contracts/v3/reference/deployments)
{% endhint %}

