---
description: Overview of the REX Version 2.0 Contracts
---

# 🦖 - REX Contracts

{% hint style="warning" %}
This technical documentation is for Ricochet Exchange's Version 2.0 contracts which are currently under development. Find the work in progress on these contracts here: [https://github.com/Ricochet-Exchange/ricochet-protocol](https://github.com/Ricochet-Exchange/ricochet-protocol)
{% endhint %}

Ricochet Exchange (REX) contracts power the backend of Ricochet's products and services. This page gives an overview of the contract architecture. This is written for blockchain engineers interested in integrating with REX as well as strategists interested in extending the base contracts to create new strategies for how exchanges work.

### Architecture

#### `REXMarket` Contract

REX Markets support Ricochet Exchanges (i.e. stream exchange). They contain these basic methods which are triggered by keeper:

* `distribute` - converts tokens and distributes them to holders
* `claim` - accumulated fees can be claimed by the DAO
* `harvest` (optional)- aggregates yield, called separately from `distribute` to save gas

Internally, REX Market Contract keeps track of oracle price feeds and the output tokens. A REX Market may support many output tokens (subsidy tokens, tokens acquired from yield aggregation). Below is a topology diagram highlighting the internal structures within a REX Market:

![](<../.gitbook/assets/Screen Shot 2021-12-13 at 9.12.17 AM.png>)

* **`REXMarketBase`** contains two internal structures: `OracleInfo`, `OutputPool`
* **`Oracles`** is a `mapping(token => OracleInfo)`, each oracle price is updated independently
* **`OutputPools`** is a `mapping(uint => OutputPool)` (probably needs to become linked list)
  * If `feeRate != 0` then output token
  * If `emissionRate != 0` then subsidy token

#### Integrating with REX Markets&#x20;

REX contracts follow a similar pattern to Yearn or Pickle finance where a base contract is extended and customized for each new strategy. REX has the following hierachy:

* **`REXMarket`** - Contains the basic functionality shared by all markets
  * **`REXSushiFarmMarket`** - Extends basic functionality to support yield aggregating from Sushiswap Farms
  * **`REXStakeDAOFarmMarket`** - Extends basic functionality to support yield aggregating from StakeDAO LP Farms
  * **`REXLaunchpad`** - Supports streaming ICOs where the input is sent to a benificiary in exchange for a token that is held by the contract

Below is a graphical representation of the hierarchy:

![](<../.gitbook/assets/Screen Shot 2021-12-13 at 9.05.17 AM.png>)

####

