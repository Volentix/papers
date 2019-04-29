# THE VOLENTIX VDEX WHITE PAPER

- Version: 0.1.4
- Aggiornata il: 11-03-2019
- Sito web: www.volentix.io

## 1. INTRODUZIONE

Volentix presenta VDex, progettato come una piattaforma decentralizzata per lo scambio di beni digitali con enfasi sull'user experience, sullo sviluppo della comunità e sulla governance. Attraverso l'utilizzo di tecnologie consolidate e la programmazione di nuovi protocolli selettivi dando priorità a sicurezza, velocità, autenticazione, facilità di utilizzo, scalabilità e supporto multi-asset, VDex vuole facilitare le transazioni di tipo peer-to-peer mettendo insieme un portfolio di applicazioni decentralizzate costruite sulla base degli smart contract di EOS.IO.

Il punto di lancio VDex anticipa l'adeguamento dei requisiti di progettazione di Volentix alle tecnologie disponibili sovrapposte al sistema operativo decentralizzato EOS.IO. Abbiamo intenzione di testare le nostre ipotesi creando dei prototipi tramite software EZEOS personalizzato, che abbiamo costruito e personalizzato attraverso gli strumenti a riga di comando cleos di EOS.IO. Questo software risiede in: https://github.com/Volentix/ezeos

![](../main3-3000px.jpg)

## 2. VOLENTIX

L'ecosistema Volentix si reggerà su 4 pilastri, una serie di applicazioni di inizializzazione specificamente note come Venue, Verto, Vespucci, e VDex.

### 2.1 VENUE

Venue è progettato come una piattaforma dinamica comunitaria che recruta e assegna i membri della comunità Volentix per facilitare la distribuzione di VTX, l'asset digitale nativo dell'ecosistema Volentix e promuovere la consapevolezza delle iniziative Volentix.

Lanciata recentemente nella versione di beta test, Venue permette agli utenti di ricevere VTX in cambio, ad esempio, per la partecipazione alle comunità dedicate allo sviluppo, presentando soluzioni ai bug, e rivendicando le bounty. Le classifiche e le metriche live riflettono la partecipazione dell'utente. La prima campagna di raccolta firme è stata lanciata sul forum di https://bitcointalk.org/ il 13 luglio 2018. Per ulteriori informazioni visita https://venue.volentix.io.

### 2.2 VERTO

Verto viene costruito come un wallet multi-valuta da utilizzare con l'exchange decentralizzato Vdex, e intendo facilitare la custodia pesonale e la gestione locale delle chiavi private e delle chiavi pubbliche nelle transazioni peer-to-peer, con l'obiettivo di eliminare i rischi di devastanti perdite di stake associate a fallimenti traumatici degli operatori centrali. Verto intende utilizzare un sistema di smart contract per mantenere lo stato tra due clienti commerciali, mentre le operazioni più semplici sono effettuate con atomic swap.[1]

### 2.3 VESPUCCI

Vespucci è concepito come un motore di analisi accessibile tramite un'interfaccia facile da usare, contenenti dati, nascosti preziosi, di mercato in tempo reale e storici, come i rating dei beni digitali e l'analisi del sentimento. Vogliamo consentire agli utenti di generare grafici e confrontare gli asset digitali, accedere e analizzare i record di trading passati, tracciare tendenze e modelli, e monitorare e stimare gli sviluppi dei software open source. Vespucci seeks to bring to your fingertips confident and comprehensive market-relevant data by aggregating the information currently scattered throughout many different blockchains, websites, chat rooms, and exchanges.

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

Il noto e popolare linguaggio di programmazione C++ appare altamente adatto a WASM. C++ ha un supporto di debug e delle librerie altamente maturo. Il codebase di EOS utilizza liberamente i template, e C++ permette l'uso di template e sovraccarico dell'operatore per definire una convalida delle unità senza costi di runtime. Il programma si reinizializza a clean state all'inizio di ogni messaggio, un grosso vantaggio che semplifica la formulazione degli smart contract. Il framework Web Assembly rifiuta automaticamente qualsiasi transazione che fa riferimento alla memoria in modo impreciso. Nel caso in cui sia necessaria l'allocazione di memoria dinamica, gli utenti possono passare a puntatori intelligenti perché i contratti di EOS.IO utilizzano C++14. È degno di nota il fatto che la prima implementazione della tecnologia Directed Acyclic Graph (DAG) di PARSEC dovrebbe avvenire in Rust.

#### 3.0.2 Messaggi e database definiti da uno schema

