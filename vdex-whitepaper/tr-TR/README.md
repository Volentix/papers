# VOLENTIX VDEX TANITIM BELGESİ

- Sürüm: 0.1.4
- Güncellendi: 11-03-2019
- Web sitesi: www.volentix.io

## 1. GİRİŞ

Volentix, kullanıcı deneyimi ve toplum gelişimi ve yönetişimi üzerinde durularak dağıtılmış, merkezi olmayan bir dijital varlık değişimi olarak tasarlanan VDex'i tanıtıyor. VDex, yerleşik teknolojilere erişerek ve güvenlik konusunda öncelikli seçici yeni protokoller, hız, kimlik doğrulama, kullanım kolaylığı, ölçeklenebilirlik ve çoklu varlık desteği konularında öncelikli seçici yeni protokoller planlayarak, EOS.IO akıllı sözleşmelerine dayanan bir merkezi olmayan uygulama portföyü oluşturarak eşler arası işlemleri kolaylaştırmayı amaçlamaktadır.

VDex başlangıç noktası, Volentix'in tasarım gereksinimlerini EOS.IO merkezi olmayan işletim sisteminde bulunan mevcut teknolojilerle eşleştirmeyi öngörüyor. Varsayımlarımızı, EOS.IO'nun cleos komut satırı araçları ile oluşturup özelleştirdiğimiz özel EZEOS yazılımı aracılığıyla prototipleyerek test etmeyi amaçlıyoruz. Bu yazılım şurada bulunur: https://github.com/Volentix/ezeos

![](../main3-3000px.jpg)

## 2. VOLENTIX

Volentix ekosistemi, özellikle Venue, Verto, Vespucci ve VDex olarak bilinen bir dizi uygulama başlatan dört sütunun üzerinde olacaktır.

### 2.1 VENUE

Venue, Volentix ekosisteminin yerel dijital varlığı olan VTX'in dağıtımını kolaylaştırmak ve Volentix girişimlerinin farkındalığını arttırmak için Volentix topluluğunun üyelerini işe alan ve hizalayan dinamik bir topluluk platformu olarak planlanmıştır.

Beta testlerinde yeni piyasaya sürülen Venue, kullanıcıların, örneğin adanmış topluluklar geliştirmek, hata düzeltmeleri göndermek ve ikramiye talep etmek karşılığında VTX almalarına olanak tanıyor. Liderler sıralaması ve canlı ölçümler kullanıcının katılımını yansıtır. İlk imza kampanyası, 13 Temmuz 2018'de https://bitcointalk.org/ forumunda başlatıldı. Lütfen daha fazla bilgi için https://venue.volentix.io ziyaret edin.

### 2.2 VERTO

Verto, VDex merkezi olmayan borsası ile kullanılmak üzere çoklu para birimi cüzdan olarak inşa ediliyor ve merkezi operatörlerin travmatik başarısızlıklarıyla ilişkili yıkıcı kayıpların risklerini ortadan kaldırmak için eşler arası işlemlerde özel ve halka açık anahtarlarının kişisel velayetini ve yerel yönetimini kolaylaştırmayı amaçlamaktadır. Verto, iki ticaret müşterisi arasındaki durumu korumak için akıllı sözleşmeler sistemini kullanmayı planlıyor, en basit işlemler atomik takaslarla gerçekleştiriliyor.[1]

### 2.3 VESPUCCI

Vespucci, dijital varlık derecelendirmeleri ve duyarlılık analizi gibi gerçek zamanlı ve tarihsel piyasa verilerinin hazine askerleri ile kullanıcı dostu bir arayüzle erişilebilen bir analitik motoru olarak öngörülmektedir. Kullanıcıları, takas edilebilir dijital varlıkları grafiklemek ve karşılaştırmak, geçmiş alım satım kayıtlarına erişmek ve ayrıştırmak, trendleri ve kalıpları çizmek ve açık kaynaklı yazılım gelişmelerini izlemek ve değerlendirmek için araçlarla güçlendirmek istiyoruz. Vespucci, şu anda birçok farklı blok zincirleri, web siteleri, sohbet odaları ve borsalara dağılmış olan bilgileri bir araya getirerek parmaklarınızın ucunda güvenli ve piyasa ile ilgili kapsamlı verileri bulmaya çalışıyor.

### 2.4 VDEX

