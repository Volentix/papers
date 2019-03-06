# VOLENTIX VDEX TANITIM BELGESİ

- Sürüm: 0.1.4
- Güncellendi: 10-24-2018
- Web sitesi: www.volentix.io

## 1. GİRİŞ

Volentix, kullanıcı deneyimi ve toplum gelişimi ve yönetişimi üzerinde durularak dağıtılmış, merkezi olmayan bir dijital varlık değişimi olarak tasarlanan VDex'i tanıtıyor. VDex, yerleşik teknolojilere erişerek ve güvenlik konusunda öncelikli seçici yeni protokoller, hız, kimlik doğrulama, kullanım kolaylığı, ölçeklenebilirlik ve çoklu varlık desteği konularında öncelikli seçici yeni protokoller planlayarak, EOS.IO akıllı sözleşmelerine dayanan bir merkezi olmayan uygulama portföyü oluşturarak eşler arası işlemleri kolaylaştırmayı amaçlamaktadır.

VDex başlangıç noktası, Volentix'in tasarım gereksinimlerini EOS.IO merkezi olmayan işletim sisteminde bulunan mevcut teknolojilerle eşleştirmeyi öngörüyor. Varsayımlarımızı, EOS.IO'nun cleos komut satırı araçları ile oluşturup özelleştirdiğimiz özel EZEOS yazılımı aracılığıyla prototipleyerek test etmeyi amaçlıyoruz. Bu yazılım şurada bulunur: https://github.com/Volentix/ezeos

## 2. VOLENTIX

Volentix ekosistemi, özellikle Venue, Verto, Vespucci ve VDex olarak bilinen bir dizi uygulama başlatan dört sütunun üzerinde olacak.

### 2.1 VENUE

Venue, Volentix ekosisteminin yerel dijital varlığı olan VTX'in dağıtımını kolaylaştırmak ve Volentix girişimlerinin farkındalığını arttırmak için Volentix topluluğunun üyelerini işe alan ve hizalayan dinamik bir topluluk platformu olarak planlanmıştır. Beta testlerinde yeni piyasaya sürülen Venue, kullanıcıların, örneğin adanmış topluluklar geliştirmek, hata düzeltmeleri göndermek ve ikramiye talep etmek karşılığında VTX almalarına olanak tanıyor. Liderler sıralaması ve canlı ölçümler kullanıcının katılımını yansıtır. İlk imza kampanyası 13 Temmuz 2018'de https://bitcointalk.org/ forumunda başlatıldı. Daha fazla bilgi için lütfen https://venue.volentix.io adresini ziyaret edin.

![](../main3-3000px.jpg)

### 2.2 VERTO

Verto, VDex merkezi olmayan borsası ile kullanılmak üzere çoklu para birimi cüzdan olarak inşa ediliyor ve merkezi operatörlerin travmatik başarısızlıklarıyla ilişkili yıkıcı kayıpların risklerini ortadan kaldırmak için eşler arası işlemlerde özel ve halka açık anahtarlarının kişisel velayetini ve yerel yönetimini kolaylaştırmayı amaçlamaktadır. Verto, iki ticaret müşterisi arasındaki durumu korumak için akıllı sözleşmeler sistemini kullanmayı planlıyor, en basit işlemler atomik takaslarla gerçekleştiriliyor.[1]

### 2.3 VESPUCCI

Vespucci, dijital varlık derecelendirmeleri ve duyarlılık analizi gibi gerçek zamanlı ve tarihsel piyasa verilerinin hazine askerleri ile kullanıcı dostu bir arayüzle erişilebilen bir analitik motoru olarak öngörülmektedir. Kullanıcıları, takas edilebilir dijital varlıkları grafiklemek ve karşılaştırmak, geçmiş alım satım kayıtlarına erişmek ve ayrıştırmak, trendleri ve kalıpları çizmek ve açık kaynaklı yazılım gelişmelerini izlemek ve değerlendirmek için araçlarla güçlendirmek istiyoruz. Vespucci, şu anda birçok farklı blok zincirleri, web siteleri, sohbet odaları ve borsalara dağılmış olan bilgileri bir araya getirerek, parmaklarınızın ucunda güvenli ve piyasa ile ilgili kapsamlı verileri bulmaya çalışıyor.

