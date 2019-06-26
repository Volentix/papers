# ANG VOLENTIX VDEX WHITE PAPER

- Bersyon: 0.1.4
- Na-update nuong: 11-03-2019
- Website: www.volentix.io

## 1. PASIMULA

Inilunsad sa Volentix ang VDex, na dinisenyo bilang isang desentralisadong digital asset exchange na pinagtuunan ang user experience, ang pagpapaunlad ng komunidad, at pamamahala. Sa pamamagitan ng pag-akses sa mga itinatag na teknolohiya at pagpaplano ng mga bagong protokol na may prayoridad sa seguridad, bilis, awtentikasyon, madaling gamitin, kakayahang sumukat, at suporta sa multi-asset, VDex ay nagnanais na mapadali ang mga transaksyong peer-to-peer sa pamamagitan ng pag-assemble ng isang porporlyo ng mga desentralisadong aplikasyon na binuo sa EOS.Ito ang mga matatalinong kontrata.

Ang VDex ay inilunsad ang mga point anticipatena tumutugma sa mga kinakailangan sa disenyo ng Volentix para maging available na mga teknolohiya na pinapalampas sa EOS.IO desentralisadong operating system. Nais naming subukan ang aming mga haka-haka sa pamamagitan ng pag-prototype sa pamamagitan ng pasadyang software na EZEOS, na aming binuo at na-customize gamit ang mga tool ng linya ng command ng EOS.IO's cleos. Nakalagay ang software na ito sa: https://github.com/Volentix/ezeos

![](../main3-3000px.jpg)

## 2. VOLENTIX

Ang ekosistema ng Volentix ay umiiral sa ibabaw ng apat na mga pillar, isang nagsisimula ng maraming mga aplikasyon na partikular na kilala bilang Venue, Verto, Vespucci, at VDex.

### 2.1 VENUE

Ang Venue ay pinlano bilang isang daynamiko na plataporma ng komunidad na nagre-recruit at nakahanay sa mga miyembro ng komunidad ng Volentix para mapabilis ang pamamahagi ng VTX, ang katutubong digital na asset ng ekosistema ng Volentix, at upang itaguyod ang kamalayan ng mga pagkukusa ng Volentix.

Kamakailan inilunsad ang pag-test sa beta, ang Venue ay nagbibigay-daan sa mga gumagamit na makatanggap ng VTX bilang kapalit, halimbawa, para sa pakikilahok sa pagbubuo ng mga dedikadong komunidad, pagsusumite ng mga pag-aayos ng bug, at pagkuha ng mga bounty. Ang mga leaderboard at live na metriko ay sumasalamin sa pakikilahok ng gumagamit. Ang unang signature na kampanya ay inilunsad sa https://bitcointalk.org/ forum nuong Hulyo 13, 2018. Para sa karagdagang impormasyon mangyaring bisitahin sa https://venue.volentix.io.

### 2.2 VERTO

Ang Verto ay itinayo bilang isang multi-currency na wallet para gamitin sa VDex desentrilado na palitan, at nagnanais na mapadali ang personal na pag-iingat at lokal na pamamahala ng pribado at pampublikong mga key sa mga transaksyong peer-to-peer, na may layuning alisin ang mga panganib ng mga nagwawasak na pagkalugi ng taya na nauugnay sa mga traumatikong pagkabigo ng mga sentral na opereytor. Pinaplano ng Verto na mag-employ ng isang sistem ng mga matalinong kontrata para mapanatili ang estado sa pagitan ng dalawang trading client, ang pinakasimpleng operasyon na natapos sa atomic swaps.[1]

### 2.3 VESPUCCI