I contratti di servizio sono standardizzati per fornire una misura di base dell'interoperabilità tra sistemi diversi attraverso l'armonizzazione dei modelli di dati. Infatti, il principio del modello del Contratto di Servizio Standardizzato prevede che i contratti di servizio siano basati su modelli di dati standardizzati. L'analisi viene effettuata sul progetto dell'inventario dei servizi per scoprire i documenti aziendali più comuni che vengono scambiati tra i servizi. Questi documenti aziendali vengono poi riprodotti in un modo standardizzato. The Canonical Schema pattern reduces the need for application of the data model transformation design pattern. [3]

#### 3.0.3 Comunicazione Inter-Contract

I dati sono condivisi tra i contratti attraverso un oracolo, che, "nel contesto delle blockchain e degli smart contract, è un agente che trova e verifica eventi del mondo reale e invia queste informazioni ad una blockchain per essere utilizzati dagli smart contract". [4] Ogni nodo avrà una copia identica di questi dati, da utilizzare nella computazione degli smart contract. Piuttosto che essere lo smart contract a funzionare per estrarre i dati, è invece l'oracolo a inviare i dati alla blockchain. In the instance of a blockchain, most reading of the data is done via polling "models" in order to monitor blockchain state and to perform certain responsive actions.

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

EOS.IO ha una latenza bassa per la conferma dei blocchi (0.5 secondi). [5] Questo grado di latenza può essere mantenuto nelle transazioni con altre blockchain se queste chain hanno una latenza simile. Ma sostanzialmente la transazione è rapida solo come la catena meno rapida dell'equazione. Per esempio, è risaputo, che un blocco Bitcoin necessita circa 10 minuti per l'elaborazione. Ricevere l'hash di una transazione non significa che la transazione è stata confermata; significa soltanto che un nodo ha accettato la transazione senza alcun errore, anche se in genere c'è un alta probabilità che anche altri produttori di blocchi la accetteranno.

### 3.2 REGISTRO ORDINI

Il registro ordini è la lista degli ordini di acquisto e vendita che VDex registra dagli utenti interessati. Un matching engine utilizza un registro ordini per determinare quali ordini possono essere sodisfatti. Il protocollo Loopring permette la personalizzazione della struttura del registro ordini.[5] Per prestazioni ottimali, si possono utilizzare i container forniti da EOS.IO.[8]

#### 3.2.1 Strutture di dati

Utilizzando il buffer circolare FIFO (primo ad entrare primo ad uscire) del Protocollo Loopring, i nodi possono progettare i loro registri degli ordini per mostrare e soddisfare l'ordine di un utente. Questo metodo segue un modello OTC, dove i limit order vengono posizionati solo in base al prezzo.[5]

Facendo riferimento alla persistence API di EOS.IO, il registro ordini può trarre vantaggio dal potente container multi-index condiviso tra i nodi nello stesso account EOS.IO.

#### 3.2.2 Registro ordini On-Chain

Un registro ordini on-chain è un registro di offerte che risiedono nel wallet (nodo) scelto per impostare il registro ordini. Questo si trova in un database persistente su ogni nodo che si iscrive allo stesso account come tutti gli altri nodi.

#### 3.2.3 Registro ordini Off-Chain

Risiedenti sull'aggregatore, i registri ordini offline hanno come scopo la sicurezza e le simulazioni.

#### 3.2.4 Processo di decentralizzazione dell'impostazione del registro ordini

Ai fini della decentralizzazione, I nodi faranno a turno per impostare il registro ordini. The settling node must be designated by the protocol and all order book entries from all nodes must be available to the settling nodes. Secondo noi i meccanismi di consenso RAFT[9] e PARSEC[10] offrono soluzioni efficaci. RAFT è un algoritmo ben consolidato ed è facile da implementare.[7] PARSEC è più recente ed efficace, utilizza la tecnologia Directed Acyclic Graph (DAG) ed elimina la necessità di copiare i log.

### 3.3 IMPOSTAZIONE ORDINE

L'impostazione degli ordini contiene elementi noti delle operazioni tradizionali del mercato finanziario. Utilizing FIFO technology to design the order book, VDex intends to check order, inventory, and fill rate, as well as limit orders and cancellations. ![](../7.jpg)

### 3.4 VTX

#### 3.4.1 VTX Issuance and Use

VTX è l'asset digitale nativo da emettere e utilizzare sull'exchange decentralizzato VDex. Attualmente abbiamo intenzione di utilizzare un contratto eosio.token del framework EOS.IO per emettere 2.1 miliardi di token VTX compatibili con EOS.IO con una supply di 1.3 miliardi. VTX avrà un'ampia gamma di utilizzi, ad esempio:

Per ricompensare i partecipanti nel processo del consenso e nelle campagne Venue.