### 2.4 VDEX

Volentix'in dördüncü sütunu, VDex borsası, tanıtım belgesinde ayrıntılı olarak tanıtılan alınıp satılabilir dijital varlık platformudur. Sorunsuz ve güvenli bir kullanım için, VDex'i kendi kişisel Verto cüzdanınız ve Vespucci arayüzünüzle entegre etmeyi planlıyoruz. VDex’in hem VTX’i hem de dünya genelinde zaman zaman mevcut olan çok sayıda dijital varlık ve blok zincirini içeren işlemleri yönetebilmesini bekliyoruz. VTX tabanlı yerel girişimleri teşvik etmek ve yönlendirmek için öncelikle bir tamamlayıcı yardımcı olarak Venue'yü geliştiriyoruz.

## 3. MİMARİ

#### 3.0.1 İşletim sistemi

VDex değişiminin altyapısı için çeşitli işletim sistemlerini aday olarak değerlendirdik. Dijital varlıklar ve blok zinciri teknolojisinde yerleşik liderlerin bir kısmının yaptığı çalışmaları onurlandırmamıza rağmen, bu öncüler arasında EOS.IO'nun merkezi olmayan uygulamaların işletim sistemi benzeri bir çerçeve olarak çalışması bizim görüşümüze göre örnek olarak öne çıkmaktadır. Yazılım, hesaplar, kimlik doğrulama, veritabanları, zaman uyumsuz iletişim ve kümeler arasında zamanlama sağlar. Bileşenler ve protokoller platforma zaten yerleştirilmiştir ve VDex gereksinimlerimizi karşılamak için bir alt küme kullanılabilir. VDex başlangıçta hesap ve cüzdan oluşturma ve çalınan anahtarların kurtarılması gibi EOS.IO tarafından sunulan standart özelliklerden faydalanacak, ancak daha sonra EOS sözleşmeleri ve diğer araçlar aracılığıyla merkezi olmayan bir borsanın oluşturulması için protokoller uygulamayı planlıyoruz.[2] İşte teşvik edici metodojilerin bir özeti:

### Ücretsiz İçerik İşlemleri

Ethereum (Sharding, Raiden, Plazma, Devlet Kanalları) tarafından önerilen ölçeklenebilirlik tekniklerinin çoğu, daha verimli, paralelleştirilebilir ve pratik olarak aynı zamanda blok zincirleri arası hızlı iletişim ve bozulmamış ölçeklenebilirlik sağlarken pratik hale gelir. Ücretsiz Bir Bağlam Hareketi blok zinciri durumuna değil, yalnızca işlem verilerine dayanan hesaplamaları içerir.

### Binary/JSON dönüştürme

EOS sözleşmeleri, JSON'un insan tarafından okunabilirliğini ikili verimlilik ile birleştiriyor.

### Paralelleştirme ve optimizasyon

Kimlik doğrulamasını uygulamadan ayırmak daha hızlı işlem süresi sağlar ve bant genişliğini artırır. EOS.IO bloklarının her 500ms'de bir üretildiği bildiriliyor.

### Web Meclisi(WASM)

Web Meclisi yüksek-performanslı Web uygulamalarını mümkün kılar ve aynı zamanda VDex'in ağ erişimi, dosya sistemi ad kısıtlamaları ve zorunlu kural-tabanlı yürütme sağladığı işlevsellikler sayesinde her uygulamayı kendi sanal alanında güvence altına alır.

### Rust/C++ sözleşmeleri

