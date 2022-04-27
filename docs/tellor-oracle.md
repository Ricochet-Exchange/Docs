---
description: Protecting our swaps with external pricing data
---

# 🧙♂ - Tellor Oracle

## What is Tellor?

Tellor is an oracle system where parties can request the value of an off-chain data point (e.g. BTC/USD) and miners compete to add this value to an on-chain data-bank, accessible by all Ethereum smart contracts.  The inputs to this data-bank are secured by a network of staked miners. Tellor utilizes crypto-economic incentive mechanisms, rewarding honest data submissions by miners and punishing bad actors, through the issuance of Tellor’s token, Tributes (TRB) and a dispute mechanism. [\[1\]](https://docs.tellor.io/tellor/whitepaper/introduction)

![](../.gitbook/assets/tellor\_infographics2\_Median\_DEF\_CROPPED.png)

Prices are submitted to the Tellor Smart Contract by a decentralized network of reporters. Tellor SC takes the median value of the prices submitted and stores it in the data-bank.



## How does Ricochet Exchange use Tellor?

Ricochet Exchange uses Tellor's on-chain data-bank to get the current value of the assets listed. Prices are submitted to Tellor by the decentralized network of price reporters.&#x20;

The price provided by Tellor protects Ricochet Exchange against slippage while swapping on other DEXes like SushiSwap or QuickSwap. The snippet below shows how the price is pulled from Tellor's data-bank and used to protect the swaps:

```javascript
// The amount of USDC to swap
uint amount = usdc.balanceOf(address(this));

// Tellor Request ID for WBTC/USD price
uint wbtcRequestId = 60; 

// _value is WBTC/USDC price scaled up by 1e6
(, _value, ) = tellor.getCurrentValue(wbtcRequestId);

// Use Tellor value to get a minOutput amount
uint minOutput = amount * 1e18 / _value / 1e12;

// Accept any outputAmount but will fail if exchange rate is 
// too far from the oracle price
sushiRouter.swapExactTokensForTokens(
    amount,
    0, 
    path,
    address(this),
    deadline
);

// See how much WBTC we got now
outputAmount = wbtc.balanceOf(address(this));

// If we receive less than the minOutput amount then revert
require(outputAmount >= minOutput, "BAD_EXCHANGE_RATE: Try again later");  
```

