## Light Client
keeping a shallow-copy

don’t have the system resources to download and maintain the full blockchain in their system? They can choose to become “Light clients”. By being a Light Client, they get high-security assurances about certain states of Ethereum and also the power to verify the execution of a transaction.

## Full node
Fully enforces all the consensus rules of Ethereum is called a Full Node. A full node downloads the entire blockchain in the user’s desktop. validate the nodes and transactions and relay the information to the other nodes (using the gossip protocol).

- Making sure that the correct block reward is given out for each block mined (5 ETH)
- Transactions have the correct signatures
- Transactions and blocks are in the correct data format
- No double spending is occurring in any of the blocks

all miners are full nodes, but not all full nodes are miners. Miners need to be running full nodes to access the blockchain. Anyone who runs a full node need not mine for blocks.

## Increase the block size
improve the performance by increasing the number of transactions going into one block

this will still not solve the problem of nodes coming to a consensus at a slower pace. In fact, as the number of transactions per block increases, the number of calculations and verifications per node will increase as well.

In order to accommodate for more and more transactions, the block sizes need to be increased periodically. This will centralize the system more because normal computers and users won’t be able to download and preserve such bulky blockchains. This goes against the egalitarian spirit of a blockchain.

Finally, block size increase will happen only via hardfork, which can split the community. The last time a major hardfork happened in Ethereum the entire community was divided and two separate currencies came about. People don’t really want this to happen again.


## Make users use different altcoins.
Another proposal was to run parallel blockchains instead of one main blockchain.

It is not wise to split up the hashrate of a chain. The hashrate of the chain after all determines how secure it is from external hackers and fast the system is.

It will be easier for malicious miners to get 51% majority on the smaller chains.



-----------------

## Consensus Protocols
Consensus Protocols are a set of protocols that lets the miners come to a consensus on which block (set of transactions) comes next on the totally ordered chain of blocks. The biggest problem when it comes to reaching a consensus is what is called the Byzantine Generals Problem [1]

### Proof of Work
Bitcoin uses a probabilistic consensus protocol called the proof-of-work mechanism in order to solve the Byzantine Generals Problem. In this, all the miners calculate the hash
value of the constantly changing block headers, which contains metadata such as timestamp, nonce and  hash values of previous blocks. When one of the miners finds the relevant value, all the
other nodes that participated need to confirm the correctness of the value (19).

### Proof of Stake
Proof-of-Stake is a deterministic mechanism that works by staking a portion of wealth of the miner and
demanding proof of ownership on the amount of currency they possess in order to verify a block. It follows the reasoning that someone with more stake in the currency would be less likely to attack the network [19]. Ethereum plans to implement proof of stake by using a relatively stricter protocol called the casper protocol, which "slashes" the stakes of misbehavers [2]. Another variant of PoS uses the "age" of the stake to determine who gets to verify the next block.
The age is determined
by the value multiplied with the time period of its creation [17, 19].
The miners with more rights in the network are the ones with more stake and who have also been holding the wealth for longer time, which decreases the incentive for them to attack the
blockchain [17, 19].

The security
of the blockchain utilizing a PoS mechanism increases with net value in the blockchain network, since buying out 51% of the net value becomes costlier for 51% attacks.
PoS also reduces the power consumption compared to PoW systems because of the whole mechanism being virtual. Bitcoin's power usage was roughly estimated to be in the ballpark
of 0.1-10 GW [49].

Formal guarantees of system convergence are lacking for PoS mechanisms [18].

### scalability

PoS algorithm also allows implementation of sharding to improve scalability and transaction throughput. Sharding is a database management concept where separate partitions of the database are stored in separate server instances, thus improving performance.
proof-of-stake makes the implementation of sharding easier.


## BFT
A trust
model with stronger assumptions than those in Bitcoin can support a more
efficient consensus protocol, achieving better latency and throughput with less
computation, bandwidth, and storage. Specically, using a standard Byzantine
Fault Tolerant (BFT) replication protocol with a small number of pre-designated
trusted entities removes many of the scaling obstacles in Bitcoin.