İyi bilinen ve popüler programlama dili C++ WASM için oldukça uygun görünüyor. C++ son derece olgun hata ayıklama desteğine ve kütüphanelerine sahiptir. EOS kod temeli, özgürce şablonları kullanır ve C++ birimlerin çalışma zamanı maliyetsiz doğrulamasını tanımlamak için şablonların ve operatörün aşırı yüklenmesinin kullanılmasına izin verir. Program, her mesajın başında durumu temizlemek için yeniden başlatıldı, akıllı sözleşmelerin formülasyonunu kolaylaştıran belirgin bir avantaj. WebAssembly çerçevesi, hafızada hatalı adresleme yapan herhangi bir işlemi otomatik olarak reddeder. Dinamik bellek tahsisi gerektiğinde, EOS.IO sözleşmeleri C++14 kullandığı için kullanıcılar akıllı göstergelere gidebilir. PARSEC Yönlendirilmiş Asiklik Grafik (DAG) teknolojisinin dikkat çekici ilk uygulamasının Rust'ta olması beklenmektedir.

#### 3.0.2 Şema tanımlı mesajlar ve veritabanı

Hizmet sözleşmeleri veri modellerinin uyumlaştırılması ile farklı sistemler içinde ve birlikte çalışabilirlik arasında temel bir ölçümü sağlamak için standartlaştırılmıştır. Gerçekten de, Standart Servis Sözleşmesi tasarım ilkesi servis sözleşmelerinin standartlaştırılmış veri modellerine dayanmasını savunuyor. Servisler arasında değiş tokuş edilen yaygın iş belgelerini bulmak için servis envanter planı üzerinde analiz yapılır. Bu iş belgeleri daha sonra standartlaştırılmış bir şekilde modellenmiştir. Kanonik Şema deseni veri modeli dönüşüm tasarım modelinin uygulama ihtiyacını azaltır. [3]

#### 3.0.3 Sözleşmeler-Arası İletişim

Veriler, bir uzman yoluyla sözleşmeler arasında paylaşılır, bu, "Blok zincirleri ve akıllı sözleşmeler bağlamında, gerçek dünyadaki olayları bulan ve doğrulayan ve bu bilgileri akıllı sözleşmeler tarafından kullanılacak bir blok zincirine ileten bir temsilcidir." [4] Her düğüm akıllı sözleşme hesaplamasında kullanmak için bu verilerin özdeş bir kopyasına sahip olacaktır. Verileri çekmek için çalışan akıllı sözleşmenin yanı sıra, bunun yerine uzman, verileri blok zincirine iter. Bir blok zinciri örneğinde, çoğu verinin okunması, blok zinciri durumunu izlemek ve belirli duyarlı eylemleri gerçekleştirmek için "modeller" seçilerek yapılır.

#### 3.0.4 Yan zincirler

EOS.IO'da, dijital bir varlığın verilmesi, bir yan zincir oluşturur, bu, bir blok zincirinden gelen dijital varlıkların ayrı bir blok zincirinde güvenli bir şekilde kullanılmasını ve daha sonra orijinal blok zincirine geri taşınmasını sağlayan yeni bir mekanizmadır. Çoklu yan zincir oluşturularak işleme verimliliğini arttırır. Farklı blok zincirleri arasındaki TCP benzeri bir iletişim kanalı kanıtları değerlendirir. Her bir kırılma için (bir devirde paralelleştirilebilir bir uygulama birimi), geçici bir ortak merkle kökü oluşturmak için bu aksiyon taahhütlerinden dengeli bir merkle ağacı oluşturulur; bu paralel hesaplama hızı için yapılır. Blok başlığı, yaprakları tek tek kırma bireysel ağaçlarının kökleri olan dengeli bir merkle ağacının kökünü içerir. [2]

#### 3.0.5 Likidite

Bir dijital varlık geçerli piyasa fiyatlarına kısa vadeli bir etkisi olmadan, normal işlem hacimlerinde kolayca satılır veya satın alınırsa likit olur. In order to achieve such a status, traditionally any tradable asset must surmount a trading volume threshold sufficient to support stability. Specifically, we anticipate adopting the following methodologies: Loopring protocol with the use of EOS.IO contracts acting as nodes.[5] Bancor algorithm used to bring stability to the digital asset.[6] Toggles between these protocols and HTLC (atomic swaps) according to Vespucci analyses on the VDex network.

