# BIAŁA KSIĘGA VDEX VOLENTIX

- Wersja: 0.1.4
- Ostatnia aktualizacja: 11-03-2019
- Strona internetowa: www.volentix.io

## 1. WPROWADZENIE

Volentix wprowadza VDex, zaprojektowany jako rozproszona, zdecentralizowana wymiana zasobów cyfrowych z naciskiem na doświadczenie użytkownika i rozwój społeczności oraz zarządzanie. Dzięki dostępowi do ustalonych technologii i planowaniu selektywnych nowych protokołów z priorytetem w zakresie bezpieczeństwa, szybkości, uwierzytelniania, łatwości użycia, skalowalności i obsługi wielu zasobów, VDex zamierza ułatwić transakcje peer-to-peer, tworząc portfolio zdecentralizowanych aplikacji zbudowanych na inteligentnych umowach EOS.IO.

Punkt startowy VDex przewiduje dopasowanie wymagań projektowych Volentix do dostępnych technologii nałożonych na zdecentralizowany system operacyjny EOS.IO. Zamierzamy przetestować nasze założenia poprzez prototypowanie za pomocą spersonalizowanego oprogramowania EZEOS, które zbudowaliśmy i dostosowaliśmy za pomocą narzędzi wiersza poleceń EOS.IO. Oprogramowanie to znajduje się na: https://github.com/Volentix/ezeos

![](../main3-3000px.jpg)

## 2. VOLENTIX

Ekosystem Volentix będzie istniał na czterech filarach, szeregu inicjujących aplikacji znanych jako Venue, Verto, Vespucci i VDex.

### 2.1 VENUE

Venue zaplanowano jako dynamiczną platformę społecznościową, która rekrutuje i dostosowuje członków społeczności Volentix do ułatwiania dystrybucji VTX, rodzimego zasobu cyfrowego ekosystemu Volentix oraz promowania świadomości inicjatyw Volentix.

Niedawno uruchomiona w testach beta, Venue umożliwia użytkownikom odbieranie VTX w zamian, na przykład, za uczestnictwo w tworzeniu oddanej społeczności, zgłaszanie poprawek błędów i ubiegania się o nagrody. Tabele wyników i wskaźniki na żywo odzwierciedlają udział użytkowników. Pierwszą kampanię podpisów uruchomiono na forum https://bitcointalk.org/ 13 lipca 2018 r. Odwiedź stronę https://venue.volentix.io, aby uzyskać więcej informacji.

### 2.2 VERTO

Verto jest budowany jako portfel wielowalutowy do użytku ze zdecentralizowaną wymianą VDex i ma na celu ułatwienie osobistej pieczy i lokalnego zarządzania kluczami prywatnymi i publicznymi w transakcjach peer-to-peer, w celu wyeliminowania ryzyka wyniszczających strat udziału związanego z traumatycznymi niepowodzeniami operatorów centralnych. Verto planuje zastosować system inteligentnych umów, aby utrzymać oświadczenie między dwoma klientami handlowymi, a najprostsze operacje są realizowane przy użyciu niepodzielnych wymian.[1]

### 2.3 VESPUCCI

Vespucci jest przewidziany jako silnik analityczny dostępny za pośrednictwem przyjaznego dla użytkownika interfejsu ze skarbnicą danych rynkowych w czasie rzeczywistym i historycznym, takich jak oceny zasobów cyfrowych i analiza nastrojów. Chcemy umożliwić użytkownikom tworzenie wykresów i porównywanie cyfrowych zasobów handlowych, uzyskiwanie dostępu do historycznych danych handlowych i ich analizę, śledzenie trendów i wzorców oraz monitorowanie i szacowanie rozwoju oprogramowania typu open source. Vespucci dąży do tego, aby uzyskać w zasięgu ręki pewne i wszechstronne dane dotyczące rynku, agregując informacje obecnie rozproszone na wielu różnych blockchainach, stronach internetowych, czatach i giełdach.

### 2.4 VDEX

