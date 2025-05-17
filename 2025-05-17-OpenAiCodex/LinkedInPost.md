Felkaptam a fejem az OpenAI, pár órás, új Codex-bejelentésére.
Több AI-ügynök dolgozik ugyanazon a kódbázison? Git-merge konfliktusok nélkül? Ez elsőre meglepőnek tűnhet.

Amit a Codex koncepciójából leszűrök:

* **A git-merge problémák kezeltek**: az ügynökök feladatokra bontva, elkülönítve (sandboxban) dolgoznak. Az eredményük pull requestként érkezik, nem írnak közvetlenül a főágra.  

* Az agentek nem általános AI-ok, hanem **toolformer-alapú szakosodott „eszközhasználók” – fejlesztői toolchainekkel dolgoznak**, így célzottan és kontrolláltan lépnek be a fejlesztési folyamatba.  

* Értelmet nyer a Windsurf felvásárlása: a Windsurf mostanra készült el a **self-hosted AI coding stack**-jével, amely lehetővé teszi a vállalati kód helyben tartását, elemzését és módosítását.  

* A Codex ezzel szemben a **felhős, együttműködésre tervezett oldal**: a kettő kombinációja egyesíti a privát kontroll és a kollektív hatékonyság előnyeit.  

* A szinergia lényege:
A lokális (privát) és felhős (csoportos) fejlesztési modellek eddig alternatívák voltak – most egymást kiegészítik. **A fejlesztés így gyorsabb, jobban skálázható, és biztonságosabb lehet.**  

* A valós probléma: a kódbázis fokozatos elhasználódása.
A tapasztalat azt mutatja, hogy a módosítások többsége (akár 90%-a) hosszú távon szuboptimálissá teszi a kódot, mert minden fejlesztő más kontextussal és fejben más struktúrával dolgozik.  

* Az AI-val támogatott fejlesztés célja: a folyamatos szerkezeti optimalitás.
A Codex ígérete szerint a rendszer agilis módon, automatikusan fenntartja a kód minőségét – és **elméletileg ezzel hosszú távon a merge-konfliktusok gyökeres csökkenését is eléri.**  

* Fontos különbség: nincs automatizmus-mánia.
A merge-et továbbra is ember vagy CI/CD automatizmus végezheti – ez már nem az agentek dolga, hanem a DevOps szint része. De a cél, hogy **a rendszer fokozatosan az önkarbantartás irányába fejlődjön**.  

* Nincs varázslat: **csak hatékonyabb workflow**.
A hangsúly a folyamatok átalakításán van – hogy **a konfliktusok előre csökkenthetők legyenek, anélkül hogy elveszne a fejlesztés rugalmassága**.  

* A vide-coding új szintre lép.
Itt már nem prompt-alapú szöveges kérésről van szó, hanem a teljes kódbázis kontextusában végzett, strukturált AI-fejlesztésről. Az ügynökök valóban „belelátnak” a projektbe, és úgy dolgoznak rajta.  

* **Nem kell többé a context window méretén és a hallucinációkon aggódni**.
A rendszer háttérben indexel és reprezentációkat épít – így nem szükséges minden információt manuálisan belesűríteni a promptba.  

* **A fő ígéret:**
Nem csak gyorsabban kódolhatunk, hanem AI-kompatibilisen máshogy is – mintha maga a kódbázis tanulna együtt velünk. **Ha a Git volt a nyelvtan, most az AI a stilisztika.** És együtt végre gördülékenyen beszél a csapat – a kód nyelvén.  

https://www.reddit.com/r/ChatGPT/comments/1ko3tp1/ama_with_openai_codex_team/    