#### 3.0.6 Şifreli Zaman Aşımı Sözleşmeleri (Atomik Takaslar)

A Hashed Timelock Contract (HTLC)[1] is a smart contract enabling the implementation of time-bound transactions. Users will be offered a variable lock-in period for their transactions, with a discount on transaction fees in exchange for choosing a longer lock-in period.

### 3.1 AĞ TOPOLOJİSİ

#### 3.1.1 Düğümler

Düğümler VDex borsasının son noktalarıdır. İşlevleri:

1. Verto cüzdanı vasıtasıyla VDex'e portallar olarak rol yapın.

2. Emir kitabı bilgilerini birleştir.

3. Emir kitabını kapat.

4. Emir iptalini yönet.

5. RAFT protokolü için zaman aşımlarını atayın.

6. Doldurulan emirler için sözleşmeleri başlat.

Düğümler her işlem için ücretin bir kısmını kazanır. Eğer bir kullanıcının yeterli fonu varsa ve iyi bir sicile sahipse, Verto cüzdanı bir düğüm gibi davranabilir.

#### 3.1.2 Toplayıcılar

VDex toplayıcıları simülatör ve güvenlik amacıyla Volentix sunucularına verilmiştir. One of their functions is to pull logs and order book data from nodes into sparse distributed representations for hierarchical temporal memory as intrusion [7] analysis for detecting anomalies in the system. Toplayıcılar ayrıca metachain defterleri ve blok zinciri sıyırıcıları gibi diğer bileşenlere de ev sahipliği yapacaktır.

#### 3.1.3 Gecikme

EOS.IO düşük gecikmeli blok onayına sahip (0.5 saniye).[5] Bu gecikme derecesi, bu zincirler benzer gecikmeyi kabul ettiğinde diğer blok zincirleriyle yapılan işlemlerde korunabilir. But fundamentally the transaction is only as rapid as the lesser-rapid chain in the equation. Örneğin, bir Bitcoin bloğunun işlem için yaklaşık on dakika gerektirdiği iyi bilinmektedir. Receiving a transaction hash does not mean the transaction is confirmed; it means only that a node accepted the transaction without error, although there is generally a high probability other block producers will accept it.

### 3.2 EMİR KİTABI

Emir defteri ilgili kullanıcılardan VDex kayıtları al-ve-sat emirlerinin listesidir. Eşleşen bir motor hangi emirlerin yerine getirilebileceğini belirlemek için bir emir defteri kullanır. Döngü protokolü, emir defteri veri yapısını özelleştirmeye izin verir.[5] EOS.IO tarafından sağlanan kaplar, optimum performans için kullanılabilir.[8]

#### 3.2.1 Veri yapıları

Döngü Protokolü FIFO (ilk-giren ilk-çıkan) dairesel arabelleği kullanan düğümler, emir defterlerini bir kullanıcının emrini görüntülemek ve eşleştirmek için tasarlayabilir. Bu yöntem limit emirlerinin yalnızca fiyata göre konumlandırıldığı OTC modelini izler.[5] EOS.IO süreklilik API'ına atıfta bulunarak, emir kitabı, aynı EOS.IO hesabı üzerinden düğümler arasında paylaşılan çok dizinli güçlü kapsayıcıdan yararlanabilir.

#### 3.2.2 Açık-Zincir emir kitabı

An on-chain order book is a record of offers residing on the wallet (node) chosen to settle the order book. It resides in a persistent database on each node subscribing to the same account as all the other nodes.

#### 3.2.3 Kapalı-Zincir emir kitabı

Residing on the aggregator, offline order books serve for simulator and security purposes.

#### 3.2.4 Decentralization process of order book settlement

For decentralization purposes, nodes will take turns to settle the order book. The settling node must be designated by the protocol and all order book entries from all nodes must be available to the settling nodes. We believe the RAFT[9] and PARSEC[10] consensus mechanisms offer effective solutions. RAFT is a well-established algorithm and is easy to implement.[7] PARSEC is more recent and more efficient, using Directed Acyclic Graph (DAG) technology and eliminating the need for copying logs.