Ang Vespucci ay inaasahan bilang isang analytics engine naa-access sa pamamagitan ng isang user-friendly na interface na may treasure troves ng real-time at historikal na datos sa merkado, tulad ng mga digital na mga pang-rate ng asset at sentiment na pagsusuri. Nais naming bigyan ng kapangyarihan ang mga gumagamit na may mga tool para talaguhitan at ihambing ang mga tradeable digital assets, upang ma-akses at mai-parse ang historikal na mga talaan ng kalakalan, para mag-plot ng mga trend at mga pattern, at para masubaybayan at suriin ang mga pag-develop ng open-source software. Naglalayong dalhin sa iyong mga kamay ang tiwala at komprehensibong data ng Vespucci na nauugnay sa merkado sa pamamagitan ng pagsasama ng impormasyon na kasalukuyang nakakalat sa maraming iba't ibang mga block, website, chat room, at palitan.

### 2.4 VDEX

Ang ika-apat na pillar ng Volentix, ang VDex na palitan, ay ang tradable digital assets na plataporma na ipinakilala sa detalye sa white paper na ito. Para sa makinis at siguradong magagamit, pinaplano namin ang VDex para maisama ang iyong sariling personal na Verto na wallet at interface ng Vespucci. Inaasahan namin na mapamahalaan ng VDex ang mga transaksyon na kinasasangkutan ng parehong VTX at ang malawak na hanay ng mga digital na asset at mga blockchain na umiiral oras-oras sa buong mundo. Dini-develop namin ang Venue bilang isang komplimentaryong adjunct lalo na para magbigay-diin at i-drive ng mga katutubong VTX-based na inisyatibo.

## 3. ARKITEKTURA

![](../8.jpg)

#### 3.0.1 Operating system

Sinuri namin ang iba't ibang mga operating system bilang mga candidate para sa substructure ng aming VDex na palitan. Bagama't pinararangalan natin ang natapos na gawain ng isang bilang na itinatag na mga lider sa mga digital na asset at blockchain na teknolohiya, kabilang sa mga trailblazer na ang gawain ng EOS.IO bilang isang operating system na tulad ng balangkas kung saan ang mga desentralisadong aplikasyon ay maaaring itayo, sa aming opinyon, bilang kapuri-puri. Software na nagbibigay ng mga akawnt, awtentikasyon, database, asynchronous na komunikasyon, at pag-iiskedyul ng mga klaster. Ang mga bahagi at mga protokol ay naitayo na sa plataporma, at isang subset ang pwedeng magamit para masunod ang aming mga kinakailangan sa VDex. Unang makikinabang ang VDex mula sa mga karaniwang katangian na inalok ng EOS.IO tulad ng paglikha ng akawnt at wallet at pag-rekober ng mga ninakaw na key, pero plano namin sa dakong huli na ipatupad ang mga protokol para sa paglikha ng isang desentralisado na palitan sa pamamagitan ng mga kontrata ng EOS at iba pang mga tool.[2] Narito ang isang buod ng naghihikayat sa mga pamamaraan:

### Konteksto ng mga Libreng Aksyon

Karamihan sa teknik na iskabilidad na iminungkahi ng Ethereum (Sharding, Raiden, Plasma, State Channels) ay nagiging mas mahusay, parallelizable, at praktikal habang tinitiyak din ang mabilis na inter-blockchain na komunikasyon at unimpaired na iskabilidad. Ang isang Konteksto ng Libreng Aksyon ay nadadamay ng mga pag-compute na nakasalalay lamang sa datos ng transaksyon, at hindi sa estado ng blockchain.

### Binary/JSON na pang-convert

Ang EOS ay pinagsasama-sama ang human readability ng JSON sa kahusayan ng binary.

### Paralesisasyon at optimisasyon

Ang paghiwalay ng awtentikasyon mula sa aplikasyon ay nagpapahintulot sa mas mabilis na mga oras ng transaksyon at nagdaragdag ng bandwidth. Bawat 500ms ay inuulat ang mga ginawa sa mga block ng EOS.IO.

### Web Assembly(WASM)

Ang Web Assembly ay nagbibigay-daan sa mga Web na aplikasyon na may mataas na pagganap at sinisiguro din ang bawat aplikasyon sa sarili nitong sandbox, kung saan ang mga functionality ng VDex ay pwedeng makakuha ng akses sa network, mga paghihigpit sa namespace ng filesystem, at pagpapatupad ng pagpapatupad batay sa patakaran.

