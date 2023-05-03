---
description: This explains protocol fees on the platform in a clear way
---

# 📊 Fees

## Protocols' Fees Table

This table shows the breakdown of fees taken on from during the swap and distribute steps in the protocol. Uniswap and [Gelato](https://gelato.network/) each take a fee for their use. [Uniswap](https://uniswap.org/) Automated Market Maker fees are paid to Liquidity Providers. Gelato Network is paid a fee as a reimbursement for gas used to execute the transaction.&#x20;

| Markets                                                                                                                                                                                                                        | Net Fee                                        | Protocol Fee                                  | Other Protocol Fees                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- | --------------------------------------------- | ----------------------------------------------------------------------------------- |
| <p><strong>Polygon:</strong><br>USDC>>ETH<br>USDC>>WBTC<br>USDC>>MATIC<br>DAI>>ETH<br>DAI>>WBTC<br>DAI>>MATIC<br><br><strong>Optimism:</strong><br>USDC>>ETH<br>USDC>>WBTC<br>USDC>>OP<br>DAI>>ETH<br>DAI>>WBTC<br>DAI>>OP</p> | <p>1.55%<br>(Protocol  + Uniswap + Gelato)</p> | 0.5% of the output distributed after the swap | <p>0.05% fee from Uniswap V3<br><br>1% of the input amount for Gelato execution</p> |

{% hint style="danger" %}
Ricochet Exchange is a management application for decentralized finance protocols that run on Polygon, including but not limited to Superfluid, Uniswap, Gelato, Chainlink, SushiSwap, and Quickswap. Ricochet Exchange is not affiliated with companies or teams behind these protocols and we can make no guarantees regarding their stability or security.&#x20;

Additionally, there are no guarantees regarding the safety of funds that have been in any way used within Ricochet Exchange contracts. We cannot compensate users for funds that have been lost during use within Ricochet Exchange or that have at any point in time been used within Ricochet Exchange. By using Ricochet Exchange you agree to these terms and acknowledge that you are aware of the existing risk and knowingly accept it.
{% endhint %}

### Fee Reductions

The Gelato fee can be reduced from the current 1% down to a lower limit of 0.01% (_1 basis point_). The fee can be lowered by the DAO after markets execute with a frequency less than 4 hours. Swaps less than every 4 hours is not going to make much of a difference relative to other DCA protocols. Some markets may have Gelato fees lower than 1%, this is the case for the USDC>>ETH.

### Version 2.0 Protocol Fee Table

| Markets                                                                                          | Protocol Fee                    | Other Protocol                    |
| ------------------------------------------------------------------------------------------------ | ------------------------------- | --------------------------------- |
| <p>USDC&#x3C;>ETH<br>USDC&#x3C;>WBTC<br>USDC&#x3C;>MATIC<br>DAI&#x3C;>ETH<br>DAI&#x3C;>MATIC</p> | 2% of the output distributed    | 0.3% fee from Sushiswap/Quickswap |
| <p>ibAlluoUSD&#x3C;>ibAlluoETH<br>ibAlluoUSD&#x3C;>ibAlluoBTC</p>                                | 0.5% of the output distributed  | 0.3% fee from Sushiswap/Quickswap |

## Referral Program Fees

{% content-ref url="../contributor-resources/affiliates.md" %}
[affiliates.md](../contributor-resources/affiliates.md)
{% endcontent-ref %}

The Ricochet Exchange protocol has a built in Referral System (REX Referral contract). Accounts can register as an affiliate through this contract. As an affiliate they can refer accounts using a link to the frontend application. Fees are then split 50/50 with the affiliate.&#x20;

The protocol takes no more and no less fees on accounts referred by the affiliate. All accounts interacting with Ricochet get the same fee, set at the smart contract level.&#x20;

| Protocol Fee distribution for referrals | Fee Share |
| --------------------------------------- | --------- |
| REX Registered Affiliate Account        | 50%       |
| Protocol Fee Collector Account          | 50%       |