### 3.3 EMİR VERME

Emir verme geleneksel finansal piyasa işlemlerinin bilinen öğelerini içerir. Utilizing FIFO technology to design the order book, VDex intends to check order, inventory, and fill rate, as well as limit orders and cancellations.

### 3.4 VTX

#### 3.4.1 VTX Çıkarma ve Kullanımı

VTX is the native digital asset to be issued and used on the VDex decentralized exchange. We currently plan to use an eosio.token contract from the EOS.IO framework to issue 2.1 billion EOS.IO-compliant VTX tokens with a supply of 1.3 billion. VTX çeşitli kullanım alanlarına sahip olacaktır, örneğin:

Fikir birliği sürecinde ve Venue kampanyalarında katılımcıları ödüllendirmek için.

To pay and redistribute transaction fees on the VDex exchange.

To submit and vote on proposals to the Volentix ecosystem, using the voting rights allocated to VTX holders.

To stake support for reviewing proposals and implementing projects.

To incentivize users to participate in order book settlement by becoming nodes via their Verto wallets.

To incentivize users to lock funds in for \>24 hours by HTLC time-bound transactions.

#### 3.4.2 VTX Tahsisi

A digital assets ecosystem requires an array of certain fundamental human constituents who shepherd the project forward.[11] It is essential to compensate those individuals for their participation. Subject to adjustment, Volentix currently anticipates the following allocations:

1. Katkıda Bulunanlar. %12. An array of individuals, akin to founders, who contribute insights, time and talent, though often work without early compensation.

2. Destekçiler.

1. Aşama %5. Erken pasif tohum fon sağlayıcıları.

2. Aşama %28. Nitelikli özel ön satışlar ve olası kamu satışları aracılığıyla fon verenler.

3. Yardımcılar. (Danışmanlar, Geliştiriciler, Destekleyiciler, Saklayıcılar). Bu kategorideki alt kategorilerden yardım taleplerinin, projenin önemli miktarda finansman desteği almadan önce ve sonra önemli ölçüde farklılık gösterebileceğini unutmayın ancak bazı kişiler her iki aşamada da hizmet verebilir.

1. Aşama %10.

2. Aşama %10.

4. Merkezi olmayan hazine. %35. Topluluk üyeleri merkezi olmayan özerk bir organizasyonun (DAO) ilerici gelişimine katılım için teşvik edildi ve ödüllendirildi. Merkezi olmayan bir hazinenin akıllı sözleşmeler ve topluluk fikir birliği ile yönetilmesi bekleniyor.

#### 3.4.3 VTX Dağıtımı

Bu yazım sırasındaki piyasa koşulları ışığında Volentix, VTX dağıtımının zamanlamasını, araçlarını ve şartlarını ve koşullarını özel satış öncesi ve olası kamu satışının bir fonksiyonu olarak görüyor. Lütfen güncellemeler için Web sitemizi izleyin.

### 3.5 EOS.IO PLATFORM DAĞITIMI

Aşağıdaki hususlar EOS.IO platformunda VDex değiş tokuşunu uygulamamızla ilgilidir:

Bir sözleşmeyi dağıtmanın bir bedeli vardır ancak kullanımı ücretsizdir.

Geliştiriciler akıllı bir sözleşme yapmak için EOS.IO-uyumlu tokenler kullanır. Sözleşme dağıtıldıktan sonra, kilitli tokenler iade edilir.

Merkezi olmayan uygulamalar sözleşmelerine bellek, CPU, bant genişliği ve diğer kaynakları tahsis eder.

Aynı konuya birden fazla mesaj ve birden fazla hesap atanabilir.

### 3.6 BLOK ZİNCİRİ ETKİLEŞİMİ

#### 3.6.1 Blok Zinciri-Arası İletişim