Volentix'in dördüncü sütunu, VDex borsası tanıtım belgesinde ayrıntılı olarak tanıtılan alınıp satılabilir dijital varlık platformudur. Sorunsuz ve güvenli bir kullanım için VDex'i kendi kişisel Verto cüzdanınız ve Vespucci arayüzünüzle entegre etmeyi planlıyoruz. Hem VDex'in hem de VTX’in dünya genelinde zaman zaman mevcut olan çok sayıda dijital varlık ve blok zincirini içeren işlemleri yönetebilmesini bekliyoruz. VTX tabanlı yerel girişimleri teşvik etmek ve yönlendirmek için öncelikle bir tamamlayıcı yardımcı olarak Venue'yü geliştiriyoruz.

## 3. MİMARİ

![](../8.jpg)

#### 3.0.1 İşletim sistemi

VDex borsasının altyapısı için çeşitli işletim sistemlerini aday olarak değerlendirdik. Dijital varlıklar ve blok zinciri teknolojisinde, yerleşik liderlerin bir kısmının yaptığı çalışmaları onurlandırmamıza rağmen, bu öncüler arasında EOS.IO'nun merkezi olmayan uygulamaların işletim sistemi benzeri bir çerçeve olarak çalışması bizim görüşümüze göre örnek olarak öne çıkmaktadır. Yazılım, hesaplar, kimlik doğrulama, veritabanları, zaman uyumsuz iletişim ve kümeler arasında zamanlamayı sağlar. Bileşenler ve protokoller platforma zaten yerleştirilmiştir ve VDex gereksinimlerimizi karşılamak için bir alt küme kullanılabilir. VDex başlangıçta hesap ve cüzdan oluşturma ve çalınan anahtarların kurtarılması gibi EOS.IO tarafından sunulan standart özelliklerden faydalanacak ancak daha sonra EOS sözleşmeleri ve diğer araçlar aracılığıyla merkezi olmayan bir borsanın oluşturulması için protokoller uygulamayı planlıyoruz.[2] İşte teşvik edici metodojilerin bir özeti:

### Ücretsiz İçerik İşlemleri

Ethereum (Sharding, Raiden, Plazma, Devlet Kanalları) tarafından önerilen ölçeklenebilirlik tekniklerinin çoğu daha verimli, paralelleştirilebilir ve pratik olarak aynı zamanda blok zincirleri arası hızlı iletişim ve bozulmamış ölçeklenebilirlik sağlarken pratik hale gelir. Ücretsiz Bir Bağlam Hareketi, blok zinciri durumuna değil, yalnızca işlem verilerine dayanan hesaplamaları içerir.

### Binary/JSON dönüştürme

EOS contracts combine the human readability of JSON with the efficiency of binary.

### Paralelleştirme ve optimizasyon

Separating authentication from application allows faster transaction times and increases bandwidth. EOS.IO blocks are reportedly produced every 500ms.

### Web Meclisi(WASM)

Web Assembly enables high-performance Web applications and also secures each application in its own sandbox, through which functionalities VDex can obtain network access, filesystem namespace restrictions, and enforced rule-based execution.

### Rust/C++ sözleşmeleri

The well-known and popular programming language C++ appears highly suitable for WASM. C++ has highly mature debugging support and libraries. EOS kod temeli özgürce şablonları kullanır ve C++ birimlerin çalışma zamanı maliyetsiz doğrulamasını tanımlamak için şablonların ve operatörün aşırı yüklenmesinin kullanılmasına izin verir. Program her mesajın başında durumu temizlemek için yeniden başlatıldı, akıllı sözleşmelerin formülasyonunu kolaylaştıran belirgin bir avantaj. WebAssembly çerçevesi hafızada hatalı adresleme yapan herhangi bir işlemi otomatik olarak reddeder. Dinamik bellek tahsisi gerektiğinde, EOS.IO sözleşmeleri C++14 kullandığı için kullanıcılar akıllı göstergelere gidebilir. PARSEC Yönlendirilmiş Asiklik Grafik (DAG) teknolojisinin dikkat çekici ilk uygulamasının Rust'ta olması beklenmektedir.

#### 3.0.2 Şema tanımlı mesajlar ve veritabanı

Service contracts are standardized to provide a baseline measure of interoperability between and among disparate systems by harmonization of data models. Indeed, the Standardized Service Contract design principle advocates that service contracts be based on standardized data models. Servisler arasında değiş tokuş edilen yaygın iş belgelerini bulmak için servis envanter planı üzerinde analiz yapılır. These business documents are then modeled in a standardized manner. The Canonical Schema pattern reduces the need for application of the data model transformation design pattern. [3]

