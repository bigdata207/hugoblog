---
title: "OverView"
date: 2017-08-24T15:48:31+08:00
draft: true
categories:
- Blockchain
thumbnailImagePosition: "top"
thumbnailImage: //d1u9biwaxjngwg.cloudfront.net/welcome-to-tranquilpeak/city-750.jpg
coverImage: //d1u9biwaxjngwg.cloudfront.net/welcome-to-tranquilpeak/city.jpg
---

A blockchain[1][2][3] – originally block chain[4][5] – is a continuously growing list of records, called blocks, which are linked and secured using cryptography.[1][6] Each block contains typically a hash pointer as a link to a previous block,[6] a timestamp and transaction data.[7] By design, blockchains are inherently resistant to modification of the data. Functionally, a blockchain can serve as "an open, distributed ledger that can record transactions between two parties efficiently and in a verifiable and permanent way."[8] For use as a distributed ledger a blockchain is typically managed by a peer-to-peer network collectively adhering to a protocol for validating new blocks. Once recorded, the data in any given block cannot be altered retroactively without the alteration of all subsequent blocks and a collusion of the network majority.
Blockchains are secure by design and are an example of a distributed computing system with high Byzantine fault tolerance. Decentralized consensus has therefore been achieved with a blockchain.[9] This makes blockchains potentially suitable for the recording of events, medical records,[10][11] and other records management activities, such as identity management,[12][13][14] transaction processing, and documenting provenance.
The first distributed blockchain was conceptualised by Satoshi Nakamoto in 2008 and implemented the following year as a core component of the digital currency bitcoin, where it serves as the public ledger for all transactions.[1] The invention of the blockchain for bitcoin made it the first digital currency to solve the double spending problem, without the use of a trusted authority or central server. The bitcoin design has been the inspiration for other applications.[1][3]

History[edit]

Bitcoin transactions (January 2009 – September 2015)
The first work on a cryptographically secured chain of blocks was described in 1991 by Stuart Haber and W. Scott Stornetta,[15] in 1992, Bayer, Haber and Stornetta incorporated Merkle trees to the blockchain as an efficiency improvement to be able to collect several documents into one block.[16][6]
The first distributed blockchain was then conceptualised by Satoshi Nakamoto in 2008 and implemented the following year as a core component of the digital currency bitcoin, where it serves as the public ledger for all transactions.[1] Through the use of a peer-to-peer network and a distributed timestamping server, a blockchain database is managed autonomously. The use of the blockchain for bitcoin made it the first digital currency to solve the double spending problem without requiring a trusted administrator.[4] The bitcoin design has been the inspiration for other applications.[1][3]
The words block and chain were used separately in Satoshi Nakamoto's original paper in October 2008,[17] and when the term moved into wider use it was originally block chain,[4][5] before becoming a single word, blockchain, by 2016. In August 2014, the bitcoin blockchain file size reached 20 gigabytes.[18] In January 2015, the size had grown to almost 30 gigabytes, and from January 2016 to January 2017, the bitcoin blockchain grew from 50 gigabytes to 100 gigabytes in size.[19]
By 2014, "Blockchain 2.0" was a term referring to new applications of the distributed blockchain database.[20] The Economist described one implementation of this second-generation programmable blockchain as coming with "a programming language that allows users to write more sophisticated smart contracts, thus creating invoices that pay themselves when a shipment arrives or share certificates which automatically send their owners dividends if profits reach a certain level."[1] Blockchain 2.0 technologies go beyond transactions and enable "exchange of value without powerful intermediaries acting as arbiters of money and information". They are expected to enable excluded people to enter the global economy, enable the protection of privacy and people to "monetize their own information", and provide the capability to ensure creators are compensated for their intellectual property. Second-generation blockchain technology makes it possible to store an individual's "persistent digital ID and persona" and are providing an avenue to help solve the problem of social inequality by "[potentially changing] the way wealth is distributed."[21]:14–15 As of 2016, Blockchain 2.0 implementations continue to require an off-chain oracle to access any "external data or events based on time or market conditions [that need] to interact with the blockchain."[22]
In 2016, the central securities depository of the Russian Federation (NSD) announced a pilot project based on the Nxt Blockchain 2.0 platform that would explore the use of blockchain-based automated voting systems.[23] Various regulatory bodies in the music industry have started testing models that use blockchain technology for royalty collection and management of copyrights around the world.[24][better source needed] IBM opened a blockchain innovation research centre in Singapore in July 2016.[25] A working group for the World Economic Forum met in November 2016 to discuss the development of governance models related to blockchain.[26] According to Accenture, an application of the diffusion of innovations theory suggests that in 2016 blockchains attained a 13.5% adoption rate within financial services, therefore reaching the early adopters phase.[27] In 2016, industry trade groups joined to create the Global Blockchain Forum, an initiative of the Chamber of Digital Commerce.[28]
In early 2017, the Harvard Business Review suggested that blockchain is a foundational technology and thus "has the potential to create new foundations for our economic and social systems." It further observed that while foundational innovations can have enormous impact, "It will take decades for blockchain to seep into our economic and social infrastructure."[8]

