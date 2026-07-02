# Bevezetés az Adatetikába

|![ Vázlatkép [(@sketchthedocs)](https://sketchthedocs.dev) készítésében ](../../sketchnotes/02-Ethics.png)|
|:---:|
| Adattudomány etikája - _Vázlatkép készítette [@nitya](https://twitter.com/nitya)_ |

---

Mindannyian adatpolgárok vagyunk egy adatfürdő világban.

A piaci trendek azt jelzik, hogy 2022-re három nagy szervezetből egy online [piactereken és tőzsdéken](https://www.gartner.com/smarterwithgartner/gartner-top-10-trends-in-data-and-analytics-for-2020/) fogja megvásárolni és értékesíteni az adatait. Mint **alkalmazásfejlesztők**, könnyebbnek és olcsóbbnak fogjuk találni az adatvezérelt betekintések és algoritmusvezérelt automatizációk integrálását a napi felhasználói élményekbe. De amint az MI általánossá válik, értenünk kell a potenciális károkat is, amelyeket az ilyen algoritmusok [fegyverkezése](https://www.youtube.com/watch?v=TQHs8SA1qpk) okozhat nagyszabásban.

A trendek szerint 2025-re több mint [180 zettabájt](https://www.statista.com/statistics/871513/worldwide-data-created/) adatot fogunk generálni és fogyasztani. A **data scientist-ek** számára ez az információrobbanás páratlan hozzáférést biztosít személyes és viselkedési adatokhoz. Ez a hatalom lehetővé teszi részletes felhasználói profilok létrehozását és a döntéshozatal finom befolyásolását – gyakran olyan módokon, amelyek az [önkéntes választás illúzióját](https://www.datasciencecentral.com/the-pareto-set-and-the-paradox-of-choice/) keltik. Bár ez használható arra, hogy a felhasználókat preferált eredmények felé tereljük, kritikus kérdéseket vet fel az adatvédelem, az autonómia és az algoritmikus befolyás etikai határai kapcsán.

Az adatetika most már _szükséges védősánc_ az adattudomány és mérnökség számára, amelyek segítenek minimalizálni a lehetséges károkat és a nem szándékolt következményeket adatvezérelt cselekedeteinkből. A [Gartner Hype Cycle az MI-ről](https://www.gartner.com/smarterwithgartner/2-megatrends-dominate-the-gartner-hype-cycle-for-artificial-intelligence-2020/) olyan releváns trendeket azonosít, amelyek a digitális etika, a felelős MI és az MI-kormányzás területén kulcsfontosságúak az MI _demokratizálásának_ és _iparosításának_ nagyobb megatrendjeiben.

![Gartner Hype Cycle az MI-hez - 2020](https://images-cdn.newscred.com/Zz1mOWJhNzlkNDA2ZTMxMWViYjRiOGFiM2IyMjQ1YmMwZQ==)

Ebben a leckében megvizsgáljuk az adatetika lenyűgöző területét - az alapfogalmaktól és kihívásoktól kezdve esettanulmányokon és alkalmazott MI-konceptusokon át, mint a kormányzás - amelyek segítenek etikai kultúrát kialakítani azokban a csapatokban és szervezetekben, amelyek adattal és MI-vel dolgoznak.




## [Előadás előtti kvíz](https://ff-quizzes.netlify.app/en/ds/quiz/2) 🎯

## Alapfogalmak

Kezdjük az alapvető terminológia megértésével.

Az "etika" szó a [görög "ethikos"](https://en.wikipedia.org/wiki/Ethics) (és annak "ethos" gyökere) szóból ered, ami _jellemet vagy erkölcsi természetet_ jelent.

Az **etika** a közösen elfogadott értékekről és erkölcsi elvekről szól, amelyek a társadalomban viselkedésünket irányítják. Az etika nem törvényeken alapul, hanem a széles körben elfogadott normákon, hogy mi a „helyes és helytelen”. Azonban az etikai megfontolások befolyásolhatják a vállalati kormányzási kezdeményezéseket és a kormányzati szabályozásokat, amelyek erősebb ösztönzőket hoznak létre a megfelelésre.

Az **adatetika** egy [az etika új ága](https://royalsocietypublishing.org/doi/full/10.1098/rsta.2016.0360#sec-1), amely „tanulmányozza és értékeli az adatokat, algoritmusokat és kapcsolódó gyakorlatokat érintő erkölcsi problémákat”. Itt az **„adat”** az adatok keletkezésével, rögzítésével, kurátori munkával, feldolgozással, terjesztéssel, megosztással és használattal kapcsolatos cselekvésekre fókuszál, az **„algoritmusok”** az MI-re, ágensekre, gépi tanulásra és robotokra koncentrálnak, míg a **„gyakorlatok”** felelősségteljes innováció, programozás, hackelés és etikai kódexek témáit foglalják magukban.

Az **alkalmazott etika** az [erkölcsi megfontolások gyakorlati alkalmazása](https://en.wikipedia.org/wiki/Applied_ethics). Ez aktívan vizsgálja az etikai kérdéseket a _valós cselekvések, termékek és folyamatok_ kontextusában, és korrigáló intézkedéseket hoz annak érdekében, hogy ezek összhangban maradjanak a meghatározott etikai értékekkel.

Az **etikai kultúra** az [_alkalmazott etika operacionalizálásáról_](https://hbr.org/2019/05/how-to-design-an-ethical-organization) szól, hogy etikai elveinket és gyakorlatainkat következetes és skálázható módon alkalmazzuk az egész szervezeten belül. A sikeres etikai kultúrák meghatározzák a szervezet egészére kiterjedő etikai elveket, jelentős ösztönzőket nyújtanak a megfelelésre, és erősítik az etikai normákat azáltal, hogy minden szinten bátorítják és erősítik a kívánatos viselkedést.


## Etikai Fogalmak

Ebben a részben megvitatjuk a **közös értékek** (elvek) és az **etikai kihívások** (problémák) fogalmait az adatetika kapcsán – továbbá megvizsgálunk **esettanulmányokat**, amelyek segítenek megérteni ezeket a fogalmakat a valós helyzetekben.

### 1. Etikai Elvek

Minden adatetikai stratégia azzal kezdődik, hogy meghatározzuk az _etikai elveket_ – azokat a „közös értékeket”, amelyek leírják az elfogadható viselkedést és irányítják a megfeleléshez szükséges cselekvéseket adat- és MI-projektjeinkben. Ezeket egyéni vagy csapatszinten is meg lehet határozni. A legtöbb nagy szervezet azonban egy _etikus MI_ küldetésnyilatkozatban vagy keretrendszerben fogalmazza meg ezeket, amelyet vállalati szinten definiálnak és következetesen betartanak minden csapatban.

**Példa:** A Microsoft [Felelős MI](https://www.microsoft.com/en-us/ai/responsible-ai) küldetésnyilatkozata így szól: _„Elkötelezettek vagyunk az etikai elveket szem előtt tartó, embereket első helyre tevő MI-fejlesztés iránt”_ – az alábbi 6 etikai elvet azonosítva a keretrendszerben:

![Felelős MI a Microsoftnál](https://docs.microsoft.com/en-gb/azure/cognitive-services/personalizer/media/ethics-and-responsible-use/ai-values-future-computed.png)

Nézzük át röviden ezeket az elveket. A _transzparencia_ és _elszámoltathatóság_ alapvető értékek, amelyekre a többi elv épül, ezért kezdjük ezekkel:

* [**Elszámoltathatóság**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) biztosítja, hogy az adat- és MI-műveletek gyakorlói _felelősek_ legyenek ezekért és az etikai elvek betartásáért.
* [**Átláthatóság**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) biztosítja, hogy az adat- és MI-cselekvések _érthetőek_ (értelmezhetőek) legyenek a felhasználók számára, magyarázva a döntések „mit” és „miért” aspektusait.
* [**Méltányosság**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6) arra fókuszál, hogy az MI _mindenkit_ igazságosan kezeljen, foglalkozva az adat- és rendszerszintű vagy implicit társadalmi-technikai torzításokkal.
* [**Megbízhatóság és Biztonság**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) gondoskodik arról, hogy az MI _következetesen_ viselkedjen a meghatározott értékekkel összhangban, minimalizálva a lehetséges károkat vagy nem kívánt következményeket.
* [**Adatvédelem és Biztonság**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) az adatvonaliság megértéséről, valamint a felhasználók számára nyújtott _adatvédelmi és kapcsolódó védelmi intézkedésekről_ szól.
* [**Befogadás**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) az MI-megoldások szándékos megtervezéséről szól, hogy azok alkalmazkodjanak egy _széles emberi szükséglet- és képesség-spektrumhoz_.

> 🚨 Gondold át, milyen lehet a te adatetikai küldetésnyilatkozatod. Vizsgáld meg más szervezetek etikus MI-keretrendszereit – itt van néhány példa az [IBM](https://www.ibm.com/cloud/learn/ai-ethics), [Google](https://ai.google/principles) és [Facebook](https://ai.facebook.com/blog/facebooks-five-pillars-of-responsible-ai/) oldalairól. Milyen közös értékek vannak bennük? Hogyan kapcsolódnak ezek az elvek az MI-termékükhöz vagy az iparághoz, amelyben működnek?

### 2. Etikai Kihívások

Miután meghatároztuk az etikai elveket, a következő lépés az, hogy értékeljük adat és MI-cselekvéseinket, hogy megfelelnek-e ezeknek a közös értékeknek. Két kategóriában gondolkodjunk: _adatgyűjtés_ és _algoritmustervezés_.

Az adatgyűjtés esetén cselekvéseink nagy valószínűséggel személyes adatokat, illetve személy szerint azonosítható információkat (PII) érintenek. Ide tartozik [számos nem személyes adat](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-personal-data_en), amelyek _együttesen_ képesek az egyén azonosítására. Az etikai kihívások érinthetik az _adatvédelmet_, az _adatbirtoklást_ és kapcsolódó témákat, mint az _értelmes beleegyezés_ és az _intellektuális tulajdonjogok_.

Az algoritmustervezés esetében cselekvéseink adatgyűjtéssel és adatkurátorlással foglalkoznak, majd ezeket a **készleteket** használják fel **adati modellek** tréningjéhez és alkalmazásához, amelyek előrejelzik az eredményeket vagy automatizálják a döntéseket valós kontextusokban. Etikai kihívások merülhetnek fel az _adatkészlet torzítás_ , _adatminőség_ problémák, _igazságtalanság_ és _hamis ábrázolás_ formájában az algoritmusokban – ideértve néhány rendszerszintű problémát is.

Mindkét esetben az etikai kihívások kiemelik azokat a területeket, ahol cselekvéseink összeütközhetnek közös értékeinkkel. E kérdések felismerésére, mérséklésére, minimalizálására vagy megszüntetésére erkölcsi „igen/nem” kérdéseket kell feltennünk, majd szükség szerint helyesbítenünk kell. Nézzünk meg néhány etikai kihívást és az ezekből fakadó erkölcsi kérdéseket:


#### 2.1 Adatbirtoklás

Az adatgyűjtés gyakran személyes adatokat tartalmaz, amelyek az adat alanyokat azonosítják. Az [adatbirtoklás](https://permission.io/blog/data-ownership) a _kontrollról_ és a [_felhasználói jogokról_](https://permission.io/blog/data-ownership) szól az adatok létrehozásának, feldolgozásának és terjesztésének vonatkozásában.

Az erkölcsi kérdések, amelyeket fel kell tennünk:
 * Ki birtokolja az adatokat? (felhasználó vagy szervezet)
 * Milyen jogai vannak az adat alanyoknak? (pl. hozzáférés, törlés, hordozhatóság)
 * Milyen jogai vannak a szervezeteknek? (pl. rosszindulatú felhasználói vélemények javítása)

#### 2.2 Értelmes Beleegyezés

Az [értelmes beleegyezés](https://legaldictionary.net/informed-consent/) azt jelenti, hogy a felhasználók elismerik egy cselekvést (például adatgyűjtést) úgy, hogy _teljes körűen megértik_ az érintett tényeket, beleértve a célt, a potenciális kockázatokat és az alternatívákat.

Végiggondolandó kérdések:
 * Adott-e a felhasználó (adat alany) engedélyt az adatok rögzítésére és használatára?
 * Értette a felhasználó, milyen célból gyűjtötték az adatokat?
 * Tudatában volt a kockázatoknak, amelyek a részvételéből fakadnak?

#### 2.3 Szellemi Tulajdon

A [szellemi tulajdon](https://en.wikipedia.org/wiki/Intellectual_property) az emberi kezdeményezésből származó immateriális alkotásokra utal, amelyek _gazdasági értékkel bírhatnak_ egyének vagy vállalkozások számára.

Itt vizsgálandó kérdések:
 * Van-e a begyűjtött adatnak gazdasági értéke egy felhasználó vagy vállalkozás számára?
 * Rendelkezik a **felhasználó** itt szellemi tulajdonnal?
 * Rendelkezik a **szervezet** itt szellemi tulajdonnal?
 * Ha ezek a jogok léteznek, hogyan védjük őket?

#### 2.4 Adatvédelem

Az [adatvédelem](https://www.northeastern.edu/graduate/blog/what-is-data-privacy/) vagy információvédelem a felhasználói adatvédelmet és személyazonosság védelmét jelenti a személy szerint azonosítható információk esetén.

Vizsgálandó kérdések:
 * Védettek-e a felhasználók (személyes) adatai a hackelés és adatlopás ellen?
 * Érhető-e el a felhasználói adat csak jogosult felhasználók és kontextusok számára?
 * Megőrződik-e a felhasználók anonimitása, amikor az adat megosztásra vagy terjesztésre kerül?
 * Az anonimított adatállományból azonosítható-e egy felhasználó?

#### 2.5 Elfeledtetéshez Való Jog

Az [Elfeledtetéshez Való Jog](https://en.wikipedia.org/wiki/Right_to_be_forgotten) vagy [Törléshez Való Jog](https://www.gdpreu.org/right-to-be-forgotten/) további személyes adatvédelmet biztosít a felhasználóknak. Kifejezetten arra jogosítja a felhasználókat, hogy kérhessék személyes adatok törlését vagy eltávolítását az internetes keresésekből és más helyekről, _meghatározott körülmények között_ – engedve nekik egy újrakezdést online anélkül, hogy múltbeli cselekvéseik ellenük szólnának.

Vizsgálandó kérdések:
 * Lehetővé teszi-e a rendszer az adat alanyoknak, hogy törlést kérjenek?
 * Kell-e a felhasználói hozzájárulás visszavonásának automatikus törlést kiváltania?
 * Gyűjtöttek-e adatot beleegyezés nélkül vagy törvénytelen eszközökkel?
 * Megfelelünk-e az adatvédelmi kormányzati szabályozásoknak?

#### 2.6 Adatkészlet-torzítás

Az adatkészleti vagy [gyűjtési torzítás](http://researcharticles.com/index.php/bias-in-data-collection-in-research/) arról szól, hogy egy _nem reprezentatív_ adatmintát választanak az algoritmusfejlesztéshez, ami potenciális igazságtalanságot eredményez a különböző csoportok eredményeiben. A torzítási típusok közé tartozik a kiválasztási vagy mintavételi torzítás, önkéntes torzítás és műszaki eszközökkel kapcsolatos torzítás.

Kérdések, amelyeket érdemes feltenni:
 * Reprezentatív adatokat gyűjtöttünk az adat alanyokról?
 * Teszteltük az összegyűjtött vagy kurált adatállományt különféle torzításokra?
 * Tudjuk mérsékelni vagy eltávolítani a feltárt torzításokat?

#### 2.7 Adatminőség

Az [adatminőség](https://lakefs.io/data-quality-testing/) azt vizsgálja, hogy az algoritmusaink fejlesztésére használt adatállomány mennyire érvényes, ellenőrizve, hogy a jellemzők és rekordok megfelelnek-e a pontosság és következetesség szintjének, amely az MI célnak szükséges.

Vizsgálandó kérdések:
 * Rögzítettünk érvényes _jellemzőket_ az esettanulmányunkhoz?
 * Az adatokat _következetesen_ gyűjtöttük különböző forrásokból?
 * Az adatállomány _teljes_ a különböző körülmények vagy forgatókönyvek esetén?
 * Az információkat _pontos_ módon rögzítettük a valóság tükrözésére?
#### 2.8 Az algoritmusok méltányossága

Az [algoritmusok méltányossága](https://towardsdatascience.com/what-is-algorithm-fairness-3182e161cf9f) azt vizsgálja, hogy az algoritmus-tervezés rendszerszinten diszkriminál-e bizonyos adat-alanyok alcsoportjai ellen, ami [potenciális károkat](https://docs.microsoft.com/en-us/azure/machine-learning/concept-fairness-ml) eredményezhet az _elosztásban_ (ahol erőforrásokat tagadnak meg vagy vonnak vissza az adott csoporttól) és a _szolgáltatás minőségében_ (ahol az MI nem olyan pontos egyes alcsoportok számára, mint másoknak).

Itt megvizsgálandó kérdések:
 * Értékeltük-e a modell pontosságát különböző alcsoportok és feltételek esetén?
 * Átvizsgáltuk-e a rendszert a potenciális károk (pl. sztereotipizálás) szempontjából?
 * Felülvizsgálhatjuk-e az adatokat vagy újrataníthatjuk-e a modelleket a feltárt károk mérséklése érdekében?

További információkhoz böngésszen olyan forrásokat, mint az [MI méltányossági ellenőrzőlisták](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE4t6dA).

#### 2.9 Félrevezetés

Az [adatok félrevezetése](https://www.sciencedirect.com/topics/computer-science/misrepresentation) arra vonatkozik, hogy vajon őszintén jelentett adatokról származó betekintéseket megtévesztő módon kommunikálunk-e a kívánt narratíva támogatása érdekében.

Itt megvizsgálandó kérdések:
 * Jelentünk-e hiányos vagy pontatlan adatokat?
 * Olyan módon vizualizáljuk-e az adatokat, hogy félrevezető következtetésekre jusson a közönség?
 * Szelektív statisztikai módszereket használunk-e az eredmények manipulálására?
 * Vannak-e alternatív magyarázatok, amelyek más következtetéshez vezethetnek?

#### 2.10 Szabad választás illúziója
A [szabad választás illúziója](https://www.datasciencecentral.com/profiles/blogs/the-illusion-of-choice) akkor fordul elő, amikor a rendszer "választási architektúrái" döntéshozatali algoritmusokat használnak arra, hogy az embereket egy előnyben részesített eredmény felé tereljék, miközben úgy tűnik, hogy választási lehetőségeket és kontrollt adnak nekik. Ezek a [sötét mintázatok](https://www.darkpatterns.org/) társadalmi és gazdasági károkat okozhatnak a felhasználóknak. Mivel a felhasználói döntések befolyásolják a viselkedési profilokat, ezek a lépések potenciálisan alakíthatják a jövőbeli döntéseket, amelyek erősíthetik vagy meghosszabbíthatják ezen károk hatását.

Itt megvizsgálandó kérdések:
 * Értette-e a felhasználó a választás következményeit?
 * Tudott-e a felhasználó (alternatív) választási lehetőségekről és azok előnyeiről, hátrányairól?
 * Meg tudja-e a felhasználó később fordítani az automatikus vagy befolyásolt döntést?

### 3. Esettanulmányok

Ahhoz, hogy ezeket az etikai kihívásokat valós világban értelmezzük, hasznos megnézni olyan esettanulmányokat, amelyek kiemelik az egyénekre és a társadalomra gyakorolt potenciális károkat és következményeket, amikor ezen etikai megsértések figyelmen kívül maradnak.

Íme néhány példa:

| Etikai kihívás | Esettanulmány  | 
|--- |--- |
| **Tájékozott beleegyezés** | 1972 - [Tuskegee szifilisz tanulmány](https://en.wikipedia.org/wiki/Tuskegee_Syphilis_Study) - A tanulmányban résztvevő afroamerikai férfiaknak ingyenes orvosi ellátást ígértek, _de megtévesztették_ őket a kutatók, akik nem tájékoztatták őket diagnózisukról vagy a kezelés elérhetőségéről. Sok alany meghalt, partnerük vagy gyermekeik érintettek voltak; a tanulmány 40 évig tartott. | 
| **Adatvédelem** | 2007 - A [Netflix adatversenye](https://www.wired.com/2007/12/why-anonymous-data-sometimes-isnt/) 10 millió anonimizált filmértékelést biztosított 50 ezer ügyféltől a kutatók számára a ajánlóalgoritmusok fejlesztéséhez. Azonban a kutatók képesek voltak összekapcsolni az anonimizált adatokat személyazonosításra alkalmas külső adatkészletekkel (pl. IMDb hozzászólások) – lényegében "de-anonimizálva" bizonyos Netflix előfizetőket.|
| **Gyűjtési torzítás**  | 2013 - Boston városa kifejlesztette a [Street Bump](https://www.boston.gov/transportation/street-bump) nevű alkalmazást, amely lehetővé tette az állampolgároknak, hogy kátyúkat jelentsenek, ezzel jobb úti adatokat adva a városnak a problémák felderítéséhez és javításához. Azonban [az alacsonyabb jövedelmű csoportoknak kevesebb hozzáférésük volt autókhoz és telefonokhoz](https://hbr.org/2013/04/the-hidden-biases-in-big-data), így az ő útproblémáik láthatatlanok maradtak ebben az appban. A fejlesztők együttműködtek akadémikusokkal az _egyenlő hozzáférés_ és a digitális szakadék kérdéseinek kezelésére a méltányosság érdekében. |
| **Algoritmikus méltányosság**  | 2018 - Az MIT [Gender Shades tanulmány](http://gendershades.org/overview.html) azonosító AI termékek nemi osztályozási pontosságát értékelte, feltárva a nők és színes bőrűek pontossági hiányosságait. Egy [2019-es Apple Card](https://www.wired.com/story/the-apple-card-didnt-see-genderand-thats-the-problem/) kevesebb hitelt kínált nőknek, mint férfiaknak. Mindkettő az algoritmikus torzításból eredő társadalmi-gazdasági károkat példáz.|
| **Adathamisítás** | 2020 - A [Georgia Köztársaság Egészségügyi Minisztériuma COVID-19 grafikonokat tett közzé](https://www.vox.com/covid-19-coronavirus-us-response-trump/2020/5/18/21262265/georgia-covid-19-cases-declining-reopening), amelyek látszólag megtévesztették a polgárokat a megerősített esetek trendjeiről az x-tengely nem kronologikus sorrendjével. Ez a vizualizációs trükkök által megvalósított félrevezetést mutatja be. |
| **Szabad választás illúziója** | 2020 - Az ABCmouse tanulóalkalmazás [10 millió dollárt fizetett az FTC panasz rendezésére](https://www.washingtonpost.com/business/2020/09/04/abcmouse-10-million-ftc-settlement/), mivel a szülőket csapdába ejtették, fizetésre kényszerítve olyan előfizetésekért, amelyeket nem tudtak lemondani. Ez a választási architektúrák sötét mintáit illusztrálja, ahol a felhasználókat potenciálisan káros döntések felé terelték. |
| **Adatvédelem és felhasználói jogok** | 2021 - A Facebook [adatvédelmi incidens](https://www.npr.org/2021/04/09/986005820/after-data-breach-exposes-530-million-facebook-says-it-will-not-notify-users) 530 millió felhasználó adatait tette hozzáférhetővé, aminek következtében 5 milliárd dolláros kártérítést fizettek az FTC-nek. Azonban megtagadta a felhasználók értesítését az incidensről, megsértve a felhasználói jogokat az adatátláthatóság és hozzáférés terén. |

Szeretne még több esettanulmányt felfedezni? Tekintse meg ezeket a forrásokat:
* [Ethics Unwrapped](https://ethicsunwrapped.utexas.edu/case-studies) - etikai dilemmák különböző iparágakban.
* [Adattudomány etika kurzus](https://www.coursera.org/learn/data-science-ethics#syllabus) - mérföldkő esettanulmányok bemutatása.
* [Hol mentek félre a dolgok](https://deon.drivendata.org/examples/) - deon ellenőrzőlista példákkal.

> 🚨 Gondolkodjon el az Ön által látott esettanulmányokon – tapasztalt vagy érintett volt-e hasonló etikai kihívásban az életében? Tud-e legalább egy másik olyan esettanulmányt megnevezni, amely az ebben a fejezetben tárgyalt etikai kihívások egyikét illusztrálja?

## Alkalmazott etika

Beszéltünk etikai fogalmakról, kihívásokról és esettanulmányokról valós környezetben. De hogyan kezdjünk neki az etikai alapelvek és gyakorlatok _alkalmazásának_ a projektjeinkben? És hogyan _operacionalizáljuk_ ezeket a gyakorlatokat a jobb irányítás érdekében? Vizsgáljunk meg néhány valós megoldást:

### 1. Szakmai kódexek

A szakmai kódexek egy lehetőség arra, hogy a szervezetek „ösztönözzék” tagjaikat etikai alapelveik és küldetésük támogatására. A kódexek _erkölcsi irányelvek_ a szakmai viselkedéshez, segítve az alkalmazottakat vagy tagokat olyan döntések meghozatalában, amelyek összehangban vannak a szervezetük elveivel. Csak annyira hatékonyak, amennyire a tagok önkéntes betartása, azonban sok szervezet további jutalmakat és büntetéseket is kínál a betartás motiválására.

Példák:

 * [Oxford Munich](http://www.code-of-ethics.org/code-of-conduct/) etikai kódex
 * [Data Science Association](http://datascienceassn.org/code-of-conduct.html) magatartási kódex (2013-ban létrehozva)
 * [ACM Etikai és szakmai magatartási kódex](https://www.acm.org/code-of-ethics) (1993 óta)

> 🚨 Tagja Ön valamilyen mérnöki vagy adattudományi szervezetnek? Nézze meg honlapjukat, hogy van-e professzionális etikai kódexük. Mit mond ez az etikai elveikről? Hogyan „ösztönzik” a tagokat a kódex követésére?

### 2. Etikai ellenőrzőlisták

Míg a szakmai kódexek a gyakorlók részéről megkövetelt _etikus viselkedést_ határozzák meg, [ismert korlátozásaik vannak](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md) a végrehajtásban, különösen nagyszabású projektek esetén. Ehelyett sok adattudományi szakértő az ellenőrzőlistákat [ajanlja](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md), amelyek képesek **összekapcsolni az elveket a gyakorlatokkal** determinisztikusabb és cselekvésre alkalmas módon.

Az ellenőrzőlisták kérdéseket „igen/nem” feladatokká alakítanak, amelyeket működtetni lehet, lehetővé téve, hogy nyomon kövessék őket a szokásos termékkiadási munkafolyamat részeként.

Példák:
 * [Deon](https://deon.drivendata.org/) – általános célú adat-etikai ellenőrzőlista, amelyet ipari ajánlásokból hoztak létre, parancssori eszközzel a könnyű integrációhoz.
 * [Adatvédelmi Audit Ellenőrzőlista](https://cyber.harvard.edu/ecommerce/privacyaudit.html) – általános útmutatást nyújt az információkezelési gyakorlatokra jogi és társadalmi kockázatok szempontjából.
 * [MI Méltányossági Ellenőrzőlista](https://www.microsoft.com/en-us/research/project/ai-fairness-checklist/) – MI szakemberek készítették az igazságossági ellenőrzések integrálás támogatására az MI fejlesztési ciklusába.
 * [22 kérdés az adat- és MI etikában](https://medium.com/the-organization/22-questions-for-ethics-in-data-and-ai-efb68fd19429) – nyíltabb keretrendszer, elsősorban az etikai kérdések kezdeti feltérképezésére tervezve a tervezés, kivitelezés és szervezeti környezetekben.

### 3. Etikai szabályozások

Az etika a megosztott értékek definiálásáról és a helyes cselekvések _önkéntes_ végrehajtásáról szól. A **megfelelés** a törvény betartását jelenti, ha és ahol ez előírt. Az **irányítás** tágabb értelemben minden olyan tevékenységet lefed, ahogyan a szervezetek működnek az etikai elvek érvényesítésére és a jogszabályok betartására.

Ma az irányítás két formában valósul meg a szervezetekben. Először is, az **etikus MI** elveinek meghatározásáról és az alkalmazás operatív gyakorlatairól van szó minden MI-hez kapcsolódó projektben. Másodszor, a működési területein kötelező érvényű **adatvédelmi szabályozások** betartásáról van szó.

Adatvédelmi és privát szféra szabályozások példái:

 * `1974`, az [USA adatvédelmi törvénye](https://www.justice.gov/opcl/privacy-act-1974) - szabályozza a _szövetségi kormány_ személyes adatok gyűjtését, használatát és közzétételét.
 * `1996`, az [USA egészségbiztosítási felelősség és hordozhatóság törvénye (HIPAA)](https://www.cdc.gov/phlp/publications/topic/hipaa.html) - védi a személyes egészségügyi adatokat.
 * `1998`, az [USA gyermekek online adatvédelmi törvénye (COPPA)](https://www.ftc.gov/enforcement/rules/rulemaking-regulatory-reform-proceedings/childrens-online-privacy-protection-rule) - védi a 13 év alatti gyermekek adatvédelmét.
 * `2018`, az [Általános adatvédelmi rendelet (GDPR)](https://gdpr-info.eu/) - felhasználói jogokat, adatvédelmet és privát szférát biztosít.
 * `2018`, a [Kaliforniai fogyasztói adatvédelem törvénye (CCPA)](https://www.oag.ca.gov/privacy/ccpa) - több felhasználói _jogot_ ad a személyes adatok kezelésére.
 * `2021`, Kína új [személyes adatok védelméről szóló törvénye](https://www.reuters.com/world/china/china-passes-new-personal-data-privacy-law-take-effect-nov-1-2021-08-20/) amely az egyik legerősebb online adatvédelmi szabályozást hozta létre világszerte.

> 🚨 Az Európai Unió által meghatározott GDPR (Általános Adatvédelmi Rendelet) továbbra is az egyik legbefolyásosabb adatvédelmi szabályozás. Tudta, hogy 8 különböző [felhasználói jogot](https://www.freeprivacypolicy.com/blog/8-user-rights-gdpr) is meghatároz a digitális adatvédelem és az egyéni személyes adatok védelmére? Ismerje meg ezeket és hogy miért fontosak.

### 4. Etikai kultúra

Fontos megjegyezni, hogy továbbra is van egy kézzelfoghatatlan szakadék a _megfelelés_ (azaz a „jog betűje” szerinti megfelelő cselekvés) és a [rendszerszintű problémák kezelése](https://www.coursera.org/learn/data-science-ethics/home/week/4) között (például kicsontosodás, információs aszimmetria, elosztási igazságtalanságok), amelyek felgyorsíthatják az MI fegyverként való használatát.

Utóbbiak megkövetelik az [etikai kultúrák közös megalkotását](https://towardsdatascience.com/why-ai-ethics-requires-a-culture-driven-approach-26f451afa29f), amelyek érzelmi kapcsolatokat és egységes, megosztott értékeket építenek ki _a szervezetek között_ az iparágban. Ez igényli a szervezetekben az [etikai adatkezelési kultúrák formalizálását](https://www.codeforamerica.org/news/formalizing-an-ethical-data-culture), amely lehetővé teszi, hogy _bárki_ [meghúzza az Andon zsinórt](https://en.wikipedia.org/wiki/Andon_(manufacturing)) (hogy korán etikai kérdéseket vethessen fel a folyamatban) és hogy az _etikai értékelések_ (pl. toborzásnál) alapvető kritériummá váljanak az MI projektek csapatainak alakításakor.

---
## [Előadás utáni kvíz](https://ff-quizzes.netlify.app/en/ds/quiz/3) 🎯
## Áttekintés és önálló tanulás

Tanfolyamok és könyvek segítenek megérteni az alapvető etikai fogalmakat és kihívásokat, míg esettanulmányok és eszközök támogatják az alkalmazott etika gyakorlatát a valós környezetben. Íme néhány erőforrás a kezdéshez.

* [Gépi tanulás kezdőknek](https://github.com/microsoft/ML-For-Beginners/blob/main/1-Introduction/3-fairness/README.md) - leckéje a méltányosságról, a Microsofttól.
* [A felelős MI alapelvei](https://docs.microsoft.com/en-us/learn/modules/responsible-ai-principles/) – ingyenes tanulási útvonal a Microsoft Learn-től.
* [Etika és adattudomány](https://resources.oreilly.com/examples/0636920203964) – O'Reilly E-könyv (M. Loukides, H. Mason és társai)
* [Adattudomány etika](https://www.coursera.org/learn/data-science-ethics#syllabus) – online tanfolyam a Michigan Egyetemtől.
* [Etika kibontva](https://ethicsunwrapped.utexas.edu/case-studies) – esettanulmányok a Texas Egyetemről.

# Feladat 

[Írj egy adatetikai esettanulmányt](assignment.md)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**Jogi nyilatkozat**:
Ez a dokumentum az AI fordítási szolgáltatás, a [Co-op Translator](https://github.com/Azure/co-op-translator) segítségével készült. Bár az pontosságra törekszünk, kérjük, vegye figyelembe, hogy az automatikus fordítások hibákat vagy pontatlanságokat tartalmazhatnak. Az eredeti dokumentum az anyanyelvén tekintendő hiteles forrásnak. Fontos információk esetén professzionális emberi fordítást javasolunk. Nem vállalunk felelősséget semmilyen félreértésért vagy téves értelmezésért, amely ebből a fordításból ered.
<!-- CO-OP TRANSLATOR DISCLAIMER END -->