Czwartym filarem Volentix, giełda VDex, jest platformą do obrotu cyfrowymi aktywami wprowadzona szczegółowo w tej białej księdze. Aby zapewnić płynną i bezpieczną obsługę, planujemy zintegrować VDex z Twoim osobistym portfelem Verto i interfejsem Vespucci. Oczekujemy, że VDex będzie w stanie zarządzać transakcjami obejmującymi zarówno VTX, jak i szeroki wachlarz zasobów cyfrowych i blockchainów, które istnieją od czasu do czasu na całym świecie. Rozwijamy Venue jako uzupełniający dodatek przede wszystkim w celu zachęcania i napędzania macierzystych inicjatyw opartych na VTX.

## 3. ARCHITEKTURA

![](../8.jpg)

#### 3.0.1 System operacyjny

Określiliśmy różne systemy operacyjne jako kandydatów na podstrukturę naszej giełdy VDex. Chociaż szanujemy pracę wielu uznanych liderów w dziedzinie zasobów cyfrowych i technologii blockchain, wśród tych pionierów wyróżnia się, według nas, na przykład praca EOS.IO jako systemu operacyjnego, na którym można budować zdecentralizowane aplikacje. Oprogramowanie zaopatruje w konta, uwierzytelnianie, bazy danych, komunikację asynchroniczną i planowanie w klastrach. Komponenty i protokoły są już wbudowane w platformę, a podzbiór może zostać użyty do spełnienia naszych wymagań VDex. VDex początkowo będzie korzystał ze standardowych funkcji oferowanych przez EOS.IO, takich jak tworzenie kont i portfeli oraz odzyskiwanie skradzionych kluczy, ale planujemy później wdrożyć protokoły do ​​tworzenia zdecentralizowanej wymiany za pośrednictwem umów EOS i innych narzędzi. [2] Oto podsumowanie przekonywujących metodologii:

### Działanie Bez Kontekstu

Większość technik skalowalności zaproponowanych przez Ethereum (Sharding, Raiden, Plasma, State Channels) staje się bardziej wydajna, równoległa i praktyczna, zapewniając jednocześnie szybką komunikację między blokchainami i nienaruszoną skalowalność. Działanie bez kontekstu obejmuje obliczenia, które zależą tylko od danych transakcji, a nie od stanu blockchaina.

### Konwersja binarna/JSON

Kontrakty EOS łączą czytelność JSON z wydajnością binarną.

### Równoległość i optymalizacja

Oddzielenie uwierzytelniania od aplikacji pozwala na szybszy czas transakcji i zwiększa przepustowość. Bloki EOS.IO są według doniesień produkowane co 500 ms.

### Web Assembly(WASM)

Web Assembly umożliwia wydajne aplikacje Internetowe, a także zabezpiecza każdą aplikację we własnym środowisku testowym, dzięki którym VDex może uzyskać dostęp do sieci, ograniczenia przestrzeni nazw systemu plików i wymuszona oparte na zasadach realizacji.

### Kontrakty Rust/C++

Dobrze znany i popularny język programowania C++ wydaje się bardzo odpowiedni dla WASM. C++ ma bardzo dojrzałe wsparcie debugowania i bibliotek. Baza kodowa EOS wykorzystuje szablony swobodnie, a C ++ pozwala na użycie szablonów i przeciążenie operatorów w celu zdefiniowania bezpłatnego sprawdzania jednostek w czasie wykonywania. Program ponownie inicjuje proces czyszczenia na początku każdej wiadomości, co stanowi wyraźną zaletę, która usprawnia formułowanie inteligentnych umów. Struktura WebAssembly automatycznie odrzuca każdą niedokładną pamięć adresowania transakcji. Jeśli konieczna jest dynamiczna alokacja pamięci, użytkownicy mogą odstępować od inteligentnych wskaźników, ponieważ umowy EOS.IO używają C++14. Warto zauważyć, że pierwsza implementacja technologii PARSEC Directed Acyclic Graph (DAG) ma być w Rust.

