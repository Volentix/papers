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

Ang Vespucci ay inaasahan bilang isang analytics engine naa-access sa pamamagitan ng isang user-friendly na interface na may treasure troves ng real-time at historikal na datos sa merkado, tulad ng mga digital na mga pang-rate ng asset at sentiment na pagsusuri. Nais naming bigyan ng kapangyarihan ang mga gumagamit na may mga tool para talaguhitan at ihambing ang mga tradeable digital assets, upang ma-akses at mai-parse ang historikal na mga talaan ng kalakalan, para mag-plot ng mga trend at mga pattern, at para masubaybayan at suriin ang mga pag-develop ng open-source software. Naglalayong dalhin sa iyong mga kamay ang tiwala at komprehensibong datos ng Vespucci na nauugnay sa merkado sa pamamagitan ng pagsasama ng impormasyon na kasalukuyang nakakalat sa maraming iba't ibang mga block, website, chat room, at palitan.

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

Ang kilala at tanyag na programming language na C++ ay lilitaw na lubhang angkop para sa WASM. Ang C ++ ay may mataas na mature na suporta sa pagde-debig at mga library. Ang codebase ng EOS ay gumagamit ng mga template na liberally, at C++ ay nagpapahintulot sa paggamit ng mga template at opereytor sa pag-overload para tukuyin ang isang runtime cost-free na balidasyon ng mga yunit. Ang program ay ini-reinitializes para linisin ang estado sa simula ng bawat mensahe, isang natatanging kalamangan na streamlines pagbabalangkas ng mga matalinong kontrata. Ang framework ng WebAssembly ay awtomatikong tatanggihan ang anumang transaksyon na tumutugon sa memory nang hindi wasto. Sa kaso ng dynamic na alokasyon ng memory ay kinakailangan, ang mga gumagamit ay pwedeng umalis sa mga smart pointer dahil ginagamit ng mga kontrata ng EOS.IO ang C++14. Kapansin-pansin na ang unang implimentasyon ng PARSEC Directed Acyclic Graph (DAG) na teknolohiya ay inaasahan na nasa Rust.

#### 3.0.2 Tinukoy ng iskema ang mga mensahe at database

Ginawang pamantayan ang mga kontrata ng serbisyo para magbigay ng isang baseline measure ng interoperability sa pagitan ng at sa mga sistem na disparate sa pamamagitan ng harmonisasyon ng mga modelo ng datos. Sa katotohanan, ang prinsipyo ng disenyo ng Standardised Service Contract ay nagtataguyod na ang mga kontrata sa serbisyo ay batay sa mga pamantayang modelo ng datos. Tapos na ang pagsusuri sa blueprint ng serbisyo ng imbentaryo para malaman ang mga karaniwang nangyayari na mga dokumento ng negosyo na ipinagpapalit sa pagitan ng mga serbisyo. Binubuo ng isang standardized na paraan ang mga dokumentong ito sa negosyo. Ang pattern ng Canonical na Iskema ay binabawasan ang pangangailangan para sa aplikasyon ng pattern ng transpormasyon ng disenyo ng modelo. [3]

#### 3.0.3 Inter-Contract Communication

Ibinahagi na ang datos sa pagitan ng mga kontrata sa pamamagitan ng isang orakulo, na, "sa konteksto ng mga blockchain at matalinong kontrata, ay isang ahente na nakakahanap at nagpapatunay ng mga pangyayari sa real-world at nagsusumite ng impormasyong ito sa isang blockchain na gagamitin ng mga matalinong kontrata." [4] Ang bawat node ay magkakaroon ng magkaparehong kopya ng mga datos na ito, para magamit sa matalinong kompitisyon ng kontrata. Sa halip na ang nagpa-function ang matalinong kontrata para hilahin ang datos, sa halip ang pinupush ng orakulo ang datos papunta sa blockchain. Sa halimbawa ng isang blockchain, ang karamihan sa pagbabasa ng datos ay ginagawa sa pamamagitan ng polling na "mga modelo" para masubaybayan ang estado ng blockchain at para maisagawa ang ilang mga aksyon sa pagtugon.

#### 3.0.4 Sidechains