### Rust/C++ na mga kontrata

Ang kilala at tanyag na programming language na C++ ay lilitaw na lubhang angkop para sa WASM. Ang C ++ ay may mataas na mature na suporta sa pagde-debig at mga library. Ang codebase ng EOS ay gumagamit ng mga template na liberally, at C++ ay nagpapahintulot sa paggamit ng mga template at opereytor sa pag-overload para tukuyin ang isang runtime cost-free na balidasyon ng mga yunit. Ang program ay ini-reinitializes para linisin ang estado sa simula ng bawat mensahe, isang natatanging kalamangan na streamlines pagbabalangkas ng mga matalinong kontrata. Ang framework ng WebAssembly ay awtomatikong tatanggihan ang anumang transaksyon na tumutugon sa memory nang hindi wasto. In case dynamic memory allocation is necessary, users can depart to smart pointers because EOS.IO contracts use C++14. It is noteworthy that the first implementation of PARSEC Directed Acyclic Graph (DAG) technology is expected to be in Rust.

#### 3.0.2 Schema defined messages and database

Service contracts are standardized to provide a baseline measure of interoperability between and among disparate systems by harmonization of data models. Indeed, the Standardized Service Contract design principle advocates that service contracts be based on standardized data models. Analysis is done on the service inventory blueprint to find out the commonly occurring business documents that are exchanged between services. These business documents are then modeled in a standardized manner. The Canonical Schema pattern reduces the need for application of the data model transformation design pattern. [3]

#### 3.0.3 Inter-Contract Communication

Data is shared between contracts via an oracle, which, "in the context of blockchains and smart contracts, is an agent that finds and verifies real-world occurrences and submits this information to a blockchain to be used by smart contracts.” [4] Every node will have an identical copy of these data, for use in smart contract computation. Rather than the smart contract functioning to pull the data, instead the oracle pushes the data onto the blockchain. In the instance of a blockchain, most reading of the data is done via polling "models" in order to monitor blockchain state and to perform certain responsive actions.

#### 3.0.4 Sidechains

In EOS.IO, issuance of a digital asset creates a sidechain, which is an emerging mechanism permitting digital assets from one blockchain to be securely used in a separate blockchain and then moved back to the original blockchain. Efficiency of processing is promoted by creating multiple sidechains. A TCP-like communication channel between different blockchains evaluates proofs. For each shard (a unit of parallelizable execution in a cycle), a balanced merkle tree is constructed of these action commitments to generate a temporary shared merkle root; this is done for speed of parallel computation. The block header contains the root of a balanced merkle tree the leaves of which are the roots of these individual shard merkle trees. [2]

#### 3.0.5 Liquidity

A digital asset is liquid if it is easily sold or purchased in ordinary trading volumes without a significant short-term impact on its prevailing market price. In order to achieve such a status, traditionally any tradable asset must surmount a trading volume threshold sufficient to support stability. Specifically, we anticipate adopting the following methodologies: Loopring protocol with the use of EOS.IO contracts acting as nodes.[5] Bancor algorithm used to bring stability to the digital asset.[6] Toggles between these protocols and HTLC (atomic swaps) according to Vespucci analyses on the VDex network.

#### 3.0.6 Hashed Timelock Contracts (Atomic Swaps)

A Hashed Timelock Contract (HTLC)[1] is a smart contract enabling the implementation of time-bound transactions. Users will be offered a variable lock-in period for their transactions, with a discount on transaction fees in exchange for choosing a longer lock-in period.

### 3.1 NETWORK TOPOLOGY

#### 3.1.1 Nodes

![](../9.jpg)

Nodes are the endpoints of the VDex exchange. Their functions are:

1. Act as portals to VDex through the Verto wallet.

2. Merge order book information.

3. Settle order book.

4. Manage order cancellation.

5. Assign timeouts for the RAFT protocol.

6. Initiate contracts for orders that have been filled.

