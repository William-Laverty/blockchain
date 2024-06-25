# BLOCKCHAIN

## 25 JUNE 2024
**SOFTWARE ENGINEERING**  
**WILLIAM LAVERTY**  
**YEAR 11 HSC**

---

### BLOCKCHAIN
**GITHUB REPO: https://github.com/William-Laverty/blockchain**

- **OVERVIEW**

A blockchain is a decentralized system that records transactions across a network of computers (peer-to-peer). Basically, it’s a chain of blocks where each block contains a list of transactions and is cryptographically linked using a hash to the previous block.

The Blockchain class represents this structure:

- **HOW IT WORKS**

1. Transactions are grouped into blocks
2. Each block is validated using a hash method and added to the blockchain
3. The chain is distributed and validated across multiple nodes in a peer-to-peer network

- **KEY COMPONENTS OF A BLOCKCHAIN**

**Blocks:** Containers for multiple transactions

**Transactions:** Records of data transfer

**Hashes:** Unique fingerprints for blocks using hash functions

- **BLOCKCHAIN CHARACTERISTICS**

**Decentralization:** The blockchain is distributed across multiple hosts. These means that it isn’t controlled or monitored as no one host has most of the power over transactions. While it isn’t made to do that in my code does have the potential to run on multiple servers.

**Immutability:** This means that once a block is added they can't be changed. If someone was to try and change it, it would break the chain due to differences in the hashes. To ensure that the chain can be changed it’s done by linking blocks through identifiable hashes:

**Security:** Security is very important for the blockchain. As it’s designed around cryptographic methods the blockchain is very secure. It’s basically impossible to forge a transaction as it’s checked through cryptographic hashing and the proof-of-work algorithms:

**Transparency:** All transactions are visible to the public and anyone can access it. Whilst transactions can’t be traced easily the record is published openly to view. This chain endpoint allows viewing the entire blockchain:

- **CONSENSUS MECHANISM**

**Proof of Work (PoW):** Miners must find a hash starting with a specific number of zeros

**Proof of Stake (PoS):** I haven’t implemented this in my code however it would involve validators being chosen based on the amount of cryptocurrency they hold and are willing to "stake". These validators are rewarded with cryptocurrency set by the transaction known as the “gas fee”.

**Delegated Proof of Stake (DPoS):** This is a consensus mechanism where token holders vote for a number of delegates (witnesses) to validate transactions and create new blocks. This method can offer faster transactions and lower fees compared to the Proof of Stake.

**Byzantine Fault Tolerance (BFT):** This is a property of a system that can continue operating even if some of its components fail. It is usually implemented through algorithms that allow nodes to agree on the state of the system despite the presence of "byzantine" or treacherous nodes.

- **APPLICATION OF BLOCKCHAIN TECHNOLOGY**

**Cryptocurrencies:** While this code doesn't implement a full cryptocurrency, it shows the structure that cryptocurrencies use. Bitcoin and Ethereum are both blockchain-based cryptocurrencies, but they do have different primary purposes. Bitcoin was designed mainly as a digital currency for peer-to-peer transactions, while Ethereum extends the blockchain concept to create a platform for decentralized applications (dApps) and smart contracts. Overall, these coins have enabled more complex transactions of currency beyond simple methods of centralized banking systems.

**Supply chain management:** The blockchain can track goods through a supply chain by modifying the transaction structure. Each transaction could represent a transfer of goods from one point in the supply chain to another, including details like location, time, and condition of the goods. This would create an immutable record of a product's journey, ensuring traceability and reducing fraud in the supply chain.

**Voting systems:** The transparency of the blockchain makes it suitable for secure voting systems. Each vote could be recorded as a transaction and the blockchain would ensure that votes cannot change. This could potentially increase voter confidence, reduce electoral fraud, and allow for real-time vote counting.

**Smart contracts:** Advanced blockchain systems like Ethereum support smart contracts. These are self-executing contracts with the terms directly written into code. These contracts automatically execute when predefined conditions are met without the need for intermediaries. This can streamline various processes in fields such as finance, real estate, and law by reducing costs and increasing efficiency of managing data.

---

### UML DIAGRAM

<a href="https://ibb.co/4YX0r9N"><img src="https://i.ibb.co/MGtJ0WN/Screenshot-2024-06-25-at-10-53-29-pm.png" alt="Screenshot-2024-06-25-at-10-53-29-pm" border="0"></a>

---

### DATA DICTIONARY

| Class       | Attribute                | Data Type | Description                                   |
|-------------|--------------------------|-----------|-----------------------------------------------|
| Block       | index                    | int       | The position of the block in the chain        |
| Block       | transactions             | list      | The list of transactions in the block         |
| Block       | timestamp                | float     | The time the block was created                |
| Block       | previous_hash            | str       | The hash of the previous block                |
| Block       | nonce                    | int       | The nonce used for the proof of work          |
| Block       | hash                     | str       | The hash of the current block                 |
| Blockchain  | chain                    | list      | The list of blocks in the chain               |
| Blockchain  | unconfirmed_transactions | list      | The list of new transactions yet to be mined  |
| Blockchain  | difficulty               | int       | The difficulty level for mining               |
| Transaction | author                   | str       | The author of the transaction                 |
| Transaction | content                  | str       | The content of the transaction                |
| Transaction | timestamp                | float     | The time the transaction was created          |

- **BLOCK CLASS**

  - `index`: An integer representing the block’s position in the blockchain.
  - `transactions`: A list containing the transactions included in the block.
  - `timestamp`: A floating-point number representing the creation time of the block.
  - `previous_hash`: A string representing the hash of the previous block in the chain.
  - `nonce`: An integer used to solve the proof-of-work algorithm.
  - `hash`: A string representing the hash of the current block. It is computed using the block’s content.

- **BLOCKCHAIN CLASS**

  - `chain`: A list of all blocks in the blockchain.
  - `unconfirmed_transactions`: A list of transactions that are waiting to be mined and added to a block.
  - `difficulty`: An integer defining how difficult it is to mine a new block. This value is used to set the required number of leading zeros in the hash for a block to be considered valid.

- **TRANSACTION**

  - `author`: A string representing the author of the transaction.
  - `content`: A string representing the content of the transaction.
  - `timestamp`: A floating-point number representing the creation time of the transaction.
