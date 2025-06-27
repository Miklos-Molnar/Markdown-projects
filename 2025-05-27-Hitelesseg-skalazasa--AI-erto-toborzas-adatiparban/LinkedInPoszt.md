**A hitelesség skálázása; AI-értő toborzás az adatiparban**

Az eredeti célom az alábbi LinkedIn-poszt publikálása volt, amelyben szeretném magamat meginterjúvolni 10+5 db AI által generált kérdés alapján, a fenti cím szellemében. Az egész dolog kaphatna egy olyan gamifikált keretezést, mintha napjaink mesterséges intelligenciája 10+5 kérdést tenne fel Steve Jobsnak, ha ő ma jelentkezne egy állásra.

**ChatGPT PROMPT:**  
Te most egy **AI-literate**, következő generációs HR-es vagy egy cégnél, aki **adatipari munkatársat keres** (pl. Data Engineer, Data Scientist stb.).
Számos jelölt nyújtja be pályázatát (CV, motivációs levél, LinkedIn-profil URL, stb.).
Előzetesen és opcionálisan egy junior HR-es felhívhatja az összes jelöltet, és elvégezhet minden olyan előszűrést, amit egy kezdő HR-es elvégezhet.
Ő egyben jelzi a jelöltek felé, hogy lesz egy 15 kérdésből álló AI-interjú is, és rákérdez, vállalják-e ezt a szűrési formát.
A junior HR-es kör után te, mint HR-es, szeretnél a **továbbjutott 30 jelöltből 7-et kiválasztani egy újabb előszűrés során, AI-támogatással.**

**Fontos szempontok:**  
* A cél, hogy az AI segítsen a jelöltek személyes, aktuális feltérképezésében, hasonlóan, mint egy AI-támogatott párkeresésnél ("match").  
* Nem szabad túlságosan megterhelni a jelölteket, sőt élvezniük kell a kihívást – ezért legyen **15 kérdés**. (Lásd: gamifikáció.)  
* **A kérdések legyenek nyitottak, reflektívek, önreflexiót és értékrendet feltárók, szituációsak („mi lenne, ha…” típusúak stb.).**  
* A cél nem az, hogy jó vagy rossz válaszokat adjanak, hanem hogy **személyes, eredeti reakciókat kapjunk**. Ne lehessen AI-val vagy Google-lel felkészülni rájuk.  
* A kérdések lehetőség szerint strukturáltan legyenek hasonlóak minden jelölt esetében.  
* A HR-es célja: ne a CV marketingértéke alapján szelektáljon, hanem valós, értékes információkat gyűjtsön a jelöltekről.  
* A válaszokból opcionálisan lehessen AI-val érzékelni, ha valaki „hackelni” próbál: pl. sablonosság, stílusváltás, inkoherencia alapján.  
* A jelöltek fogadják el, és higgyék el, hogy **akkor járnak a legjobban, ha őszintén és mérhetően önmagukat adják.**  
* A végén kérek **még 5 db szakmaibb, kifejtősebb kérdést** is az adatipari területekre (DataOps, BI, AI-integráció stb.).

**01. Volt már, hogy olyan döntést hoztál, ami a rendszer logikája szerint jó volt, de a kollégáid a komfortzónából való kilépésként élték meg?**

Legutolsó nagy kudarcélményem ilyen jellegű volt. Túlságosan szilárdan hittem abban, hogy a SQL Clean Code mindenek felett fontos bármelyik vállalat életében - annak könnyű összekuszálódása okán. Ám végül ez túlzottan reflektorfénybe helyezett engem, ami másokban ellenérzést szült. Tanulság végül az lett, hogy még ebben is, a szakma ellenében is, kell tudni engedni a vállalat egészének összérdekét szem elött tartva, főleg ha létezik kerülő út is, az AI támogatásával.

**02. Milyen „if–then” szabályokat látna egy gép az életedben? Pl. „Ha valami értelmetlenül bonyolult, előbb visszalépek egy szintet.”**