Nodes earn a portion of the fee for each transaction. If a user has sufficient funds and possesses a good track record, his or her Verto wallet can act as a node.

#### 3.1.2 Aggregators

The VDex aggregators are dedicated Volentix servers for simulator and security purposes. One of their functions is to pull logs and order book data from nodes into sparse distributed representations for hierarchical temporal memory as intrusion [7] analysis for detecting anomalies in the system. The aggregators will also be host to other components such as metachain ledgers and blockchain scrapers.

#### 3.1.3 Latency

EOS.IO has low latency block confirmation (0.5 seconds).[5] This degree of latency can be maintained in transactions with other blockchains if those chains admit of similar latency. But fundamentally the transaction is only as rapid as the lesser-rapid chain in the equation. It is well known, for example, that a Bitcoin block requires approximately ten minutes for processing. Receiving a transaction hash does not mean the transaction is confirmed; it means only that a node accepted the transaction without error, although there is generally a high probability other block producers will accept it.

### 3.2 ORDER BOOK

The order book is the list of buy-and-sell orders VDex records from interested users. Isang magkatugma na engine ay gumagamit ng isang order book para matukoy kung aling mga order ang matutupad. Ang protokol na Loopring ay nagpapahintulot para sa pagpapasadya ng istraktura ng datos ng order book.[5] Ang mga container na ibinigay ng EOS.IO ay maaaring gamitin para sa mahusay na pagganap.[8]

#### 3.2.1 Mga istraktura ng datos

Gamit ang FIFO ng protokol na Loopring (first-in first-out) na circular buffer, na pwedeng mag-disenyo ng mga node ang kanilang order book para maipakita at tumutugma sa isang gumagamit ng order. Ang metodong ito ay sumusunod sa isang modelo ng OTC, kung saan ang mga order ng limitasyon ay nakaposisyon batay sa presyo lamang.[5]

Ang EOS.IO ay tinutukoy ang persistence na API, ang order book ay pwedeng samantalahin ang makapangyarihang multi-index na container na ibinahagi sa mga node sa pamamagitan ng parehong akawnt na EOS.IO.

#### 3.2.2 On-Chain order book

An on-chain order book is a record of offers residing on the wallet (node) chosen to settle the order book. It resides in a persistent database on each node subscribing to the same account as all the other nodes.

#### 3.2.3 Off-Chain order book

Residing on the aggregator, offline order books serve for simulator and security purposes.

#### 3.2.4 Decentralization process of order book settlement

For decentralization purposes, nodes will take turns to settle the order book. The settling node must be designated by the protocol and all order book entries from all nodes must be available to the settling nodes. We believe the RAFT[9] and PARSEC[10] consensus mechanisms offer effective solutions. RAFT is a well-established algorithm and is easy to implement.[7] PARSEC is more recent and more efficient, using Directed Acyclic Graph (DAG) technology and eliminating the need for copying logs.

### 3.3 ORDER SETTLEMENT

Order settlement contains familiar elements of conventional financial market transactions. Utilizing FIFO technology to design the order book, VDex intends to check order, inventory, and fill rate, as well as limit orders and cancellations. ![](../7.jpg)

### 3.4 VTX

#### 3.4.1 VTX Issuance and Use

VTX is the native digital asset to be issued and used on the VDex decentralized exchange. We currently plan to use an eosio.token contract from the EOS.IO framework to issue 2.1 billion EOS.IO-compliant VTX tokens with a supply of 1.3 billion. VTX will have a diverse array of uses, for example:

To reward participants in the consensus process and in Venue campaigns.

To pay and redistribute transaction fees on the VDex exchange.

To submit and vote on proposals to the Volentix ecosystem, using the voting rights allocated to VTX holders.

To stake support for reviewing proposals and implementing projects.

To incentivize users to participate in order book settlement by becoming nodes via their Verto wallets.

To incentivize users to lock funds in for >24 hours by HTLC time-bound transactions.

#### 3.4.2 VTX Allocation

![](../6.jpg)