Sa EOS.IO, ang pagbibigay ng isang digital na asset ay lumilikha ng isang sidechain, na isang lumilitaw na mekanismo na nagpapahintulot sa mga digital na asset mula sa isang blockchain para maging ligtas sa paggamit sa isang hiwalay na blockchain at pagkatapos ay inilipat pabalik sa orihinal na blockchain. Ang kahusayan sa pagpoproseso ay na-promote sa pamamagitan ng paglikha ng maramihang mga sidechain. Ang isang TCP-na tulad ng tsanel na komunikasyon sa pagitan ng iba't-ibang mga blockchains ay sinusuri ang mga patunay. Para sa bawat shard (isang yunit ng parallelizable execution sa isang cycle), isang balanseng merkle na tree ang itinatayo ng mga aksyon na ito sa pagkilos para bumuo ng isang pansamantalang ibinahaging merkle root; ito ay ginagawa para sa bilis na pagkukuwenta ng magkakahelera. Ang block na header ay naglalaman ng root ng isang balanseng merkle na tree na ang mga dahon nito ay mga root ng mga indibidwal na shard merkle tree. [2]

#### 3.0.5 Liquidity

Ang isang digital na asset ay liquid kung ito ay madaling ibenta o binili sa karaniwang mga bolyum ng kalakalan nang walang isang makabuluhang panandaliang epekto sa kanyang umiiral na presyo sa merkado. Para makamit ang naturang estado, ayon sa tradisyon ang natitrade na asset ng namimili ay dapat magtagumpay sa limitadong dami ng kalakalan para suportahan ang katatagan. Sa partikular, inaasahan namin na gagamitin ang mga sumusunod na pamamaraan: Loopring protocol sa paggamit ng mga kontrata ng EOS.IO na nagpapanggap bilang mga node.[5] Ang algoritmo ng Bancor na ginamit para dalhin ang katatagan sa digital na asset.[6] Tina-toggle sa pagitan ng mga protocol na ito at HTLC (atomic swap) ayon sa Vespucci na pagsusuri sa network ng VDex.

#### 3.0.6 Hashed Timelock Contracts (Atomic Swaps)

Isang Hashed Timelock Contract (HTLC)[1] ay isang matalinong kontrata na nagpapahintulot sa pagpapatupad ng mga transaksyon na may takdang oras. Inaalok ang mga gumagamit ng isang variable na lock-in na period para sa kanilang mga transaksyon, na may diskwento sa mga bayarin sa transaksyon bilang kapalit ng pagpili ng mas mahabang period ng pag-lock.

### 3.1 NETWORK TOPOLOGY

#### 3.1.1 Mga Node

![](../9.jpg)

Ang mga node ay ang mga endpoint ng VDex na palitan. Ang kanilang mga function ay:

1. Nagpapanggap bilang mga portal sa VDex sa pamamagitan ng wallet ng Verto.

2. I-merge ang impormasyon ng order book.

3. I-settle ang order book.

4. Pamahalaan ang kanselasyon ng order.

5. Magtalaga ng mga timeout para sa protolol na RAFT.

6. Magsimula ng mga kontrata para sa mga order na napunan.

Ang mga node ay nag-earn ng isang porsyon ng bayad para sa bawat transaksyon. Kung ang isang gumagamit ay may sapat na pondo at nagtataglay ng isang mahusay na trak ng rekord, ang kanyang wallet na Verto ay pwedeng kumilos bilang isang node.

#### 3.1.2 Mga Aggregator

Ang mga VDex na aggregator ay nakatuon sa mga serber ng Volentix para sa mga layunin ng pag-simulate at seguridad. Ang isa sa kanilang mga function ay para kunin ang mga log at order book ng datos mula sa mga node sa kalat-kalat na ibinahagi na representasyon para sa hierarchical temporal memory bilang panghihimasok [7] sa pagsusuri para sa pag-detect ng mga anomalya sa sistem. Ang mga aggregator ay magkakaroon din ng host sa iba pang mga bahagi tulad ng mga metachain na ledger at blockchain na scraper.

#### 3.1.3 Latency

