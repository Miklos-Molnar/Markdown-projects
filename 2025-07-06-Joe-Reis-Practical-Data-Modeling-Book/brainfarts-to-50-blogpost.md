50.Post: **Just-In-Time Data Modeling**  
https://practicaldatamodeling.substack.com/p/just-in-time-data-modeling

(1) Extension of JITDM with **JIT mental modelling**  
JIT can be applied not only to data modeling, but also to our thinking. As stated in the post: “focus on doing just enough to solve today's problem” — in the same way, when thinking, we often put together explanatory or decision-supporting mental models “just in time”: we don't always need a complete, definitive map in our heads. In other words, in addition to JITDM, it is also possible to build a clever little mental JITTM=Just In Time Thinking Model.  

**EXAMPLE**: An ad hoc business question arises:
* “Can you tell me how our new feature affects churn among recently joined users, but only on mobile, and only among loyalty program members?”  
* What would happen with the old BDUF (Big Design Up Front) way of thinking:  
– You start designing a complete churn model, user segments, and feature store.  
– You map out all possible data connections, attributes, and variants.  
– It takes 3–4 weeks to come up with a large, theoretically complete model.  
* What happens with a JITDM-like mental model:  
– You don't make a grandiose plan.  
– You just think through the following:  
(a) What specific attributes do I need for this right now?  
(b) What is already in the existing data?  
(c) What is missing?  
* How can I detect this with a quick rule-of-thumb filter and mini-connection?  
– Immediate sketch: churn, entry date, loyalty flag, device type → you can already see that this requires about 3-4 tables.  
– Quick SQL, notebook, dummy model.  
– You notice that, for example, the loyalty tag status is not stable (it can change every two weeks) → the time dimension is already included in the mental model.  
* For a specific solution, the “just in time” mental model helped:  
– what exactly are you calculating (churn rate),  
– where exactly do you get it from (tables, attributes),  
– how exactly do you validate it (you run it on a subset).   
* It is not a “big theoretical” brain training, but a concrete on-the-fly problem-solving routine. This way, you get a first answer in days, not weeks. If it becomes important, it can be formalized later.   

(2) Extension of JITDM with **JIT storytelling/CoT**  
But we can not only use the mental model to implement JITDM, but also, for example, with an explanatory narrative to stakeholders.  

(3) As an **analogy, a soccer coach (and team manager)** may have a long-term strategy, but if the team quickly loses even two games in reality, the coach will be fired, regardless of his “excellent” 3-year plan.  
* The same is true for modern data modeling. No matter how beautifully designed, factory-made (industry) “universal” model it may be, which is terribly expensive and grandiose and also comes with a straitjacket – business wants answers yesterday.  
* This is why Just-In-Time Data Modeling may be necessary: not because we don't want to plan, but because the field is constantly changing. Sometimes, rapid re-planning is not a luxury, but a matter of survival.  

(4) JITDM/**JEDMO** (thx to comment) as a form of piloting — a concept that is crucial in the age of AI — inevitably raises governance considerations as well. Governance can be seen as “slow care” behind rapid models. JITDM/JEDMO can be seen as the discovery phase, and governance as the stabilization phase. These are not mutually exclusive, but complementary:  
– First, a “just enough” model is created that works.  
– If it works, governance helps to integrate, scale, and avoid chaos (duplication, drift, redundancy).  
* Governance can also be a practical gate.  
– If a model survives for more than X months or is used by Y number of users/teams, review and documentation are mandatory.  
– This does not slow down the initial iteration, but ensures that “too successful” models do not remain unowned guerrilla models.  
* Governance can also be “just enough.” You don't need a full metadata catalog, data steward, or 200-page specification right away. “Just enough governance” may be sufficient: e.g., convention, a few mandatory fields, version control.  

********************************************************************************

50.Post: **Just-In-Time Data Modeling II.**

When we talk about Just-In-Time Data Modeling (JITDM), the discussion often stops at “do less upfront.” But the real power is subtler: it’s about **building data models that are closer to how we actually think about problems**. Instead of designing grand, abstract schemas weeks in advance, we sketch just enough structure to answer today’s question. This mindset shift changes more than the scope of modeling — it changes its very shape and philosophy.  

**Time** should be a first-class citizen, not a passive column  
In classical modeling, “time” often shows up as a simple created_at or updated_at field. This reframes data models from static snapshots into living, versioned hypotheses. But in reality, what keeps our data alive is change: events, updates, versions, lifecycle stages. In JITDM, time becomes active:  
– We treat it as a dynamic axis of evolution.  
– We plan for time-aware fields (e.g., status_history, price_changes).  
– We sketch models assuming data will drift, grow, and change meaning.  

Why **non-SQL** (time-series, document, or streaming) naturally fits JITDM
* Instead of later patching time-awareness onto a rigid schema, we start from a model that assumes evolution. Non-SQL systems don’t force us to lock the entire schema upfront:  
– Time-series databases make “change over time” a native feature.  
– Document stores let us embed evolving fields, nested arrays, and histories directly. 
– Streaming platforms let the flow itself become part of the model.  

Where **Object-Oriented Databases** (OODB) add another layer
* JITDM isn’t only about how much we model, but also how closely the model mirrors our mental picture. In traditional SQL, we split the world into tables and joins. But often, our mental model sees "Order", "Customer", or "Subscription" as cohesive objects with states and behaviors. Instead of constantly translating between mental and physical models, we keep them close. Object-oriented databases let us:  
– Model real-world entities as they naturally are.  
– Capture nested attributes and historical state changes inside the object.  
– Add new fields or behaviors incrementally as business needs emerge — perfectly aligned with the JIT philosophy.  

A **practical synergy**: JITDM + time + Non-SQL + OODB  
* EXAMPLE: churn analysis prototyping:  
– Start with an Order object holding a status_history array.  
– Store it in a document DB or OODB that doesn’t mind evolving fields.  
– Stream new status updates as events, directly tied to the object.  
– Later, when this model proves critical, we promote it into governed production with proper versioning, documentation, and ownership.  
– The result: immediate answers today, sustainable structure tomorrow.  

Beyond storage: **piloting** as an architectural statement  
* In the AI era, the idea of piloting gains new depth. **Governance** isn’t the enemy of agility; it’s the safety net we deploy when yesterday’s quick fix becomes tomorrow’s core dataset. We’re not only piloting the data pipeline or dashboard — we’re piloting the very shape of our models:  
– Starting small and local.  
– Letting usage, feedback, and drift guide evolution.  
– Treating initial prototypes as living hypotheses, ready to be promoted into governed, shared assets if they succeed.  

**Conclusion:**  
* JITDM, especially when combined with non-SQL systems and object-oriented modeling, isn’t just about “less design.”  
* It’s about modeling closer to reality:  
– Treating time as an active force.  
– Letting structure evolve just-in-time.  
– Keeping mental and physical models aligned.  
– Promoting successful pilots into governed standards.  
* It’s not purely technical. It’s a way to build models — and explanations — that move at the speed of business.  

