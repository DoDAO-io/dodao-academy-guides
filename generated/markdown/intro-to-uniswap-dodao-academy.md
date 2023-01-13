## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.

---

## Intro to Uniswap


## About Uniswap

### Introduction to Exchanges
Blockchain technology is penetrating each field of finance in the world. Most of the centralised systems are being replaced by their decentralised alternatives. Traditional Crypto Exchanges such as Bitstamp or Kraken are used for trading cryptocurrencies. They are centralised and are regulated by KYC laws. Users need to deposit money on the exchange and thereon the platform controls their funds. Users submit “Buy” or “Sell” orders which are listed on the order book and then exchange matches buyers with sellers. When these trades are done on a decentralised platform, it is known as DEX (Decentralised Exchange). One such popular DEX is Uniswap, built on Ethereum. It allows the trade of ERC – 20 tokens.

### Comparision of CEX and DEX
DEXs are a part of the DeFi ecosystem. Unlike traditional systems which require a controlling system and are deployed on centralised servers, DEX consist of smart contracts based on blockchain automatic rules deployed on independent servers. They are open to all and do not require any regulation or identification. There is no need to deposit funds on DEXs, they can be directly extracted from wallets. In the Traditional Systems as the number of buyers and sellers increases, the trade is said to be more “liquid”. In the lack of buyers and sellers, these exchanges have Market Makers ready to conduct transactions at all times. Whereas on a DEX, liquidity is created through Liquidity Pools. These pools are shared collections of funds deposited by the general public to fulfil buy/sell orders. People who deposit in Liquidity Pools are Liquidity Providers (LPs). In the exchange of locked funds, LPs receive fees known as Liquidity Mining.

### Working of Uniswap
In the Traditional system, when a buyer and seller agree on a price and then successful trade is conducted then this price is the price of the coin before the next trade. Uniswap has no order book and the price is determined using a mathematical formula that is known as Automated Market Maker. This AMM works on the Constant Market Maker Model to determine the exchange price: X * Y = K i.e. the number of X-type crypto times the number of Y-type cryptos equals constant. Hence in DEX price is determined by how much one wants to buy and not by how much someone gets for it. This model makes buying in large orders extremely expensive due to the high surge in price. Moreover in Uniswap, when carrying out the trade at the time the order is placed and when it is executed can be different due to congestion in the network. Thus this can lead to differences in price at the time of trade and execution. This difference is known as price slippage.

### Advantages of Uniswap
Uniswap enables its users with P2P (Peer-to-Peer) trading and provides them with rewards as well. It provides flexibility to its users that they can supply tokens to liquidity pools, create and list their own tokens (using the ERC-20 protocol ) or trade tokens. Currency Uniswap handles hundreds of tokens some of which include the most popular stablecoins like USDC and Wrapped Bitcoin.


Potential advantages of Uniswap (Decentralised Exchange) are:

1. `Safety`: Decentralised Exchanges are extremely secure because the funds are directly transferred from the wallets of the buyer and seller. These funds are never shared with a third party or are generally subject to counterparty risk.

2. `Globally accessible`: In the decentralised world there are no bounds or restrictions to anyone across the globe to access the benefits of Defi. Anyone with a smartphone and internet connection can use it.

3. `Pseudonymous`: No personal details or account signup is required to use these exchanges.

### UNI Token
Uniswap created the UNI token to promote community ownership over the protocol, letting stakeholders vote on important protocol modifications and development efforts. This was done after years of successful operation and on its way to complete decentralisation. In September 2020, Uniswap launched the token. As a novel distribution method, it "airdropped" 400 UNI tokens to every Ethereum address that had ever used the protocol. The airdrop, which was valued at over 250,000 Ethereum addresses and about $1,400 at the time, was distributed. Since then, airdrops have gained popularity as a method for DeFi apps to thank loyal customers; Uniswap has stated that it intends to give away a total of 1 billion UNI over a four-year period.


    


---
## Evaluation





##### UNI token is a type of ?  

- [ ]  Security Token
- [ ]  Payment Token
- [x]  Governance Token
- [ ]  Utility Token





##### Uniswap AMM employs which of the following AMM model ?  

- [ ]  Constant Sum Market Maker
- [x]  Constant Product Market Maker
- [ ]  Constant Mean Market Maker.
- [ ]  None of these

    


---
## Uniswap V3

### Version 1
Uniswap V1 allows traders on the Ethereum network to use a new system of trading called Automated Market Maker (AMM) to allow traders to trade with a pool of money at any point in time with very low fees and they can theoretically trade for an infinite amount of coins. This happens because Uniswap was created using smart contracts. Here to understand the AMM, for example, if traders spent $200 they would get 1ETH and the next time when again they spent $200 they get 0.8ETH because due to buying the price of the 1ETH went up. Other investors and traders deposit the money in the pool and then trade with this money.


