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

## Tokens

Superfluid curates tokens on Mumbai for testing. Ricochet needs to make a Uniswap Liquidity Pool with these tokens so that the REX Marekt contracts have a pool to use. This table explains what tokens are available:

| Token        | Token                                      | Supertoken                                 |
| ------------ | ------------------------------------------ | ------------------------------------------ |
| fUSDC/fUSDCx | 0xbe49ac1EadAc65dccf204D4Df81d650B50122aB2 | 0x42bb40bF79730451B11f6De1CbA222F17b87Afd7 |
| fDAI/fDAIx   | 0x15F0Ca26781C3852f8166eD2ebce5D18265cceb7 | 0x5D8B4C2554aeB7e86F387B4d6c00Ac33499Ed01f |

{% hint style="info" %}
You can **mint any amount of fDAI and fUSDC** using mumbai.polygonscan.com. If you need these tokens for testing, then use this method of minting by connecting to mumbai.polygonscan.com.
{% endhint %}

{% hint style="info" %}
A full list of Supertoken contract addresses can be found here: [Supertoken Contract Addresses](https://docs.superfluid.finance/superfluid/developers/networks#test-networks)
{% endhint %}

## Liquidity Pool

There is a UniswapV3 Liquidity Pool for fDAI/fUSDC for testing the REX Market's on testnet. Use https://app.uniswap.org to access the swap, you can find contract details in the table below.

<figure><img src="../.gitbook/assets/Screen Shot 2023-03-19 at 11.27.52 AM.png" alt=""><figcaption><p>The exchange rate on Mumbai Testnet will not always be 1:1 like shown above.</p></figcaption></figure>

{% hint style="warning" %}
You may need to add fDAI and fUSDC using the contract addresses in the table above. fDAI and fUSDC may or may not show up if you have them in your wallet.
{% endhint %}

{% hint style="info" %}
**Uniswap Contract Addresses:** The contract address you may need for developing with UniswapV3 can be found here: [Uniswap Deployment Addresses](https://docs.uniswap.org/contracts/v3/reference/deployments)
{% endhint %}