A digital assets ecosystem requires an array of certain fundamental human constituents who shepherd the project forward.[11] It is essential to compensate those individuals for their participation. Subject to adjustment, Volentix currently anticipates the following allocations:

1. Contributors. 12%. An array of individuals, akin to founders, who contribute insights, time and talent, though often work without early compensation.

2. Supporters.

Phase 1. 5%. Early passive seed funders.

Phase 2. 28%. Funders via qualified private pre-sales and possible public sale.

3. Facilitators. (Advisors, Developers, Promoters, Custodians). Note that requirements for assistance from the sub-categories in this category may differ significantly before and after the project receives substantial funding support, but certain individuals may serve during both phases.

Phase 1. 10%.

Phase 2. 10%.

4. Decentralized treasury. 35%. Community members incentivized and rewarded for participation in progressive development of a decentralized autonomous organization (DAO). A decentralized treasury is anticipated to be administered by smart contracts and community consensus. ![](../5.jpg)

#### 3.4.3 VTX Distribution

In light of market conditions at the time of this writing, Volentix is considering timing, means, and terms and conditions of VTX distribution as a function of private pre-sales and possible public sale. Please monitor our website for updates.

### 3.5 EOS.IO PLATFORM DEPLOYMENT

The following considerations are relevant to our deploying the VDex exchange on the EOS.IO platform:

Deploying a contract has a cost but is free to use.

Developers stake EOS.IO-compliant tokens to deploy a smart contract. After the contract is deployed, the locked tokens are returned.

Decentralized applications allocate memory, CPU, bandwidth, and other resources to their contracts.

Multiple messages and multiple accounts can be assigned to the same thread.

### 3.6 BLOCKCHAIN INTERACTION

#### 3.6.1 Inter-Blockchain Communication

EOS.IO is designed to make Inter-Blockchain Communication (IBC) proofs lightweight. For chains with insufficient capacity for processing the IBC proofs and establishing validity, there is an option to default to trusted oracles/escrows. With an EOS.IO-based smart contract, a trusted multi-signature wallet holding the asset in escrow can be used to persuade the signing/publishing of the transaction based on IBC proofs from the originating chain.

#### 3.6.2 Multi-Blockchain Information

Comprehensible multi-blockchain information can be obtained by aggregating blockchain timelines in parallel order (with variance in the frequency of change of state). This system can trigger multi-chain load balancers, transfer states, draw data outputs from smart contracts, and foreign blockchain transaction execution. Relative block distance, relative global state, and timestamped events are recorded on a global ledger to optimize and confirm transactions before they actually happen on the native chain. This approach could also be used to determine block production coincidence between chains to access greater liquidity.[12]

### 3.7 SECURITY CONCERNS

To shake out certain assumptions, we intend to commence security testing following the prototyping phase. Security concerns are of paramount importance to users and must be addressed. Threats include, for example, an attacker executing malicious code within a transaction or manipulating the order of transactions or the timestamps of blocks. In the following sections, we address certain security measures and specific security threats and remedies.

### 3.8 SECURITY MEASURES

#### 3.8.1 Contract security

Retain vast majority of funds in a time-delayed, multi-signature-controlled account.

Use multi-signatures on a hot wallet with several independent processes/servers double-checking all withdrawals, with the concomitant benefit of creating a trusted list of accounts.

Deploy a custom contract that allows withdrawals only to accounts verified by KYC/AML.

Deploy a custom contract that accepts only deposits of known assets from accounts verified by KYC/AML.

Deploy a custom contract that requires a mandatory 24-hour waiting period for all withdrawals.

Utilize contracts with hardware wallets for all signing, including for automated withdrawals.

Upgrade broken contracts.

Include ability to pause the functionality of a contract.

Include ability to delay an action of a contract.

#### 3.8.2 Auditing rogue processes

The advanced anomaly detection algorithms provided by Numenta’s Nupic library will require less voluminous training data sets than conventional AI systems.

#### 3.8.3 Randomization