## Sharding

Similar to distributed databases, sharding in blockchains divides the whole network into shards so that every node in the network need not store the entire history of transactions, like in traditional blockchains. Unlike centralized databases, decentralization brings with it the problem of malicious actors, which needs to be solved using some consensus mechanisms.
Because each shard can process its own transactions, all the nodes in the network need not verify every transaction. This means transactions can occur parallelly and throughput is expected to increase. Zilliqa, a Blockchain platform developed by National University of Singapore researchers, recently reached a breakthrough for scalability on its platform by increasing the throughput threshold to 2,488 transactions per second on an internal testnet with 3600 nodes thanks to their “sharding” technology[233].
Vitalik Buterin, co-founder of Ethereum and other blockchain experts have stated that 1 million transactions per second (tps) is very likely.[133]
It is important to note that performance of sharded network does not grow linearly with shard count. This is due to the need to reach consensus among the shards when operations span multiple shards[144].

Single-Shard Takeover Attack, where an attacker takes over the majority of collators in a single shard to create a malicious shard that can submit invalid collations.The safety mechanism that will be implemented in Proof-of-Stake (PoS) blockchains that opt for the sharding solution is the fact that the malicious actor is unable to choose a specific shard to work on and it does not know which shard he will be assigned to in advance.

## zilliqa
They are making a very clear distinction between the state and the transaction history.
The principle is that it takes a lot more space to store the history of the transactions than the space it takes to store your current balance (state).The approach that Zilliqa has chosen with sharding is that every single node will have a copy of the current state (the bank balances in our example) but then the transactions history will be split in pieces so that not everyone will have to have a full copy of it.We have had several rounds of discussion on state sharding, and the conclusion was that there still
16
isn’t a state sharding scheme that is secure enough (e.g., resilient to attacks) and efficient (e.g., without
excessive cross-shard communication). That’s why we prefer keeping state sharding to future work
for now.

## References
[233] https://www.the-blockchain.com/2017/10/13/zilliqa-breaks-2400-transactions-per-second-sharding-blockchain/
[133] https://twitter.com/VitalikButerin/status/991021062811930624

[111] https://github.com/ethereum/wiki/wiki/Sharding-FAQs

[18] I. Bentov, C. Lee, A. Mizrahi, and M. Rosenfeld. Proof of activity: Extending
bitcoin's proof of work via proof of stake. https://eprint.iacr.org/2014/452/.

[17] Zibin Z, Shaoan X, Hongning D, Xianping C, Huaimin W, An Overview of Blockchain
Technology: Architecture, Consensus, and Future Trends. 2017 IEEE International
Congress On Big Data (Bigdata Congress), (2017); DOI: 10.1109/BigDataCongress.2017.85.

[1] Lamport, L.; Shostak, R.; Pease, M. (1982). "The Byzantine Generals Problem

[222] https://blockgeeks.com/guides/blockchain-consensus/

[19] Du M., Ma X., Zhang Z., Wang X., Chen Q., A Review on Consensus Algorithm
of Blockchain. 2017 IEEE International Conference on Systems, Man, and Cybernetics
(SMC), (2017). DOI: 10.1109/SMC.2017.8123011.

[333] Marko V., The Quest for Scalable Blockchain Fabric: Proof-of-Work vs. BFT Replication.
Open Problems in Network Security, IFIP WG 11.4 International Workshop,
iNetSec 2015. (2015, Oct). LNCS, volume 9591.

[59]Aviv Zohar. Bitcoin: under the hood. Commun. ACM, 58(9):104{113, 2015.

[499] Practical Byzantine Fault Tolerance, Miguel Castro and Barbara Liskov

[144] Kyle Croman, Christian Decker, Ittay Eyal, Adem Efe Gencer, Ari Juels, Ahmed Kosba, Andrew Miller, Prateek Saxena, Elaine Shi, Emin Gun
Sirer, Dawn Song and Roger Wattenhofer, On Scaling Decentralized Blockchains (A Position Paper).
Initiative for CryptoCurrencies and Contracts (IC3)