#### 3.0.3 Sözleşmeler-Arası İletişim

Veriler bir uzman yoluyla sözleşmeler arasında paylaşılır, bu, "Blok zincirleri ve akıllı sözleşmeler bağlamında, gerçek dünyadaki olayları bulan ve doğrulayan ve bu bilgileri akıllı sözleşmeler tarafından kullanılacak bir blok zincirine ileten bir temsilcidir." [4] Her düğüm akıllı sözleşme hesaplamasında kullanmak için bu verilerin özdeş bir kopyasına sahip olacaktır. Rather than the smart contract functioning to pull the data, instead the oracle pushes the data onto the blockchain. In the instance of a blockchain, most reading of the data is done via polling "models" in order to monitor blockchain state and to perform certain responsive actions.

#### 3.0.4 Yan zincirler

In EOS.IO, issuance of a digital asset creates a sidechain, which is an emerging mechanism permitting digital assets from one blockchain to be securely used in a separate blockchain and then moved back to the original blockchain. Efficiency of processing is promoted by creating multiple sidechains. A TCP-like communication channel between different blockchains evaluates proofs. For each shard (a unit of parallelizable execution in a cycle), a balanced merkle tree is constructed of these action commitments to generate a temporary shared merkle root; this is done for speed of parallel computation. The block header contains the root of a balanced merkle tree the leaves of which are the roots of these individual shard merkle trees. [2]

#### 3.0.5 Likidite

A digital asset is liquid if it is easily sold or purchased in ordinary trading volumes without a significant short-term impact on its prevailing market price. In order to achieve such a status, traditionally any tradable asset must surmount a trading volume threshold sufficient to support stability. Specifically, we anticipate adopting the following methodologies: Loopring protocol with the use of EOS.IO contracts acting as nodes.[5] Bancor algorithm used to bring stability to the digital asset.[6] Toggles between these protocols and HTLC (atomic swaps) according to Vespucci analyses on the VDex network.

#### 3.0.6 Şifreli Zaman Aşımı Sözleşmeleri (Atomik Takaslar)

A Hashed Timelock Contract (HTLC)[1] is a smart contract enabling the implementation of time-bound transactions. Users will be offered a variable lock-in period for their transactions, with a discount on transaction fees in exchange for choosing a longer lock-in period.

### 3.1 AĞ TOPOLOJİSİ

#### 3.1.1 Düğümler

![](../9.jpg)

Nodes are the endpoints of the VDex exchange. Their functions are:

1. Verto cüzdanı vasıtasıyla VDex'e portallar olarak rol yapın.

2. Emir kitabı bilgilerini birleştir.

3. Emir kitabını kapat.

4. Emir iptalini yönet.

5. RAFT protokolü için zaman aşımlarını atayın.

6. Doldurulan emirler için sözleşmeleri başlat.

Nodes earn a portion of the fee for each transaction. If a user has sufficient funds and possesses a good track record, his or her Verto wallet can act as a node.

#### 3.1.2 Toplayıcılar

The VDex aggregators are dedicated Volentix servers for simulator and security purposes. One of their functions is to pull logs and order book data from nodes into sparse distributed representations for hierarchical temporal memory as intrusion [7] analysis for detecting anomalies in the system. The aggregators will also be host to other components such as metachain ledgers and blockchain scrapers.

#### 3.1.3 Gecikme

EOS.IO has low latency block confirmation (0.5 seconds).[5] This degree of latency can be maintained in transactions with other blockchains if those chains admit of similar latency. But fundamentally the transaction is only as rapid as the lesser-rapid chain in the equation. It is well known, for example, that a Bitcoin block requires approximately ten minutes for processing. Receiving a transaction hash does not mean the transaction is confirmed; it means only that a node accepted the transaction without error, although there is generally a high probability other block producers will accept it.

### 3.2 EMİR KİTABI

The order book is the list of buy-and-sell orders VDex records from interested users. A matching engine uses an order book to determine which orders can be fulfilled. The Loopring protocol allows for customizing the order book data structure.[5] Containers provided by EOS.IO can be used for optimal performance.[8]

#### 3.2.1 Veri yapıları

Using the Loopring Protocol FIFO (first-in first-out) circular buffer, nodes can design their order books to display and match a user’s order. This method follows an OTC model, where limit orders are positioned based on price only.[5]

Referencing the EOS.IO persistence API, the order book is able to take advantage of the powerful multi-index container shared among nodes through the same EOS.IO account.

#### 3.2.2 Açık-Zincir emir kitabı