* Ha komplexitás-túlnövekedés kezd szárba szökkenni, akkor amögött esélyesen elmaradt feladat-particionálás fedezhető fel. Több kisebb feladat sokszor sokkal-sokkal gyorsabban oldható meg. Amúgy is általános alapelv, hogy az egyszerűbb az szebb és hozzá sokszor fenntarthatóbb is. Törekedni kell az egyszerűségre, mert az kevesebb potenciális hibát jelenthet, könnyebb azt verifikálni, validálni. Ennek antitézise, hogy a komplexitás-növelés, gyorsabban növeli a költségeket és a sérülékenységet.
* Ha túl sok a manualitás, az hamar exponenciálisan felrobbanthatja a költségeket (fejlesztési erőforrás-pazarlást), még a saját szintemen is. Triviálisan adódik, hogy minden ésszerű automatizálás erőforrást szabadit fel az embernek. Mert általánosságban is igaz, hogy minimalizált költségek mellett kell maximális értéket felmutatni.
* Ha minimális overhead mellett lehet párhuzamosítani, akkor élni kell vele. Analógiában: hiába gyengébb önmagában egy-egy AI generatív modell is, az AI Agentek csodákra képesek, teljesen más működési mechanizmusukkal.
* Ha gyenge a performancia, akkor  
(1) úgy legyen a működési lánc minden eleme stabil, hogy a teljes rendszer legyen optimális. Viszont az optimalizálási sorrend nagyon nem mindegy: érdemes lehet azzal kezdeni, amivel legkönnyebben, legnagyobbat lehet kaszálni.   
(2) el kell tudni engedni a folyamatos szükségtelen optimalizálás kényszerét is. Érthető, hogy minden változtatás fenyeget a teljes rendszer egész szuboptimumával, ám nem minden időpillanatban kell lenni optimálisnak egyetlen rendszernek sem, hanem elég csak a fontos / dedikált időpillanatokban (pl.: üzemeltetésre átadásnál). Főleg, hogy a legújabban az OpenAI Codex bevethető az automatikus optimalizálásra tett AI-s javaslatokra is.

**03. Volt olyan helyzet, ahol az igazságod kockázatos volt a rendszerre nézve, és inkább engedtél a nagyobb érdek javára?**

Nálam ez úgy alapélmény, hogy tisztában vagyok az ambivalens megítélhetőséggel. Úgy vagyok vele, ha bármilyen ötletem nem tapad természetes módon a valóságba, akkor biztosan az ötlet volt rossz. Emögött a motívációm az, hogy a közösség erejében hiszek, mert együtt nevetünk és együtt sírunk. Lehet egy vezető vagy bármelyik kitüntetett személy kiváló képességű, hatalmas talentum, de ha túlságosan dominál, akkor ez a céget óhatatlanul is sérülékennyé teheti. A vállalati jövő útja számomra, vállalati munkaközösségben, hozzáadott értékek minél zavarmentesebb összeadódásával való fejlődés.

**04. Mi az a három projekt, ötlet vagy vágy, amit évek óta cipelsz magaddal, de még nem kezdted el?**

(1) SQL CTE-alapú, vállalati Master Data Management (mint egyetlen megbízható, konszenzusos igazságforrás)  
(2) Adatvizualizálás algoritmizálása, hogyan lehet automatikusan a legerőteljesebb vizualizációt elkészíteni.  
(3) Generative-AI modeling projektek, mind külső zárt modellek esetére (pl.ChatGPT), mind nyíltsúlyú modellek esetére (pl.Mistral): a RAG-on túli világ felfedezésére.  
+1 Kideríteni, publikálni, hogy szerintem hogyan kellene a leggazdaságosabban, leggyorsabban, legnagyobb élvezettel megtanulni angolul, ha a nyelvtudás eszköz és nem cél.

**05. Ha egy kolléga téged szeretne „feltörni” mint kódrendszert, hol kezdene?**

Legnagyobb sikerrel akkor járhatna, ha beszéltetne. A gyengeségem, hogy hajlamos vagyok túlságosan bízni a saját gondolkodási kereteimben – és ezt szóban is nyíltan képviselem. Ez ad lehetőséget a „feltörésre”: beszéltetve, a rendszerem logikája megérthető. Amikor reverse engineeringről beszélünk, akkor bizony sokszor kell az ismeretlen rendszert "beszéltetni", azt példákkal tesztelni, a megoldás megtalálása előtt.

**06. Volt olyan, hogy egy bonyolultabb utat választottál, mert az mélyebb megértéshez vezetett, vagy tartósabb eredményt hozott?**

