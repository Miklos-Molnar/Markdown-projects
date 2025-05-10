Breaking News: **Amikor a gép elkezd nélkülünk gondolkodni**, 2025.május 7.
 
Egy kínai nemzetközi kutatócsoport most mutatta be azt, amit sokan évekig lehetetlennek hittek: az adatok nélküli gondolkodást. Nem memorizálás, nem utánzás, hanem **mély, iteratív, szintetikus** önjáték. A következmények? Általánosan revelatív és relevatív (aka releváns) lehet, matematikára, tudományra. Talán még arra is, ahogyan magát a tanulást definiáljuk.

👇 Íme, mi történt, és miért lehet ez a **legfontosabb mesterséges intelligencia mérföldkő az AlphaGo óta**.

Minimum 1 éve tudható, diskurzus tárgyát képező volt, hogy el fog jönni a nap, és el is jött. Jóval hamarabb, mint gondoltam volna. Érzékelhetően, negállíthatatlan a fejlődés. Mégha csak béta is, mégha csak nüansznyi is lehet a performancia-javulás, mégha csak gyerekcipőben lehet is az egész, de legalább '**first draft implemented**'. Ráadásul mégcsak nem is human in-the-loop, hanem egyenesen **human on-the-loop** irányba mozdulva. Az ész megáll, komolyan. Rögzítsük: 2025.május7-én. Szegedy Krisztián (xAi) 2026-os céldátuma előtt bő másfél évvel.

11 kínai cikke: Tsinghua University, Beijing Institute for General Artificial Intelligence & Pennsylvania State University egyetemekről
**ABSOLUTE ZERO: REINFORCED SELF-PLAY REASONING WITH ZERO DATA**
https://arxiv.org/html/2505.03335v2

Itt egy 15 percnyi magyarázó YT-videó a cikkhez:
**New „Absolute Zero” Model Learns with NO DATA**
https://www.youtube.com/watch?v=CqdqZNqljdI

TL;DR - Na és miről lenne szó minél kevesebb ám minél olvasmányosabb betűvel, sietőseknek?

(1) Tegyük fel van egy matematikus, aki **nyitott matematikai problémákat akar megoldani**. Szélső határon mondjuk egy Riemann-sejtést, az olyan jó demó-példa. 

(2) Mindehhez van neki, vagy tervez fejben és/vagy brainstormingban egy megoldási koncepciót, mondjuk **particionálással (dekomponálással)**. Lebontva nagyobb, majd kisebb lépésekre, tételekre, lemmákra, propoziciókra, egzaktan tárgyalható összefüggésekre, stb., mondjuk most így "atomi" szintig. Amik egyébként feltételezhetően - az AI számára is - még így is kezelhetetlenül komplexek. Egy ilyen matematikus nemcsak hallott már az AI-ról, de keresi is az AI "barátságát" az ilyen matek-melóhoz. Például Terence Tao, 230-as IQ-val. Néhányat saját kézben tart, másokat delegál kollégáinak, beosztottainak, privát módon, vagy publikus fórumon keresztül.

(3) A csapat tagjai beküldik az "atomi" problémát valamilyen **LLM-es Deep Reasearch** csővezetékbe. Ám eddig jó eséllyel 90+%-ban az LLM fejrefog állni, AI-s megoldhatatlanság okán. Eddig ugye ezt eddig is tudta az AI. 🙂

(4) Jön a **friss kínai ígérvény**: a betáplált problémához, egy AI-agent(ek), ami(k) kigenerál(nak) **szintetikus training adatok**at pluszba a korábbi meglévő adatok mellé, majd ezek után az így kibővített - inkrementális addicionális trainingbe bevont - adatokon próbálja folytatni a Deep Research-öt (pontossági, tanulhatósági, stb. **jutalmazási rendszer**ben, a **RL=reinforcement learning keretei között**).

(5) Ugye nem nehéz elképzelni, hogy   
  * az **iteráció kvázi végtelenszer ismételhető**, a nap 24 órájában.  
  * A számítási kapacitás bátran **felskálázható** (a **módszer tuningolásá**val párhuzamosan),   
  * miközben a DeepSeek 671 milliárd paraméteres legnagyobb modellje is futhat **home pc**-n, 220V-on, részben éjszakai tarifával.  
  * És ez még csak az **első implementálás**i lépés volt (megmért és kimutatott fejlődéssel).  
  * És akkor még nem beszéltünk az **NVidia** tervezett **Rubin architektúrájú GPU**-jairól.  
(+1) Itt **jegyzem meg**, hogy éles szakmai vitáknak lehetünk szemtanui: Google Deepmind-nál (AlphaZero, MuZero bölcsőnél), az RF-nek nem nagyon vannak barátai. Míg a kínaiak látnivalóan nagyon nyomják az RL-t, akkora potenciált érzékelnek benne. Nyilván nem ennyire fekete-fehér a dolog, de a verseny ezen a téren is nagyon jelentős (az én szememben mindenképpen).

A cikk (szikár, tömör, elevator pitch) konklúziója számomra:
(a) **Kár scaling wallról beszélni még szöveges adatoknál is**, amit pár hónapra előre vár Sam Altman (OpenAI).
(b) Szintetikus adatok, Önjutalmazó tanulás, Verfikálható eremények **hármasa kézzelfogható szimbózisba hozhatók**.
(c) Mindháromféle érvelési  (**deduktív, induktív és abduktív**) képesség integrálhatóvá tehető.
(d) **Invariáns a modell-méret**, amire lehetne mindezt alkalmazni. Lelkiszemeimmel látom a matematikust, a mobiltelefonján lévő mondjuk Microsoft Phi-4-gyel, és konferenciára utazás közben dolgozik a Riemann-sejtésen.
(e) Kiemelkedő lehet tehát a teljesítmény külső adatok nélkül is. **Na most elképzelhető milyen lesz, ha be is vonunk további külső adatokat is**.