Per pagare e ridistribuire le commissioni delle transazioni sull'exchange VDex.

Per presentare e votare le proposte per l'ecosistema Volentix, utilizzando i diritti di voto assegnati ai detentori di VTX.

Per offrire sostegno per la revisione delle proposte e per attuare progetti.

Per incentivare gli utenti a partecipare nell'impostazione del registro degli ordini assumendo la funzione di nodi attraverso i loro wallet Verto.

Per incentivare gli utenti a bloccare i loro fondi per più di 24 ore per le transazioni HTLC con scadenza.

#### 3.4.2 VTX Allocation

![](../6.jpg)

Un ecosistema di asset digitali richiede una insieme di componenti umane fondamentali che portino avanti il progetto.[11] È essenziale per compensare questi individui per la loro partecipazione. Oggetto di aggiustamenti, al momento Volentix prevede i seguenti stanziamenti:

1. Collaboratori. 12%. Un insieme di individui, simili ai fondatori, che contribuiscono con idee, tempo e talento, anche se spesso lavorano senza una compensazione anticipata.

2. Sostenitori.

Fase 1. 5%. Early passive seed funders.

Fase 2. 28%. Finanziatori tramite prevendita privata qualificata e possibile vendita pubblica.

3. Facilitatori. (Consulenti, Sviluppatori, Promotori, Custodi). Nota che i requisiti per l'assistenza da parte delle sotto categorie di questa categoria possono differire significativamente prima e dopo che il progetto abbia ricevuto il sostegno finanziario sostanziale, ma alcuni individui possono prestare servizio durante entrambe le fasi.

Fase 1. 10%.

Fase 2. 10%.

4. Tesoreria decentralizzata. 35%. Membri della comunità incentivati e ricompensati per la partecipazione nel progressivo sviluppo di un'organizzazione autonoma decentralizzata (DAO). È previsto che una tesoreria decentralizzata venga amministrata tramite l'utilizzo degli smart contract e del consenso comunitario. ![](../5.jpg)

#### 3.4.3 Distribuzione VTX

Alla luce delle condizioni del mercato al momento della presente scrittura, Volentix sta considerando i tempi, i mezzi, i termini e le condizioni per la distribuzione di VTX come una funzione di prevendite private e un eventuale vendita pubblica. Tieni sotto controllo il nostro sito per ulteriori aggiornamenti.

### 3.5 IMPIEGO DELLA PIATTAFORMA EOS.IO

Le seguenti considerazioni sono rilevanti per il nostro utilizzo dell'exchange VDex sulla piattaforma EOS.IO:

La distribuzione di un contratto ha un costo ma l'utilizzo è gratuito.

Developers stake EOS.IO-compliant tokens to deploy a smart contract. After the contract is deployed, the locked tokens are returned.

Le applicazioni decentralizzate stanziano memoria, CPU, larghezza di banda, e altre risorse per i loro contratti.

Molteplici messaggi e molteplici account possono essere assegnati allo stesso thread.

### 3.6 INTERAZIONE BLOCKCHAIN

#### Comunicazione Inter-Blockchain

EOS.IO è progettato per rendere più leggere le verifiche della Comunicazione Inter-Blockchain (IBC). For chains with insufficient capacity for processing the IBC proofs and establishing validity, there is an option to default to trusted oracles/escrows. With an EOS.IO-based smart contract, a trusted multi-signature wallet holding the asset in escrow can be used to persuade the signing/publishing of the transaction based on IBC proofs from the originating chain.

#### 3.6.2 Informazione Multi-Blockchain

Le informazioni comprensibili su più blockchain si possono ottenere aggregando le linee temporali della blockchain in ordine parallelo (con variazioni nella frequenza del cambiamento di stato). This system can trigger multi-chain load balancers, transfer states, draw data outputs from smart contracts, and foreign blockchain transaction execution. La distanza relativa del blocco, lo stato globale relativo, e gli eventi con marcatura temporale vengono registrati su un ledger globale per ottimizzare e confermare le transazioni prima che queste si verifichino effettivamente sulla catena nativa. Questo approccio potrebbe essere utilizzato anche per determinare la coincidenza tra catene nella produzione del blocco per accedere a una maggiore liquidità.[12]

### 3.7 SECURITY CONCERNS

To shake out certain assumptions, we intend to commence security testing following the prototyping phase. Le preoccupazioni in materia di sicurezza sono di vitale importanza per gli utenti e devono essere affrontate. Le minacce includono, ad esempio, un aggressore che esegue codice maligno all'interno di una transazione o manipola l'ordine delle transazioni o i timestamp dei blocchi. Nelle sezioni che seguono affrontiamo alcune misure di sicurezza e specifiche minacce alla sicurezza e rimedi.

