## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.

---

## Optimistic Rollups


## Why Layer 2

The unprecedented demand for Ethereum network, led to extraordinarily high gas fees, that made it expensive for regular users to pay for their transactions.

The Ethereum network currently has a transaction speed of around 30 (in year 2022) transactions per second. The network frequently becomes overcrowded as a result, which occasionally causes gas prices to reach extremely high levels and constant delay in transactions. This major problem of scalability can be overcomed using layers2 frameworks. Layer 2 refers to a framework or protocol of off-chain solutions  built on top of layer 1s to solve the problem of transaction speed and scaling difficulties faced by almost all cryptocurrency networks. It plays a significant part in enhancing scaling. Layer 2 solutions provide a mechanism to scale and speed up transactions while retaining the main chain's security. They have the capacity to execute thousands of transactions per second, which is essential if Ethereum is to gain main stream adoption. One of the key benefits of employing off-chain solutions is that no structural changes  are necessary in the main chain, because the second layer is simply introduced as an extra layer.

Layer-2 networks are composed of two parts: 

1. A network that processes transactions 
2. A smart contract on the underlying blockchain that settles disputes and achieves consensus on the state of the layer-2 network. The smart contract "cements" the layer-2 network to the underlying blockchain.

There are two main functions of the smart contract are:

1. Holding and releasing funds that are transferred to the layer
2. Receiving proofs from the layer 2, validating them, resolving disputes, and finalizing transactions

**The most famous type of layer 2 implementations is Rollups**

    


---
## Evaluation





##### How do we benefit from the introduction of layer 2 frameworks?  

- [ ]  More security
- [x]  provide higher scalability
- [x]  Instant transactions
- [x]  Charging less gas fee

    


---
## Rollups

Rollup is a type of layer two solution  to solve the Ethereum scalability problem Roll ups works by executing transactions outside the main ethereum  chain, while submitting data to the base chain.This means that layer-2 networks can handle the processing of transactions much faster than the base blockchain, since there is a smaller validator set with better hardware. In addition, the base blockchain only needs to execute proofs submitted to the rollup smart contract to verify the activity on the layer-2 network, rather than store raw, unexecuted transaction data.

In a rollup, all data is posted to the Layer-1 blockchain. This is because “computation is expensive but data is cheap on Ethereum”.

Optimistic and zero-knowledge rollups provide higher scalability by executing smart contract state changes off-chain and proving them on-chain. Rollups improve scalability in two ways: 
1. **Off-Chain Execution** - Rollups move transaction execution off-chain, so that the underlying base blockchain only needs to verify network activity with small proofs and store raw transaction data. 
2. **Batch Transactions** - Rollups group multiple transactions together when submitted to a blockchain, so that the on-chain gas cost is spread out over many transactions.
3. **Fewer Validators** - Rollups require a minimum of one honest validator to prove the validity of transactions to the base layer blockchain. This allows for smaller validator sets and increased hardware requirements without compromising security.

Rollups shift computation (and state storage) off-chain, but still require some data per transaction to remain on-chain. For example, an Ethereum base-layer ERC20 token transfer costs approximately 45,000 gas. In contrast, an ERC20 transfer in a rollup only takes up 16 bytes of on-chain space and costs less than 300 gas.

Since data resides on-chain and there is consensus around this fact, anyone can locally process all the operations in the rollup if they choose to do so. This allows them to detect fraud, initiate withdrawals, or start producing transaction batches themselves.

    


---
## Evaluation





##### How do roll-ups improve the layer1 scalability?  

- [ ]  By paying more to validators
- [x]  By grouping multiple transactions together.
- [x]  By executing transactions outside the main ethereum chain, while submitting data to the base chain
- [ ]  By increasing the number of active validators

    


---
## Rollup Bridges

## Bridges

Bridges are responsible for holding assets on a layer-1 blockchain while those same assets are released on another service. This defines who has custody of the funds and the conditions that must be met before the assets can be unlocked. The withdrawal request destroys coins on the off-chain system and updates the bridge contract about the user’s entitlement to withdraw their coins back to the Layer 1 blockchain. This allows users to move their coins back and forth between the two systems without having to worry about losing any of their value.

Bridges carryout functions similar to the below:
1. Deposit. A user can deposit funds into the bridge, and then corresponding assets are set up on the other system.
2. Update account balance. The bridge is told about new account balances, which can help the withdrawal process.
3. Withdrawal. A user can withdraw their assets from the bridge according to their balance on the other system, and the tokens issued on the other system are destroyed.
4. Censorship resistance. The bridge contract can enforce the eventual ordering and execution of transactions to ensure users can always unwind their positions and withdraw their funds.
        

    


---
## Evaluation





##### If an users can unwind their positions and withdraw their funds is ensured by ?  

- [ ]  Deposit
- [x]  Censorship resistance
- [ ]  Update account balance.
- [ ]  Withdrawal

    


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





##### How are transactions validated in Fraud-proof approach?  

- [ ]  By validating the evidences through proof of work mechanism.
- [x]  By validating the evidence provided during challenge time window.
- [ ]  By validating the evidence provided by the executor alongside the commitment
- [ ]  By validating the evidences through proof of stake mechanism.

    


---
## Disputes in Optimistic

There are currently two approaches for pinpointing a disputed state transition in Optimistic Rollups:

### 1. One-round fraud proof 
This means that the challenger has a list of intermediary state transitions for the commitment being asserted, which can be used to pinpoint the disputed state transition. The challenger then submits the disputed intermediary state transitions along with a list of inclusion proofs about the state transition's pre-state, the state transition itself, and the executor's asserted post-state after it is executed. This allows for quick and easy fraud detection in commitments. 
 
In Optimism, all state commitments are sent to the bridge contract, allowing a challenger to identify which state transition should be executed by the bridge contract. No cooperation with the executor is necessary, and a valid commitment cannot be evaluated as invalid by a fraud proof. If a commitment is proven to be invalid, it can be discarded, along with slashing the executor who proposed it. However, for V2 they’re moving towards using interactive proofs. 

### 2. Multi-round fraud proof
This is a method used to make it harder for fraud to happen. In this system, the list of intermediary state transitions for an asserted commitment is not sent to the bridge contract. This makes it more difficult to pinpoint an individual state transition in a single-round. Instead, the challenger and executor must agree upon the total number of instructions executed within the commitment. They will then perform a binary search until they pinpoint the disputed instruction. 
 
Arbitrum's multi-round fraud proof system is a binary search between two parties to find the first opcode of a whole block that they disagree on. Once found, only this particular opcode is executed on-chain.

    


---
## Evaluation





##### One-round fraud detection is made made by ?  

- [ ]  Sequencers
- [ ]  Executors
- [ ]  Validators
- [x]  challengers

    


---
## Footer
This is the course header. This will be added on top of every page. Go to [DoDAO.academy](https://www.dodao.academy) to know more.
    