Volt olyan projekt, ahol inkább írtam egy komplex, validációs pipeline-t gyors fix helyett, mert tudtam, hogy hosszú távon ez hozza a hibamentességet. De ennek a szemléletnek létezik elméleti és gyakorlati megalapozottsága is. A DataOps filozófiája nem zárkózik el az agilis, hatékony, automatizált adatműveletektől, elsőként és jelenlegi egyedüliként, de nagyon erős fókuszt rak a folyamatos, erőteljes adatminőség-ellenőrzésre, -biztosításra. Többet kell dolgozni a minden pillanatban biztosított adatminőségért, mert a garbage-in garbage-out szellemében végtelen nagy kára lehet a cégeknek, hibás adatok révén.

**07. Mi lenne az a hivatás vagy foglalkozás, amiért akkor is lelkesednél, ha nem lenne hozzá státusz vagy címke?**

Nagyon kiváló, talán legjobb, leginspirálóbb kérdés az összes közül. Épp a napokban konstruáltam magamnak ilyen szerepkört / TAG-et, a kérdéstől függetlenül is: AI Formalization Engineer. A sztori nem intézhető el 1-2 mondatban, így erről részletesebben írok majd a Medium weboldalon is, de dióhéjban: a dolog gyökérzetében két motíváció van:  
(1) Napjaink adatipari munkavállalójának fel kell tudni készülnie az AI-val való versengésre, amikor az ember tudhat jobb lenni, legalább egy darabig, az AI-nál.  
(2) Minden határon túl nagyon nagy igény van a white box gondolkodásra. Hiába elég sokszor a black box, lassan többször van szükség a white-verzióra.  

**08. Volt olyan „hiba”, ami végül új irányt nyitott? Amit akkor kudarcnak éltél meg, de most hálás vagy érte?**

Sokáig hittem, hogy SQL-alapú megoldások mindig jobbak. De egy ponton rájöttem: a procedurális eszközök néha jobban illeszkednek. Ez megtanított arra, hogy ne ragaszkodjak többé dogmatikusan a kedvenc eszközeimhez.

**09. Milyen érzetet, benyomást adsz, amit egy AI nem tudna hitelesen reprodukálni?**

Az innováció, az out-of-the-box gondolkodással együtt, úgy motíváló, hogy értékteremtő. Egy-egy jó vicc/poén mögött is, húzódhatnak ilyesmik. Egy másik ilyen az analógiaképzés, főleg annak erőteljes verziója.

**10. Mi lenne az a mondat, ami ott lehetne a profilképed alatt évekig, és mindig igaz lenne?**

A context-switching a tett halála – a koncentráció a siker motorja.

**11. Volt olyan adatprobléma, ahol az adat csak tünet volt, és a gyökérok emberi viselkedésben, döntésekben rejtőzött?**

Az adat önmagában nem a valóság, hanem annak egy emberi szűrőkön átszűrt, sokszor hibás tükröződése. 
Az adat nem mond igazat, nem a gyökérok, pusztán csak tünet és az AI, bármennyire segít is, nem mindenható.
Az adat olyan, mint egy árnyék – informál a tárgyról, de nem maga a tárgy. Ha elég a napfény, felismerjük a formát, ám, ha sötét van, vagy torz a fényforrás, megtéveszthet minket.

Bár a mai világban egyre nagyobb a nyomás a mindent mérni, kiszámítani, algoritmizálni törekvésén, vannak ennek természetes, elvi és gyakorlati korlátai. A gyökérok sokszor emberi döntésekben, percepciós torzításokban van. Az adatok torzulását sokszor nem technikai, hanem pszichológiai jelenségek okozzák: például megerősítési torzítás, társas megfelelési kényszer, vagy épp vakfolt a kérdező oldalán.

Ha adatot elemzünk, mindig érdemes feltenni magunknak négy kérdést:
* Mit nem mérünk? (Mellékhatások)
* Hogyan változik tőle a rendszer? (Visszacsatolás)
* Miért történt egyáltalán? (Gyökérok)
* Tanulunk-e belőle? (Visszamérés)

Probléma-felvezetés: kérdőív-kutatások alapvetően két nagy csoportba oszthatók: megengedett a szabadszöveges válaszolás avagy nem. Nyilván könnyebb feldolgozni azokat a kitöltéseket, ahol nincs szabad szöveg, viszont kvázi 100%-ban a szabad szöveges vélemény több, hasznosabb információt jelezhet, amire a kérdőív kutatók a legnagyobb jószándék, legjobb szakmai tudás ellenére sem feltétlenül fognak rákérdezni, óhatatlanul is.