### 3.8 MISURE DI SICUREZZA

#### 3.8.1 Contract security

Conservare la maggior parte dei fondi in un conto a tempo ritardato, controllato da più firme.

Utilizzare la firma multipla su un hot wallet con diversi processi/server indipendenti che controllano due volte tutti i prelievi, con il vantaggio concomitante di creare una lista di conti affidabili.

Distribuire un contract personalizzato che permette i prelievi solo per gli account verificati da KYC/AML.

Distribuire un contratto personalizzato che accetta solo i depositi di asset conosciuti provenienti da account verificati da KYC/AML.

Distribuire un contratto personalizzato che necessita un periodo di attesa obbligatorio di 24 ore per tutti i prelievi.

Utilizzare contratti con wallet di tipo hardware per firmare qualsiasi cosa, inclusi i prelievi automatici.

Aggiornare i contratti danneggiati.

Includere la possibilità di mettere in pausa la funzionalità di un contratto.

Includere la possibilità di ritardare un azione di un contratto.

#### 3.8.2 Auditing rogue processes

Gli algoritmi avanzati per la rilevazione delle anomalie forniti dalla libreria Nupic di Numenta necessiteranno degli insiemi di dati di addestramento meno voluminosi di quelli dei sistemi AI convenzionali.

#### 3.8.3 Randomizzazione

True randomisation of address space layout, route or utilizing varying lengths of timeouts as in the RAFT protocol can complexify systems enough to enhance resilience and further secure systems against a side-channel attack or front running.

#### 3.8.4 Ispezione del registro

Parsec non utilizza i registri per la determinazione del consenso. D'altro canto, RAFT ne avrà bisogno. In any case, Validator nodes will be designed to require minimal information To determine consensus as to minimize the transaction process time.

#### 3.8.5 Transazione come Proof of Stake (TaPoS)

Questo meccanismo impedisce la riproduzione di una transazione sui fork che non includono il blocco di riferimento. Segnala alla rete che un particolare utente e stake si trovano su un determinato fork.

### 3.9 Minacce alla sicurezza e rimedi

#### 3.9.1 Doppia spesa

Una doppia spesa e un tipo di attacco in cui un determinato stake di cryptocurrency viene speso in più di una transazione.

Un attacco di tipo race si verifica quando due transazioni in conflitto vengono inviate sulla rete in rapida successione.

A Finney attack pre-mines one transaction into a block and spends the same tokens before releasing the block to invalidate that transaction.

Un attacco 51% può essere effettuato da chiunque possiede più del 50% della potenza di calcolo di una rete. A majority ownership position permits reversal of any transaction and allows total control of selection of transactions appearing in blocks. Sembra che EOS.IO, Loopring, e RAFT prevengono questo problema. Se un produttore di blocchi impiega una quantità irragionevole di runtime oppure non è sufficientemente redditizia, allora il processo viene inserito nella lista nera.[5]

#### 3.9.2 Front running

Un front runner ruba uno o più ordini dall'impostazione del libro ordini di una transazione in attesa. Sia EOS.IO che Loopring offrono dei rimedi nei quali le chiavi sono protette perché non fanno parte della transazione on-chain, e quindi rimangono sconosciute ai soggetti diversi dal proprietario. Solo il nodo che imposta il registro d'ordine è in possesso delle informazioni sensibili, e ogni nodo utilizza una soluzione diversa per la risoluzione dei registri degli ordini, aggiungendo un altro livello di difficoltà per promuovere la sicurezza.

#### 3.9.4 Identità forgiate

Gli utenti malintenzionati creano identità forgiate per inviare un gran numero di piccoli ordini per attaccare i nodi di Loopring. However, most of these orders will be rejected for not yielding satisfying profit when matched.

#### 3.9.4 Saldo Insufficiente

Gli utenti malintenzionati creano ed inviano ordini il cui valore è diverso da 0 ma il cui indirizzo ha un saldo pari a 0. I nodi controllano il saldo reale, aggiornano di conseguenza lo stato di questi ordini, e poi li scarta.

#### 3.9.5 Timing attack

Gli attacchi di tipo Timing sono una classe di attacchi cryptografici attraverso i quali un osservatore di terze parti può dedurre il contenuto dei dati criptati registrando e analizzando il tempo necessario per l'esecuzione degli algoritmi di crittografia. L'algoritmo RAFT previene gli attacchi di tipo timing utilizzando i timeout in modo casuale.

### 3.10 USER EXPERIENCE

