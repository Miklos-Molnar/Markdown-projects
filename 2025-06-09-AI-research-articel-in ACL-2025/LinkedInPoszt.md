HÍR:  
* Az Intology AI által fejlesztett Zochi történelmet írt: ez az első eset, hogy egy teljesen automatikus, LLM-alapú jailbreaking rendszer önállóan, peer review-n átjutva bekerült az ACL 2025 főkiadványába – a természetes nyelvfeldolgozás egyik legrangosabb konferenciájának long paper szekciójába (**~21%-os elfogadási arány mellett**).  
* Az ArXiv.org-on is olvasható cikk címe: Tempest: Automatic Multi-Turn Jailbreaking of Large Language Models with Tree Search

ELEMZÉS:   
* Lehet érdemes mélyebbre nézni a hírbeli történésnek, hogy precízebben tudjunk értékelni.  
* Az, hogy nem szimplán peer reviewed cikkről van szó, hanem pluszban még egy rangos konferencia fő kiadvány anyagába is elfogadták a cikket a saját jogán, mindenképpen emeli a téteket. Persze minden priorizáló és/vagy válogatási folyamat hordoz némi szubjektívitást – az, hogy egy cikk bekerül egy rangos főkiadványba, nem jelent automatikusan objektív mércén kiválóságot, de ettől még komoly validációs értéke van.  
* Az, hogy fontos a téma - **LLM-biztonság** - az nem lehet kérdés. Ez óriási piros pont a cikk-elfogadáshoz, már a startnál. Az LLM-jailbreaking kutatások nem pusztán arról szólnak, hogy kijátszhatók-e a modellek, hanem arról is, hogy milyen struktúrákon és mintázatokon keresztül támadhatók – ezáltal milyen rendszerszintű sebezhetőségeket hordoznak a jövő AI-megoldásai. A Tempest modell etikus módon ("white-hat") módon demonstrálja, hogyan lehet algoritmikusan feltérképezni az LLM-ek gyenge pontjait.  
* A „**tree search**” klasszikus eszköz az AI történetében (az 1960-as évektől kezdve), de annak alkalmazása iteratív LLM-promptolásra jailbreaking céljából egyedi kombinációt jelent: régi módszer új terepen, ahol a keresési fa már nem játékállásokat, hanem nyelvi prompt-válasz párokat térképez fel, automatizáltan.  
* Mivel OpenAI esetben zárt rendszerekről (is) van szó (pl. GPT-3.5 vagy GPT-4), a modellhez való hozzáférés csak API-n keresztül történik (ahol a jailbreaking kísérletek monitorozottak mert alapértelmezésben tiltottak), így az **iteratív promptolás optimalizálása** nem csak technikailag nehéz, hanem kreatív prompt-engineeringet is igényel – ez önmagában is új kutatási tér. Még tovább menve, ha model-agnosztikus irányba visszük el a fókuszt, az még nagyobb erény lehet a perspektívákban.  
* A Tempest mögött három dolog fut össze: (1) **algoritmikus keresés** (pl. fabejárás), (2) k**ódstruktúra** és (3) **finomhangolt optimalizáció**. Épp azok a területek, ahol az LLM-ek – ha jól használjuk őket – nemcsak válaszolnak, hanem új mintázatokat tudnak feltárni. Ehhez az előzményként végzett agent-alapú adatgyűjtés és summary mára már eléggé kiforrott.  

ÖSSZEFOGLALVA:  
* Az AI/LLM – hűen önmagához – a számára legjobban illeszkedő ösvényen haladt: egy klasszikus algoritmust választott ki, és új kontextusba helyezve optimalizálta azt a saját logikája szerint. Ez az „**evolúciós adaptáció**” gépi megfelelője lehet.

TANULSÁG:  
* Mit üzen ez az AI-sztori a mának és (közel)jövőnek?  
* Jövőt illetően érdemes a **múltban** meglévő ötletekért visszanyúlni, **agent**-ekkel feltérképezni, milyen újrahasznosítható ötletek, milyen potenciállal rejlenek a múltban. Mennyire érdemes erőforrást (időt, számítási kapacitást) égetni rájuk. 
Ez ma már (akár egyenesen elégséges minőségben) rutinfeladat lehet a mai LLM/agent kombinációknak. Így mára már az LLM/Transformer esetben, símán lehet agent-robbanás az ujdonságok terében, az előttünk álló (akár közel) jövőben.  
* Ha még tovább szárnyal a fantázia: az ilyen Tempest-típusú keresési stratégiák a jövő AI-kutatásában a kreatív konstrukciót is szolgálhatják.  
* Régóta várok arra, hogy a matematikában a jól ismert Top-Down stratégiák (mint a Riemann-sejtés tételszintű felülről bontása) mellett megjelenjen egy gépi Bottom-Up szemlélet is: ahol LLM-ek és theorem proverek (pl. Lean) kombinatorikusan generálnak lemmákat, akár ezrekből egyetlen gyöngyszemet kinyerve. Lehet, hogy 999 haszontalan, de egy kulcs lehet a várva várt bizonyításhoz (vagy akárcsak a lemmáknál némileg erősebb tételek bizonyításához). Ez már a „**gépi intuíció**” első felvillanása lehet.  
* A fentiben a legszebb, hogy végig a jóval nehezebb és problémásabb **brute force human-on-the-loop**-ról beszélünk, ugye. El lehet képzelni, hogy, ha az ember belenyúl a folyamatokba, mennyit tudhat tovább gyorsítani. És akkor következő lépcső, hogy pl. DifferenciálGeometria szintű új matematikai területet kéne kreatívitással a "semmiből" létrehozni. De ennyire még ne szaladjunk előre. 🙂  

KONKLÚZIÓ:  
* A Tempest és hasonló megközelítések jól mutatják, hogy a következő AI-robbanás **már nem feltétlenül új modellekből**, hanem az LLM-ek köré épülő, okosabb és célirányosabb használatból – keresésből, adaptációból, optimalizációból – jöhet el. 
* Az Agent-ek és keresőstratégiák kreatív kombinációja az új kutatási hullám zászlóvivője lehet.