Pozitív példa a mérhetőségre, dr.Helen Fisher személyiségmodellje, amely biológiai alapokon, validált (400+ kérdéses) teszttel, a motiváltság, a szegmentálhatóság kivételesen jól találkozik.
- Az emberek szeretnék kitölteni, sőt van aki fizet is érte, hogy kitölthesse, így motíváltak is az igazság feltárására, a torzítás elkerülésére.
- Az emberek intuitívan elfogadják, sőt örömmel azonosítják be saját csoportjukat, magukra ismernek, örülnek neki (kiváló csoport-koherencia révén)
- A modell jól elkülönülő csoportokat képes feltárni.
- Sok csoportosítási/klaszterezési projekt örülne ennyire erős kimenetnek.

Negatív torzító ellenpéldák a mérhetőségre: boldogság, ösztöndíjak, tudományos pályázatok, zenei versenyek. Barabási Albert-László Siker című könyvében rámutatott, mennyi inkorrektség és probléma van az ilyen versenyek mérhetőségével, összehasonlíthatóságával. Noha például zenét illetően, a zenei iskolák alapszinttől a legmagasabb szintekig tudnak kiválasztani zenészt tanítani, fejleszteni, hagyományos érdemjegyet adni nekik, azaz mintha működne a mérhetőség. 

Az AGI körüli viták is azt mutatják: még a definiálás is vitatott – hát még a mérés és az értékelés. Mérni mindenáron? Nem mindig lehet – és nem mindig érdemes.

**12. Mikor tanultad meg, hogy a kommunikációs félreértés nem mindig a hallgató hibája?**

Már szakmai indulásom előtt is – részben a habitusomból fakadóan ez alapélményem. Az egyik legkorábbi igazán nagy felismerés az volt később (korai szakmai tapasztalatként), hogy a félremenés sosem egyoldalú. Minden érintett tehetett volna többet a jobb eredményért. Kvázi mindig "kettőn áll a vásár", minden érintett szereplő tudhatott volna korábban többet, jobbat, mást tenni, a közös, jobb eredményért. Nincs olyan, hogy bárki egyedül viszi el a balhét illetve valaki más meg érvényesen "kidumálja magát" tereléssel, fedősztorival, stb.

Elég hamar kialakult nálam az az attitüd, filozófia, hogy  
(1) Követelményként tekintek minden dialógusnál egy konszenzus-állapothoz való konvergálásra. Még ha ez csak a konfliktus tényszerű rögzítését is jelenti.  
(2) Minél vastagabb a ismeret/tudás illetve konszenzus alapzat a beszélgetők között, annál mélyebb, messzibbre vivő dialógust képesek folytatni. Tudás/ismeret nélkül illetve hisztéria közepette nem lehet beszélgetni.  
(3) Sosem szabad első benyomás alapján ítélkezni, még a legegyértelműbbnek tűnő helyzetben sem. Kell - legalább minimális - időt szánni a beszélgetőpartner hátterének, mondandójának, motívációjának megértésére.  

Ha valaki beszélgetésben nem törekszik a másik megértésére, akkor hogyan akar megérteni ügyfelet, annak igényét, aki jövedelmet termelne a vállalatnak. Az ügyfél megértése ott kezdődik, hogy előbb egymást próbáljuk megérteni.

**13. Mikor érezted azt, hogy „ez itt nem adatvezérelt, csak adatpúder”?**

Először tisztázzuk mit értek "adatvezérelt" alatt. Azt, amikor nemcsak gyűjtjük az adatokat, hanem értelmezünk, elemzünk, értéket kristályosítunk ki valamilyen konkrét forma mentén, visszamérünk, változásokhoz dinamikusan alkalmazkodó workflow(-k) keretei között, egy vállalati adatstratégia részeként, aminek a végén több-kevesebb vállalati döntés automatizálható lesz. 

Adatpúderről meg akkor beszélhetünk, amikor tipikusan már az adatvezéreltség akár legelső lépésén sem sikerül túljutni. Amikor az adattárházépítésnél a változásmenedzsment költségei elszállnak, és megbénítják a projektet. Magyarán amikor nem lesz sikersztori a nap végén, maximum szigetszerű részeredmények lesznek felmutathatók csak.

Kezdetben az 'adatpúder' természetes állapot is lehet: 

Szóval kérdésre válaszolva, az adatpúder, kezdetben és pejoratívitásától megszabadítva egy természetes állapot is lehet, és mint ilyen része is lehet projekteknek. Sokszor előbb kell adatot gyűjteni, csak később tudjuk, mi mire lesz jó (ahogy egyébként a való életben is lehet a púder hasznos). 