One of the drawbacks of the V1 was that it had many Liquidity pools but all of the pools had to contain at least Ethereum. For example, the pool can comprise of USDC and Ethereum pair or a Basic Attention Token (BAT) and Ethereum pair. Now if a trader wanted to trade USDC against BAT, they need to interact with each of the pools hence extra work.

### Version 2
The issue of interacting with various pools in V1 was resolved in V2. In V2, one can create any pool they want. For example, one can have USDC and BAT pair liquidity pool. Uniswap became famous for this transformation and since then they have grown exponentially. This update made Uniswap the most forked project in the  DeFi space.

### Version 3

  #### Concentrated Liquidity
  Uniswap V3 was launched on March 2021, on the Ethereum Mainnnet and Optimism Mainnet (Secondary Network used to scale Ethereum). The big update in V3 is the concept of concentrated Liquidity. The basic advantage of concentrated liquidity is that one can make their money work harder by applying some rules to it. Generally, when an investor puts their money in the liquidity pool and this pool lets other traders trade back and forth in the same pool and the liquidity provider (the investor) collects some small fraction of fees for each trade. In V3, the investor chooses a certain price range where they want to concentrate their liquidity. For example, if the investor chooses the bracket of $3000-$4000 for the Ethereum pool it means they want to trade their assets only within this range of Ethereum, This concentrated liquidity provides better return rates compared to fairly distributed funds. However there is a disadvantage of Impermanent loss, but as long as the price range of Ethereum is within the range of the concentrated liquidity the investor earns better returns.

  #### Flexible Fees
  Uniswap V1 consisted only of flat fees of 0.3% and V2 had a 0.05% protocol fee which could be turned on/off. Whereas V3 onwards there is a three-tier fee structure:

  1. `0.05%`- predicted for stablecoin pools like DAI/USDC
  2. `0.30%`- for standard non-correlated pools like ETH/DAI
  3. `1.00%`- for exotic non-correlated pairs

  #### Advanced Oracles
  The TWAP (Time-weighted average price) oracles saw substantial advancements with Uniswap v3. As opposed to Uniswap v2, it stores an array of cumulative sums, making it feasible to calculate any recent TWAP within the last nine days with just one on-chain call.


  This enhancement makes it simpler and less expensive to produce more sophisticated oracles. According to the team, this will result in a 50% reduction in the cost of gas used to maintain oracles.


    


---
## Evaluation





##### Which of the following is the prime update in V3 ?  

- [ ]  Flexible Fees
- [x]  Concentrated Liquidity
- [ ]  Non-Fungible Liquidity
- [ ]  Active Liquidity





##### Which of the following three-tier fess structure is used in V3?  

- [ ]  0.05% for Non-correlated Pairs, 0.30% for DAI, 1.00% for ETH
- [ ]  0.05% for ETH, 1.00% for DAI, 0.30% for Non-correlated Pairs
- [x]  0.05% for DAI, 0.30% for ETH, 1.00% for Non-correlated Pairs
- [ ]  1.00% for DAI, 0.30% for foNon-correlated Pairs, 0.05% for ETH

    


---
## Uniswap for Liquidity Providers

Anyone who is able to furnish a Uniswap exchange contract with an equal amount of ETH and an ERC-20 token qualifies as a liquidity provider. They receive tokens from the exchange contract in exchange, which they may use at any moment to withdraw their share of the liquidity pool. A 0.3% fee is charged for each trade made on the exchange, and this fee is allocated to the liquidity pool. This has the effect of dividing the transaction cost proportionally among all current liquidity providers since no new liquidity tokens are created.


In fact, trades are not only guaranteed to happen when the price in the larger market changes, but liquidity providers also get paid from all deals. This is due to the fact that if the price on another exchange changes, the price difference between that exchange and Uniswap will present an arbitrage opportunity. Liquidity providers gain from Uniswap exchange fees when an arbitrageur performs the lucrative trade that returns the Uniswap exchange to parity with the larger market. Sure enough, arbitrageurs are hard at work to keep prices closely aligned with the rest of the market on all Uniswap exchanges with considerable liquidity.


    


---
## Evaluation





##### Uniswap LPs can face significant losses primarily due to -  

- [x]  Impermanent Loss
- [ ]  Arbitrage
- [ ]  The rising price of Ethereum
- [ ]  Declining use of Uniswap





##### Suppose in the ETH-USDC liquidity pool there are 79,180 Ethereum tokens and 134,457,994 USDC tokens, then the price of ETH will be ?  

- [ ]  $1500
- [ ]  $1000
- [ ]  $1200
- [x]  $1700

    


---
## Footer
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.
    