True randomisation of address space layout, route or utilizing varying lengths of timeouts as in the RAFT protocol can complexify systems enough to enhance resilience and further secure systems against a side-channel attack or front running.

#### 3.8.4 Log inspection

Parsec does not rely on logs for the determination of consensus. On the other hand, RAFT will require this. In any case, Validator nodes will be designed to require minimal information To determine consensus as to minimize the transaction process time.

#### 3.8.5 Transaction as Proof of Stake (TaPoS)

This mechanism prevents the replay of a transaction on forks that do not include the referenced block. Signals the network that a particular user and stake are on a specific fork.

### 3.9 Security threats and remedies

#### 3.9.1 Double spend

A double spend is an attack in which a particular cryptocurrency stake is spent in more than one transaction.

A race attack occurs when two conflicting transactions are sent in rapid succession into the network.

A Finney attack pre-mines one transaction into a block and spends the same tokens before releasing the block to invalidate that transaction.

A 51% attack can be mounted by anyone owning >50% of the total computing power of a network. A majority ownership position permits reversal of any transaction and allows total control of selection of transactions appearing in blocks. EOS.IO, Loopring, and RAFT appear to prevent this problem. If a block producer takes an unreasonable amount of runtime or is not sufficiently profitable, then the process is blacklisted.[5]

#### 3.9.2 Front running

A front runner steals one or more orders from a pending order book settlement transaction. Both EOS.IO and Loopring offer remedies in which keys are protected because they are not part of the on-chain transaction, and therefore remain unknown to parties other than the owner. Only the order book settling node is possessed of the sensitive information, and each node uses a different solution for resolving the order books, introducing yet another level of complexity to promote security.

#### 3.9.3 Forged identities

Malicious users create forged identities to send a large number of small orders to attack Loopring nodes. However, most of these orders will be rejected for not yielding satisfying profit when matched.

#### 3.9.4 Insufficient Balance

Malicious users sign and spread orders the value of which is non-zero but the address of which has a zero balance. Nodes monitor actual balances, update these order states accordingly, and then discard them.

#### 3.9.5 Timing attack

Timing attacks are a class of cryptographic attacks through which a third-party observer can deduce the content of encrypted data by recording and analyzing the time taken to execute cryptographic algorithms. The RAFT algorithm prevents timing attacks by using randomness of timeouts.

### 3.10 USER EXPERIENCE

Our focus on user experience is primary. We wish to make VTX and the four pillars of Volentix -- Venue, Verto, Vespucci, and VDex -- easily accessible to and useable by all those who wish to join our community. We expect the experience continually to be educational as well, with templates and simulators to support a superior UX/UI relationship.

### 3.11 TRUE DECENTRALIZATION

EOS.IO is an open-source, scalable infrastructure for decentralized applications. Its goal is a fair and transparent block producer (BP) election process utilizing a democratic delegated proof of stake (DPoS) consensus. Particularly as such a system just begins to proliferate, there will be glitches. Therefore, some degree of retained centralization is inevitable and necessary. But our guiding philosophy is one of decentralization, and our ongoing efforts are targeted to promoting a reduction in dependence on central authority.

For example, initially we plan to erect a system for electing nodes (when solving order books) that will not use a shared central clock or DPoS but instead will be based either on random timeouts for the determination of leaders in an election (RAFT) or on Directed Acyclic Graph (DAG) in the PARSEC protocol.

### 3.12 SYSTEM RECOVERY

The RAFT and PARSEC protocols provide a robust system for recovery in the case of node failure. Security measures are also provided for trading between and among native blockchains. If a chain defies identification, the system defaults to the next block or a short time lock.

### 3.13 EVOLVING ARCHITECTURE

Daily announcements of fresh code developments impacting on use of digital assets reveal the tremendous benefit of the open-source code philosophy. We at Volentix recognize we are the beneficiaries of the enormous financial resources dedicated by many early movers to developing digital assets applications over the past decade. We now have an opportunity to take the next step by creating VDex, a decentralized exchange for the next generation of digital assets transactions.

