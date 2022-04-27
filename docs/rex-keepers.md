---
description: A network of Keepers support Ricochet Exchange
---

# 🤖 - REX Keepers

## **Overview**

Ricochet Exchange requires keepers help with distributions/harvests and provide other services to streams on our platform. These documents outline how to set up a keeper.&#x20;

Repository

{% embed url="https://github.com/Ricochet-Exchange/ricochet-keeper" %}
Find the code for the REX keeper in Github
{% endembed %}

## **System Requirements**

* Virtual machine with&#x20;
  * \>4 GB of memory
  * a network connection (e.g. Digital Ocean Droplet)
* Four (4) funded Polygon wallets
  * You'll need to have the public address and private key for these wallets
  * Each wallet should be different to avoid collisions with nonces across workflows

## Keeper Workflows

This is a list that details the workflows that are run by the REX Keeper:

* **`ricochet_distribute`** - Periodically distributes for each REX Market
* **`ricochet_harvest`** - Periodically harvests yield from REX markets that support yield aggregation
* **`ricochet_tellor_reporter`** - Reports the price to the Tellor oracle
* **`ricochet_stream_closure`** - Checks on streamers balances, close before they run out

## Getting Started

Read the setup instructions in the REX Keeper repo:&#x20;

{% embed url="https://github.com/Ricochet-Exchange/ricochet-keeper" %}

