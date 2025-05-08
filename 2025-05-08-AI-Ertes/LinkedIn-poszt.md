**Mi az, hogy "érteni" az AI-hoz, ezt mégis hogyan kell. Ki "ért" hozzá?**

Folytatnám a Vincent-blog posztjának feldolgozását, maradva a Github-on publikált markdown fileformátumú posztoknál, továbbra is leküzdendő a LinkedIn méretbeli korlátait.

**Vincent-blog: AI avagy a hülyék. Az önkritikus posztok sorozatból**  
https://www.orulunkvincent.hu/ai-avagy-a-hulyek-az-onkritikus-posztok-sorozatbol/

Top-down és bottom-up iteráció lehetőségét szem előtt tartva **távoli analógiával** kezdem (azaz mindkét irány szem előtt tartva fókuszálok a két témában): az emberiség mintha **"tűzzel játszana"**, amikor AI-zik". Vajon mennyiben áll az analógia, mai fejünkkel?  

Érveim; az őseink előtt is nyilvánvaló lett  
- ...a tűz **értékei**, található benne használható funkció (pl.: melegedés, ételmelegítés, stb.)  
- ...a tűz **pusztító ereje**, hogy nagyobb terület is le tudhat égni  
- ...amennyiben belegondolnak, akkor tulajdonképpen **NEM értik** a tűz lényegét, velejét, miközben azért próbálják használni.  
- ...**hiába a legjobb tűzvédelmi keretrendszer**, elkerülendő és elkerülhető tűzesetek folyamatosan lesznek.  
- ...nemcsak véletlenül, hanem **szándékoltan is lehet pusztítani** tűzzel. Később pl.: Néro emlékezetes módon "művészi" szintre emelte a műfajt.  
- ...**relatíve kevés ember**(erőforrás) is **relatíve nagyon nagy kár**t okozni a tűzzel, ami ellen **védelmi szabályozással tehát nem könnyű védekezni**.  

És akkor forduljunk rá az AI-értés topikjára, a tűz analógia üzenetét szem előtt tartva.

Vajon az alábbiak kellenek az AI "értés"-éhez?

(1) Fogalmunk sincs, hogy egy transzformer LLM modell (legyen most ez az AI szinonimája nagyon legyszerűsítve és végtelenül pongyolán), egy konkrét kérdésre **pontosan hogyan miért azt válaszolta, amit**. A mélyben  lévő mélytanulásos neurális hálók működése **fekete doboz** a részleteiben. Vannak sikeres törekvések a kifehérítésben már jelenleg is, de az effektív megértés még messze van. Sajnos az emberi agynak ezt a korlátot **nehéz felfognia**, megemésztenie.  

Merthogy **mentálisan nehezebben emészthető témák** folyamatosan kísérik az átlagembert, kezdve pl.: matekban a komplex számokkal, vagy fizikában a fény kettős természetével. Miközben például a fény **áldásait kezdettől fogva igényli** az ember.

Talán legszebb idevágó példa a **kvantum-számítástudomány**, amit azért kevesen látnak át mélységeiben, részleteiben, talán kijelenthetően, hogy kevesebben, mint az AI-t. Mégis, amikor kiderül, hogy Shor prímfaktorizációs algoitmusának műveletigénye polinomiális benne, akkor azért arra jóval többen kapják fel a fejüket. **Fekete dobozban ütős alkalmazás lehetősége.**  

(2) **Grounding** (=megalapozottság). OK. Rendben van és tegyük fel megbarátkoztunk a fekete doboz effekttel. Jön a kövekező kérdés, hogy ugyan nem tudjuk hogyan, de feltehető-e, hogy azért az AI **TUDJA** a fekete dobozon belül, hogy mit miért, hogyan válaszol és ebben az ember kivülről, ezt képes hitelesnek látni és betudni. A gond az, hogy tudhatóan nem képes erre a transzformer architektúra.  

Hétköznapi nyelven szólva úgy merül fel a kérdés, hogy matek érettségin vizsgáztatja szóbelin a tanár a diákot (egy feladat kapcsán) és kiderül, hogy bár a diák megoldása csillagos ötös, látnivalóan megmagyarázhatatlanul és védhetetlenül a semmiből jött a megoldás: mintha a diák puskázott volna, valami - tanár számára értelmetlen - puskából. Követelmény-e, hogy a tanár elhiggye a diák **megalapozottan érti** is vajon az általa adott feladat-megoldást avagy elégséges-e, ha amúgy egyébként jó a megoldás a matematika-vizsgáztatás értékelési szabályai szerint?   

**Univerzálisabban**, generálisabban szólva a tudásnak mennyire része a védhetőség, és indokolhatóság, hiszen egy síma Pitagorász-tétel működőképes lehet nélkülük is, nem? Ami viszont felveti a felelős használat kérdését. Kvázi leszűkül a téma az alábbi kizáró "vagy"-ra.: **VAGY grounding, VAGY felelős használat**, ha AI-ról beszélünk.  

