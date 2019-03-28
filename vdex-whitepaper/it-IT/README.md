# THE VOLENTIX VDEX WHITE PAPER

- Versione: 0.1.4
- Aggiornata il: 11-03-2019
- Sito web: www.volentix.io

## 1. INTRODUZIONE

Volentix presenta VDex, progettato come una piattaforma decentralizzata per lo scambio di beni digitali con enfasi sull'user experience con amministrazione e sviluppo gestiti dalla comunità. Attraverso l'utilizzo di tecnologie già esistenti e programmando nuovi protocolli selettivi dando priorità a sicurezza, velocità, autenticazione, facilità di utilizzo, scalabilità, e supporto multi-asset, VDex vuole facilitare le transazioni di tipo peer-to-peer mettendo insieme un portfolio di applicazioni decentralizzate costruite sulla base degli smart contract di EOS.IO.

The VDex launch point anticipates matching Volentix's design requirements to available technologies superimposed on the EOS.IO decentralized operating system. Abbiamo intenzione di testare le nostre ipotesi creando dei prototipi tramite software EZEOS personalizzato, che abbiamo costruito e personalizzato attraverso gli strumenti a riga di comando cleos di EOS.IO. Questo software risiede in: https://github.com/Volentix/ezeos

![](../main3-3000px.jpg)

## 2. VOLENTIX

L'ecosistema Volentix esisterà sulla base di 4 pilastri, un array di applicazioni di inizializzazione specificamente note come Venue, Verto, Vespucci, e VDex.

### 2.1 VENUE

Venue è progettato come una piattaforma comunitaria dinamica che recruta e assegna i membri della comunità Volentix per facilitare la distribuzione di VTX, l'aset digitale nativo dell'ecosistema Volentix, e promuove la consapevolezza delle iniziative Volentix.

Lanciata recentemente nella versione di beta test, Venue permette agli utenti di ricevere VTX in cambio, ad esempio, per la partecipazione alle comunità dedicate allo sviluppo, presentando soluzioni ai bug, e rivendicando le bountie (taglie). Le classifiche e le metriche live riflettono la partecipazione dell'utente. La prima campagna di raccolta firme è stata lanciata sul forum di https://bitcointalk.org/ il 13 luglio 2018. Per ulteriori informazioni visita https://venue.volentix.io.

### 2.2 VERTO

Verto is being built as a multi-currency wallet for use with the VDex decentralized exchange, and intends to facilitate personal custody and local management of private and public keys in peer-to-peer transactions, with the goal of eliminating the risks of devastating losses of stake associated with traumatic failures of central operators. Verto plans to employ a system of smart contracts to maintain the state between two trading clients, the simplest operations being accomplished with atomic swaps.[1]

### 2.3 VESPUCCI

Vespucci è concepito come un motore di analisi accessibile tramite un'interfaccia facile da usare, con forzieri contenenti dati di mercato in tempo reale e storici, come i rating dei beni digitali e l'analisi del sentimento. We wish to empower users with tools to graph and compare tradeable digital assets, to access and parse historical trading records, to plot trends and patterns, and to monitor and assess open-source software developments. Vespucci seeks to bring to your fingertips confident and comprehensive market-relevant data by aggregating the information currently scattered throughout many different blockchains, websites, chat rooms, and exchanges.

### 2.4 VDEX

Il quarto pilastro di Volentix, l'exchange VDex, è la piattaforma di commercio dei beni digitali presentata in dettaglio in questo white paper. Per un utilizzo fluido e sicuro, abbiamo intenzione di integrare VDex con il tuo wallet Verto personale e con l'interfaccia di Vespucci. Ci aspettiamo che VDex sia in grado di gestire le transazioni che coinvolgono sia VTX che la vasta gamma di asset digitali e blockchain esistenti di volta in volta in tutto il mondo. Stiamo sviluppando Venue come un'aggiunta complementare principalmente per incentivare e guidare le iniziative autoctone basate su VTX.

## 3. ARCHITETTURA

![](../8.jpg)

#### 3.0.1 Sistema operativo