Our focus on user experience is primary. Vogliamo rendere VTX e i quatro pilastri di Volentix --Venue, Verto, Vespucci, e VDex -- facilmente accessibili e utilizzabili da tutti coloro che desiderano unirsi alla nostra comunità. Ci aspettiamo che l'esperienza sia continuamente anche educativa, con modelli e simulatori per supportare una migliore relazione UX/UI.

### 3.11 TRUE DECENTRALIZATION

EOS.IO è un'infrastruttura scalabile e di tipo open source per applicazioni decentralizzate. Its goal is a fair and transparent block producer (BP) election process utilizing a democratic delegated proof of stake (DPoS) consensus. In particolare, poichè un sistema del genere è ancora agli inizi, ci saranno dei difetti. Pertanto, un certo grado di centralizzazione mantenuta è inevitabile e necessario. Però la nostra filosofia guida è una di decentralizzazione, e i nostri sforzi sono mirati a promuovere una riduzione nell'indipendenza da un autorità centrale.

Per esempio, inizialmente abbiamo intenzione di erigere un sistema per l'elezione dei nodi (per la risoluzione dei libri degli ordini) che non utilizzerà un orologio centrale condiviso o DPoS ma che si baserà o su timeout casuali per la determinazione dei leader in un elezione (RAFT) oppure su Directed Acyclic Graph (DAG) nel protocollo PARSEC.

### 3.12 SYSTEM RECOVERY

I protocolli RAFT e PARSEC forniscono un sistema robusto per il recupero nel caso di un errore in un nodo. Sono inoltre fornite misure di sicurezza per il commercio tra blockchain native. If a chain defies identification, the system defaults to the next block or a short time lock.

### 3.13 ARCHIETETTURA IN EVOLUZIONE

Gli annunci quotidiani dello sviluppo di nuovo codice che influiscono sull'utilizzo degli asset digitali rivelano l'enorme vantaggio della filosofia del codice open-source. Noi di Volentix siamo consapevoli di essere i beneficiari delle enormi risorse finanziarie fornite dagli investitori iniziali per lo sviluppo delle applicazioni di asset digitali nell'ultimo decennio. Ora abbiamo l'opportunità di fare il prossimo passo creando VDex, un exchange decentralizzato per la prossima generazione delle transazioni di asset digitali.

## 4. PENSIERI CONCLUSIVI

Tutti noi di Volentix stiamo dedicando il nostro lavoro e i nostri pensieri allo sviluppo di un programma basato sull'indipendenza e sull'empowerment. Se vuoi unirti a noi, qualunque siano le tue abilità, allora ti preghiamo di farlo e di studiare gli argomenti contenuti in questa white paper e le ulteriori pubblicazioni Volentix che condividiamo con la nostra community.

## 5. TIMELINE

Controlla il nostro sito web e i nostri social media per aggiornamenti e altri annunci importanti. Vi ringraziamo per la vostra attenzione e il vostro interesse.

## DISCLAIMER (dichiarazione di esclusione di responsabilità)

Questa white paper è stata preparata, ed è presentata, solo a scopo informativo. Le informazioni presentate non pretendono di essere complete. Le informazioni sono soggette a cambiamenti totali o parziali in qualsiasi momento senza alcun preavviso. Volentix Labs si riserva il diritto di modificare, sostituire, rimuovere, o cancellare qualsiasi informazione a discrezione unica ed esclusiva di Volentix. Volentix Labs non rilascia alcuna dichiarazione o garanzia, espressa o implicita, circa l'accuratezza o la completezza delle informazioni e declina espressamente ogni e qualsiasi responsabilità di qualsiasi tipo per le informazioni contenute o meno. Volentix Labs chiede ad ogni lettore di leggere le informazioni in modo completo e con la massima attenzione, e di intraprendere un'indagine e un'analisi indipendente delle informazioni e di chiedere e ottenere una consulenza professionale ai fini della valutazione delle informazioni. Per quanto a conoscenza di Volentix Labs, nessuna agenzia di regolamentazione, ente governativo o altro ente di terze parti di applicazione della legge ha esaminato, valutato o approvato in tutto o in parte le informazioni. Queste informazioni non sono un offerta o una richiesta di alcun tipo e non formano le base per alcun tipo di contratto o di impegno. Qualsiasi dichiarazione considerata lungimirante è puramente una questione di opinioni, e nessun lettore dovrebbe fare affidamento su tale dichiarazione o su qualsiasi parte o su tutte le informazioni in alcun modo.

## NOTE A PIÈ DI PAGINA

1. K. Kurokawa, trasferimenti cross chain Atomic, una panoramica, (2015).

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