AI-t tekintve sajnos az ember előtt jelenleg csak rossz és rosszabb lehetőségek állnak:  
(a) **vagy Gofai** (szabályalapú) mesterséges intelligencia van, ami grounding-os, ám gyenge performanciájú  
(b) **vagy elképesztő sebesség**gel szárnyal az AI, fejlődik a transzformerek révén, ám nincs hozzá grounding (jelenleg)  
Talán nem véletlen, hogy a Google Deepmind egyre sikeresen társítja őket matekot tekintve.  

(3) Egy villanyszerelő érti tudja a villany funkcióit, veszélyeit, ki van képezve munkavédelmileg (engedélykötelesség kontextusában) hogyan nyúljon a villanyhoz. A nagy kérdés, hogy az AI a művelői számára belepréselhető-e egy hasonló **védelmi, megelőzési keretrendszerbe**, egyáltalán ez elvárás-e és ha igen mennyiben, hogyan.   

Azaz mi van azokkal, akik "értenek" az AI-hoz? Magyarán bárki "értő" bármit, gondol, tesz AI ügyben, akkor **kiszámíthatja-e** hatását, bármiféle megkövetelhető mérlegeléshez? Nekem úgy tűnik jelenleg, hogy a villanyszerelés túl egyszerű, míg az AI túl komplex, így nem nagyon lehet védelmi adaptálódásról beszélni jelenleg.  

Lehet **szabályozni** tág keretek között, de a védelem távolról sem lesz **annyira garantált**, mint villanyszerelésnél.  

Mindezek után én az **első körben** amellett érvelnék, hogy ezek  a fenti amúgy triviálisan jogos követelmények NEM kellenek az AI "értés"-hez. Így a fentiek zöldmezős 100%-os megértését, belőlük való 100%-os levizsgázást peremfeltételnek kikiáltani az értéshez és addig nem használni AI-t, az **túlzott önkorlátozás**nak hat. 

Bizony vannak, lesznek fekete dobozok, amik működését nem érti az ember (vagy tudhatóan egyenesen problémás ez a működés). Az ember mégis megbízik a kimenetben, és fogja akarni használni, addig a fokig, amíg tudja.

A **második kör** az akadémikusságé, ami külön probléma-felvetés a linkelt posztban. Lesz-e, várható-e **"ex cathedra"**, mindenki által megbízható, konszenzussal elfogadhatól hosszú távra is gyors, friss, elégséges megnyilvánulás az AI-ban? Nem gondolnám több dolog miatt sem. A tudományos publikálás a review-kal eléggé lassú folyamat, miközben a **tudás demokratizálódása** a tömegekben feltartózhatatlan és relatíve gyors folyamat. Sokan akarnak érteni az AI-hoz (mint a focihoz) és részesülni előnyeiből. Így aztán egyre többen haználhatják egyre ütősebben az AI-t, bármilyen akadémiai gyökérzetű (ön)korlátozással szemben is.

Na és akkor **harmadik körben** próbáljuk meg megválaszolni a címbeli kérdést. Mi az, hogy "érteni" az AI-hoz? 

Számomra elsősorban ez viszonyulási kultúra kérdése, nem tudáshalmazé, az információk exponenciális robbanása közepette. Magyarán az AI nem tárgy, eszköz, hanem **közeg**.

Azt tekintem "értő"-nek, aki táguló értelmezési keretben fejlődve, képes követni a történéseket, együttlélegezni velük, a korlátok szem előtt tartásával.   Kompetenciahatáron, digitális készségek határain belül  
* fel tud tenni kérdéseket,  
* utána tud menni válaszoknak relatíve kis erőforrásigénnyel, sztoikus értelemben   kellően megnyugtatóan,  
* majd állást tud foglalni,  
* és vállalja állásfoglalásának megvédését is.  
Magyarán saját keretrendszere elég rugalmas ahhoz, hogy funkcionálisan működően, érdemben interaktáljon másokkal.

És ez mire is futhat ki a gyakorlatban? Aki az AI meglévő funkcionalitását képes optimálisan használni, vagy egyenesen bővíteni saját értékteremtési láncában, á lá mint egy szimpla oop-s osztálykönyvtárat a programozásban. Saját magát ÉS embertársi környezetét inspirálja, segíti, kezdve a verbalitással.

Mi lehetne egy záró konkluzió? Nem attól "ért" valaki az AI-hoz, hogy "mérhetően" tud róla ismereteket, hanem attól, hogy épít magának egy olyan méltányolható keretrendszert, amiben kreatívan és felelősen viszonyulhat hozzá.