#### 3.0.2 Komunikaty zdefiniowane w schemacie i baza danych

Kontrakty serwisowe są standaryzowane, aby zapewnić bazową miarę interoperacyjności między różnymi systemami i poprzez ich harmonizację. W istocie zasada projektowania Standaryzowanej Umowy o Świadczeniu Usług popiera te umowy o świadczenie usług opierające się na standardowych modelach danych. Analiza odbywa się na planie spisu usług, aby znaleźć powszechnie występujące dokumenty biznesowe wymieniane między usługami. Te dokumenty biznesowe są następnie modelowane na standaryzowanych zasadach. Kanoniczny Wzór schematu zmniejsza potrzebę stosowania wzorca projektowego transformacji modelu danych. [3]

#### 3.0.3 Komunikacja między kontraktami

Dane są dzielone między umowami za pośrednictwem wyroczni, która „w kontekście blockchainów i inteligentnych umów jest agentem, który znajduje i weryfikuje rzeczywiste zdarzenia i przekazuje te informacje do blokchaina, który ma być używany przez inteligentne umowy”. [4] Każdy węzeł będzie miał identyczną kopię tych danych do wykorzystania w obliczeniach inteligentnych kontraktów. Zamiast inteligentnego funkcjonowania umowy, aby wyciągnąć dane, wyrocznia przesyła dane do blockchaina. W przypadku bblockchain większość odczytu danych odbywa się poprzez odpytywanie „modeli” w celu monitorowania stanu blockchaina i wykonywania pewnych działań reagujących.

#### 3.0.4 Łańcuchy boczne

W EOS.IO wydanie zasobu cyfrowego tworzy łańcuch boczny, który jest nowym mechanizmem pozwalającym na bezpieczne korzystanie z zasobów cyfrowych z jednego blockchaina w oddzielnym blockchainie, a następnie powrót do oryginalnego blockchaina. Efektywność przetwarzania jest wspierana przez tworzenie wielu łańcuchów bocznych. Kanał komunikacji typu TCP pomiędzy różnymi blokchainami pozwala ocenić dowody. Dla każdego odłamu (jednostki równoległego wykonania w cyklu), zbudowane jest zrównoważone drzewo hash z tych zobowiązań działania, aby wygenerować tymczasowy odłamek korzenia hash; odbywa się to dla szybkości obliczeń równoległych. Nagłówek bloku zawiera korzeń zbalansowanego drzewa hash, którego liście są korzeniami tych pojedynczych odkłamów drzew hash. [2]

#### 3.0.5 Płynność

Zasób cyfrowy jest płynny, jeśli łatwo go sprzedać lub kupić w zwykłych wolumenach obrotu, bez znaczącego krótkoterminowego wpływu na jego dominującą cenę rynkową. W celu zdobycia takiego satusu, zazwyczaj każdy wymienialny zasób musi pokrywać pułap wolumenu obrotu wystarczający do podtrzymania stabilności. W szczególności przewidujemy przyjęcie następujących metodologii: Zapętlanie protokołu z wykorzystaniem kontraktów EOS.IO działających jako węzły.[5] Algorytm Bancora używany do zapewnienia stabilności zasobu cyfrowego. [6] Przełączanie między tymi protokołami i HTLC (atomic swap) zgodnie z analizami Vespucci w sieci VDex.

#### 3.0.6 Mieszany Timelock Umów (Atomic Swap)

Umowa Hashed Timelock (HTLC)[1] to inteligentna umowa umożliwiająca realizację transakcji ograniczonych w czasie. Użytkownicy otrzymają zmienny okres blokady dla swoich transakcji, ze zniżką na opłaty transakcyjne w zamian za wybór dłuższego okresu blokady.

### 3.1 TOPOLOGIA SIECI

#### 3.1.1 Węzły

![](../9.jpg)

Węzły są punktami końcowymi wymiany VDex. Ich funkcjami są:

1. Działanie jako portale dla VDex za pośrednictwem portfela Verto.

2. Scalanie informacji o arkuszu zleceń.