Ang EOS.IO ay may mababang latency sa pag-block ng kumpirmasyon na (0.5 segundo).[5] Ang antas ng latency na ito ay maaaring mapanatili sa mga transaksyon sa iba pang mga blockchains kung ang mga chain ay ina-admint ng mga katulad na latency. Pero sa panimula ang transaksyon ay kasing bilis lamang ng mas mababang-rapid na chin sa pagpapantay. Ito ay kinikilala na mahusay, halimbawa, na ang isang Bitcoin block ay nangangailangan ng humigit-kumulang sampung minuto para sa pagpoproseso. Ang pagtanggap ng isang transaksyon ay hindi nangangahulugan na ang transaksyon ay nakumpirma; ito ay nangangahulugan lamang na ang isang node ay tinanggap ang transaksyon nang walang error, bagama't sa pangkalahatan ay isang mataas na posibilidad ng iba pang mga nagpo-produce na block ay tanggapin ito.

### 3.2 ORDER BOOK

Ang order book ay ang listahan ng mga buy-and-sell na mga order ng mga rekord ng VDex mula sa mga interesadong gumagamit. Isang magkatugma na engine ay gumagamit ng isang order book para matukoy kung aling mga order ang matutupad. Ang protokol na Loopring ay nagpapahintulot para sa pagpapasadya ng istraktura ng datos ng order book.[5] Ang mga container na ibinigay ng EOS.IO ay maaaring gamitin para sa mahusay na pagganap.[8]

#### 3.2.1 Mga istraktura ng datos

Gamit ang FIFO ng protokol na Loopring (first-in first-out) na circular buffer, na pwedeng mag-disenyo ng mga node ang kanilang order book para maipakita at tumutugma sa isang gumagamit ng order. Ang metodong ito ay sumusunod sa isang modelo ng OTC, kung saan ang mga order ng limitasyon ay nakaposisyon batay sa presyo lamang.[5]

Ang EOS.IO ay tinutukoy ang persistence na API, ang order book ay pwedeng samantalahin ang makapangyarihang multi-index na container na ibinahagi sa mga node sa pamamagitan ng parehong akawnt na EOS.IO.

#### 3.2.2 On-Chain order book

Ang isang on-chain na order book ay isang talaan ng mga nag-aalok na nakalagay sa wallet (node) na pinili para bayaran ang order book. Ito ay nakalagay sa isang persistent na database sa bawat node na nag-subscribe sa parehong akawnt tulad ng lahat ng iba pang mga node.

#### 3.2.3 Off-Chain order book

Nakalagay sa aggregator, sini-serve ang offline na order book para simulator at layunin ng seguridad.

#### 3.2.4 Desentralisasyon sa pagproseso ng pag-settle sa order book

Para sa mga layuning desentralisasyon, ang mga node ay magpapalitan para ma-settle ang order book. Ang node sa pagse-settle ay dapat na itinalaga ng protokol at ang lahat ng mga entry ng order book mula sa lahat ng mga node ay dapat na magagamit sa pagse-settle ng mga node. Naniniwala kami na ang RAFT[9] at PARSEC[10] na mga mekanismo ng pinagkasunduan ay nag-aalok ng mga epektibong solusyon. Ang RAFT ay isang mahusay-na-itinatag na algoritmo at madaling ipatupad.[7] Ang PARSEC ay mas bago at mas mahusay, gamit ang Directed Acyclic Graph (DAG) na teknolohiya at inaalis ang mga kinakailangan para sa mga log ng pagkopya.

### 3.3 ORDER SETTLEMENT

Ang order settlement ay naglalaman ng mga pamilyar na elemento ng pinansyal na kagawianin na transaksyon sa pamilihan. Ang teknolohiya na FIFO ay ginagamit para mag-disenyo ng order book, nais ng VDex na suriin ang order, imbentaryo, at fill rate, pati na rin ang limitasyon ng mga order at pagkansela. ![](../7.jpg)

### 3.4 VTX

#### 3.4.1 Pag-isyu at Paggamit ng VTX

Ang VTX ay ang katutubong digital na asset na iisyu at ginagamit sa VDex desentralisadong palitan. Pinaplano namen sa kasalukuyan na gumamit ng isang kontrata ng eosio.token mula sa framework ng EOS.IO para mag-isyu ng 2.1 na bilyon na mga token ng VOS ng EOS.IO na may suplay na 1.3 na bilyon. Ang VTX ay magkakaroon ng magkakaibang hanay ng paggamit, para sa halimbawa:

Para gantimpalaan ang mga kalahok sa proseso ng pinagkasunduan at sa mga kampanya sa Venue.

Para magbayad at mamahagi ng mga bayarin sa transaksyon sa palitan na VDex.

Para magsumite at bumoto sa mga panukala sa ekosistema na Volentix, gamit ang mga karapatan sa pagboto na inilalaan sa mga may hawak ng VTX.

Para sa suporta sa stake para sa pagri-ribyu ng mga panukala at pagpapatupad ng mga proyekto.

Para sa insentibo ng mga gumagamit para lumahok sa pagse-settle sa order book ay sa paparating na node sa pamamagitan ng kanilang mga wallet ng Verto.

Para sa insentibo ng mga gumagamit para i-lock ang mga pondo sa loob ng >24 na oras sa pamamagitan ng mga transaksyon na may takdang oras ng HTLC.

#### 3.4.2 Alokasyon ng VTX

![](../6.jpg)

Ang isang digital assets ecosystem ay nangangailangan ng isang hanay ng ilang pangunahing mga nasasakupan ng human na nagpapastol sa proyektong ito.[11] Mahalaga na bayaran ang mga indibidwal para sa kanilang pakikilahok. Alinsunod sa pag-aayos, kasalukuyang binabanggit ng Volentix ang mga sumusunod na alokasyon:

1. Mga kontribyutor. 12%. Ang isang hanay ng mga indibidwal, katulad ng mga tagapagtatag, na nag-aambag ng mga pananaw, oras at talento, kahit na madalas ay nagtatrabaho nang walang maagang kabayaran.

2. Mga taga-suporta.

Yugto 1.5%. Maagang mga funder sa pasibong seed.

Yugto 2. 28%. Mga funder sa pamamagitan ng kwalipikadong pribadong pre-sales at posibleng pagbebenta sa publiko.

3. Mga facilitator. (Mga Tagapayo, Mga Nag-develop, Mga Tagapagtaguyod, Mga Tagapangalaga). Paalala na ang mga kinakailangan para sa tulong mula sa mga sub-na kategorya sa kategoryang ito ay pwedeng magkakaiba bago at pagkatapos ng proyekto ay tumatanggap ng malaking suporta sa pagpopondo, pero ang ilang mga indibidwal ay maaaring maglingkod sa panahon ng parehong mga yugto.

Yugto 1. 10%.

Yugto 2. 10%.

4. Desentralisadong pananalapi. 35%. Ang mga miyembro ng komunidad ay insentibado at ginantimpalaan para sa partisipasyon sa progresibong pag-unlad ng isang decentralized autonomous organization (DAO). Ang isang desentralisadong pananalapi ay inaasahang ibibigay ng mga matalinong kontrata at consensus ng komunidad. ![](../5.jpg)

#### 3.4.3 Distribusyon ng VTX

Sa liwanag ng mga kondisyon sa merkado sa panahon ng pagsulat nito, Kinukonsidura ang pag-timing ng Volentix, paraan, at mga tuntunin at kondisyon ng pamamahagi ng VTX bilang isang function ng pribadong pre-sales at posibleng pagbebenta sa publiko. Para sa mga update mangyaring subaybayan ang aming websayt.

### 3.5 EOS.IO PLATFORM DEPLOYMENT

Ang mga sumusunod na konsiderasyon ay may kaugnayan sa aming pag-deploy ng palitan na VDex sa platapormang EOS.IO:

Ang pag-deploy ng isang kontrata ay may bayad pero libreng gamitin.

Nagtatakda ng mga token ang mga Nag-develop ng EOS.IO para mag-deploy ng matalinong kontrata. Matapos i-deploy ang kontrata, ibabalik ang naka-lock na mga token.

Ang mga aplikasyon na desentralisado mga ay naglalaan ng memory, CPU, bandwidth, at iba pang mga mapagkukunan sa kanilang mga kontrata.

Ang maramihang mga mensahe at maraming mga akawnt ay maaaring italaga sa parehong thread.

### 3.6 INTERASKYON NG BLOCKCHAIN

#### 3.6.1 Komunikasyon ng Inter-Blockchain