Abbiamo valutato diversi sistemi operativi come candidati per la sottostruttura del nostro exchange VDex. Pur onorando il lavoro svolto da alcuni dei leader affermati nel campo degli asset digitali e della tecnologia blockchain, tra questi pionieri spicca, a nostro avviso, il lavoro di EOS.IO come struttura simile a un sistema operativo su cui si possono costruire applicazioni decentralizzate. Il software fornisce account, autenticazione, database, comunicazione asincrona, e pianificazione tra cluster. Componenti e protocolli sono già incorporati nella piattaforma, e un sottoinsieme può essere utilizzato per soddisfare i requisiti del nostro VDex. Inizialmente VDex beneficerà delle caratteristiche standard offerte da EOS.IO come la creazione di account e wallet e il recupero di chiavi rubate, ma in seguito prevediamo di implementare protocolli per la creazione di un exchange decentralizzato attraverso l'utilizzo dei contratti EOS e altri strumenti.[2] Ecco un riepilogo di metodi incoraggianti:

### Azioni Acontestuali

La maggior parte delle tecniche di scalabilità proposte da Ethereum (Sharding, Raiden, Plasma, State Channels) diventano più efficienti, parallelizzabili e pratiche, garantendo allo stesso tempo una rapida comunicazione inter-blockchain e una scalabilità inalterata. Un'Azione Acontestuale comporta computazioni che dipendono solo dai dati delle transazioni, e non dallo stato della blockchain.

### Conversione Binaria/JSON

I contratti EOS combinano la leggibilità umana di JSON con l'efficienza del binario.

### Parallelizzazione e ottimizzazione

La separazione dell'autenticazione dall'applicazione permette transazioni più rapide e aumenta la larghezza di banda. Secondo quanto riferito, i blocchi di EOS.IO vengono prodotti ogni 500ms.

### Web Assembly(WASM)

Web Assembly abilita applicazioni Web ad alte prestazioni e inoltre mette al sicuro ogni applicazione nella propria sandbox, attraverso le cui funzionalità VDex può ottenere l'accesso alla rete, le restrizioni del namespace dei filesystem e l'esecuzione forzata basata su determinate regole.

### Contratti Rust/C++

Il noto e popolare linguaggio di programmazione C++ appare altamente adatto a WASM. C++ ha un supporto di debug e delle librerie altamente maturi. Il codebase di EOS utilizza liberamente i template, e C++ permette l'uso di template e sovraccarico dell'operatore per definire una convalida delle unità senza costi di runtime. Il programma si reinizializza a stato pulito all'inizio di ogni messaggio, un distinto vantaggio che semplifica la formulazione degli smart contract. Il framework Web Assembly rifiuta automaticamente qualsiasi transazione che fa riferimento alla memoria in modo impreciso. Nel caso in cui sia necessaria l'allocazione di memoria dinamica, gli utenti possono passare a puntatori intelligenti perché i contratti di EOS.IO utilizzano C++14. È degno di nota il fatto che la prima implementazione della tecnologia Directed Acyclic Graph (DAG) di PARSEC dovrebbe avvenire in Rust.

#### 3.0.2 Schema defined messages and database

Service contracts are standardized to provide a baseline measure of interoperability between and among disparate systems by harmonization of data models. Infatti, il principio del modello del Contratto di Servizio Standardizzato prevede che i contratti di servizio siano basati su modelli di dati standardizzati. L'analisi viene effettuata sul progetto dell'inventario dei servizi per scoprire i documenti aziendali più comuni che vengono scambiati tra i servizi. Questi documenti aziendali vengono poi modellati in un modo standardizzato. The Canonical Schema pattern reduces the need for application of the data model transformation design pattern. [3]

#### 3.0.3 Comunicazione Inter-Contract

I dati sono condivisi tra i contratti attraverso un oracolo, che, "nel contesto delle blockchain e degli smart contract, è un agente che trova e verifica eventi del mondo reale e invia queste informazioni ad una blockchain per essere utilizzati dagli smart contract". [4] Ogni nodo avrà una copia identica di questi dati, da utilizzare nella computazione degli smart contract. Piuttosto che sia lo smart contract a funzionare per estrarre i dati, è invece l'oracolo a inviare i dati alla blockchain. In the instance of a blockchain, most reading of the data is done via polling "models" in order to monitor blockchain state and to perform certain responsive actions.

#### 3.0.4 Sidechains

