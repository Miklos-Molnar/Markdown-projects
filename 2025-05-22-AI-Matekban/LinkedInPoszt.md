AI a matematikában

Több független paraméter mentén elég vadul szétágazik a téma – már ha csak a matematikára koncentrálunk, akkor is (és akkor még hol van a fizika):  

* Olyan problémát szeretnénk kezelni, amelyre az emberiségnek már létezik legalább egy ismert megoldása, avagy olyat, amely továbbra is nyitott (gondoljunk például a Riemann-sejtésre)?  

* Programozható formában adnánk inputot (pl. Lean, Coq, Wolfram), vagy inkább természetes nyelvű szabad szöveggel dolgoznánk?  

* Elméleti matematikusként inkább human-in-the-loop módon iterálnánk az AI-jal, vagy van egy konkrét feladat (pl. egy differenciálegyenlet), amit megoldásra adnánk át? Azt már fel sem merem vetni, hogy human-on-the-loop megközelítés érdekelne-e minket – ebben mostanában a kínai kutatók gurítottak nagyot az **AZR**-rel (Autoformalization via Retrieval), ami elég komoly jövőképet villantott fel.  

* Milyen nehézségi szint a cél? Általános iskolai szint? Nemzetközi tudományos diákolimpiai feladatok (IMO, IPhO)? Vagy ezeknél is komolyabb, kutatási szintű problémák?  

* Ingyenesen és nyilvánosan elérhető modellekkel dolgoznánk, vagy inkább becsatlakoznánk egy kutatási projektbe, akár zárt infrastruktúrával?  

Ha valódi újdonságot akarunk az AI-jal, az a terület még eléggé gyerekcipőben jár – főleg ad hoc, egyedi megközelítésekkel. A Google DeepMind valóban elért néhány említésre méltó eredményt ezen a téren. Például a **FunSearch** projektjükben mesterséges intelligenciával fedeztek fel új struktúrákat egyes kombinatorikai problémákban – igaz, ez nem formális bizonyítás, hanem kreatív példagenerálás volt. A Qubit is írt róla, azaz megjelent még a magyar mainstreamben is.

Frissebb hír az **AlphaEvolve**, ahol a régóta ismert evolúciós algoritmusokat vetik be kreatív felfedezések támogatására.

A jelenlegi tudásom szerint a DeepMind **AlphaProof** és az **AlphaGeometry** (korábban Geometry2 néven ismert) állnak legközelebb ahhoz, hogy magas szintű matematikai problémákat – akár olimpiai feladatokat – közel 100%-os pontossággal oldjanak meg.

Sokan szkeptikusak abban, hogy klasszikus LLM/Transformer architektúrával ez a probléma „feljebb tekerhető”. Az architektúrából ugyanis hiányzik a grounding, vagyis a fogalmak belső jelentéshez kötése. Ezért is látni, hogy a DeepMind vegyíti a neurális modelleket régi, de robusztus formális módszerekkel – más néven **GOFAI** (Good Old-Fashioned AI) megközelítéssel.

Ami a **Nemotron** modellt illeti: Transformer és **Mamba** hibrid architektúrára épül, épp azért, hogy hosszabb kontextust és stabilabb működést nyújtson, kevesebb erőforrással. A benchmarkjai valóban erősek, de jelen állás szerint főként általános iskolai szintű matematikai feladatokra alkalmas. Pozitívum viszont, hogy a fizika területén is alkalmazható – különösen, ha digitális ikrek vagy fizikai szimulációk érdekelnek.

Egy további gyakorlati szempont: a Google DeepMind modelljei (pl. AlphaCode, AlphaGeometry) jelenleg nem hozzáférhetők sem nyíltan, sem pénzért. Csak szűk kutatási együttműködések révén lehet belépni. Ezzel szemben az **NVIDIA Nemotron** modellek nyilvánosan elérhetők az **NGC platformon**.
