## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.

---

## Intro to Curve


## About Curve


## Curve Intro
Curve is a popular decentralized automated market maker focused on stablecoin swaps that helps you efficiently invest and exchange tokens from various pools. Yes, it is one of the largest non-custodial decentralized exchanges with one of the highest assets in Total Value Locked (TVL). It has low gas fees and also overcomes the problem of slippage by creating pools of similarly behaving assets.Staker’s funds are liquid, meaning that they can be used in other secondary markets. This is a major benefit when compared to other liquidity providers. Curve Finance is by far the most advanced and reliable automated market maker (AMM) for stablecoins and wrapped tokens. It provides users with the ability to trade these assets without having to worry about the volatility of the markets. 

Curve's StableSwap invariant allows for significantly more efficient and stable stablecoin trades than many other prominent invariants, such as the constant-product invariant. Keep in mind that when we refer to stablecoins in this context, we're talking about tokens that are stable representations of one another. This includes USD-pegged stablecoins like DAI and USDC, but also ETH and sETH (synthetic ETH) or different versions of wrapped BTC.
## Curve Pools

Curve pools are designed to allow the exchange of two or more tokens while maintaining the StableSwap invariant. There are three main types of Curve pools:

**Plain pools**: these pools pair two or more stablecoins against each other.

**Lending pools**: these pools pair two or more wrapped tokens (e.g., cDAI) against each other, while the underlying is lent out on some other protocol.

**Metapools**: these pools pair a stablecoin against the LP token from another pool.

Depositing coins into a Curve pool allows liquidity providers to receive pool-specific LP tokens, which are ERC20 contracts. These tokens are transferable, so holders of the LP tokens can stake them into a pool's liquidity gauge to receive CRV token rewards. If the LP token is supported by a metapool, it can be deposited into the metapool in exchange for the metapool's LP token.

    

## Liquidity Providers

Liquidity providers are people who deposit tokens in liquidity pools. Liquidity pools are like reservoirs for tokens that help create exchange liquidity. Traders swap tokens within the liquidity pool, which in turn creates buy and sell pressures that help determine token prices. AMM algorithms work to efficiently price the tokens in the liquidity pool according to various factors, such as buy and sell pressures driven by traders. This system helps to create a more stable environment for tokens, which is beneficial for both traders and liquidity providers. Liquidity providers in return get a cut of trading fees and other boosted rewards.         

    


---
## Evaluation





##### How does curve finance overcome the problem of slippage that occurs due to volatality, while order being executed ?  

- [ ]  Through bribes
- [x]  By creating pools of similarly behaving assets
- [ ]  By Automated Market Maker (AMM)
- [ ]  By creating tripool





##### How is the price of token in liquidity pool decided?  

- [ ]  By veCRV voting
- [x]  Through AMM alorithm
- [x]  Through buy and sell pressure
- [ ]  Through gauge weight of that particular pool of token.

    


---
## veCRV & Rewards

## veCRV
In order to participate in Curve DAO governance, you must have a certain amount of CRV (veCRV) locked up in your account. veCRV is a non-standard ERC20 implementation, used by the Aragon DAO to calculate each account’s voting power.

Since veCRV can't be transferred, the only way to obtain it is by locking up CRV. The maximum lock time is four years. For example, if you lock up one CRV for four years, you'll have an initial balance of one veCRV.

However, as time goes on and the CRV unlock date gets closer, your veCRV balance will decay linearly. For example, a balance of 4000 CRV locked for one year provides the same amount of veCRV as 2000 CRV locked for two years, or 1000 CRV locked for four years

veCRV tokens give you the opportunity to increase your rewards for offering liquidity on Curve. veCRV tokens allow you to earn up to 2.5x more on the liquidity you provide on Curve.

## Rewards
Curve's most valuable accomplishment is that it gives people an incentive to contribute liquidity and earn rewards over their idle assets. One of the major incentives of CRV is the ability to boost the rewards on provided liquidity. Vote locking CRV allows you to acquire voting power to participate in the DAO voting and earn a boost of up to 2.5x on the liquidity you are providing on Curve. The goal is to incentivize users to participate in governance by rewarding them with a bigger share of the CRV inflation.This is a great way to increase your earnings and get more involved in the community.

When users lock their CRV tokens into the Curve DAO, they receive veCRV. The ratio of CRV to veCRV is not 1:1 and depends on how long the user locks their CRV tokens. If a user locks their CRV tokens for four years, they get the same amount of veCRV as the number of CRV tokens locked. If they lock for less than four years, then the number of veCRV tokens they get decreases linearly. So a user who locks their CRV tokens for two years would get half the amount of veCRV as the number of CRV tokens locked. The more veCRV a user has, the more boost they are eligible for.

The Curve DAO system is designed to keep the community engaged and informed on critical decisions, while also providing incentives for doing so. Locking your CRV into the Curve DAO is a great way to get more veCRV, boost your CRV rewards, and get trading fees..

Half of all trading fees go straight to the pockets of veCRV holders. This was set up in order to keep the interests of liquidity providers and governance participants (veCRV holders) aligned. The collected trading fees are used to buy 3CRV (the LP token for 3Pool) and distribute it among veCRV holders. This currently adds up to more than $15 million in trading fees per year. veCRV stands for vote escrowed $CRV, which is when $CRV votes are locked in the Curve DAO.


    


