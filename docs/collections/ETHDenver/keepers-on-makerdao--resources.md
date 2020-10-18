---
title: Keepers on MakerDAO  Resources 
summary: Github- https-//github.com/makerdao/developerguides/tree/master/keepers Keepers This document contains the necessary resources for partners to implement Keepers - programs that automatically monitor and interact with CDPs and the Dai Credit System. Prerequisites This document assumes familiarity with Ethereum, and in-depth knowledge of the Maker platform. Multi Collateral Dai (MCD) KeepersAuction Keeper The Auction Keeper program enables automatic interaction with CDP auctions - more specificall
authors:
  - David Utrobin (@davidutro)
date: 2019-02-06
some_url: 
---

# Keepers on MakerDAO  Resources 


## Github: [https://github.com/makerdao/developerguides/tree/master/keepers](https://github.com/makerdao/developerguides/tree/master/keepers)


## Keepers

This document contains the necessary resources for partners to implement Keepers - programs that automatically monitor and interact with CDPs and the Dai Credit System.


### Prerequisites

This document assumes familiarity with Ethereum, and in-depth knowledge of the Maker platform.


## Multi Collateral Dai (MCD) Keepers


### [Auction Keeper](https://github.com/makerdao/auction-keeper)

The Auction Keeper program enables automatic interaction with CDP auctions - more specifically flip (collateral sale), flap (MKR buy and burn), and flop (MKR minting). You can read more about the different auction types [here](https://github.com/makerdao/dss/wiki/Fuss).

This is automated by specifying bidding models that define the decision making process, such as when to bid, how high to bid etc.


## Single Collateral Dai (SCD) Keepers

For the current implementation of Dai (SCD) you can utilize the following reference keepers for automation of interactions with the Dai Credit System.


### [Pymaker](https://github.com/makerdao/pymaker)

Pymaker is a Python API which provides endpoints to interact with the Maker smart contracts. It exposes most of the functionality of the Maker platform, but most importantly for this guide it can be used to create Keepers - programs that monitor CDPs, and liquidates undercollateralized positions to buy the collateral for arbitraging opportunities.

Based on this, a series of reference Keepers have been developed to carry out specific operations in the Maker system.


### [Bite Keeper](https://github.com/makerdao/bite-keeper)

The Bite Keeper is a very simple implementation which continuously monitors the Dai Credit System for unsafe CDPs, and executes the bite function (liquidation) the moment they become unsafe. This Keeper does not guarantee that you are able to buy the bitten collateral, and thus does not take into account profitability of biting a certain CDP in terms of gas price vs buying collateral.


### [Arbitrage Keeper](https://github.com/makerdao/arbitrage-keeper)

The Arbitrage Keeper monitors arbitrage opportunities in the Dai Credit System by exchanging between the tokens of the system: DAI, WETH and PETH.


### [CDP Keeper](https://github.com/makerdao/cdp-keeper)

The CDP Keeper can be used to automatically manage CDPs. Features include:



*   Automatic top up of collateral, if collateral value decreases, and the CDP approaches the liquidation ratio
*   Wiping debt instead of top-up
*   Managing Dai volume


### Additional source code and developer docs

**Running a keeper node**



*   [https://github.com/makerdao/keeper-node](https://github.com/makerdao/keeper-node)

**Multi Collateral Dai**



*   Docs: [https://github.com/makerdao/dss/blob/master/DEVELOPING.md](https://github.com/makerdao/dss/blob/master/DEVELOPING.md)
*   Wiki: [https://github.com/makerdao/dss/wiki](https://github.com/makerdao/dss/wiki)
*   Source: [https://github.com/makerdao/dss](https://github.com/makerdao/dss)

**Current Dai credit system implementation (Single Collateral Dai)**



*   Docs: [https://developer.makerdao.com/dai/1/api/](https://developer.makerdao.com/dai/1/api/)
*   Docs: [https://github.com/makerdao/sai/blob/master/DEVELOPING.md](https://github.com/makerdao/sai/blob/master/DEVELOPING.md)
*   Source: [https://github.com/makerdao/sai](https://github.com/makerdao/sai)

**Maker platform in general**



*   [Whitepaper](https://makerdao.com/whitepaper/)


### Need help?

Contact integrate@makerdao.com or #dev channel on chat.makerdao.com



---

- **Kauri original title:** Keepers on MakerDAO  Resources 
- **Kauri original link:** https://kauri.io/keepers-on-makerdao:-resources/b5c74816b2034971aec5add073ae16c5/a
- **Kauri original author:** David Utrobin (@davidutro)
- **Kauri original Publication date:** 2019-02-06
- **Kauri original tags:** EthDenver
- **Kauri original hash:** QmbcNFM1kPbP12jjmjkUzb6fzM1wpNoGaChgnXn4LJ5hBr
- **Kauri original checkpoint:** QmZSRFGq9bnBLosiVwSTANrDR9YdXbWkwG71aw35jAjyLo



