---
description: How does Ricochet leverage Superfluid's real-time finance rails?
---

# 🚿 - Superfluid

## Super Tokens

When you upgrade your ERC20 tokens in order to start streaming with them, you're wrapping them into Super Tokens, an ERC777 version of the token which gains Superfluid capability. Super Tokens can be downgraded (unwrapped) into their original ERC20 form.

Super Tokens are denoted by {Original Ticker}x, so **SUSHI** as a  Super Token would be denoted as **SUSHIx**.

[Example of an upgrade transaction](https://polygonscan.com/tx/0x1c257f0efdef0807a1ecbcf60ae5d7d07324f816229d8fe579199c357110d2b3)\
_DAI sent to DAIx Super Token contract (wrapping), same amount of DAIx minted to caller_

__[Example of a downgrade transaction](https://polygonscan.com/tx/0x24bb66591e36f4095c4f01c09ba946194bb5ce44691d19ae4822d9f3a8530992)\
_DAIx burned, DAI sent from DAIx Super Token contract to caller (unwrapping)_

#### Where we use:

If a user were to stream their DAI into the DAI>>ETH market, they would have to upgrade their DAI to DAIx to begin streaming. The ETHx that's distributed back to them would have to be downgraded to be converted to plain ETH.

## Constant Flow Agreement (CFA)

When you open a stream to an address, you're entering into a Constant Flow Agreement. You are agreeing to transfer a specified Super Token to a specified destination at a constant per second rate (in our app, we have users choose their number per month because it's simpler). The created stream can be updated and cancelled as the stream initiator pleases.&#x20;

**Note:** Once the user's Super Token balance runs out, the stream automatically closes!

More info: [https://docs.superfluid.finance/superfluid/docs/constant-flow-agreement](https://docs.superfluid.finance/superfluid/docs/constant-flow-agreement)

#### Where we use:

When you hit "Start" and begin streaming, you are entering into a Constant Flow Agreement with our Super App.

## Super App

A Super App is a smart contract that can manage agreements and respond to occurrences within them. It contains custom logic/behaviour where the contract can respond to things like stream initiation, updates, and perform its own CFAs and distributions

![](<../.gitbook/assets/image (1) (1).png>)

#### Where we use:

When a new stream is opened to the Ricochet Super App, a proportional amount of distribution "shares" are assigned to the stream initiator.\
\
The Ricochet Super App accumulates incoming Super Tokens. When "[distribute](https://github.com/mikeghen/ricochet/blob/main/01-Contracts/contracts/StreamExchangeHelper.sol#L50)" is called, the Super App takes the accumulation to SushiSwap where it's swapped to the desired token. \
\
That proportional amounts of the desired token are distributed to all stream initiators to the Super App in accordance to their shares owned _at once_ using a special agreement called an [Instant Distribution](https://docs.superfluid.finance/superfluid/protocol-tutorials/perform-an-instant-distribution).

## Security Deposit & Liquidation

When you start a stream, the Superfluid protocol takes a "security deposit" worth 4 hours of your stream rate.

So, let's say you start a stream to a Stream Market at 1000 DAIx/month.

```
Security Deposit = 4 * ( Monthly Stream Rate / (30 * 24) )
                 = 4 * ( 1000 / (30 * 24) )
                 = 5.56 DAIx
```

You must put down a security deposit of \~5.56 DAIx&#x20;

* If you let your DAIx balance fall to zero, then you will lose that deposit.&#x20;
* If you cancel your stream before your DAIx balance hits zero, then you recover the deposit