Description[edit]
A blockchain facilitates secure online transactions.[29][better source needed] A blockchain is a decentralized and distributed digital ledger that is used to record transactions across many computers so that the record cannot be altered retroactively without the alteration of all subsequent blocks and the collusion of the network.[30][1] This allows the participants to verify and audit transactions inexpensively.[31] They are authenticated by mass collaboration powered by collective self-interests.[32] The result is a robust workflow where participants' uncertainty regarding data security is marginal. The use of a blockchain removes the characteristic of infinite reproducibility from a digital asset. It confirms that each unit of value was transferred only once, solving the long-standing problem of double spending. Blockchains have been described as a value-exchange protocol.[20] This blockchain-based exchange of value can be completed more quickly, more safely and more cheaply than with traditional systems.[33] A blockchain can assign title rights because it provides a record that compels offer and acceptance.[1]
A blockchain database consists of two kinds of records: transactions and blocks.[1] Blocks hold batches of valid transactions that are hashed and encoded into a Merkle tree.[1] Each block includes the hash of the prior block in the blockchain, linking the two. Variants of this format were used previously, for example in Git. The format is not by itself sufficient to qualify as a blockchain.[34] The linked blocks form a chain.[1] This iterative process confirms the integrity of the previous block, all the way back to the original genesis block.[35] Some blockchains create a new block as frequently as every five seconds.[36] As blockchains age they are said to grow in height.
Sometimes separate blocks can be produced concurrently, creating a temporary fork. In addition to a secure hash based history, any blockchain has a specified algorithm for scoring different versions of the history so that one with a higher value can be selected over others. Blocks not selected for inclusion in the chain are called orphan blocks.[35] Peers supporting the database don't have exactly the same version of the history at all times. Instead, they keep the highest scoring version of the database that they currently know of. Whenever a peer receives a higher scoring version (usually the old version with a single new block added) they extend or overwrite their own database and retransmit the improvement to their peers. There is never an absolute guarantee that any particular entry will remain in the best version of the history forever. Because blockchains are typically built to add the score of new blocks onto old blocks and because there are incentives to work only on extending with new blocks rather than overwriting old blocks, the probability of an entry becoming superseded goes down exponentially[37] as more blocks are built on top of it, eventually becoming very low.[1][38]:ch. 08[39] For example, in a blockchain using the proof-of-work system, the chain with the most cumulative proof-of-work is always considered the valid one by the network. There are a number of methods that can be used to demonstrate a sufficient level of computation. Within a blockchain the computation is carried out redundantly rather than in the traditional segregated and parallel manner.[40]

Decentralization[edit]
By storing data across its network, the blockchain eliminates the risks that come with data being held centrally.[1] Decentralised blockchains may use ad-hoc message passing and distributed networking. Its network lacks centralized points of vulnerability that computer hackers can exploit or any central point of failure. Blockchain security methods include the use of public-key cryptography.[4]:5 A public key (a long, random-looking string of numbers) is an address on the blockchain. Value tokens sent across the network are recorded as belonging to that address. A private key is like a password that gives its owner access to their digital assets or otherwise interact with the various capabilities that blockchains now support. Data stored on the blockchain is generally considered incorruptible.[1]
Every node or miner in a decentralized system has a copy of the blockchain. Data quality is maintained by massive database replication[9] and computational trust. No centralized "official" copy exists and no user is "trusted" more than any other.[4] Transactions are broadcast to the network using software. Messages are delivered on a best effort basis. Mining nodes validate transactions,[35] add them to the block they’re creating, and then broadcast the completed block to other nodes.[38]:ch. 08 Blockchains use various time-stamping schemes, such as proof-of-work to serialize changes.[41] Alternate consensus methods include proof-of-stake and proof-of-burn.[35] Growth of a decentralized blockchain is accompanied by the risk of node centralization because computer resources required to operate bigger data become more expensive.[42]

Hard forks[edit]
Per Investopedia, a hard fork term refers to a situation when a blockchain splits into two separate chains in consequence of the use of two distinct sets of rules trying to govern the system.[43] For example, Ethereum has hard-forked to "make whole" the investors in The DAO, which had been hacked by exploiting a vulnerability in its code.[44] In 2014 the Nxt community was asked to consider a hard fork that would have led to a rollback of the blockchain records to mitigate the effects of a theft of 50 million NXT from a major cryptocurrency exchange. The hard fork proposal was rejected, and the majority of the funds were recovered after negotiations.[45]

Openness[edit]

Blockchain data
Open blockchains are more user friendly than some traditional ownership records, which, while open to the public, still require physical access to view. Because all early blockchains were permissionless, controversy has arisen over the blockchain definition. An issue in this ongoing debate is whether a private system with verifiers tasked and authorized (permissioned) by a central authority should be considered a blockchain.[46][47][48][49][50] Proponents of permissioned or private chains argue that the term "blockchain" may be applied to any data structure that batches data into time-stamped blocks. These blockchains serve as a distributed version of multiversion concurrency control (MVCC) in databases.[51] Just as MVCC prevents two transactions from concurrently modifying a single object in a database, blockchains prevent two transactions from spending the same single output in a blockchain.[21]:30–31 Opponents say that permissioned systems resemble traditional corporate databases, not supporting decentralized data verification, and that such systems are not hardened against operator tampering and revision.[46][48] The Harvard Business Review defines blockchain as a distributed ledger or database open to anyone.[52] In 2016, Nikolai Hampton of Computerworld claimed that "much of [permissioned blockchain hype] is nothing more than snake oil and spin".[53]