EOS.IO Blok Zincir-Arası İletişim (IBC) hafif kanıtlar yapmak için tasarlanmıştır. For chains with insufficient capacity for processing the IBC proofs and establishing validity, there is an option to default to trusted oracles/escrows. With an EOS.IO-based smart contract, a trusted multi-signature wallet holding the asset in escrow can be used to persuade the signing/publishing of the transaction based on IBC proofs from the originating chain.

#### 3.6.2 Çoklu-Blok Zinciri Bilgisi

Comprehensible multi-blockchain information can be obtained by aggregating blockchain timelines in parallel order (with variance in the frequency of change of state). This system can trigger multi-chain load balancers, transfer states, draw data outputs from smart contracts, and foreign blockchain transaction execution. Relative block distance, relative global state, and timestamped events are recorded on a global ledger to optimize and confirm transactions before they actually happen on the native chain. This approach could also be used to determine block production coincidence between chains to access greater liquidity.[12]

### 3.7 GÜVENLİK ENDİŞELERİ

Bazı varsayımları ortadan kaldırmak için prototip aşamasını takiben, güvenlik testine başlamak istiyoruz. Security concerns are of paramount importance to users and must be addressed. Threats include, for example, an attacker executing malicious code within a transaction or manipulating the order of transactions or the timestamps of blocks. In the following sections, we address certain security measures and specific security threats and remedies.

### 3.8 GÜVENLİK ÖNLEMLERİ

#### 3.8.1 Güvenlik sözleşmesi

Retain vast majority of funds in a time-delayed, multi-signature-controlled account.

Use multi-signatures on a hot wallet with several independent processes/servers double-checking all withdrawals, with the concomitant benefit of creating a trusted list of accounts.

Deploy a custom contract that allows withdrawals only to accounts verified by KYC/AML.

Deploy a custom contract that accepts only deposits of known assets from accounts verified by KYC/AML.

Deploy a custom contract that requires a mandatory 24-hour waiting period for all withdrawals.

Utilize contracts with hardware wallets for all signing, including for automated withdrawals.

Bozuk sözleşmeleri yükseltin.

Include ability to pause the functionality of a contract.

Include ability to delay an action of a contract.

#### 3.8.2 Hileli işlemleri denetleme

Numenta'nın Nupic kütüphanesi tarafından sağlanan gelişmiş anomali tespit algoritmaları geleneksel AI sistemlerine göre daha az hacimli eğitim veri setleri gerektirecektir.

#### 3.8.3 Rasgeleleştirme

True randomisation of address space layout, route or utilizing varying lengths of timeouts as in the RAFT protocol can complexify systems enough to enhance resilience and further secure systems against a side-channel attack or front running.

#### 3.8.4 Günlük denetim

Parsec fikir birliğinin tespiti için kayıtlara dayanmaz. Diğer yandan, RAFT buna ihtiyaç duyacaktır. Her durumda, Doğrulayıcı düğümleri, işlem süreci süresini en aza indirmek İçin fikir birliği belirlemek için minimum bilgi gerektirecek şekilde tasarlanacaktır.

#### 3.8.5 Alım Kanıtı olarak İşlem (TaPoS)

This mechanism prevents the replay of a transaction on forks that do not include the referenced block. Signals the network that a particular user and stake are on a specific fork.

### 3.9 Güvenlik tehditleri ve çözüm yolları

#### 3.9.1 Çifte harcama

Çifte harcama belirli bir kripto para birimi hissesinin birden fazla işlemde harcandığı bir saldırıdır.

Çakışan iki işlem hızlı bir şekilde ağa art arda gönderildiğinde bir yarış saldırısı gerçekleşir.

A Finney attack pre-mines one transaction into a block and spends the same tokens before releasing the block to invalidate that transaction.

Bir ağın toplam bilgi işlem gücünün \>%50'sine sahip olan herhangi biri tarafından %51 saldırısı gerçekleştirilebilir. A majority ownership position permits reversal of any transaction and allows total control of selection of transactions appearing in blocks. EOS.IO, Loopring ve RAFT bu problemi önlüyor gibi görünüyor. Eğer bir blok üreticisi makul olmayan miktarda bir çalışma süresi alırsa veya yeterince karlı değilse, işlem kara listeye alınır.[5]