An on-chain order book is a record of offers residing on the wallet (node) chosen to settle the order book. It resides in a persistent database on each node subscribing to the same account as all the other nodes.

#### 3.2.3 Kapalı-Zincir emir kitabı

Residing on the aggregator, offline order books serve for simulator and security purposes.

#### 3.2.4 Emir defteri anlaşmasının merkezi olmayan süreci

For decentralization purposes, nodes will take turns to settle the order book. The settling node must be designated by the protocol and all order book entries from all nodes must be available to the settling nodes. We believe the RAFT[9] and PARSEC[10] consensus mechanisms offer effective solutions. RAFT is a well-established algorithm and is easy to implement.[7] PARSEC is more recent and more efficient, using Directed Acyclic Graph (DAG) technology and eliminating the need for copying logs.

### 3.3 EMİR VERME

Order settlement contains familiar elements of conventional financial market transactions. Utilizing FIFO technology to design the order book, VDex intends to check order, inventory, and fill rate, as well as limit orders and cancellations. ![](../7.jpg)

### 3.4 VTX

#### 3.4.1 VTX Çıkarma ve Kullanımı

VTX is the native digital asset to be issued and used on the VDex decentralized exchange. We currently plan to use an eosio.token contract from the EOS.IO framework to issue 2.1 billion EOS.IO-compliant VTX tokens with a supply of 1.3 billion. VTX will have a diverse array of uses, for example:

To reward participants in the consensus process and in Venue campaigns.

To pay and redistribute transaction fees on the VDex exchange.

To submit and vote on proposals to the Volentix ecosystem, using the voting rights allocated to VTX holders.

To stake support for reviewing proposals and implementing projects.

To incentivize users to participate in order book settlement by becoming nodes via their Verto wallets.

To incentivize users to lock funds in for >24 hours by HTLC time-bound transactions.

#### 3.4.2 VTX Tahsisi

![](../6.jpg)

A digital assets ecosystem requires an array of certain fundamental human constituents who shepherd the project forward.[11] It is essential to compensate those individuals for their participation. Subject to adjustment, Volentix currently anticipates the following allocations:

1. Katkıda Bulunanlar. %12. Kuruculara benzer, içgörülere, zamana ve yeteneğe katkıda bulunan bir dizi insan, genellikle erken tazminat olmadan çalışır.

2. Destekçiler.

Phase 1. 5%. Early passive seed funders.

Phase 2. 28%. Funders via qualified private pre-sales and possible public sale.

3. Yardımcılar. (Danışmanlar, Geliştiriciler, Destekleyiciler, Saklayıcılar). Bu kategorideki alt kategorilerden yardım taleplerinin, projenin önemli miktarda finansman desteği almadan önce ve sonra önemli ölçüde farklılık gösterebileceğini unutmayın ancak bazı kişiler her iki aşamada da hizmet verebilir.

Phase 1. 10%.

Phase 2. 10%.

4. Merkezi olmayan hazine. %35. Topluluk üyeleri merkezi olmayan özerk bir organizasyonun (DAO) ilerici gelişimine katılım için teşvik edildi ve ödüllendirildi. Merkezi olmayan bir hazinenin akıllı sözleşmeler ve topluluk fikir birliği ile yönetilmesi bekleniyor. ![](../5.jpg)

#### 3.4.3 VTX Dağıtımı

In light of market conditions at the time of this writing, Volentix is considering timing, means, and terms and conditions of VTX distribution as a function of private pre-sales and possible public sale. Please monitor our website for updates.

### 3.5 EOS.IO PLATFORM DAĞITIMI

The following considerations are relevant to our deploying the VDex exchange on the EOS.IO platform:

Deploying a contract has a cost but is free to use.

Developers stake EOS.IO-compliant tokens to deploy a smart contract. After the contract is deployed, the locked tokens are returned.

Decentralized applications allocate memory, CPU, bandwidth, and other resources to their contracts.

Multiple messages and multiple accounts can be assigned to the same thread.

### 3.6 BLOK ZİNCİRİ ETKİLEŞİMİ

#### 3.6.1 Blok Zinciri-Arası İletişim

EOS.IO is designed to make Inter-Blockchain Communication (IBC) proofs lightweight. For chains with insufficient capacity for processing the IBC proofs and establishing validity, there is an option to default to trusted oracles/escrows. With an EOS.IO-based smart contract, a trusted multi-signature wallet holding the asset in escrow can be used to persuade the signing/publishing of the transaction based on IBC proofs from the originating chain.