3. Regulowanie arkusza zleceń.

4. Zarządzanie anulowaniem zlecenia.

5. Przypisanei czasu oczekiwania dla protokołu RAFT.

6. Inicjowanie kontraktów na zlecenia, które zostały wypełnione.

Węzły pobierają część opłaty za każdą transakcję. Jeśli użytkownik posiada wystarczające środki i posiada historię potwierdzającą dobre wyniki, to jej lub jego portfel Verto może zachowywać się jak węzeł.

#### 3.1.2 Agregatory

Agregatory VDex są dedykowanymi serwerami Volentix do celów symulatora i bezpieczeństwa. Jedną z ich funkcji jest pobieranie rejestrów i danych z węzłów do rzadkich rozproszonych reprezentacji dla hierarchicznej pamięci czasowej jako analizy włamań [7] do wykrywania anomalii w systemie. Agregatory będą także hostować inne komponenty, takie jak księgi metachain i skrobaki blockchain.

#### 3.1.3 Opóźnienie

EOS.IO ma potwierdzenie bloku o niskim opóźnieniu (0,5 sekundy).[5] Ten stopień opóźnienia można utrzymać w transakcjach z innymi blockchainami, jeśli łańcuchy te dopuszczają podobne opóźnienie. Ale zasadniczo transakcja jest tak szybka, jak mniej gwałtowny łańcuch w równaniu. Wiadomo na przykład, że blok Bitcoin wymaga około dziesięciu minut na przetworzenie. Otrzymanie sumy kontrolnej transakcji nie oznacza potwierdzenia transakcji; oznacza to tylko, że węzeł zaakceptował transakcję bez błędu, chociaż generalnie istnieje duże prawdopodobieństwo, że inni producenci bloków ją zaakceptują.

### 3.2 ARKUSZ ZLECEŃ

Arkusz zleceń to lista zamówień kupna i sprzedaży rekordów VDex od zainteresowanych użytkowników. Dopasowany silnik używa arkusza zleceń, aby określić, które zamówienia mogą zostać zrealizowane. Protokół Loopring umożliwia dostosowanie struktury danych arkusza zleceń.[5] Pojemniki dostarczane przez EOS.IO mogą być używane do optymalnej wydajności.[8]

#### 3.2.1 Struktury danych

Używając Pętli Protokołu FIFO (pierwszy wchodzi pierwszy opuszcza) buforu kołowego, węzły mogą projektować swoje arkusze zleceń, aby wyświetlały i pasowały do ​​zamówienia użytkownika. Metoda ta opiera się na modelu OTC, w którym zlecenia limitowe są pozycjonowane wyłącznie w oparciu o cenę.[5]

Odwołując się do interfejsu API trwałości EOS.IO, arkusz zleceń jest w stanie wykorzystać potężny pojemnik o wielu indeksach współdzielony przez węzły za pośrednictwem tego samego konta EOS.IO.

#### 3.2.2 Arkusz zleceń w łańcuchu

Arkusz zleceń w łańcuchu to rejestr ofert znajdujących się w portfelu (węźle) wybranym do rozliczenia arkusza zleceń. Znajduje się w trwałej bazie danych na każdym węźle subskrybującym to samo konto, co wszystkie pozostałe węzły.

#### 3.2.3 Arkusz zleceń poza łańcuchem

Znajdując się w agregatorze, książki zamówień offline służą do celów symulatora i bezpieczeństwa.

#### 3.2.4 Decentralizacja procesu rozliczenia księgi zamówień

W celu decentralizacji, węzły będą zmieniać kolejność zamówień. The settling node must be designated by the protocol and all order book entries from all nodes must be available to the settling nodes. Wierzymy, że mechanizmy konsensusowe RAFT[9] i PARSEC[10] oferują skuteczne rozwiązania. RAFT jest sprawdzonym algorytmem i jest łatwy do wdrożenia.[7] PARSEC jest nowszy i bardziej wydajny, dzięki technologii Directed Acyclic Graph (DAG) i eliminuje potrzebę kopiowania rejestrów.

