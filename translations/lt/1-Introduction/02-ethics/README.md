# Įvadas į duomenų etiką

|![ Sketchnote by [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/02-Ethics.png)|
|:---:|
| Duomenų mokslo etika - _Sketchnote by [@nitya](https://twitter.com/nitya)_ |

---

Mes visi esame duomenų piliečiai, gyvenantys duomenų supančiame pasaulyje.

Rinkos tendencijos sako, kad iki 2022 m. 1 iš 3 didelių organizacijų pirks ir parduos savo duomenis internetu per [turgavietes ir biržas](https://www.gartner.com/smarterwithgartner/gartner-top-10-trends-in-data-and-analytics-for-2020/). Kaip **programų kūrėjai** mes lengviau ir pigiau integruosime duomenimis grindžiamas įžvalgas ir algoritmine automatizaciją į kasdienes naudotojų patirtis. Tačiau, kai DI taps visur paplitęs, taip pat turėsime suprasti potencialią žalą, kurią gali sukelti tokių algoritmų [ginklavimas](https://www.youtube.com/watch?v=TQHs8SA1qpk) dideliais mastais.

Tendencijos rodo, kad iki 2025 m. generuosime ir naudosime daugiau nei [180 zettabaitų](https://www.statista.com/statistics/871513/worldwide-data-created/) duomenų. **Duomenų mokslininkams** ši informacijos sprogstanti apimtis suteikia precedento neturintį prieinamumą prie asmeninių ir elgsenos duomenų. Kartu tai suteikia galią kurti detalius naudotojų profilius ir subtiliai daryti įtaką sprendimų priėmimui – dažnai tokiu būdu, kuris kuria [laisvos pasirinkimo iliuziją](https://www.datasciencecentral.com/the-pareto-set-and-the-paradox-of-choice/). Nors tai galima naudoti nukreipiant naudotojus link pageidaujamų rezultatų, tai taip pat kelia esminių klausimų apie duomenų privatumą, autonomiją ir etinius algoritminės įtakos ribojimus.

Duomenų etika dabar yra _būtinos saugos priemonės_ duomenų moksle ir inžinerijoje, padedančios sumažinti potencialią žalą ir nepageidaujamas pasekmes mūsų veiksmams, grindžiamiems duomenimis. [Gartner AI Hype ciklas](https://www.gartner.com/smarterwithgartner/2-megatrends-dominate-the-gartner-hype-cycle-for-artificial-intelligence-2020/) nustato aktualias tendencijas skaitmeninės etikos, atsakingo DI ir DI valdymo srityse kaip pagrindinius varomuosius jėgas platesnėse megatrendų temose apie DI _demokratizavimą_ ir _pramoninimą_.

![Gartner's Hype Cycle for AI - 2020](https://images-cdn.newscred.com/Zz1mOWJhNzlkNDA2ZTMxMWViYjRiOGFiM2IyMjQ1YmMwZQ==)

Šioje pamokoje nagrinėsime įdomią duomenų etikos sritį – nuo pagrindinių sąvokų ir iššūkių iki atvejų studijų ir taikomosios DI koncepcijų, tokių kaip valdymas, kurie padeda užtikrinti etikos kultūrą komandose ir organizacijose, dirbančiose su duomenimis ir DI.




## [Priešpaskaitos testas](https://ff-quizzes.netlify.app/en/ds/quiz/2) 🎯

## Pagrindinės sąvokos

Pradėkime nuo pagrindinės terminologijos supratimo.

Žodis „etika“ kilęs iš [graikiško žodžio „ethikos“](https://en.wikipedia.org/wiki/Ethics) (ir jo šaknies „ethos“), reiškiančio _charakterį arba moralinę prigimtį_. 

**Etika** reiškia bendrąsias vertybes ir moralinius principus, kurie reguliuoja mūsų elgesį visuomenėje. Etika remiasi ne įstatymais, o plačiai priimtomis normomis apie tai, kas yra „teisinga prieš klaidingą“. Tačiau etiniai svarstymai gali turėti įtakos korporaciniam valdymui ir vyriausybės reglamentams, kurie sukuria daugiau paskatų laikytis reikalavimų.

**Duomenų etika** yra [nauja etikos šaka](https://royalsocietypublishing.org/doi/full/10.1098/rsta.2016.0360#sec-1), kuri „tiriama ir vertina moralius klausimus, susijusius su _duomenimis, algoritmais ir susijusiomis praktikomis_“. Čia **„duomenys“** orientuojasi į veiksmus, susijusius su generavimu, registravimu, tvarkymu, apdorojimu, sklaida, dalijimusi ir naudojimu, **„algoritmai“** orientuojasi į DI, agentus, mašininį mokymąsi ir robotus, o **„praktikos“** apima temas, tokias kaip atsakinga inovacija, programavimas, kibernetinės atakos ir etikos kodeksai.

**Taikomoji etika** yra [praktinis moralinių svarstymų taikymas](https://en.wikipedia.org/wiki/Applied_ethics). Tai aktyvus etinių problemų tyrimas realaus pasaulio veiksmų, produktų ir procesų kontekste, bei korekcinių priemonių taikymas, kad būtų užtikrinta atitiktis mūsų apibrėžtoms etinėms vertybėms.

**Etikos kultūra** reiškia [_taikomosios etikos įgyvendinimą_](https://hbr.org/2019/05/how-to-design-an-ethical-organization), kad užtikrintų, jog mūsų etiniai principai ir praktikos būtų nuosekliai ir masteliniškai taikomi visoje organizacijoje. Sėkmingos etikos kultūros apibrėžia organizacijos lygiu etinius principus, suteikia prasmingų paskatų atitikčiai ir stiprina etikos normas, skatindamos ir stiprindamos pageidaujamą elgesį kiekviename organizacijos lygmenyje.


## Etikos sąvokos

Šioje skiltyje aptarsime tokias sąvokas kaip **bendros vertybės** (principai) ir **etikiniai iššūkiai** (problemų) duomenų etikos srityje – ir nagrinėsime **atvejų studijas**, kurios padės geriau suprasti šias sąvokas realaus pasaulio kontekstuose.

### 1. Etikos principai

Kiekviena duomenų etikos strategija prasideda nuo _etinių principų_ apibrėžimo – „bendrų vertybių“, apibūdinančių priimtinus elgesio modelius ir nurodančių tinkamus veiksmus mūsų duomenų ir DI projektuose. Juos galima apibrėžti individualiai arba komandiniu lygiu. Tačiau dauguma didelių organizacijų juos įtraukia į _atsakingo DI_ misijos pareiškimą arba sistemą, kuri apibrėžta įmonių lygiu ir nuosekliai taikoma visuose skyriuose.

**Pavyzdys:** Microsoft atsakingo DI misijos pareiškimas skamba taip: _„Mes esame įsipareigoję DI plėtrai, remiantis etiniais principais, kurie pirmiausia rūpinasi žmonėmis“_ – identifikuodamas toliau esančiame sistemos apraše 6 etikos principus:

![Responsible AI at Microsoft](https://docs.microsoft.com/en-gb/azure/cognitive-services/personalizer/media/ethics-and-responsible-use/ai-values-future-computed.png)

Trumpai apžvelkime šiuos principus. _Skaidrumas_ ir _atsekamumas_ yra pamatinės vertybės, ant kurių remiasi kiti principai – pradėkime nuo jų:

* [**Atsekamumas**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) daro praktiką _atsakingą_ už jų duomenų ir DI veiklas bei šių etikos principų laikymąsi.
* [**Skaidrumas**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) užtikrina, kad duomenų ir DI veiksmai būtų _suprantami_ (aiškiai interpretuojami) naudotojams, paaiškinant sprendimų esmę ir priežastis.
* [**Teisingumas**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6) orientuojasi į DI lygiavertį _visų žmonių_ traktavimą, sprendžiant bet kokias sistemines ar paslėptas socialines-technines šališkumo problemas duomenyse ir sistemose.
* [**Patikimumas ir saugumas**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) užtikrina, kad DI elgiasi _nuosekliai_ pagal apibrėžtas vertybes, mažinant galimą žalą ar nepageidaujamas pasekmes.
* [**Privatumas ir saugumas**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) reiškia duomenų kilmės supratimą ir _naudotojų duomenų privatumo bei susijusių apsaugų_ suteikimą.
* [**Įtrauktis**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) reiškia DI sprendimų kūrimą su ketinimu, pritaikant juos įvairiems _žmonių poreikiams ir gebėjimams_.

> 🚨 Pagalvokite, koks galėtų būti jūsų duomenų etikos misijos pareiškimas. Išnagrinėkite kitų organizacijų atsakingo DI sistemas – štai pavyzdžiai iš [IBM](https://www.ibm.com/cloud/learn/ai-ethics), [Google](https://ai.google/principles) ir [Facebook](https://ai.facebook.com/blog/facebooks-five-pillars-of-responsible-ai/). Kokias bendras vertybes jie turi? Kaip šie principai susiję su DI produktu ar pramone, kurioje veikia?

### 2. Etikos iššūkiai

Kai turime apibrėžtus etinius principus, kitas žingsnis – įvertinti mūsų duomenų ir DI veiksmus, ar jie atitinka tas bendras vertybes. Galvokite apie savo veiksmus dviem kategorijomis: _duomenų rinkimas_ ir _algoritmų kūrimas_.

Duomenų rinkimo atveju veiksmai greičiausiai apims **asmeninius duomenis** arba identifikuojamąjį asmens informaciją (PII) apie įžvelgiamus gyvus asmenis. Tai apima [įvairius neasmeninius duomenis](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-personal-data_en), kurie _kartu_ leidžia identifikuoti asmenį. Etiniai iššūkiai gali būti susiję su _duomenų privatumu_, _duomenų savininkyste_ ir susijusiomis temomis, kaip _informed consent_ (informuotas sutikimas) ir _intelektinės nuosavybės teisės_ naudotojams.

Algoritmų kūrimo atveju veiksmai apima **duomenų rinkinių** surinkimą ir tvarkymą, vėliau naudojimą treniruoti ir diegti **duomenų modelius**, kurie prognozuoja rezultatus arba automatizuoja sprendimus realaus pasaulio kontekstuose. Etiniai iššūkiai gali kilti dėl _duomenų rinkinio šališkumo_, _duomenų kokybės_ problemų, _neteisingumo_ ir _klaidingo atstovavimo_ algoritmuose – įskaitant sisteminių pobūdžių problemas.

Abiem atvejais etikos iššūkiai rodo sritis, kur mūsų veiksmai gali prieštarauti bendroms vertybėms. Norėdami aptikti, sumažinti ar pašalinti šiuos klausimus, turime užduoti moralinius „taip/ne“ klausimus, susijusius su mūsų veiksmais, ir prireikus imtis korekcinių veiksmų. Pažiūrėkime keletą etikos iššūkių ir moralinių klausimų, kuriuos jie kelia:


#### 2.1 Duomenų savininkystė

Duomenų rinkimas dažnai apima asmeninius duomenis, kurie gali identifikuoti duomenų subjektus. [Duomenų savininkystė](https://permission.io/blog/data-ownership) yra susijusi su _kontrole_ ir [_naudotojų teisėmis_](https://permission.io/blog/data-ownership), susijusiomis su duomenų kūrimu, tvarkymu ir sklaida.

Moraliniai klausimai, kuriuos turime užduoti, yra:
 * Kas valdo duomenis? (naudotojas ar organizacija)
 * Kokias teises turi duomenų subjektai? (pvz.: prieiga, ištrynimas, perkeliamumas)
 * Kokias teises turi organizacijos? (pvz.: neteisingų naudotojų atsiliepimų pataisymai)

#### 2.2 Informuotas sutikimas

[Informuotas sutikimas](https://legaldictionary.net/informed-consent/) apibrėžia veiksmą, kai naudotojai sutinka su veiksmu (pvz., duomenų rinkimu) _visiškai suprasdami_ susijusias aplinkybes, įskaitant tikslą, galimas rizikas ir alternatyvas.

Klausimai čia yra:
 * Ar naudotojas (duomenų subjektas) leido surinkti ir naudoti duomenis?
 * Ar naudotojas suprato, kam tie duomenys surinkti?
 * Ar naudotojas suprato galimas rizikas savo dalyvavime?

#### 2.3 Intelektinė nuosavybė

[Intelektinė nuosavybė](https://en.wikipedia.org/wiki/Intellectual_property) reiškia nematerialius kūrinius, atsirandančius iš žmogaus iniciatyvos, kurie gali turėti _ekonominę vertę_ asmenims ar verslui.

Klausimai čia yra:
 * Ar surinkti duomenys turėjo ekonominę vertę naudotojui ar verslui?
 * Ar **naudotojas** turi intelektinę nuosavybę šiuose duomenyse?
 * Ar **organizacija** turi intelektinę nuosavybę šiuose duomenyse?
 * Jei teisės egzistuoja, kaip mes jas apsaugome?

#### 2.4 Duomenų privatumas

[Duomenų privatumas](https://www.northeastern.edu/graduate/blog/what-is-data-privacy/) arba informacijos privatumą reiškia naudotojo privatumo išlaikymą ir naudotojo tapatybės apsaugą, susijusią su identifikuojamais asmens duomenimis.

Klausimai čia yra:
 * Ar naudotojų (asmens) duomenys apsaugoti nuo įsilaužimų ir nutekėjimų?
 * Ar naudotojų duomenys prieinami tik autorizuotiems naudotojams ir kontekstams?
 * Ar naudotojų anonimiškumas išsaugomas dalijantis ar skleidžiant duomenis?
 * Ar naudotojas gali būti identifikuotas iš anonimizuotų duomenų rinkinių?

#### 2.5 Teisė būti pamirštam

[Teisė būti pamirštam](https://en.wikipedia.org/wiki/Right_to_be_forgotten) arba [teisė į ištrynimą](https://www.gdpreu.org/right-to-be-forgotten/) pateikia papildomą asmeninių duomenų apsaugą naudotojams. Ji suteikia teisę prašyti asmeninių duomenų ištrynimo ar pašalinimo iš interneto paieškų ir kitų vietų, _tam tikromis aplinkybėmis_ – leidžiančią naują pradžią internete be praeities veiksmų neigiamų pasekmių.

Klausimai čia yra:
 * Ar sistema leidžia duomenų subjektams prašyti ištrynimo?
 * Ar naudotojo sutikimo atšaukimas turėtų inicijuoti automatinį ištrynimą?
 * Ar duomenys surinkti be sutikimo arba neteisėtais būdais?
 * Ar mes atitinkame vyriausybės duomenų privatumo reglamentus?

#### 2.6 Duomenų rinkinio šališkumas

Duomenų rinkinio arba [rinkimo šališkumas](http://researcharticles.com/index.php/bias-in-data-collection-in-research/) reiškia _nereprezentatyvios_ duomenų pogrupio parinkimą algoritmų kūrimui, sukuriant galimą neteisingumą rezultatų grupėse. Šališkumo rūšys apima atrankos arba imties šališkumą, savanorių šališkumą ir įrankių šališkumą.

Klausimai čia yra:
 * Ar surinkome reprezentatyvią duomenų subjektų imtį?
 * Ar išbandėme mūsų surinktą ar tvarkomą duomenų rinkinį dėl įvairių šališkumų?
 * Ar galime sumažinti ar pašalinti rastą šališkumą?

#### 2.7 Duomenų kokybė

[Duomenų kokybė](https://lakefs.io/data-quality-testing/) reiškia paruošto duomenų rinkinio, naudojamo algoritmams kurti, patikimumo patikrinimą, ar savybės ir įrašai atitinka reikalavimus tikslumo ir nuoseklumo požiūriu mūsų DI tikslams.

Klausimai čia yra:
 * Ar surinkome galiojančias _savybes_ mūsų naudojimo atvejui?
 * Ar duomenys surinkti _nuosekliai_ iš įvairių duomenų šaltinių?
 * Ar duomenų rinkinys yra _pilnas_ įvairioms sąlygoms ar scenarijams?
 * Ar informacija surinkta _tiksliai_, atspindinti realybę?
#### 2.8 Algoritmų teisingumas

[Algoritmų teisingumas](https://towardsdatascience.com/what-is-algorithm-fairness-3182e161cf9f) tikrina, ar algoritmo dizainas sistemingai diskriminuoja tam tikras duomenų subjektų pogrupius, dėl ko gali kilti [galimų žalų](https://docs.microsoft.com/en-us/azure/machine-learning/concept-fairness-ml) _resursų paskirstyme_ (kai resursai yra atimami ar neprieinami tam pogrupiui) ir _paslaugos kokybėje_ (kai DI nėra tokia tiksliai kai kuriems pogrupiams, kaip kitiems).

Štai klausimai, kuriuos čia verta nagrinėti:
 * Ar vertinome modelio tikslumą skirtingiems pogrupiams ir sąlygoms?
 * Ar sistemą tikrinome dėl galimų žalų (pvz., stereotipavimo)?
 * Ar galime atnaujinti duomenis arba išmokyti modelius iš naujo, kad sumažintume nustatytas žalas?

Pasidomėkite ištekliais, tokiais kaip [DI teisingumo kontroliniai sąrašai](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE4t6dA), kad sužinotumėte daugiau.

#### 2.9 Duomenų iškraipymas

[Duomenų iškraipymas](https://www.sciencedirect.com/topics/computer-science/misrepresentation) susijęs su klausimu, ar mes sąžiningai ir teisingai pateikiame įžvalgas, ar klaidinančiai iškreipiame duomenis, kad palaikytume norimą naratyvą.

Štai klausimai, kuriuos verta nagrinėti:
 * Ar mes pateikiame neišsamius ar netikslius duomenis?
 * Ar vizualizuojame duomenis taip, kad tai skatintų klaidingas išvadas?
 * Ar naudojame atrinktus statistinius metodus rezultatų manipuliavimui?
 * Ar yra alternatyvių paaiškinimų, galinčių pasiūlyti kitokią išvadą?

#### 2.10 Laisvos valios iliuzija

[Laisvos valios iliuzija](https://www.datasciencecentral.com/profiles/blogs/the-illusion-of-choice) atsiranda, kai sistemos "pasirinkimų architektūros" naudoja sprendimų priėmimo algoritmus, kad paskatintų žmones priimti pageidaujamą rezultatą, tuo pačiu atrodydamos tarsi suteiktų pasirinkimo laisvę ir kontrolę. Šie [tamsūs modeliai](https://www.darkpatterns.org/) gali sukelti socialinę ir ekonominę žalą vartotojams. Kadangi vartotojų sprendimai veikia elgesio profilius, šie veiksmai gali skatinti ateities sprendimus, kurie stiprina ar pailgina šių žalų poveikį.

Štai klausimai, kuriuos verta nagrinėti:
 * Ar vartotojas suprato, kokias pasekmes turi tie pasirinkimai?
 * Ar vartotojas žinojo apie (alternatyvius) pasirinkimus ir jų privalumus bei trūkumus?
 * Ar vartotojas gali vėliau atšaukti automatizuotą ar paveiktą sprendimą?

### 3. Atvejų analizė

Kad geriau suprastume šiuos etikos iššūkius realiame pasaulyje, naudinga pažvelgti į atvejų analizes, kurios išryškina galimas žalas ir pasekmes asmenims bei visuomenei, kai etikos pažeidimai yra nepastebimi.

Pateikiami keli pavyzdžiai:

| Etikos iššūkis | Atvejo analizė  | 
|--- |--- |
| **Informatyvus sutikimas** | 1972 m. - [Tuskegee sifilio tyrimas](https://en.wikipedia.org/wiki/Tuskegee_Syphilis_Study) – afroamerikiečiams vyrams, dalyvavusiems tyrime, buvo pažadėta nemokama medicininė pagalba, tačiau tyrėjai _apgavo_, nes nepateikė informacijos apie diagnozę ir gydymo galimybes. Daug dalyvių mirė, o jų partneriai ar vaikai nukentėjo; tyrimas truko 40 metų. | 
| **Duomenų privatumas** | 2007 m. - [Netflix duomenų premija](https://www.wired.com/2007/12/why-anonymous-data-sometimes-isnt/) suteikė tyrėjams _10 mln. anonimizuotų filmų įvertinimų iš 50 tūkst. klientų_ rekomendacijų algoritmų gerinimui. Tačiau tyrėjai sugebėjo susieti anonimizuotus duomenis su asmeniškai identifikuojančia informacija _iš išorinių duomenų rinkinių_ (pvz., IMDb komentarų), taip efektyviai "deanonimizuodami" kai kuriuos Netflix abonentus.|
| **Duomenų surinkimo šališkumas**  | 2013 m. - Bostono miestas sukūrė programėlę [Street Bump](https://www.boston.gov/transportation/street-bump), leidžiančią gyventojams pranešti apie duobes, taip surenkant geresnius duomenis apie kelių būklę. Tačiau [žmonėms mažesnes pajamas turinčiose grupėse buvo mažiau prieigos prie automobilių ir telefonų](https://hbr.org/2013/04/the-hidden-biases-in-big-data), todėl jų kelių problemos programėje liko nematomos. Kūrėjai bendradarbiavo su akademikais, kad spręstų _teisingo prieinamumo ir skaitmenines atskirtis_. |
| **Algoritminis teisingumas**  | 2018 m. - MIT [Gender Shades tyrimas](http://gendershades.org/overview.html) vertino lyties atpažinimo DI produktų tikslumą ir atskleidė spragas tikslume moterims bei spalvotųjų žmonių atžvilgiu. 2019 m. [Apple Card](https://www.wired.com/story/the-apple-card-didnt-see-genderand-thats-the-problem/) atrodė suteikianti mažiau kredito moterims nei vyrams. Abu atvejai iliustruoja algoritmų šališkumo problemas, sukeliančias socialines ir ekonomines žalas.|
| **Duomenų iškraipymas** | 2020 m. Gruzijos visuomenės sveikatos departamentas paskelbė COVID-19 diagramas, kurios atrodė klaidinančios dėl nechronologinės tvarkos x ašyje, sukeldamos klaidingą įspūdį apie patvirtintų atvejų tendencijas. Tai iliustruoja iškraipymą naudojant vizualizavimo triukus. |
| **Laisvos valios iliuzija** | 2020 m. Learning app [ABCmouse sumokėjo 10 mln. dolerių, kad išspręstų FTC skundą](https://www.washingtonpost.com/business/2020/09/04/abcmouse-10-million-ftc-settlement/), nes tėvai buvo įkalinti mokėti už prenumeratas, kurių negalėjo atšaukti. Tai iliustruoja tamsius modelius pasirinkimų architektūrose, kai vartotojai buvo skatinami rinktis galimai žalingus sprendimus. |
| **Duomenų privatumas ir vartotojų teisės** | 2021 m. Facebook [duomenų nutekėjimas](https://www.npr.org/2021/04/09/986005820/after-data-breach-exposes-530-million-facebook-says-it-will-not-notify-users) atskleidė 530 mln. vartotojų duomenis, dėl ko buvo sumokėta 5 mlrd. dolerių bauda FTC. Tačiau vartotojai nebuvo informuoti apie incidentą, pažeidžiant skaidrumo ir prieigos teisę. |

Norite sužinoti daugiau atvejų analizės? Pažiūrėkite šiuos išteklius:
* [Ethics Unwrapped](https://ethicsunwrapped.utexas.edu/case-studies) – etikos dilemos įvairiose pramonės šakose.
* [Duomenų mokslo etikos kursas](https://www.coursera.org/learn/data-science-ethics#syllabus) – nagrinėjamos svarbiausios atvejų analizės.
* [Kur kas nors nepavyko](https://deon.drivendata.org/examples/) – Deon kontrolinis sąrašas su pavyzdžiais.

> 🚨 Pagalvokite apie atvejus, kuriuos matėte – ar savo gyvenime susidūrėte su panašiu etikos iššūkiu? Ar galite įvardyti bent vieną kitą atvejį, kuris iliustruoja vieną iš šio skyriaus aptartų etikos iššūkių?

## Taikomoji etika

Aptarėme etikos sąvokas, iššūkius ir atvejų analizę realaus pasaulio kontekste. Bet kaip pradėti _taikyti_ etikos principus ir praktiką projektuose? Ir kaip _operacionalizuoti_ šias praktikas geresniam valdymui? Pažvelkime į keletą realių sprendimų:

### 1. Profesiniai kodeksai

Profesiniai kodeksai yra viena iš galimybių organizacijoms „skatinti“ savo narius remti jų etikos principus ir misijos deklaraciją. Kodeksai yra _moralinės gairės_ profesiniam elgesiui, padedančios darbuotojams arba nariams priimti sprendimus, atitinkančius organizacijos principus. Jie veiksmingi tik jei nariai savanoriškai jų laikosi; tačiau daugelis organizacijų taiko papildomas paskatas ir sankcijas, kad paskatintų narių laikymąsi.

Pavyzdžiai:

 * [Oxford Munich](http://www.code-of-ethics.org/code-of-conduct/) etikos kodeksas
 * [Data Science Association](http://datascienceassn.org/code-of-conduct.html) elgesio kodeksas (sukurtas 2013 m.)
 * [ACM etikos ir profesinio elgesio kodeksas](https://www.acm.org/code-of-ethics) (nuo 1993 m.)

> 🚨 Ar priklausote kokiai nors inžinerijos ar duomenų mokslo profesionalų organizacijai? Pažvelkite į jų svetainę, ar jie apibrėžia profesinį etikos kodeksą. Ką šis kodeksas sako apie jų etikos principus? Kaip jie „skatina“ narius jo laikytis?

### 2. Etikos kontroliniai sąrašai

Nors profesiniai kodeksai apibrėžia privalomą _etišką elgesį_ praktikams, jie [turi žinomų ribotumų](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md) vykdyme, ypač didelio masto projektuose. Vietoje to daugelis duomenų mokslo ekspertų [rekomenduoja kontrolinius sąrašus](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md), kurie gali **jungti principus su praktika** deterministiškai ir veiksmingai.

Kontroliniai sąrašai paverčia klausimus „taip/ne“ užduotimis, kurias galima įgyvendinti ir stebėti kaip įprastos produktų leidimo darbo eigą.

Pavyzdžiai:
 * [Deon](https://deon.drivendata.org/) – bendros paskirties duomenų etikos kontrolinis sąrašas, sukurtas pagal [pramonės rekomendacijas](https://deon.drivendata.org/#checklist-citations), su komandinės eilutės įrankiu integracijai.
 * [Privatumo audito kontrolinis sąrašas](https://cyber.harvard.edu/ecommerce/privacyaudit.html) – teikia bendras gaires informacijos tvarkymo praktikoms iš teisinių ir socialinių rizikų perspektyvos.
 * [DI teisingumo kontrolinis sąrašas](https://www.microsoft.com/en-us/research/project/ai-fairness-checklist/) – sukurtas DI specialistų, siekiant paremti teisingumo patikras DI kūrimo cikluose.
 * [22 klausimai apie etiką duomenų ir DI srityje](https://medium.com/the-organization/22-questions-for-ethics-in-data-and-ai-efb68fd19429) – atviresnis rėmimo rinkinys, skirtas pradinei etikos klausimų analizė dizaino, įgyvendinimo ir organizacinėse srityse.

### 3. Etikos reglamentai

Etika susijusi su bendrų vertybių apibrėžimu ir teisingo elgesio vykdymu _savanoriškai_. **Atitiktis** yra _teisės laikymasis_, jei ir kur ji nustatyta. **Valdymas** apima visus būdus, kaip organizacijos veikia, kad užtikrintų etikos principų vykdymą ir laikymąsi galiojančių įstatymų.

Šiandien valdymas organizacijose vykdomas dviem būdais. Pirma, tai etinio DI principų apibrėžimas ir praktikų, užtikrinančių jų taikymą visuose DI projektuose, nustatymas. Antra, tai atitiktis visiems valdžios institucijų nustatytiems **duomenų apsaugos reglamentams** regionuose, kuriuose organizacija veikia.

Duomenų apsaugos ir privatumo reglamentų pavyzdžiai:

 * `1974`, [JAV privatumo įstatymas](https://www.justice.gov/opcl/privacy-act-1974) – reglamentuoja _federalinės vyriausybės_ asmens duomenų rinkimą, naudojimą ir atskleidimą.
 * `1996`, [JAV sveikatos draudimo skaidrumo ir atskaitomybės įstatymas (HIPAA)](https://www.cdc.gov/phlp/publications/topic/hipaa.html) – saugo asmens sveikatos duomenis.
 * `1998`, [JAV vaikų internetinės privatumo apsaugos įstatymas (COPPA)](https://www.ftc.gov/enforcement/rules/rulemaking-regulatory-reform-proceedings/childrens-online-privacy-protection-rule) – saugo vaikų iki 13 metų duomenų privatumą.
 * `2018`, [Bendrasis duomenų apsaugos reglamentas (GDPR)](https://gdpr-info.eu/) – suteikia vartotojų teises, duomenų apsaugą ir privatumą.
 * `2018`, [Kalifornijos vartotojų privatumo įstatymas (CCPA)](https://www.oag.ca.gov/privacy/ccpa) suteikia vartotojams daugiau _teisų_ dėl jų (asmeninių) duomenų.
 * `2021`, Kinijos [Asmeninės informacijos apsaugos įstatymas](https://www.reuters.com/world/china/china-passes-new-personal-data-privacy-law-take-effect-nov-1-2021-08-20/) – neseniai priimtas, sukuriantis vieną griežčiausių interneto duomenų privatumo reglamentų pasaulyje.

> 🚨 Europos Sąjungos apibrėžtas GDPR (Bendrasis duomenų apsaugos reglamentas) yra vienas įtakingiausių šiandienos duomenų privatumo reglamentų. Ar žinojote, kad jis taip pat apibrėžia [8 vartotojų teises](https://www.freeprivacypolicy.com/blog/8-user-rights-gdpr), saugančias piliečių skaitmeninį privatumą ir asmeninius duomenis? Sužinokite, kas tai yra ir kodėl tai svarbu.

### 4. Etikos kultūra

Reiktų pažymėti, kad yra nematoma spraga tarp _atitikties_ (pakanka laikytis „teisės raidės“) ir [_sisteminių problemų_](https://www.coursera.org/learn/data-science-ethics/home/week/4) sprendimo (tokios kaip sustabarėjimas, informacijos asimetrija, paskirstymo neteisybė), kurios gali paspartinti DI ginklavimą.

Pastarieji reikalauja [bendradarbiavimo kuriant etikos kultūrą](https://towardsdatascience.com/why-ai-ethics-requires-a-culture-driven-approach-26f451afa29f), kuri kuriama remiantis emociniais ryšiais ir nuosekliomis vertybėmis _visose organizacijose_ pramonėje. Tai reikalauja labiau [formalizuotos duomenų etikos kultūros](https://www.codeforamerica.org/news/formalizing-an-ethical-data-culture/) organizacijose – leidžiančios _bet kam_ [pabėgti už Andon virvutės](https://en.wikipedia.org/wiki/Andon_(manufacturing)) (ankstyvam etikos problemų kėlimui) ir padaryti _etinius vertinimus_ (pvz., atrankose) pagrindiniu komandos formavimo kriterijumi DI projektuose.

---
## [Po paskaitos testas](https://ff-quizzes.netlify.app/en/ds/quiz/3) 🎯
## Peržiūra ir savarankiškas mokymasis

Kursai ir knygos padeda suprasti pagrindines etikos sąvokas ir iššūkius, o atvejų analizės ir įrankiai padeda taikyti etiką realaus pasaulio kontekste. Štai keletas pradinių išteklių.

* [Pradžiamokslis apie mašininį mokymąsi](https://github.com/microsoft/ML-For-Beginners/blob/main/1-Introduction/3-fairness/README.md) – pamoka apie teisingumą, Microsoft.
* [Atsakingo DI principai](https://docs.microsoft.com/en-us/learn/modules/responsible-ai-principles/) - nemokamas mokymosi kelias iš Microsoft Learn.
* [Etika ir duomenų mokslas](https://resources.oreilly.com/examples/0636920203964) - O'Reilly el. knyga (M. Loukides, H. Mason ir kt.)
* [Duomenų mokslo etika](https://www.coursera.org/learn/data-science-ethics#syllabus) - internetinis kursas iš Mičigano universiteto.
* [Etika atskleista](https://ethicsunwrapped.utexas.edu/case-studies) - atvejų analizės iš Teksaso universiteto.

# Užduotis 

[Parašykite duomenų etikos atvejo analizę](assignment.md)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**Atsakomybės apribojimas**:
Šis dokumentas buvo išverstas naudojant dirbtinio intelekto vertimo paslaugą [Co-op Translator](https://github.com/Azure/co-op-translator). Nors siekiame tikslumo, prašome atkreipti dėmesį, kad automatiniai vertimai gali turėti klaidų ar netikslumų. Originalus dokumentas jo gimtąja kalba laikomas autoritetingu šaltiniu. Svarbiai informacijai rekomenduojama naudoti profesionalų žmogiškąjį vertimą. Mes neatsakome už jokius nesusipratimus ar neteisingą interpretaciją, kilusią naudojantis šiuo vertimu.
<!-- CO-OP TRANSLATOR DISCLAIMER END -->