In EOS.IO, l'emissione di un asset digitale crea una sidechain, cioè un meccanismo emergente che permette ad un bene digitale proveniente da una blockchain di essere utilizzato in modo sicuro in un altra blockchain e poi essere nuovamente spostato sulla blockchain originale. L'efficienza dell'elaborazione è incentivata dalla creazione di molteplici sidechain. Un canale di comunicazione tra blockchain diverse tipo TCP valuta le prove. Per ogni frammento (un'unità di esecuzione parallelizzabile in un ciclo), con questi impegni di azione viene costruito un albero di merkle equilibrato per generare una radice di merkle condivisa temporaneamente; ciò viene fatto per la velocità di calcolo parallelo. The block header contains the root of a balanced merkle tree the leaves of which are the roots of these individual shard merkle trees. [2]

#### 3.0.5 Liquidità

Un asset digitale è liquido se può essere facilmente venduto o comprato in volumi di scambio ordinari senza che nel breve termine ci sia alcun impatto significativo sul suo prezzo di mercato prevalente. Per ottenere tale status, di solito qualsiasi asset negoziabile deve superare una soglia di volume di negoziazione sufficiente per sostenere la stabilità. In particolare, prevediamo di adottare le seguenti metodologie: Protocollo Loopring con l'utilizzo di contratti EOS.IO che agiscono come nodi.[5] Algoritmo di Bancor utilizzato per portare stabilità all'asset digitale.[6] Commutazioni tra questi protocolli e gli HTLC (atomic swap) secondo le analisi di Vespucci sulla rete VDex.

#### 3.0.6 Hashed Timelock Contracts (Atomic Swaps)

Un Hashed Timelock Contract (HTLC)[1] è uno smart contract che consente l'implementazione di transazioni con scadenza. Agli utenti sarà offerto un periodo di lock-in variabile per le loro transazioni, con uno sconto sulle commissioni della transazione in cambio della scelta di un periodo di lock-in più lungo.

### 3.1 TOPOLOGIA DI RETE

#### 3.1.1 Nodi

![](../9.jpg)

I nodi sono gli endpoint dell'exchange VDex. Le loro funzioni sono:

1. Agire come portali per VDex attraverso il wallet di Verto.

2. Unire le informazioni del registro ordini.

3. Impostare il registro ordini.

4. Gestire l'anullamento dell'ordine.

5. Assegnare timeout per il protocollo RAFT.

6. Inizializzare i contratti per gli ordini che sono stati completati.

I nodi guadagnano una parte delle commissioni per ogni transazione. Se un utente ha fondi sufficienti e possiede una buona reputazione, il suo portafoglio Verto può fungere da nodo.

#### 3.1.2 Aggregatori

Gli aggregatori di VDex sono server dedicati di Volentix che hanno come scopo la sicurezza e le simulazioni. One of their functions is to pull logs and order book data from nodes into sparse distributed representations for hierarchical temporal memory as intrusion [7] analysis for detecting anomalies in the system. The aggregators will also be host to other components such as metachain ledgers and blockchain scrapers.

#### 3.1.3 Latenza

EOS.IO ha una latenza bassa per la conferma dei blocchi (0.5 secondi). [5] Questo grado di latenza può essere mantenuto nelle transazioni con altre blockchain se queste chain hanno una latenza simile. Ma fondamentalmente la transazione può essere rapida solo quanto la chain meno rapida dell'equazione. Per esempio, è risaputo, che un blocco Bitcoin necessita circa 10 minuti per l'elaborazione. Receiving a transaction hash does not mean the transaction is confirmed; it means only that a node accepted the transaction without error, although there is generally a high probability other block producers will accept it.

### 3.2 ORDER BOOK

The order book is the list of buy-and-sell orders VDex records from interested users. A matching engine uses an order book to determine which orders can be fulfilled. The Loopring protocol allows for customizing the order book data structure.[5] Containers provided by EOS.IO can be used for optimal performance.[8]

#### 3.2.1 Data structures

Using the Loopring Protocol FIFO (first-in first-out) circular buffer, nodes can design their order books to display and match a user’s order. This method follows an OTC model, where limit orders are positioned based on price only.[5]

Referencing the EOS.IO persistence API, the order book is able to take advantage of the powerful multi-index container shared among nodes through the same EOS.IO account.

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