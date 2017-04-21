![FAQ image](https://cdn-images-1.medium.com/max/1400/1*zsBAnzRQJuhIJ4phSDoEEA.png)

Table of Contents
=================

   * [Table of Contents](#table-of-contents)
   * [How is Aeternity different from Ethereum?](#how-is-aeternity-different-from-ethereum)
   * [Why is Aeternity faster than Ethereum?](#why-is-aeternity-faster-than-ethereum)
   * [How does Aeternity protect from the next DAO happening?](#how-does-aeternity-protect-from-the-next-dao-happening)
   * [Is smart contract verification on the roadmap?](#is-smart-contract-verification-on-the-roadmap)
   * [How does on-chain conflict resolution work? (crypto-court)](#how-does-on-chain-conflict-resolution-work-crypto-court)
   * [What is the Circulating Supply of AE?](#what-is-the-circulating-supply-of-ae)
   * [What is Maximum Supply of AE?](#what-is-maximum-supply-of-ae)
   * [Can malicious rich people make an oracle lie?](#can-malicious-rich-people-make-an-oracle-lie)
   * [How does aeternity compare to ...?](#how-does-aeternity-compare-to-)
   * [æternity, a new blockchain?](#æternity-a-new-blockchain)
   * [What can the AE token be used for?](#what-can-the-ae-token-be-used-for)
   * [What are some of the more interesting applications that can be created on æternity?](#what-are-some-of-the-more-interesting-applications-that-can-be-created-on-æternity)
   * [What makes æternity smart contracts special?](#what-makes-æternity-smart-contracts-special)
   * [What are some of the features of æternity virtual machine?](#what-are-some-of-the-features-of-æternity-virtual-machine)
   * [Why do we need Ethereum?](#why-do-we-need-ethereum)
   * [What is the legal status of æternity?](#what-is-the-legal-status-of-æternity)
   * [What’s the difference between an account and the æternity wallet?](#whats-the-difference-between-an-account-and-the-æternity-wallet)
   * [Will there be different types of nodes in æternity?](#will-there-be-different-types-of-nodes-in-æternity)
   * [What can I expect to happen from æternity in the near future?](#what-can-i-expect-to-happen-from-æternity-in-the-near-future)

# How is Aeternity different from Ethereum? #

On Ethereum contracts exist on-chain for multiple blocks. They hold state and can interact with other contracts.
On Aeternity each contract only exists for a moment. It is settled independently of all the other contracts.

# Why is Aeternity faster than Ethereum? #
Since contracts on Aeternity are independent, they can be processed in parallel.

On Ethereum it is possible to move computation, but it is much more complicated than standard contracts. A lot of boilerplate code needs to be reimplemented for every contract.

On Aeternity computation by default happens off-chain.

# How does Aeternity protect from the next DAO happening? #
Since contracts are independent, it is much easier to prove and verify what each contract does.

The DAO was a problem where some people trusted other people to spend their money for them.
If you give your money to someone, and trust them to spend it for you wisely, there is nothing that I can do to stop them from robbing you.

Aeternity supports many trustless contracts. There is no reason you should ever use trust with Aeternity, or any other blockchain system.
Any smart contract that requires trust is not so smart.

# Is smart contract verification on the roadmap? #

The language for Aeternity is very simple. Smart contracts do not depend on each other's state, so it is easy to prove the correctness of a smart contract.
We wont need any special verification software to be sure of the correctness of Aeternity contracts.

Channels can be connected to each other using hashlocking. This is how cross chain atomic swaps work. This is how the lightning network works. This is how we can build prediction markets with more than 2 users.

# How does on-chain conflict resolution work? (crypto-court) #

Answer by agorism1337 from [reddit](https://www.reddit.com/r/Aeternity/comments/64x1u7/how_does_onchain_conflict_resolution_work/).

It is possible that you each submit conflicting final channel states to the blockchain. The blockchain processes both options, and examines which has a higher nonce. The higher nonced version of the state is accepted, and the other is rejected.

So every time we make a channel payment or update the channel state, we also have to update the nonce in the channel state. That way the blockchain will prefer the most recent channel state we made.

The blockchain is not completely stateless. It keeps a record of each account balance, and the results of every oracle, and some other things. What is important for scalability is that channels cannot edit any shared memory. It is deterministic to let processes read data in parallel, but it is not deterministic to let processes edit data in parallel. Since channels can't edit shared memory, we can process all the channel transactions in parallel.

# What is the Circulating Supply of AE? #
AE currently in circulation: TODO

AE in circulation after contribution phase 2: TODO

# What is Maximum Supply of AE? #
Answer by vdramaliev on [reddit](https://www.reddit.com/r/Aeternity/comments/64z73r/will_there_have_the_cap_amount_of_aeon/).

It is very much possible for the mining reward amount to be modifiable by the users through a prediction market.

# Can malicious rich people make an oracle lie? #

Answered by agorism1337 on [reddit](https://www.reddit.com/r/Aeternity/comments/64x733/the_highest_stakes_the_whales_decide_what_will_be/). (modified)

If people try to make the oracle lie, then the blockchain ends up forking into two. One side is honest, and the other is dishonest. The attackers lose their bets on both side of the fork, and the defenders win their bets on both sides. The side that answers the question honestly is the official Aeternity blockchain, the other is a new altcoin.

The people who caused the attack lose all the money they attacked with. The defenders all earn twice as much money as they used to defend with.

Even a whale can't afford to do this attack many times, and we quickly recover after each attack with an honest oracle.

# How does aeternity compare to ...? #

Based on replies by agorism1337 at reddit from [here](https://www.reddit.com/r/Aeternity/comments/63tabp/aeternity_vs_qtum_vs_cosmos/) and [here](https://www.reddit.com/r/Aeternity/comments/63mhg7/how_does_aeternity_contrast_with_truebit/).

* Ethereum is a turing complete stateful smart contract system. It allows for examples apps like: subcurrencies, domain name servers, and blackjack card game gambling.
* Cosmos is a way to move coins from one blockchain to another.
* Qtum is a proposal for a software suite for making dapps on blockchains like Aeternity or Ethereum.
* Ethereum's oracle systems, like Augur and Gnosis, will probably be much more expensive than the Aeternity oracle. Aeternity's oracle is market based instead of voting based. Aeternity's oracle is connected to the blockchain consensus mechanism in a way that makes it more secure.
* Aeternity is a turing complete stateless smart contract system with a built in oracle. It allows for the creation of trustless Dapps. For example: insurance, sports betting, stablecoins, prediction markets, insured crowdfunding, blackjack card game gambling.

# æternity, a new blockchain? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

Yes, æternity is a next-level, brand new blockchain technology in the making, with many features that tackle current issues of blockchain systems in an elegant way.

One can learn more about æternity’s blockchain technology by [looking at the whitepaper](https://uploads.strikinglycdn.com/files/8a476e2a-e859-4e5b-8d37-a21c88b1cf93/aeternity-trustless-decentralized%20%2853%29.pdf). Going through it is the best way to understand æternity’s technology design.

Interested to see some action? Access our Twitch account to look at our live coding sessions. We also have a [public Gitter chat](https://gitter.im/aeternity/Lobby). More channels coming soon!

æternity’s first testnet is now online. You can use it in order to check out some of its features. You can create an account and start mining AE right away. Start interacting with æternity by visiting [GitHub](http://github.com/aeternity/testnet).

# What can the AE token be used for? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

AE are the access tokens to the æternity blockchain and act as a unit of account for the resources spent on æternity. AE are the energy (or “crypto-fuel”) used to power any application implemented on the platform. Every action (and even inaction) on the æternity platform costs something, even if only fractions of cents.

AE are the fuel for the new types of trustless apps that will be be enabled. For more information regarding applications, consult the [æternity whitepaper](https://uploads.strikinglycdn.com/files/8a476e2a-e859-4e5b-8d37-a21c88b1cf93/aeternity-trustless-decentralized%20%2853%29.pdf), visit the [website](http://www.aeternity.com/) or continue reading this FAQ.

# What are some of the more interesting applications that can be created on æternity? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

æternity enables a high transaction throughput. Broadly speaking, any type of application that requires high transactional speed will run smoothly on æternity. Here are some of those:

* Nano and micro payments.
* Smart-contracts using oracles to initiate millions of parallel transactions.
* Side-chained blockchain networks that can communicate efficiently and securely.
* Multiplayer video games where the rules are enforced by the blockchain. Poker, chess, Go, first person shooter games.
* Investment opportunities for ventures that are specializing in predicting the price of food.
* Contracts for powering crowdsales to finance public goods and create a sustainable economy.
* Lie detectors to know when leaders or experts are hiding the truth.
* Prediction markets that can help us better prepare for the future.
* Everything else that we (and You) haven’t thought of yet.

# What makes æternity smart contracts special? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

Manifold factors contribute to æternity’s uniqueness! One major advantage of æternity smart contracts is the fact that they are created off-chain. This allows to — once created — to interact with other participating parties blazingly fast and has important privacy implications. The users’ interactions stay off-chain and are kept secure. Only in cases of disagreement, a transaction will be submitted on-chain. The æternity blockchain will function as a crypto-court.

Furthermore, there is no limit to the volume of smart contracts that can be processed per second, since æternity smart contracts don’t share state, they can be processed in parallel.

In comparison to ‘legacy’ Ethereum, we switched from being goto-based to being function-based. Thus, it is a lot simpler to reason about and write more secure smart contract code.

# What are some of the features of æternity virtual machine? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

We are building a state-of-the-art virtual machine for secure and efficient blockchain computations. For example, we have added a tool for ‘merklizing’ the code, so that the users only publish the portion of code that actually gets executed.

æternity’s smart contracts can be massive, gigabytes to terabytes in volume, not a problem — as long as the part that gets executed is relatively small.

# Why do we need Ethereum? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

The primary reason for using Ethereum-created tokens for the token sale is that æternity is not functional yet. Once æternity launches, tokens will exist on æternity. However even if æternity did exist, it wouldn’t give us the ability to do a decentralized token sale — Ethereum is great for this type of use-cases, that require a fully public index of things (e.g. tokens, …). æternity is focusing on scalable, real-world uses-cases. Most of those don’t require data to be openly shared all of the time.

# What is the legal status of æternity? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

We will provide a rock-solid technology to build on, but that wouldn’t be enough if it wasn’t based on a legally safe foundation. æternity is incorporated in Liechtenstein and is in regular contact with regulators to keep track of the project’s legal status. The team includes a legal adviser and makes use of additional legal consultancy on an ad-hoc basis.

# What’s the difference between an account and the æternity wallet? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

A wallet is a piece of software that is used to interact with æternity. It allows you to make accounts and channels. It will allow users to make channel contracts, to bet, to play games, to buy/sell assets, provides identity, communicate with other users, etc.

# Will there be different types of nodes in æternity? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

Yes!

* Some nodes will be providing liquidity to the lightning network. They will have lots of channels with lots of people, so if you make a channel with them, you will be able to establish state channel contracts with many users. Using a channel contract through such a node will involve a fee.
* Some nodes will run trustless exchanges for any asset. They will also collect transaction fees. We envision nodes that let people use state channels to play games like Go, Monopoly, slot machines, or poker. Either single player, or with your friends, or with strangers. æternity enables trustless financial applications. They are not necessarily decentralized. Anyone can start a “centralized server” and use our software to create trustless financial tools.
* There can be ‘servers/nodes’ which you can use to invest in stocks, derivatives or metals. You can gamble at sports in a fully trustless and efficient way. Other nodes can specialize in recycling old accounts. There is a fee for having an account open. If the account runs out of money, anyone will be able to delete it and get a small reward.
* Some nodes will just run trading software. They will buy and sell assets offered by market makers in order to make a profit. Some nodes will specialize in participation in prediction markets, running the consensus mechanism. This will be profitable because transaction fees are the initial liquidity in these markets.

# What can I expect to happen from æternity in the near future? #
source: [website FAQ](https://blog.aeternity.com/%C3%A6ternity-frequently-asked-questions-faq-9cb0e34e0740)

The first testnet is now ready! We will be adding more features all the time. Start interacting with æternity by visiting [GitHub](http://github.com/aeternity/testnet).

Your feedback will be highly appreciated! Join our [public chat on Gitter](https://gitter.im/aeternity/Lobby).

You can also get in touch with us through our [Facebook page](https://www.facebook.com/aeternityproject), [Twitter profile](https://twitter.com/aetrnty), [LinkedIn](https://www.linkedin.com/company/aeternity) account, [Bitcointalk post](https://bitcointalk.org/index.php?topic=1733140.0) and our [subreddit](https://www.reddit.com/r/Aeternity).

A detailed roadmap is also in the making. You can get an update on this by [subscribing to our newsletter](http://www.aeternity.com/#newsletter).