Dinisenyo ang EOS.IO ay para gumawa ng Inter-Blockchain Communication (IBC) ng mga magagaang patunay. Para sa mga chain na may sapat na kapasidad para sa pagpoproseso ng mga patunay ng IBC at pagtatatag ng bisa, mayroong isang pagpipilian para i-default sa mga pinagkakatiwalaang mga orakulo/escrow. Sa pamamagitan ng isang EOS-bases na matalinong kontrata, ang isang pinagkakatiwalaang multi-signature na wallet na may hawak na asset sa escrow ay pwedeng magamit para hikayatin ang pag-sig /paglalathala ng transaksyon batay sa mga patunay ng IBC mula sa nagbuo ng chain.

#### 3.6.2 Impormasyon ng Multi-Blockchain

Pwedeng makuha ang impormasyon ng multi-blockchain na pwedeng maunawaan sa pamamagitan ng pag-aggregate ng mga timeline ng blockchain na magkakasabay (na may pagkakaiba sa frequency ng pagbabago ng estado). Ang sistem na ito ay pwedeng mag-trigger ng multi-chain sa pag-load ng mga balancer, mga estado ng paglipat, gumuhit ng mga output ng datos mula sa mga matalinong kontrata, at pagpapatupad ng transaksyon ng foreign blockchain. Kaugnay sa block ng distansya, relative sa pandaigdigang estado, at timestamped na mga kaganapan ay naitala sa isang global ledger para ma-optimize at kumpirmahin ang mga transaksyon bago sila aktwal na mangyari sa katutubong chain. Ang paraan na ito ay pwede ding gamitin para matukoy ang pagkakataon sa produksyon ng block sa pagitan ng mga chain para ma-akses ang mas higit na liquidity.[12]

### 3.7 MGA ALALAHANIN SA SEGURIDAD

Para maiwasan ang ilang mga pagpapalagay, nilalayon naming magsimula ng pagsubok sa seguridad kasunod ng yugto ng pagproto-type. Higit na mahalaga ang mga alalahanin sa seguridad sa mga gumagamit at dapat na matugunan. Kabilang sa mga pagbabanta, halimbawa, ang isang umaatake na nagsasagawa ng malisyosong code sa loob ng isang transaksyon o pagmamanipula ng pagkakasunud-sunod ng mga transaksyon o mga timestamp ng mga block. Sa mga sumusunod na seksyon, tinutugunan namin ang ilang mga hakbang sa seguridad at mga pag-tukoy sa pagbabanta sa seguridad at mga remedyo.

### 3.8 MGA KATANGIAN SA SEGURIDAD

#### 3.8.1 Kontrata sa seguridad

Panatilihin ang karamihan sa mga pondo sa isang oras na naantala, isang multi-signature na kinokontrol na akawnt.

Gumamit ng mga multi-signature sa isang mainit na wallet na may ilang mga independiyenteng proseso/mga serber na dobleng-itsitsek ang lahat ng mga withdrawal, na may kasamang benepisyo ng paglikha ng isang pinagkakatiwalaang listahan ng mga akawnt.

Magtakda ng pinasadyang kontrata na nagpapahintulot sa mga withdrawal lamang sa mga akawnt na napatunayan ng KYC/AML.

Magtakda ng pinasadyang kontrata na tumatanggap lamang ng mga deposito ng mga kilalang asset mula sa mga akawnt na napatunayan ng KYC/AML.

Magtakda ng pinasadyang kontrata na nangangailangan ng isang sapilitan na 24 na oras na paghihintay para sa lahat ng mga withdrawal.

Gamitin ang mga kontrata sa mga hardware na wallet para sa lahat ng pag-sign, kabilang ang para sa automated na mga withdrawal.

I-upgrade ang nasirang mga kontrata.

Kasama ang kakayahan na ihinto ang pag-function ng isang kontrata.

Kasama ang kakayahan na para maantala ang isang aksyon ng isang kontrata.

#### 3.8.2 Pag-awdit ng mga proseso ng pagnanakaw

Ang mga advance na algoritmo sa pagtuklas ng anomalya na ibinigay ng Nupic na library ng Nupu ay mangangailangan ng mas mababang mga hanay ng datos ng pagsasanay kaysa sa mga sistema ng conventional AI.