A gond akkor merül fel, ha rögzül az adatpúder-állapot, a költségek növekedése / elszállása mellett. A dolog nehézsége abban rejlik, hogy az ilyen projektek úgy (voltak) költségesek, hogy nem voltak jövőállók, nem követték elég gyorsan a változásokat, miközben túl sok – gyakran egymásnak ellentmondó – biztonsági, üzleti, üzemeltetési, auditálási stb. követelménynek próbáltak egyszerre megfelelni.

Az adat önmagában nem érték – csak akkor válik azzá, ha információt, döntést, tanulást vagy változást dinamizál.

**14. Volt már, hogy egy új AI-eszköz vagy trend nagyon csábított, de mégis inkább egy régimódi, de robusztus megoldást választottál?**

Számomra, a legemlékezetesebb módon, és az első pillanattól kezdve, a trillion-dollar AI-cluster hype-ja - már bőven a 2024.decemberi Deepseek V3 előtt is - inkább riasztó volt, semmint inspiráló – és azóta sem győzött meg. 

Pedig ez a mai napig tartja magát Sam Altmannél is (OpenAI), Elon Musknál is (xAI). Az utóbbi a 200.000 GPU-s Colossus-át a hírek szerint 1.000.000-ra akarja felhízlalni, merthogy az Oracle-nek is van kb. ennyi GPU-ja. 

Ugyan algoritmus-elméletben van olyan, amikor a brute force műveletigényű algoritmusok optimálisak lehetnek, mert bármilyen változtatási kísérlet költségesebbé válhat, például naiv stringkeresés (brute force substring search), értelmes méretlimit mellett nyilván. Azonban 99%-ban mindig megéri optimalizálni, mert nagyon jelentős nyereségre lehet szert tenni. 

A Deepseek R2, 1.200 milliárd paraméterrel, home pc-n is futtatható lokálisan (mégha kell is hozzá a legerősebb elérhető NVidia GPU-kártya), miközben Elon Musk Colossus-a 100.000 darab Nvidia H100 GPU-val összesen 7 milliárd dollárba került – ebből 4 milliárd maga a GPU, amihez általános performancia szintjén a Grok2 még el is maradt a Deepseek mögött.

Összegzésként arra számítok, hogy a nagy AI-csatározás nem a nyers GPU-kapacitáson, hanem az optimalizált teljesítményen és az algoritmikus intelligencián fog eldőlni. A jövőt nem a legnagyobb klaszterek, hanem a legokosabb architektúrák fogják nyerni.”

**15. Milyen „belső szoftvert” szeretnél átadni egy juniornak, amit nem a Stack Overflow-n tanul meg?**

**Senior Data Engineerként** azt adnám át, hogy például CTE-k (=Common Table Expression) segítségével rendezett, jól strukturált SQL-ekkel dolgozva... (ami nem ömlesztett betűhalmaz, spagetti kódban), könnyebben lehet fejleszteni, továbbjutni, változásmanagement-et csinálni hosszabb távon is, és a céges Data Governance-t is megtámogatni.

**Senior Data Scientistként** azt próbálnám meg átadni, hogy egyrészt a domain-független Data Science-nél (mint a Kaggle-versenyek is sokszor), sokkal-sokkal erősebb potenciállal bírhat a domain-specifikus változat:
* fel kell tudni ismerni a potenciális értékeket, tudni kell azokat priorizálni
* meg kell érteni rendesen az üzletet, az igényeiket, amit kiszolgál a Data Scientist.
* időben a triviálisnál távolabbra kell tudni látni bármilyen gyorsan pörög fel a világ, 
* kell tudni, költséget, hasznot, kockázatot, erőforrásigényt, kapacitást, függőségeket, ütemezést, kivitelezési símaságot elemezni hozzájuk
* vállalati adatstratégiába, folyamatokba való minél zökkenőmentesebb illeszkedést meg kell találni 
* a fentiek megkövetelik az életciklus-tervezést, a változási pontok (change point) meghatározását, és az igények jövőállóságának, változástűrésének értékelését is.”

**Senior Python fejlesztőként** arra helyezném a legfontosabb fókuszt, hogy egészen más otthoni magányban kis Python programokat magunknak írni, mint vállalati folyamatok keretei között működő és üzemeltethető szoftvert fejleszteni.
