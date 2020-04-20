##Glossary

**Bundle**
In the course of a transfer within the IOTA network, related transactions are combined into a so-called bundle. This includes the inputs and outputs of the transaction as well as zero value transactions. Bundles are atomic; this means that if one of the transactions within the bundle is not accepted by the network, none of the other transactions will be processed. An IOTA bundle is identified by the bundle hash. They are linked to each other via the trunkTransaction field.

**Blow Ball**
A wheel-shaped structure in the tangle which arises when new transactions repeatedly confirm the same old transaction.

**DAG**
A DAG (Directed Acyclic Graph) denotes the data structure on which the tangle is based. Instead of the blockchain where the individual blocks are linked together in a continuous chain, a DAG has a branched structure where different branches of transactions exist at the same time that can overlap but can only continue in one direction without ever returning to the starting point.

**Curl**
The ternary hash function Curl, developed especially for IOTA, was temporarily replaced by a variant of Keccak in 2017 after a working group of MIT found vulnerabilities in Curl (the significance of which was doubted by IF members).

**Depth**
The depth of a transaction is the longest backward path in the tangle to a tip.

**Genesis transaction**
The first transaction of the tangles, shown in the tangle diagram far left. In the IOTA tangle this was the transaction with which all IOTA tokens were created.

**IOTA Foundation**
A non-profit foundation established in 2017 by Dominik Schiener and David Sønstebø with the purpose of developing the IOTA Protocol and the underlying technology and promoting the IOTA ecosystem. It is financed by the sale of IOTA tokens which were given to it by the community for this purpose.

**IRI**
IRI (IOTA Reference Implementation) is the reference implementation of the IOTA Network Client developed by the IOTA Foundation in Java.

**Lazy Tip**
An unconfirmed transaction that only confirms the same old transactions again and again. Such a behavior can lead to the development of a so-called blowball, which was a problem in the early days of the tangles but now seems to be successfully prevented by updates in the IOTA Reference Implementation (IRI).

**Minimum Weight Magnitude (MWM)**
MWM determines the difficulty of the proof of work required to confirm a transaction. It corresponds to the length of the sequence of 9s (zeros in ternary notation) that the hash of bundle hash, signature, trunk, and branch transaction must have at the end. This value is currently set to 14 in the IOTA Mainnet and 9 in the Devnet/Testnet. If a transaction has less than the PoW (Proof of Work) required in the network, it is ignored by the tip selection algorithm and remains in the pending state.

**Permanode**
A node that stores the entire transaction history of the tangle, even beyond a snapshot. They are already operated by some providers, such as https://iota.partners and https://thetangle.org/. With "Chronicle", the IF presented their own solution.

**Qubic**
Stands for quorum-based computing and is a protocol that uses the tangle as a medium for transporting messages and tokens and provides a mechanism to outsource computing capacities within the decentralized IOTA network or to subject data from outside the tangles to a trust check via a process known as quorum.

**Seed**
An 81 tryte long string (consisting of the letters A-Z and the number 9) from which addresses and the corresponding private keys can be derived via an additional index IOTA.

**Side Tangle**
A structure in the tangle that follows on from an earlier transaction and then develops independently of the main tangle. This can have different causes; besides valid use cases it can also be an attack on the tangle or the result of a bug.

**Snapshot**
A distinction is made between global and local snapshots: with a global snapshot, the transaction data in the tangle is shortened starting from a milestone that is far enough in the past, all transactions that do not correspond to a value transfer are deleted and the transactions are combined with value transfer. This serves the purpose to get the enormous amount of data that accumulates over time under control. Local snapshots are a new feature of the IRI client, which can then be flexibly configured to store the tangle only to a specified depth, and are expected to eliminate the need for global snapshots.

**Tangle**
The tangle is the IOTA underlying open structure (Distributed Ledger), which is organized according to a directed acyclic graph (DAG) and serves the storage as well as the verification of all transactions made therein. It allows scalability and requires no fees from its users to perform transactions, but computing power. In contrast to other distributed ledger technologies, the proof of work, which ensures the integrity of the transactions, is not carried out by miners but by each participant. Each new transaction must confirm two old ones with proof of work. The resulting peer-to-peer network is thus self-regulating.

**Tip**
Unconfirmed transactions, i.e. transactions to which no further transactions refer. They are called tip because they represent the loose ends of the tangles. For optimum operation, the number of tips should be kept as low as possible.

**Tip Selection**
In order to feed a new transaction into the tangle, two previous transactions must be selected for confirmation. This process is standardly performed by the Random Walk.

**Ternary System: **
IOTA is not based on the binary system but on the ternary system, which describes a numerological system based on the number 3 (see also Trit and Tryte). The system is nevertheless compatible with binary systems since ternary values can easily be converted to binary and vice versa.

**Trit**
The smallest unit in a ternary system. IOTA uses a balanced ternary system where a trit can take the values -1, 0 and 1.

**Tryte**
In the ternary system used by IOTA, three trits form a tryte. With one tryte 27 different values can be displayed.  A tryte can be represented by one of the characters A-Z and 9 (for the value zero).

**Weight**
A necessary variable for the tip selection algorithm. The weight of a transaction is proportional to the work invested by a node in that transaction. It is the sum of all transactions that directly or indirectly confirm a transaction.

**Weighted Random Walk**
This describes the algorithm where a new tip is selected in the tangle for confirmation (Tip Selection). Starting from a milestone sufficiently deep in the tangle, a random path is taken to a tip, giving preference to those transactions that have a higher weight.

**Winternitz One-Time Signatures (WOTS)**
The cryptographic process used by IOTA to create signatures. This is a quantum-secure signature procedure. A special feature of this procedure is that part of the private key is revealed during the signing process. This means that a private key should only be used once at a time.