#### 3.6.2 Çoklu-Blok Zinciri Bilgisi

Comprehensible multi-blockchain information can be obtained by aggregating blockchain timelines in parallel order (with variance in the frequency of change of state). This system can trigger multi-chain load balancers, transfer states, draw data outputs from smart contracts, and foreign blockchain transaction execution. Relative block distance, relative global state, and timestamped events are recorded on a global ledger to optimize and confirm transactions before they actually happen on the native chain. This approach could also be used to determine block production coincidence between chains to access greater liquidity.[12]

### 3.7 GÜVENLİK ENDİŞELERİ

To shake out certain assumptions, we intend to commence security testing following the prototyping phase. Security concerns are of paramount importance to users and must be addressed. Threats include, for example, an attacker executing malicious code within a transaction or manipulating the order of transactions or the timestamps of blocks. In the following sections, we address certain security measures and specific security threats and remedies.

### 3.8 GÜVENLİK ÖNLEMLERİ

#### 3.8.1 Güvenlik sözleşmesi

Retain vast majority of funds in a time-delayed, multi-signature-controlled account.

Use multi-signatures on a hot wallet with several independent processes/servers double-checking all withdrawals, with the concomitant benefit of creating a trusted list of accounts.

Deploy a custom contract that allows withdrawals only to accounts verified by KYC/AML.

Deploy a custom contract that accepts only deposits of known assets from accounts verified by KYC/AML.

Deploy a custom contract that requires a mandatory 24-hour waiting period for all withdrawals.

Utilize contracts with hardware wallets for all signing, including for automated withdrawals.

Upgrade broken contracts.

Include ability to pause the functionality of a contract.

Include ability to delay an action of a contract.

#### 3.8.2 Hileli işlemleri denetleme

The advanced anomaly detection algorithms provided by Numenta’s Nupic library will require less voluminous training data sets than conventional AI systems.

#### 3.8.3 Rasgeleleştirme

True randomisation of address space layout, route or utilizing varying lengths of timeouts as in the RAFT protocol can complexify systems enough to enhance resilience and further secure systems against a side-channel attack or front running.

#### 3.8.4 Günlük denetim

Parsec does not rely on logs for the determination of consensus. On the other hand, RAFT will require this. In any case, Validator nodes will be designed to require minimal information To determine consensus as to minimize the transaction process time.

#### 3.8.5 Alım Kanıtı olarak İşlem (TaPoS)

This mechanism prevents the replay of a transaction on forks that do not include the referenced block. Signals the network that a particular user and stake are on a specific fork.

### 3.9 Güvenlik tehditleri ve çözüm yolları

#### 3.9.1 Çifte harcama

A double spend is an attack in which a particular cryptocurrency stake is spent in more than one transaction.

A race attack occurs when two conflicting transactions are sent in rapid succession into the network.

A Finney attack pre-mines one transaction into a block and spends the same tokens before releasing the block to invalidate that transaction.

A 51% attack can be mounted by anyone owning >50% of the total computing power of a network. A majority ownership position permits reversal of any transaction and allows total control of selection of transactions appearing in blocks. EOS.IO, Loopring, and RAFT appear to prevent this problem. If a block producer takes an unreasonable amount of runtime or is not sufficiently profitable, then the process is blacklisted.[5]

#### 3.9.2 Ön koşu

A front runner steals one or more orders from a pending order book settlement transaction. Both EOS.IO and Loopring offer remedies in which keys are protected because they are not part of the on-chain transaction, and therefore remain unknown to parties other than the owner. Only the order book settling node is possessed of the sensitive information, and each node uses a different solution for resolving the order books, introducing yet another level of complexity to promote security.

#### 3.9.3 Sahte kimlikler

Malicious users create forged identities to send a large number of small orders to attack Loopring nodes. However, most of these orders will be rejected for not yielding satisfying profit when matched.

#### 3.9.4 Yetersiz Bakiye

Malicious users sign and spread orders the value of which is non-zero but the address of which has a zero balance. Nodes monitor actual balances, update these order states accordingly, and then discard them.

#### 3.9.5 Zamanlama saldırısı

Timing attacks are a class of cryptographic attacks through which a third-party observer can deduce the content of encrypted data by recording and analyzing the time taken to execute cryptographic algorithms. The RAFT algorithm prevents timing attacks by using randomness of timeouts.

### 3.10 KULLANICI DENEYİMİ