## 4. CONCLUDING THOUGHTS

All of us at Volentix are dedicating our work and insights to developing a program premised on empowerment and independence. If you are of a mind to join us, in whatever capacity, then please do so and please become educated on the topics contained in this white paper and additional Volentix publications as we share them with our community.

## 5. TIMELINE

Please monitor our website and social media for updates and other important announcements. Thank you very much for your attention and interest.

## DISCLAIMER

This white paper was prepared, and is presented, for information purposes only. The information presented does not purport to be comprehensive. The information is subject to change in whole or in part at any time without notice. Volentix Labs reserves the right to amend, replace, remove, or delete any and all information at the sole and exclusive discretion of Volentix. Volentix Labs makes no representation or warranty, expressed or implied, concerning the accuracy or completeness of the information and expressly disclaims any and all liability of any and all kinds whatsoever for the information contained or not contained. Volentix Labs requests each and every reader to read the information fully and carefully, and to undertake independent investigation and analysis of the information, and to seek and obtain professional advice for purposes of evaluating the information. To the knowledge of Volentix Labs, no regulatory agency, government, or other third-party enforcement entity has reviewed, evaluated, or approved any part or all of the information. This information is not an offer or solicitation of any kind whatsoever and does not form the basis for any contract or commitment of any kind whatsoever. Any statement considered to be forward-looking is purely a matter of opinion, and no viewer should rely on any such statement or on any part or all of the information in any way whatsoever.

## FOOTNOTES

1. K. Kurokawa, Atomic cross chain transfer, an overview, (2015).

2. EOS.IO, Eos.io technical white paper v2, (2018).

3. T. Earl, Soa principles of service design, (2016).

4. blockchainhub.net, blockchain-oracles, (2017).

5. F. Zhou, Wang, Loopring: A decentralized token exchange protocol, (2018).

6. G. B. Eyal Hertzog, Guy Benartzi, Bancor protocol: Continuous liquidity for cryptographic tokens through their smart contracts, (2018).

7. L. Lamport, The part time parliament, (1998).

8. D. Larimer, eosio.boot telegram chat, (2018).

9. J. O. Diego Ongaro, In search of an understandable consensus algorithm, (2018).

10. F. H. Q. M. S. S. Pierre Chevalier, Bart lomiej KamiÂťnski, Protocol for asynchronous, reliable, secure and efficient consensus (parsec), (2018).

11. Dane Keller Rutledge, Fundamental Human Constituents of a Digital Assets Ecosystem (DAE). (2018).

12. BlockColliderTeam, Block collider white paper, (2018).

## SUPPLEMENTAL REFERENCES

Aelf, A multi-chain parallel computing blockchain framework, (2018).

ARK, A platform for consumer adoption, (2018).

V. Buterin, Ethereum: a next generation smart contract and decentralized application platform, (2013).

S. Cormier, A machine based societal model for curbing citizen cynicism, (2017).

M. Duncan, Quale, Halo platform, (2018).

S. D. K. M. T. S. H. Garcia-Molina, The eigentrust algorithm for reputation management in p2p networks, (2018).

M. R. Garrick Hileman, Global cryptocurrency benchmarking study, (2017).

Komodo, An advanced blockchain technology, focused on freedom, (2018).

Q. Liquid, Providing liquidity to the non-liquid crypto economy, (2018).

S. R. M.P.M-S, Aniket Kate Matteo Maffei, Concurrency and privacy with payment-channel networks, (2017).

SingularityNET, A decentralized, open market and inter-network for ais, (2018).

M. M. Timo Hanke and D. Williams, Dfinity technology overview series consensus system, (2018).

A. B. Will Warren, 0x: An open protocol for decentralized exchange on the ethereum blockchain, (2017).

G. Wood, Ethereum: A secure decentralised generalised transaction ledger.ethereum project yellow paper, (2014).

Dane Keller Rutledge, Creating a Comprehensive Digital Assets Ecosystem (DAE), (2018).

## END OF PAPER