# Beaker Finance Documentation
<p align="center"> 
    <img 
        src="https://user-images.githubusercontent.com/8098163/159962500-ed6b6459-747b-4cc7-bc2a-cb9c319ac96a.png" 
        alt="beaker finance documentation" 
        height="70%"
        width="100%">
</p>

## Protocol Overview
[Beaker Finance](https://twitter.com/beakerfinance) is a decentralized financial protocol created by [Greenwood Labs](https://twitter.com/GreenwoodLabs). With Beakers, you can buy fractions of DeFi trades that were created by other people, giving you a faster and cheaper alternative to doing trades alone. Beakers are designed to make decentralized finance a group activity and help traders build a diverse portfolio without the effort or expense of doing trades on their own.

## Motivation
The development of Beaker Finance was motivated by the desire to make decentralized finance more social and simpler to use. Beakers exist to permissionlessly wrap arbitrary code representing financial exposure into a single token that you can trade on a DEX, reducing the cost and complexity of using DeFi and giving people a vehicle to crowdfund trades with their frens and famiglia.

## How it Works

### Creating a Beaker
* The Beaker deployer structures the Beaker, deciding how much AVAX to raise, what transactions to execute upon reaching the fundraising goal, the initial buyout price, and the minimum buyout price.
* The Beaker is "initialized", beginning the fundraising period.
* Contributors contribute AVAX in exchange for an allocation of Beaker LP (BLP) tokens proportional to their contribution.
* After the fundraising period ends the Beaker is "finalized" or contributors are refunded.
    * If the fundraising goal is reached the Beaker can be "finalized", triggering execution of the transactions specified by the Beaker deployer.
    * If the fundraising goal is not reached, contributors can claim an AVAX refund.
* Finalization triggers predefined arbitrary code execution. Beaker deployers can structure the exposure of a Beaker by calling any function on any smart contract.
* Contributors can claim their BLP tokens after contract finalization. 

<p align="center"> 
    <img 
        src="https://user-images.githubusercontent.com/8098163/159964111-81e9bf0d-7b03-4c59-aac4-ffc0f62a2a24.png" 
        alt="creating a beaker" 
        height="70%"
        width="100%">
</p>

### Trading Beaker LP Tokens
* BLP tokens can be traded on decentralized exchanges or over the counter.
     * BLP tokens implement the ERC20 token standard, so they can be traded on decentralized exchanges.
     * BLP tokens can be traded over the counter via the `submitBlockTrade()` function. Anyone can submit an offer to buy BLP tokens at a given price by calling `submitBlockTrade()` and transferring AVAX into the Escrow contract. BLP token holders can choose to accept a block trade price for a portion, or all, of their BLP tokens. Accepting a block trade sends AVAX to the BLP token holder and transfers the BLP tokens to the buyer.
     * The price of a block trade is how much the buyer believes all outstanding BLP tokens for a given Beaker are worth.
     * Anyone may submit a block trade and the block trade with the highest value is always offered to BLP token holders.

<p align="center"> 
    <img 
        src="https://user-images.githubusercontent.com/8098163/159964775-8d9a4943-7a49-4629-81a5-96927354b1a0.png" 
        alt="trading beakers" 
        height="70%"
        width="100%">
</p>

### Beaker Buyouts
* The Beaker deployer sets the initial buyout price and the minimum buyout price (the lowest amount the Beaker can ever be bought out for).
* BLP token holders can continuously vote on a desired buyout price. The weighted average of this vote decides on the price needed to force a buyout once a quorum of BLP token holders have voted. Until a quorum of BLP token holders have voted the initial buyout price set by the Beaker deployer is the buyout price of the Beaker.
* Anyone can submit an offer to buyout all outstanding BLP tokens for a given Beaker by calling `submitBuyout()` and transferring AVAX into the Escrow contract. If the buyout offer is valid, the buyer is granted the ability to execute arbitrary code from the Beaker contract and BLP tokens no longer represent frations of the assets held by the Beaker. 
* A BLP token holder's proportion of the buyout can be claimed from the Escrow by calling `acceptBuyout()`.

<p align="center"> 
    <img 
        src="https://user-images.githubusercontent.com/8098163/159964892-0ccc3cec-4c38-4a7a-a487-a5f0a5279c77.png" 
        alt="beaker buyouts" 
        height="70%"
        width="100%">
</p>

## Deployed Contracts

#### Avalanche
|Contract Name|Address|Block Explorer|
|-|-|-|
|Escrow|Coming soon|[View on Snowtrace](https://snowtrace.io/address/0x0)|
|Factory|Coming soon|[View on Snowtrace](https://snowtrace.io/address/0x0)|
|BeakerImplementation|Coming soon|[View on Snowtrace](https://snowtrace.io/address/0x0)|

## Disclaimer
This software is unaudited and is provided on an "as is" and "as available" basis. If you choose to interact with these smart contracts, please do so with the understanding that your assets are at risk of being lost. This software is meant only for demonstration purposes, we do not give any warranties and will not be liable for any loss incurred through any use of this codebase.