---
## Evaluation





##### Advantages of owning veCRV:  

- [ ]  To earn new tokens for veCRV votes in bribing
- [ ]  To get voting power in gauge weight
- [ ]  Participate in Curve DAO governance
- [x]  All of the above





##### What rewards does curve finance offers to liquidity provider?  

- [x]  They get more governance power over other
- [ ]  They get 0.1 USDC for every dollar locked
- [x]  Earn a boost of up to 2.5 times 
- [x]  They earn a cut of trading fees

    


---
## Liquidity Gauges and CRV Rewards

## Liquidity Gauge

Inflation in the CRV protocol is directed to users who provide liquidity within the protocol. This usage is measured via “Liquidity Gauge”. Each pool has an individual liquidity gauge. The Gauge Controller maintains a list of gauges and their types, with the weights of each gauge and type.

To measure liquidity over time, the user deposits their LP tokens into the liquidity gauge. Coin rates which the gauge is getting depends on current inflation rate, gauge weight, and gauge type weights. Each user receives a share of newly minted CRV proportional to the amount of LP tokens locked.

The liquidity of each pool is measured by a unique gauge. There are currently several different versions of liquidity gauge contracts in use.


## Gauge Weight Voting

Users can choose to invest their veCRV in one or more liquidity gauges. These gauges receive a portion of newly minted CRV tokens based on how much veCRV is allocated to them. Each user with a veCRV balance can change their preferences at any time. When a user applies a new weight vote, it takes effect at the beginning of the next epoch week. A weight vote for any one gauge cannot be changed more than once every 10 days.


## Bribes
Curve.fi uses gauge weights to determine how much CRV each pool gets. The heavier the weight, the higher the rewards for providing liquidity. Every Thursday, curve.fi lets people use their veCRV to vote for the coming week’s gauge weights. The results of the vote dictate the amount of veCRV allocated to a particular gauge for the coming week. The heavier the gauge, the higher the rewards. 

Bribes are a recent addition to make things more interesting. Now protocol teams can bribe veCRV holders to vote for their gauge each week. Through bribing, some people are trying to influence the weekly votes that decide how much CRV rewards should be allocated to the various liquidity pools on the Curve Finance platform. In exchange for their vote, the voters are given another token. 

In August 2021, Andre Cronje, the founder of Yearn Finance, released a tool for bribing called [bribe.crv.finance](https://bribe.crv.finance/).  It is a platform that CRV bribers can use to create offers, and others can use to claim offers.In order to vote lock your CRV for a particular gauge, you will be bribed in accordance with the amount of CRV you vote with. You are bribed with spell token, which can later be sold on DEXs. Thus, increasing your APY and one can generate more returns through bribing.  Here is the example of Unit Protocol distributing bribes on Curve [https://docs.unit.xyz/guides-1/bribes-on-curve.fi](https://docs.unit.xyz/guides-1/bribes-on-curve.fi) 


    


---
## Evaluation





##### On what basis are newly minted CRV distributed to various gauges  

- [x]  Current Inflation rate
- [ ]  Randomly
- [x]  Gauge weight
- [x]  veCRV votes





##### Benifits of participating in bribes ?  

- [ ]  You get additional veCRV
- [x]  You are rewarded with different tokens
- [ ]  You get more boost in your rewards
- [ ]  You are rewarded with additional CRV tokens

    


---
## Cuve & Convex

## Pain Points in Curve 

The challenge with staking on curve finance is that there are a lot of manual steps involved and it can be complicated. The interface of the curve finance is not very user friendly. Once locked you cant use CRV tokens on Curve Finance. After locking your crypto assets in any pool, you will receive veCRV tokens. However, these veCRV tokens cannot be moved to different wallets, and you also cannot sell them. The veCRV tokens simply remain locked. The other major loophole of curve finance is that the rewards allocated to particular pools are decided by voting conducted every week. This voting is badly influenced by bribes. Thereby allocating more rewards to the pool of big players with more veCRV.


## Convex Intro

Convex Finance is a protocol built on top of Curve Finance in order to make yield farming much easier for stakers and to automatically get boosted rewards,it also provides a way to keep your locked CRV tokens unlocked through the cvxCRV tokens. Instead of staking CRV on Curve Finance, you can stake your CRV on Convex Finance and receive all of the boosted rewards and benefits. You can stake your LP 3Pool Curve (3CRV) tokens on Convex Finance for even more benefits. If you have already provided liquidity for Curve Finance, you can collect your 3CRV LP tokens and stake them on Convex Finance. As there are extra benefits for staking LP tokens. CVX is a convex governance token that can be staked in order to earn rewards.It is more convenient to stake your curve on convex and receive benefits like returns from trade fees in the liquidity pools, as well as returns from providing liquidity to those pools.


    


---
## Evaluation





##### Pain points in curve finance:  

- [x]  Complicated steps involved,which makes staking difficult for new user
- [x]  Gauge votes are influenced by bribes
- [ ]  Uncontrollable slippage
- [x]  veCRV tokens don't remain liquid as they are locked for a time period





##### Advantage of investing in convex finance over curve finance  

- [x]  Extra benefits for staking  LP tokens
- [x]  No complicated steps involved, that makes staking easier
- [x]  Automatically get boosted rewards
- [x]  Keep your locked CRV tokens unlocked through the cvxCRV tokens

    


---
## Footer
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.
    
