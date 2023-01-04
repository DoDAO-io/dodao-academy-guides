## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.

---

## Bridges - Deep Dive


## What is a bridge

Bridges are responsible for holding assets on a layer-1 blockchain while those same assets are released on another service. This defines who has custody of the funds and the conditions that must be met before the assets can be unlocked. The withdrawal request destroys coins on the off-chain system and updates the bridge contract about the user’s entitlement to withdraw their coins back to the Layer 1 blockchain. This allows users to move their coins back and forth between the two systems without having to worry about losing any of their value.

Bridges carryout functions similar to the below:
1. Deposit. A user can deposit funds into the bridge, and then corresponding assets are set up on the other system.
2. Update account balance. The bridge is told about new account balances, which can help the withdrawal process.
3. Withdrawal. A user can withdraw their assets from the bridge according to their balance on the other system, and the tokens issued on the other system are destroyed.
4. Censorship resistance. The bridge contract can enforce the eventual ordering and execution of transactions to ensure users can always unwind their positions and withdraw their funds.

Trust assumptions for bridge contracts can be classified into three types:
1. Single organisation. One party has the authority to update the user’s balance in the bridge contract. For example, a cryptocurrency exchange.
2. Multi-organisation. A set of independent parties (K of N) can notify the bridge about a user’s new balance. 
3. Crypto-economic. A dynamic set of parties, appointed by their weight in assets, can notify the bridge about a user’s new balance.

    


---
## Evaluation





##### what are the usecases of Bridge?  

- [ ]  To solve the security issue of rollups
- [x]  To transfer tokens between different layers
- [ ]  To help quickly validate transactions
- [ ]  To help in increasing transactions per second

    


---
## Workers

There are three types of workers involved in assessing the security of a validating bridge: 
1. Sequencers - who propose an ordered list of transactions to the bridge contract. They offer information about the pending state of the off-chain system's database (including account balances, smart contract state, etc). 
2. Executors - who propose the final execution result for a batch of transactions by posting state commitments to the bridge contract. 
3. Challengers/Validators - who validate commitments proposed by the executors.

    


---
## Evaluation





##### What type of workers are involved in assessing the security of a validating bridge?  

- [x]  Sequencers
- [x]  Challengers
- [x]  Executors
- [x]  Validators

    


---
## Bridge Contract Security Goals

Following are the security goals considered while designing a bridge

1. Data availability: How can the bridge be sure that all data for the other blockchain network is publicly available, so that users can independently recompute the layer-2 database?
2. State transition integrity: How can the bridge be sure that all state transitions for the layer-2 network are well-formed and valid?
3. Withdrawal integrity: How can the bridge guarantee that all honest users' funds can be withdrawn if the layer-2 network is compromised?
4. Protocol liveness: How can the bridge guarantee that transactions can still be executed if the layer-2 protocol is stalled or offline?

The most popular way of solving the data availability problem is called a rollup. In a rollup, all data is posted to the Layer-1 blockchain. This is because “computation is expensive but data is cheap on Ethereum”.

Now, the executor can periodically assert a cryptographic commitment to the bridge contract about the off-chain database's new state. This commitment is only finalized when the bridge contract is convinced that it is valid.

    


---
## Evaluation





##### The most popular way of solving the data availability problem is through?  

- [x]  Through data compression
- [x]  Rollups
- [ ]  Cloud Storage
- [ ]  Layer2 frameworks

    


---
## Validators

The validating bridge contract is tasked with protecting the integrity of the database and ensuring that proposed state updates are eventually applied to the database. This ensures that the database remains live and accessible to all users.

There are two ways in which the commitments can be verified:

### Fraud-proof approach(Optimistic) 
Challengers are responsible for validating commitments posted to the bridge contract. There is a challenge time window to provide time for a challenger to send indisputable evidence (proof of fraud) about the commitment’s validity. If there is no evidence of fraud by the time the challenge expires, then the commitment is accepted as valid.

### Validity-proof approach (Zero-knowledge)
The executor must present evidence alongside the commitment to prove that all state transitions are valid. There is no challenge period and the bridge contract can accept the commitment immediately.

Zero-knowledge proofs allow the prover to show that a commitment is valid without revealing any information about the inputs. This proof can be verified quickly and easily, making it a valuable tool for ensuring computational integrity. However, the downside of zero-knowledge proofs is that they can be computationally intensive for the prover, especially for generic computations. Engineers are actively working to improve this technology so that it is more efficient and easier to use.

    


---
## Evaluation





##### How are transactions validated in Validity-proof approach?  

- [ ]  By validating the evidence provided during challenge time
- [ ]  By validating the evidences through proof of stake mechanism.
- [ ]  By validating the evidences proof of work mechanism.
- [x]  By validating the evidence provided by the executor alongside the commitment

    


---
## Footer
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.
    