#### 3.8.3 Randominisasyon

Ang tunay na randomisasyon ng address ng layout ng space, ruta o paggamit ng iba't ibang mga haba ng mga timeout tulad ng sa protokol na RAFT ay maaaring kumplikado sapat na sistem para mapahusay ang kabanatan at karagdagang mga siguridad na sistem laban sa isang side-channel na pag-atake o harapang gumagana.

#### 3.8.4 Inspeksyon sa Pag-log

Ang Parsec ay hindi umaasa sa mga log para sa determinasyon ng mga consensus. Sa kabilang banda, kinakailangan ito ng RAFT. Sa anumang kaso, Ang mga node ng pagpapatunay ay idinisenyo apra mangailangan ng kaunting impormasyon Para matukoy ang pinagkasunduan para mabawasan ang oras ng proseso ng transaksyon.

#### 3.8.5 Transaction as Proof of Stake (TaPoS)

Pinipigilan ng mekanismong ito ang replay ng isang transaksyon sa mga fork na hindi kasama ang reperensiya ng block. Nag-signal ang network na ang isang partikular na gumagamit at stake ay nasa isang tiyak na fork.

### 3.9 Mga banta sa seguridad at mga remedyo

#### 3.9.1 Dobleng paggastos

Ang isang dobleng paggastos ay isang pag-atake kung saan ang isang partikular na cryptocurrency stake ay ginugol sa higit sa isang transaksyon.

Isang race ng pag-atake ay nangyayari kapag ang dalawang magkakontrahan na mga transaksyon ay ipinadala sa mabilis na pagkakasunud-sunod sa network.

Ang isang Finney na pag-atake ay nag-pre-mines ng isang transaksyon sa isang block at gumastos ng parehong mga token bago ilalabas ang block para magpawalang-bisa sa transaksyong iyon.

Ang isang 51% na pag-atake ay pwedeng ma-mount ng sinuman na may-ari >50% ng kabuuang power ng pagkwenta ng isang network. Karamihan sa pagmamay-ari ay pinapahintuloran ang isang pagsaliwa ng anumang transaksyon at nagpapahitulot sa kabuuang kontrol sa pagpili ng mga transaksyon na lumalabas sa mga block. Lumilitaw ang EOS.IO, Loopring, at RAFT para maiwasan ang problemang ito. Kung ang isang prodyuser ng block ay tumatagal ng isang hindi makatwiran na halaga ng runtime o hindi sapat na kapaki-pakinabang, pagkatapos ay ang proseso ay naka-blacklist.[5]

#### 3.9.2 Front running

Ang isang front runner ay kumukuha ng isa o higit pang mga order mula sa isang nakabinbing order book na transaksyon. Ang parehong EOS.IO at Loopring ay nag-aalok ng mga remedyo kung saan ang mga key ay protektado dahil hindi sila bahagi ng transaksyon sa on-chain, at samakatuwid ay nananatiling hindi kilala sa mga partido maliban sa may-ari. Tanging ang pagsi-settle node ng order book ay may nagmamay-ari sa sensitibong impormasyon, at ang bawat node ay gumagamit ng ibang solusyon para sa paglutas ng mga order book, na nagpapakilala ng isa pang antas ng pagiging kumplikado upang itaguyod ang seguridad.

#### 3.9.3 Mga huwad na pagkakakilanlan

Ang mga malisyoso na gumagamit ay lumikha ng mga huwad na pagkakakilanlan para magpadala ng isang malaking bilang ng mga maliliit na order para atakihin ang mga node ng Loopring. Gayunpaman, karamihan sa mga order na ito ay tatanggihan para sa hindi pagbibigay ng kasiya-siyang kita kapag naitugma.

#### 3.9.4 Hindi sapat ang balanse

Ang mga malisyoso na mga gumagamit ay nag-sign at kumakalat ng mga order na ang halaga ng kung saan ay di-sero per ang address na may sero na balanse. Ang aktwal na balanse ay sinusubaybayan ng mga node, i-update ang mga order na ito ayon sa naaayon, at pagkatapos ay itapon ang mga ito.

#### 3.9.5 Oras ng pag-atake

