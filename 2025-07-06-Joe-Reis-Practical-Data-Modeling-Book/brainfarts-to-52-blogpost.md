52.Post: **Common Analytical Architectures and Components, Part 1**  
https://practicaldatamodeling.substack.com/p/common-analytical-architectures-and

(1) **WINO** as a zero step and its legitimacy
- The phenomenon of WINO (=Warehouse In Name Only) is at first sight seductively simple: a quick response to business pressure, and sometimes a realistic zero step. It is not only an unforgivable sin, but at a certain level of organisational maturity it is almost a necessity: until there is a common data asset culture and clear modelling principles, this 'powder' can be the first layer of experiential learning.
- But therein lies the biggest danger: that this pragmatic "quick and dirty" first step becomes permanent. The business, meanwhile, gets used to the spectacular dashboards, the BI experience, and the APPARENT success preserves a fundamentally weak, ad-hoc architecture. Thus WINO - which started out as a transitional structure - becomes not only "bad" but actually a stuck structure, making it difficult to integrate and improve quality later.
- Hence the paradox: a clever compromise in the short term, but in the long term it can become the biggest obstacle to the path of integration and clarity if there is no clear exit strategy.

(2) **Warehouse:** 'for everyone but no one' - and the pitfalls of a monolithic vision
- The data warehouse has often failed by trying to serve everyone at once, so that in the end no one really felt like it was theirs. Data marts, on the other hand, provided local proximity, quick profits and a sense of "owning your data". This alone is a clear reason why they became more popular.
- However, some of this criticism is simplistic: not all warehouse projects failed - there are many successful examples, especially where there was strong business commitment and governance. Rather, the problem was that warehouse projects often tried to cover the whole organisation with a preconceived definition, while business issues changed faster than the models could be updated.
- Moreover, monolithic architectures are not only expensive, but also poorly responsive to change management: cost and complexity grow exponentially, not linearly. Therefore, warehousing can be understood not as a technological failure but as a vision failure: too static thinking in an ever-changing business space.

(3) Data modelling as a **political act:** who says what is real?
- Data modelling is not just a technical activity: it is actually an imprint of how we think about our business. The warehouse vs mart debate has therefore been partly about who has the right to define what is 'reality'.
- This is a very exciting interpretation, but it also risks over-philosophising: in most organisations, these conflicts are not conscious power plays, but rather organic differences of interest and perspective. Yet, behind the model building there is always the political question: "who gets to say what the definition of 'customer' is?"
- And sometimes that's not a bad thing: different data marts create parallel realities that can be perfectly legitimate and useful "little truths" from a particular perspective.

(4) **Kimball and the non-compliant dimensions:** legitimate concern or excessive rigour?
- The post also says that Kimball "hated the data mart concept", but this may be inaccurate. Kimball himself considered data marts to be the best tool for fast data access - what he was against was the handling of non-conforming dimensions: i.e. if the same dimension (e.g. customer, product) is modelled differently in different marts.
- This is not just a technical aesthetic: conforming dimensions are the common language of the enterprise. If they are broken, not only is the coherence of the analysis lost, but also the ability to see the same reality.
- In this, Kimball was indeed right: non-conforming approaches are not only maintenance nightmares, but also risk 'conceptual chaos' at the organisational level. So data mart in itself is not a problem - the problem starts when each starts building its own reality, without common definitions.