#### 3.9.2 Ön koşu

A front runner steals one or more orders from a pending order book settlement transaction. Both EOS.IO and Loopring offer remedies in which keys are protected because they are not part of the on-chain transaction, and therefore remain unknown to parties other than the owner. Only the order book settling node is possessed of the sensitive information, and each node uses a different solution for resolving the order books, introducing yet another level of complexity to promote security.

#### 3.9.3 Sahte kimlikler

Kötü niyetli kullanıcılar Loopring düğümlerine saldırmak için çok sayıda küçük sipariş göndermek için sahte kimlikler oluştururlar. Bununla birlikte, bu siparişlerin çoğu eşleştiğinde tatmin edici kar elde etmediği için reddedilecektir.

#### 3.9.4 Yetersiz Bakiye

Kötü niyetli kullanıcılar değeri sıfır olmayan, ancak adresi sıfır bakiyeli olan siparişleri imzalar ve yayarlar. Nodes monitor actual balances, update these order states accordingly, and then discard them.

#### 3.9.5 Zamanlama saldırısı

Timing attacks are a class of cryptographic attacks through which a third-party observer can deduce the content of encrypted data by recording and analyzing the time taken to execute cryptographic algorithms. RAFT algoritması, zamanlama saldırılarını zaman aşımlarının rastgeleliğini kullanarak önler.

### 3.10 KULLANICI DENEYİMİ

Kullanıcı deneyimine odaklanmamız önceliklidir. VTX ve Volentix'in dört ayağını -- Venue, Verto, Vespucci ve VDex -- topluluğumuza katılmak isteyen herkes tarafından kolayca erişilebilir ve kullanılabilir hale getirmek istiyoruz. We expect the experience continually to be educational as well, with templates and simulators to support a superior UX/UI relationship.

### 3.11 DOĞRU MERKEZSİZLEŞME

EOS.IO, merkezi olmayan uygulamalar için açık kaynaklı ölçeklenebilir bir altyapıdır. Its goal is a fair and transparent block producer (BP) election process utilizing a democratic delegated proof of stake (DPoS) consensus. Particularly as such a system just begins to proliferate, there will be glitches. Therefore, some degree of retained centralization is inevitable and necessary. But our guiding philosophy is one of decentralization, and our ongoing efforts are targeted to promoting a reduction in dependence on central authority.

For example, initially we plan to erect a system for electing nodes (when solving order books) that will not use a shared central clock or DPoS but instead will be based either on random timeouts for the determination of leaders in an election (RAFT) or on Directed Acyclic Graph (DAG) in the PARSEC protocol.

### 3.12 SİSTEM KURTARMA

The RAFT and PARSEC protocols provide a robust system for recovery in the case of node failure. Security measures are also provided for trading between and among native blockchains. If a chain defies identification, the system defaults to the next block or a short time lock.

### 3.13 GELİŞEN MİMARİ

Daily announcements of fresh code developments impacting on use of digital assets reveal the tremendous benefit of the open-source code philosophy. Volentix olarak, son on yılda dijital varlık uygulamaları geliştirmeye yönelik birçok erken göçmen tarafından tahsis edilen muazzam finansal kaynakların lehtarları olduğumuzu biliyoruz. We now have an opportunity to take the next step by creating VDex, a decentralized exchange for the next generation of digital assets transactions.

## 4. SON DÜŞÜNCELER

All of us at Volentix are dedicating our work and insights to developing a program premised on empowerment and independence. If you are of a mind to join us, in whatever capacity, then please do so and please become educated on the topics contained in this white paper and additional Volentix publications as we share them with our community.

## 5. ZAMAN ÇİZELGESİ

Please monitor our website and social media for updates and other important announcements. İlginiz ve dikkatiniz için çok teşekkür ederiz.

## FERAGATNAME