### 3.3 ROZLICZENIE ZAMÓWIENIA

Rozliczenie zamówienia zawiera znane elementy konwencjonalnych transakcji na rynku finansowym. Wykorzystując technologię FIFO do projektowania arkusza zleceń, VDex zamierza sprawdzić zamówienie, ewidencję i wskaźnik wypełnienia, a także ograniczyć zamówienia i anulowania. ![](../7.jpg)

### 3.4 VTX

#### 3.4.1 Emisja i Użycie VTX

VTX to natywny zasób cyfrowy, który ma być wydawany i używany poprzez zdecentralizowaną wymianę VDex. Obecnie planujemy wykorzystać umowę eosio.token ze struktury EOS.IO do emisji 2,1 miliarda tokenów VTX zgodnych ze standardem EOS.IO przy dopływie 1,3 miliarda. VTX będzie miał różne zastosowania, na przykład:

Nagradzać uczestników w procesie konsensusu i w kampaniach Venue.

Płacić i redystrybuować opłaty transakcyjne na giełdzie VDex.

Przesyłać i głosować na propozycje do ekosystemu Volentix, wykorzystując prawa głosu przydzielone posiadaczom VTX.

Udzielać wsparcia za przeglądanie propozycji i wdrażanie projektów.

Aby zachęcić użytkowników do uczestnictwa w rozliczaniu arkusza zleceń, stając się węzłami za pośrednictwem portfeli Verto.

Aby zachęcić użytkowników do zablokowania środków na >24 godziny przez transakcje HTLC ograniczonych w czasie.

#### 3.4.2 Alokacja VTX

![](../6.jpg)

Ekosystem zasobów cyfrowych wymaga szeregu podstawowych składników ludzkich, które prowadzą projekt do przodu.[11] Istotne jest, aby zrekompensować tym osobom ich udział. Poddany dostosowaniu, Volentix przewiduje obecnie następujące przydziały:

1. Współautorzy. 12%. Szereg osób podobnych do założycieli, którzy wnoszą spostrzeżenia, czas i talent, choć często pracują bez wcześniejszej rekompensaty.

2. Wspierający.

Faza 1. 5%. Wcześni pasywni fundatorzy seed.

Faza 2. 28%. Fundatorzy za pośrednictwem kwalifikowanej prywatnej wyprzedaży i możliwej publicznej sprzedaży.

3. Mediatorzy. (Doradcy, Deweloperzy, Promotorzy, Opiekunowie). Należy zauważyć, że wymagania dotyczące pomocy z podkategorii w tej kategorii mogą się znacznie różnić przed i po otrzymaniu przez projekt znacznego wsparcia finansowego, ale niektóre osoby mogą służyć w obu fazach.

Faza 1. 10%.

Faza 2. 10%.

4. Zdecentralizowany skarbiec. 35%. Członkowie społeczności zachęcali i nagradzali za udział w stopniowym rozwoju zdecentralizowanej autonomicznej organizacji (DAO). Oczekuje się, że zdecentralizowany skarbiec będzie zarządzany przez inteligentne umowy i konsensus społeczny. ![](../5.jpg)

#### 3.4.3 dystrybucja VTX

W świetle warunków rynkowych w momencie pisania niniejszego tekstu Volentix rozważa harmonogram, środki i warunki dystrybucji VTX w zależności od prywatnej przedprzedaży i możliwej publicznej sprzedaży. Prosimy o śledzenie naszej witryny w poszukiwaniu aktualizacji.

### 3.5 ZASTOSOWANIE PLATFORMY EOS.IO

Poniższe uwagi są istotne dla naszego wdrożenia wymiany VDex na platformie EOS.IO:

Wdrożenie umowy wiąże się z kosztami, ale można go używać bezpłatnie.

Deweloperzy stosują żetony kompatybilne z EOS.IO, aby wdrożyć inteligentną umowę. Po wdrożeniu umowy zablokowane tokeny są zwracane.

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