# Whitepaper

- [English (original)](http://blockchain.aeternity.com/%C3%A6ternity-blockchain-whitepaper.pdf)
- [Chinese (translation)](http://blockchain.aeternity.com/Aeternity%E5%8C%BA%E5%9D%97%E9%93%BE%E7%99%BD%E7%9A%AE%E4%B9%A6.pdf)
- [Indonesian (translation)](Whitepaper_Indonesia)
- [Korean (translation)](Whitepaper_korean-%28%ED%95%9C%EA%B5%AD%EC%96%B4%29)
- [Spanish (translation)](http://blockchain.aeternity.com/Aeternity-blockchain-espaniol.pdf)
- [Russian (translation)](Whitepaper_Russian)
- [German (translation)](Whitepaper_Deutsch)

# Concepts

## State Channels

The state channel design in æternity enables off-chain verification of
data and smart contracts. If the verification in the channel fails, the
blockchain is asked to resolve. This, in return, permits high
transactional throughput and parallel processing of smart contracts.

Therefore, the programmability of complex relationships for large
numbers of users and handling a high volume of products and information in
parallel is æternity's strong suit. Only the parties who participated in
a smart contract know about the contents of that smart contract. 

When a channel is settled on-chain, the only way it changes the blockchain
state is by changing account balances. No contract state is stored
on-chain, so all channels are independent of each other. Transaction
speed is limited only by bandwidth, so the æternity system can scale as
well as known centralized solutions available today. For more
information, refer to
[State Channel](http://www.jeffcoleman.ca/state-channels/)

## Decentralised Oracles

An oracle is a mechanism that tells the blockchain facts about the world
we live in e.g. the closing price of Apple shares on a particular date.
æternity's oracle system uses the same consensus system as the æternity
blockchain itself i.e. it does not require a separate consensus layer on
top of the æternity mainnet.

To launch an oracle, an aeon holder has to commit to answering a yes or
no question (e.g. whether the price of an Apple share is above $200) and
specify additional conditions such as the time frame in which the Aeon
holder can answer that question. The aeon holder then has to
deposit/commit a certain amount of aeon, which is proportional to the
time frame during which the oracle is operational. When the oracle
supplies an answer that is accepted as the truth by users, the deposit
will be returned to the creator of the oracle. Otherwise, the deposit
will be destroyed.

Once the oracle has submitted an answer, other users are free to dispute
the answer by submitting a counter-claim by depositing the same amount
of aeon as the oracle creator. If there are no counter-claims by the end
of the time frame, the answer supplied by the oracle is deemed to be
truth. If there are counter-claims, the consensus system for the
æternity main-net will be used to decide on which is the correct answer.

Therefore, what is in effect achieved is a decentralised oracle system.
The truth value of oracle answers, if in dispute, will be ultimately
determined by the decentralised consensus system of the AE network.

![æternity Oracle at work](http://i66.tinypic.com/2emjrzm.png)

For more information, refer to the
[æternity White Paper](https://blockchain.aeternity.com/%C3%A6ternity-blockchain-whitepaper.pdf)

## Prediction Markets

### 1. What are prediction markets?

Prediction markets are exchange-traded markets where participants can
trade around the probability of events, like the outcome of a
presidential election, the likelihood of a natural disaster, the likely
winner of a music competition and so on.


### Prediction markets serve two important functions:

**a) They allow participants to profit from making accurate
predictions.**

Participants in a prediction market buy and sell shares based on what
they think the likelihood of an outcome will be. It is important to note
that in order for a market participant to win consistently, he/she must
not only predict the outcome correctly but must also correctly assess
the probability of that outcome. Take for example an event that has a
90% probability. If on a market the current price signals a probability
of 95% instead of 90%, it can still be very profitable in the long run
for a trader to bet against such events, even if that trader believes
that the event will likely happen given the 90% probability. This is
very counter-intuitive, but it is easily explained by doing the math.

If Alice makes 100 different bets against events that have a 90%
probability, she will be right 10 times and wrong 90 times. However,
because the odds given for each event were 19 to 1 (0.95/0.05=19), Alice
will still make a nice profit assuming all bets were made for the same
amount of money. In this case, if every bet was a 1000 AE bet, Alice
will make a profit of 5000 AE (10x950-90x50=5000).

**b) They reveal information using the price mechanism.**

Given that the participants in a prediction market are rewarded for
being correct and punished for being wrong, they will try and be
economically incentivized to be as accurate as possible and the prices
will reflect that. In prediction markets, prices can be understood as
showing the probabilities of the outcome that is being traded.

An example here could be a miner who wants to plan his hardware
purchases in advance and needs to know the probability of the total
hash rate getting past a certain level in the following six months. In
this case, instead of guessing or relying on his intuition, the miner
can set up the prediction market that will give him very accurate
probabilities. The people betting on those opportunities would not be
random people on the internet (As we see in normal forums), but
"experts", who will provide very likely guesses, as they will lose their
money if they are wrong, and will only gain money if they are right.

### 2. How do prediction markets work on æternity

Prediction markets (Oracles) are one of the most anticipated use cases
for blockchains. They can make possible the harnessing of the wisdom of
the crowds in a decentralised and transparent manner for the first time.

Ethereum has Augur and Gnosis trying to build prediction markets on top
of it, with each its different system and currency. æternity
differentiates itself, by integrating the oracle into blockchain
consensus.

Any user may create an oracle by posing a question or statement, staking
coins and providing a binary or a scaled answering option. AE coins can
be used to acquire stakes of those specific outcomes. The surer a
user is about the outcome, the more stakes he may acquire and hence more
likely (he thinks) the outcome will be correct. Applying the wisdom of
the crowd to all participating users of the prediction market, it is
possible to:

a) statistically predict the probability of a future event occurring

b) verify historic data from legacy systems or other blockchains

c) verify API data from legacy systems or other blockchains

Meaning any data outside the blockchain can be translated into a
deterministic value that can be used in æternity smart contracts, making
real-world data easily accessible and actionable.

And what is even better in æternity is that this source of information
would come from inside the Blockchain, and not from an outside entity
built on top of it. This makes the source of information more reliable,
more decentralised and not relying on a 3rd Party company or entity
(Like Augur and Gnosis).

##### Prediction Market - High Level Concept

![æternity prediction market](http://i66.tinypic.com/2emjrzm.jpg)

##### Oracle & Prediction Market - High Level Concept

![æternity oracle & prediction market](http://i63.tinypic.com/30c291s.png)

## Governance & Consensus

![æternity governance](http://i67.tinypic.com/axehab.png)

## Futarchy

Here follows a collections of in-depth analysis about Futarchy ordered
by publication date:
* [Futarchy: Vote Values, But Bet Beliefs - by Robin Hanson - July 2000](http://mason.gmu.edu/~rhanson/futarchy.html) see also papers from [2013](http://mason.gmu.edu/~rhanson/futarchy2013.pdf), [2007](http://hanson.gmu.edu/futarchy2007.pdf), [2003](http://hanson.gmu.edu/futarchy2003.pdf), [2000 (original)](http://hanson.gmu.edu/futarchy2000.pdf)
* [Futarchy vs. Predictocracy - by Robin Hanson - February 1st, 2008](http://www.overcomingbias.com/2008/02/futarchy-vs-pre.html)
* [An Introduction to Futarchy - by Vitalik Buterin - August 21st, 2014](https://blog.ethereum.org/2014/08/21/introduction-futarchy/)
* [Futarchy: Two-Step Democracy with Voting + Prediction Markets - by Melanie Swan - January 2015](https://books.google.it/books?id=RHJmBgAAQBAJ&pg=PA51&lpg=PA51&redir_esc=y#v=onepage&q&f=false)
* [Empirical Cryptoeconomics - by Vitalik Buterin - February 10th, 2016](https://www.reddit.com/r/ethereum/comments/453sid/empirical_cryptoeconomics/)
* [An Introduction to Cryptoeconomics and Futarchy experiments on Gnosis - by Matt Liston - Apr 28th, 2016](https://medium.com/@consensus/an-introduction-to-cryptoeconomics-and-futarchy-experiments-on-gnosis-df85220f840a)
* [Markets for the Future - by Matt Liston - May 4th, 2016](https://medium.com/@ConsenSys/markets-for-the-future-c73fa73fe35d)
* [DAOs, Democracy and Governance - by Ralph C. Merkle - May 31st, 2016 ](http://merkle.com/papers/DAOdemocracyDraft.pdf)
* [Response to Merkle’s DAO Paper - by Dan Finlay - Jun 16th, 2016](https://medium.com/@danfinlay/response-to-merkles-dao-paper-61d76d2dd333)
* [Merkle’s Futarchy - By Robin Hanson - July 6th, 2016](http://www.overcomingbias.com/2016/07/merkles-futarchy.html)
* [BFF: A Recursive Merkle DAO - by Dan Finlay - July 29th, 2016](https://medium.com/@danfinlay/bff-a-recursive-merkle-dao-121327d48493)
* A mathematics approach to Futarchy: [Prediction market mechanics - By Victor Shnayder & Mike Ruberry](http://www.eecs.harvard.edu/cs286r/courses/fall10/lecture/5-slides.pdf)

## Research

Publications dealing with æternity-specific technical concerns:

Turing-completeness - what does it mean, and what does it enable?

* [Stateful Turing-Complete Policies - by Vitalik Buterin](https://blog.ethereum.org/2015/11/09/stateful-turing-complete-policies/)
* [Godfather of Ethereum - by Yanislav Georgiev Malahov](https://medium.com/@yanislav/king-of-bitcoin-godfather-of-ethereum-a9af9ecf56d5)

State Channels - further reading and examples.

* [From Smart Contracts to Courts with not so Smart Judges - by Christian Reitwiessner ](https://blog.ethereum.org/2016/02/17/smart-contracts-courts-not-smart-judges/)
* [Universal Payment Channels By Jehan Tremback](http://jtremback.github.io/universal-payment-channels/universal-payment-channels.pdf)
* [Ethereum Lightning Network and Beyond - by Arcturnus](http://www.arcturnus.com/ethereum-lightning-network-and-beyond/) - a discussion of state channel significance and implementation on Bitcoin and Ethereum.
* [Raiden](http://raiden.network/) - forthcoming Ethereum state channel implementation.
* [Abstracted State Channels](https://github.com/AnnaIsAWang/LedgerLabsCoops2016/tree/master/AbstractedStateChannel) Example by Ledger Labs
* [Avocado](https://github.com/jtremback/avocado) - Example of an "judge" or oracle-based state channel implementation

Blockchains - spinal column of cryptocurrency past, present, and future.

* [Bitcoin: A Peer-to-Peer Electronic Cash System - by Satoshi Nakamoto](https://bitcoin.org/bitcoin.pdf)

Nontraditional DRAM architectures - background on innovations in Tromp's Cuckoo Cycle.

* [Rethinking DRAM Design and Organization for Energy-Constrained Multi-Cores - by Udipi et al.](https://www.cs.utah.edu/~rajeev/pubs/isca10.pdf)
* [The Dynamic Granularity Memory System - Yoon et. al](http://mbsullivan.info/attachments/papers/yoon2012dgms.pdf)

Consensus, Proof-Of-Stake, and Slasher

* [Proof of Stake: How I Learned to Love Weak Subjectivity by Vitalik Buterin](https://blog.ethereum.org/2014/11/25/proof-stake-learned-love-weak-subjectivity/)
* [Slasher: A Punitive Proof-of-Stake Algorithm by Vitalik Buterin](https://blog.ethereum.org/2014/01/15/slasher-a-punitive-proof-of-stake-algorithm/)
* [Slasher implementation by Zach Hess](https://github.com/zack-bitcoin/slasher)
* [Comparison of Failure Modes between Flying Fox Consensus and Traditional Byzantine Fault Tolerant Consensus by Zach Hess](https://github.com/BumblebeeBat/FlyingFox/blob/master/docs/failure_modes.md)
* [The Honey Badger of BFT Protocols by Miller et. al](https://eprint.iacr.org/2016/199.pdf)
* [On Stake and Consensus by Andrew Poelstra](https://download.wpsoftware.net/bitcoin/pos.pdf)(contrarian account)
* [A History of Casper by Vlad Zamfir](https://blog.ethereum.org/2016/12/06/history-casper-chapter-1/) A 5-chapter account.
* [Tendermint: Consensus without Mining by Jae Kwon](https://cdn.relayto.com/media/files/LPgoWO18TCeMIggJVakt_tendermint.pdf)

# Working Theories

# Open problems

## Optimal properties of consensus algorithms

## Censorship resistance

## Maximally accurate time stamping

## Scalable validation

## Optimal data availability solutions