This white paper was prepared, and is presented, for information purposes only. The information presented does not purport to be comprehensive. The information is subject to change in whole or in part at any time without notice. Volentix Labs reserves the right to amend, replace, remove, or delete any and all information at the sole and exclusive discretion of Volentix. Volentix Labs makes no representation or warranty, expressed or implied, concerning the accuracy or completeness of the information and expressly disclaims any and all liability of any and all kinds whatsoever for the information contained or not contained. Volentix Labs requests each and every reader to read the information fully and carefully, and to undertake independent investigation and analysis of the information, and to seek and obtain professional advice for purposes of evaluating the information. To the knowledge of Volentix Labs, no regulatory agency, government, or other third-party enforcement entity has reviewed, evaluated, or approved any part or all of the information. This information is not an offer or solicitation of any kind whatsoever and does not form the basis for any contract or commitment of any kind whatsoever. Any statement considered to be forward-looking is purely a matter of opinion, and no viewer should rely on any such statement or on any part or all of the information in any way whatsoever.

## DİPNOTLARI

1. K. Kurokawa, Atomic cross chain transfer, an overview, (2015).

2. EOS.IO, Eos.io teknik tanıtım belgesi v2, (2018).

3. . T. Earl, Soa hizmet tasarım ilkeleri, (2016).

4. blockchainhub.net, blockchain-oracles, (2017).

5. F. Zhou, Wang, Loopring: Merkezi olmayan bir token değiş tokuş protokolü, (2018).

6. G. B. Eyal Hertzog, Guy Benartzi, Bancor protocol: Continuous liquidity for cryptographic tokens through their smart contracts, (2018).

7. L. Lamport, yarı zamanlı parlamento, (1998).

8. D. Larimer, eosio.boot telegram sohbeti, (2018).

9. J. O. Diego Ongaro, Anlaşılabilir bir fikir birliği algoritması arayışı içinde, (2018).

10. F. H. Q. M. S. S. Pierre Chevalier, Bart lomiej KamiÂťnski, Eş zamanlı olmayan, dürüst, güvenli ve verimli bir fikir birliği için protokol (parsec), (2018).

11. Dane Keller Rutledge, Dijital Varlıklar Ekosisteminin (DAE) Temel İnsan Bileşenleri. (2018).

12. BlockColliderTeam, Blok çarpıştırıcısı tanıtım belgesi, (2018).

## EK REFERANSLAR

Aelf, Bir çoklu-zincir paralel hesaplama blok zinciri çatısı, (2018).

ARK, Tüketici kabulü için bir platform, (2018).

V. Buterin, Ethereum: yeni nesil akıllı sözleşme ve merkezi olmayan bir uygulama platformu, (2013).

S. Cormier, A machine based societal model for curbing citizen cynicism, (2017).

M. Duncan, Quale, Halo platformu, (2018).

S. D. K. M. T. S. H. Garcia-Molina, P2p ağlarında itibar yönetimi için eigentrust algoritması, (2018).

M. R. Garrick Hileman, Küresel kripto para birimi kıyaslama çalışması, (2017).

Komodo, Özgürlük odaklı, gelişmiş bir blok zinciri teknolojisi, (2018).

Q. Likit, Likit olmayan kripto ekonomisine likidite sağlanması, (2018).

S. R. M.P.M-S, Aniket Kate Matteo Maffei, Ödeme kanalı ağlarıyla eş zamanlılık ve gizlilik, (2017).

SingularityNET, Bir merkezi olmayan, açık pazar ve ais için ağlar arası, (2018).

M. M. Timo Hanke ve D. Williams, Dfinity teknolojisine genel bakış serisi fikir birliği sistemi, (2018).

A. B. Will Warren, 0x: Ethereum blok zinciri üzerindeki merkezi olmayan borsa için açık bir protokol, (2017).

G. Wood, Ethereum: A secure decentralised generalised transaction ledger.ethereum project yellow paper, (2014).

Dane Keller Rutledge, Creating a Comprehensive Digital Assets Ecosystem (DAE), (2018).

## BELGENİN SONU