Our focus on user experience is primary. We wish to make VTX and the four pillars of Volentix -- Venue, Verto, Vespucci, and VDex -- easily accessible to and useable by all those who wish to join our community. We expect the experience continually to be educational as well, with templates and simulators to support a superior UX/UI relationship.

### 3.11 DOĞRU MERKEZSİZLEŞME

EOS.IO is an open-source, scalable infrastructure for decentralized applications. Its goal is a fair and transparent block producer (BP) election process utilizing a democratic delegated proof of stake (DPoS) consensus. Particularly as such a system just begins to proliferate, there will be glitches. Therefore, some degree of retained centralization is inevitable and necessary. But our guiding philosophy is one of decentralization, and our ongoing efforts are targeted to promoting a reduction in dependence on central authority.

For example, initially we plan to erect a system for electing nodes (when solving order books) that will not use a shared central clock or DPoS but instead will be based either on random timeouts for the determination of leaders in an election (RAFT) or on Directed Acyclic Graph (DAG) in the PARSEC protocol.

### 3.12 SİSTEM KURTARMA

The RAFT and PARSEC protocols provide a robust system for recovery in the case of node failure. Security measures are also provided for trading between and among native blockchains. If a chain defies identification, the system defaults to the next block or a short time lock.

### 3.13 GELİŞEN MİMARİ

Daily announcements of fresh code developments impacting on use of digital assets reveal the tremendous benefit of the open-source code philosophy. We at Volentix recognize we are the beneficiaries of the enormous financial resources dedicated by many early movers to developing digital assets applications over the past decade. We now have an opportunity to take the next step by creating VDex, a decentralized exchange for the next generation of digital assets transactions.

## 4. SON DÜŞÜNCELER

All of us at Volentix are dedicating our work and insights to developing a program premised on empowerment and independence. If you are of a mind to join us, in whatever capacity, then please do so and please become educated on the topics contained in this white paper and additional Volentix publications as we share them with our community.

## 5. ZAMAN ÇİZELGESİ

Please monitor our website and social media for updates and other important announcements. Thank you very much for your attention and interest.

## FERAGATNAME

This white paper was prepared, and is presented, for information purposes only. The information presented does not purport to be comprehensive. The information is subject to change in whole or in part at any time without notice. Volentix Labs reserves the right to amend, replace, remove, or delete any and all information at the sole and exclusive discretion of Volentix. Volentix Labs makes no representation or warranty, expressed or implied, concerning the accuracy or completeness of the information and expressly disclaims any and all liability of any and all kinds whatsoever for the information contained or not contained. Volentix Labs requests each and every reader to read the information fully and carefully, and to undertake independent investigation and analysis of the information, and to seek and obtain professional advice for purposes of evaluating the information. To the knowledge of Volentix Labs, no regulatory agency, government, or other third-party enforcement entity has reviewed, evaluated, or approved any part or all of the information. This information is not an offer or solicitation of any kind whatsoever and does not form the basis for any contract or commitment of any kind whatsoever. Any statement considered to be forward-looking is purely a matter of opinion, and no viewer should rely on any such statement or on any part or all of the information in any way whatsoever.

## DİPNOTLARI

1. K. Kurokawa, Atomik çapraz zincir transferi, bir genel bakış, (2015).

2. EOS.IO, Eos.io teknik tanıtım belgesi v2, (2018).

3. T. Earl, Soa principles of service design, (2016).

4. blockchainhub.net, blockchain-oracles, (2017).

5. F. Zhou, Wang, Loopring: Merkezi olmayan bir token değiş tokuş protokolü, (2018).

6. G. B. Eyal Hertzog, Guy Benartzi, Bancor protokolü: Akıllı sözleşmeleri vasıtasıyla kriptografik tokenler için sürekli likidite, (2018).

7. L. Lamport, yarı zamanlı parlamento, (1998).

8. D. Larimer, eosio.boot telegram sohbeti, (2018).

9. J. O. Diego Ongaro, Anlaşılabilir bir fikir birliği algoritması arayışı içinde, (2018).

10. F. H. Q. M. S. S. Pierre Chevalier, Bart lomiej KamiÂťnski, Eş zamanlı olmayan, dürüst, güvenli ve verimli bir fikir birliği için protokol (parsec), (2018).

11. Dane Keller Rutledge, Dijital Varlıklar Ekosisteminin (DAE) Temel İnsan Bileşenleri. (2018).

12. BlockColliderTeam, Blok çarpıştırıcısı tanıtım belgesi, (2018).

## EK REFERANSLAR

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

## BELGENİN SONU