Ang oras ng pag-atake ay isang uri ng cryptographic na pag-atake kung saan ang isang third-party na tagamasid ay pwedeng pagmulan ng nilalaman ng naka-encrypt na datos sa pamamagitan ng pagtatala at pag-aaral ng oras na kinuha para mag-execute ng cryptographic na algoritmo. Pinipigilan ng algoritmo ng RAFT ang oras ng pag-atake sa pamamagitan ng paggamit ng randomness ng mga timeout.

### 3.10 KARANIWANG PAGGAMIT

Naka-pokus kame sa pangunahing nararanasanng gumagamit. Gusto naming gawin ang VTX at ang apat na mga pillar ng Volentix -- Venue, Verto, Vespucci, at VDex - madaling mapupuntahan at magagamit ng lahat ng mga nais na sumali sa aming komunidad. Inaasahan namin na ang karanasan ay patuloy na pang-edukasyon din, na may mga template at mga simulator para suportahan ang isang relasyon sa superior UX/UI.

### 3.11 TOTOONG DESENTRELESASYON

Isang open-source ang EOS.IO, scalable infrastructure para sa mga desentralisadong aplikasyon. Ang layunin nito ay isang patas at transparent na block producer (BP) ng eleksyon na gumagamit ng isang demokratikong delegado na proof ng stake (DPoS) na pinagkasunduan. Lalo na tulad ng isang sistem lamang ay nagsisimula para palaganapin, magkakaroon ng mga glitche. Sakatunayan, ang ilang antas ng napanatili na sentralisasyon ay hindi maiiwasan at kinakailangan. Pero ang ating gabay na pilosopiya ay isa sa desentralisasyon, at ang aming patuloy na pagsisikap ay naka-target sa pagtataguyod ng pagbawas sa pag-asa sa sentral na awtoridad.

Para sa halimbawa, sa umpisa plano naming magtayo ng isang sistem para sa pagpili ng mga node (kapag nilutas ang mga order book) na hindi gagamit ng isang nakabahaging sentral na clock o DPoS pero sa halip ay batay sa alinman sa random na mga timeout para sa determinasyon ng mga lider sa isang halalan (RAFT) o sa Directed Acyclic Graph (DAG) sa protokol ng PARSEC.

### 3.12 PAG-REKOBER SA SISTEM

Ang protokol ng RAFT at PARSEC ay nagbibigay ng isang matatag na sistem para sa pag-rekober sakaling mabigo ang node. Ang mga panukala sa seguridad ay ipinagkakaloob para sa pagitan ng pangangalakal at sa mga katutubong blockchain. Kung ang isang chain ay nagpapahiwatig ng pagkakakilanlan, ang sistem ay nagbabago sa susunod na block o isang lock ng maiksing oras.

### 3.13 PAG-EVOLVE NG ARKITEKTURA

Ang anunsyo sa araw-araw ng mga pag-develop sa mga bagong code na nakakaapekto sa paggamit ng mga digital na asset ay nagbubunyag ng napakalaking benepisyo ng pilosopiya ng open-source code. Nauunawaan namin sa Volentix na kami ang mga benepisyaryo ng napakalaking pinansiyal na mga mapagkukunan na nakatuon sa maraming mga maagang nag-umpisa sa pagbubuo ng mga aplikasyon ng mga digital na asset sa nakalipas na dekada. Mayroon na tayong isang oportunidad na gawin ang susunod na hakbang sa pamamagitan ng paglikha ng VDex, isang desentralisadong palitan para sa susunod na henerasyon ng mga transaksyong digital na asset.

## 4. PAGTATAPOS NG MGA SALOOBIN

Lahat tayo sa Volentix ay naghahandog sa ating gawain at pananaw sa pagbuo ng isang programa na nakatuon sa pagpapalakas at pagsasarili. Kung ikaw ay nag-iisip na sumali sa amin, sa anumang kapasidad, pagkatapos ay mangyaring gawin ito at mangyaring maging edukado sa mga paksa na nakapaloob sa puting papel at karagdagang Volentix mga pahayagan bilang ibinabahagi namin ang mga ito sa aming komunidad.

## 5. TIMELINE

Para sa mga update at iba pang mahalagang mga anunsyo mangyaring subaybayan ang aming websayt at social media. Maraming salamat sa iyong atensyon at interes.

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