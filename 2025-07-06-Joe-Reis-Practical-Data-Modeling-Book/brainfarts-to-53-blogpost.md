# 53.Post：*Common Analytical Architectures and Components, Part 2*
**(Contemporary Architecture Patterns)**  
→ [Original Joe Reis post](https://practicaldatamodeling.substack.com/p/common-analytical-architectures-and-1ad)

# Part 1: The Real Stakes in the Architecture vs. Data Modeling Debate

> **TL;DR:**
> The question of whether architecture or data modeling comes first isn't just a sequencing issue — it's a battle over who defines meaning.
> In practice, architecture tends to lead — not because it's right, but because it's convenient.
> But it *should* be the model that defines the tech stack, not the other way around.

## (01) Let's Get to the Point: The Problem Is Way Deeper Than Reis’s “Mimic” Law Suggests

What comes first — the chicken or the data table?
The architecture or the model?
It’s not a trivial question. And how we answer it says *everything* about how seriously we take data modeling as a strategic practice.

This isn’t just semantics — it’s existential:
Is data modeling a **leading interpretive act**, or just **a technical formality that maps some tables together**?

Because that choice — whether we treat modeling as a first-class meaning-making tool or as post-hoc table plumbing — will literally shape projects, strategies, and the data maturity of an entire organization.

Short answer?
**In reality, architecture usually comes first** — but not for any noble reason. It’s not a principled choice, just a practical shortcut.
Very few teams have the self-awareness or strategic patience to **start with a conceptual model, and only *then* define the architecture**.

## How it really goes today — the all-too-familiar sequence:

1. **Someone picks a platform or tool**
   (“We’re going with Snowflake”, “Let’s implement dbt”, “Looker is our BI layer now”)
2. That decision **implies a whole architectural pattern**
   (batch or streaming, medallion layer, CDC, ELT, Lakehouse, etc.)
3. Then someone finally asks: “Okay... so what kind of model can we fit into this thing?”
4. And now the modeling is done under **compatibility constraints**, not business meaning.

> *“Technology drives the interpretation — instead of interpretation driving the tech.”*

## Why does architecture usually dictate the modeling?

* Because teams want **quick wins** — and modeling rarely delivers those
* Because there's “**no time for modeling**” (yes, that quote)
* Because decision-makers are **tool- or vendor-driven**, not concept-driven
* Because **conceptual modeling isn't flashy** — you can’t demo an EAR diagram to execs
* Because **architecture happens fast** (tools get bought before models get drawn)
* Because **BI/AI/dashboard needs are easier to platform than to explain**
* Because **most orgs aren’t used to conceptual reflection at all**

And that’s why Reis’s Law —

> *“Your data model mimics your architecture”*
> — ends up being true not because it’s inevitable, but because it’s a **self-fulfilling prophecy**.

---

## (02) Joe Reis — The Way I Read Him

Reis’s Law and the idea of architecture-first seem to define the *default universe*.
Am I reading this right? I think I am.

> **“The architecture is already there — let’s now figure out what we can model into it.”**

Let’s break it down:

* **Reis’s Law: "Your model will follow your architecture anyway"**

Joe drops this line like a meme — and memes are sticky for a reason.
It doesn’t feel like he’s pushing back or warning us.
It reads more like: *“this is just how things are, deal with it.”*

> *“Your data model inevitably mimics your architecture.”*

* **He always starts with architecture in his chapter structure**

It’s subtle, but it matters. Modeling seems to come across as an *adaptation*, not a driver.

For example, in the "Common Analytical Architectures and Components" chapter:
– First you get lakehouses, table formats, streaming pipelines.
– Only *then* do we hear: *“you’re free to choose your modeling style…”*

* **Even in his “We Don’t Have Time for Data Modeling” piece**

The model shows up as a sort of *practical fit* into an already defined architecture and data pipeline.

The vibe is:
– How to model within *real-world constraints*
– How to be *pragmatic*, fast, “good enough”
– How to make the model plug into the **toolchain** (dbt, BI, etc.)

What’s *not* being said is this:

> Let the model lead.
> Flip the causality.
> Start from the concepts, then choose the platform.

And *that* silence speaks volumes.

---

## (03) Why Modeling Should Come First — A PDM→LDM Analogy

The architecture-first mindset feels a bit like starting at the **PDM level**, then hoping the **LDM** and **CDM** magically follow.

Let me show you what I mean:

| Conceptual Layer | In a Model                    | In Architecture                            |
| ---------------- | ----------------------------- | ------------------------------------------ |
| CDM              | business concepts, entities   | user intent, semantic domain               |
| LDM              | logical structures            | data warehouse logic, transformation flows |
| PDM              | tables, indexes, file formats | partitions, file layout, storage engine    |

Within modeling, this is totally obvious:

> **You can’t design a PDM without an LDM. And the LDM only makes sense if it reflects a CDM.**

The same logic applies to systems:

> **You can’t build a meaningful architecture without a model behind it.**

If an org picks the platform first (“We’re going with Databricks”)
…and *then* starts modeling...
That’s like saying:

> *Let’s design some indexes and partitions first, and then figure out what the table is supposed to represent.*

That’s insane — and yet that’s exactly how architecture-first decision-making plays out.

---

## A Mature Data Strategy Framework — In One Table

| Phase                             | Key Question                                                  | Core Focus                         |
| --------------------------------- | ------------------------------------------------------------- | ---------------------------------- |
| 1. Conceptual pre-modeling        | What world are we trying to understand?                       | CDM, EAR, semantic mapping         |
| 2. Architecture fit & prototyping | Which platforms can best and accurately represent that world? | architecture comparison            |
| 3. Tech & vendor optimization     | How can we best operationalize that understanding?            | toolchain, automation, scalability |

Architecture should **not** come before modeling — unless your organization *isn’t serious* about learning, understanding, or acting on data.

> **The model doesn’t belong to the tech — it belongs to human interpretation.**

## Why Modeling Should Define the Architecture (Not the Other Way Around)

### 1. **The model gives you the goal — architecture is just the tool**

* The data model expresses **what world you’re trying to represent and make sense of**.
* Architecture expresses **how to serve that world efficiently**.

> So it only makes sense: first ask *“What do we mean?”*, then figure out *“How do we store and move it?”*

---

### 2. **Design-first means less technical debt later**

* If you build architecture first and slap a model on top later, you’ll find out *way too late* it’s rigid, costly, or just wrong.
* If you start with the model, you **only build what you actually need**.
* **Start with conceptual modeling (CDM, EAR, semantic map)**
  * Focus on business entities, core processes, time, events, goals
  * Absolutely critical in greenfield systems — not just retrofits
  * Remember: the model doesn’t describe the tables — it describes *the world*, as the business understands it

> You avoid: redundant layers, overengineering, and useless ETL/ELT spaghetti.

---

### 3. **Conceptual clarity beats technical compatibility**

* If tech leads the way, you’ll end up modeling “whatever fits in Snowflake.”
* But a model-driven approach makes sure your data **is meaningful, not just structured.**
* **Use the model to prototype several architecture options**
* Pilot the conceptual model against different setups:
  * Batch vs. streaming
  * Lakehouse vs. warehouse
  * Kafka, Iceberg, dbt, Airbyte, etc.
* The question isn’t: *“Is it fast enough?”*
  It’s: *“Can this setup faithfully represent our world?”*

---

### 4. **AI & BI systems *need* models built for human understanding**

* Semantic layers, AI interfaces, metrics layers — all **build on models**.
* If the model is tacked on later, these systems will be fragile, fuzzy, or just wrong.

> Good AI needs a **clear, intentional model** — tech just delivers it.

---

### 5. **Less rework, more durable architecture, smoother evolution**

* If the business or platform changes, but your model is solid, you can **swap out the architecture** without losing your mind.
* In this way, the model becomes a *stable API* across all your data systems.

---

### 6. **Only then weigh vendor-specific trade-offs — consciously**

* Sure, pick your preferred vendor — but **not before conceptual clarity**
* Consider things like:
  * Performance characteristics
  * Toolchain compatibility
  * Licensing, governance constraints
* But those come *after* the meaning is nailed down.

---

> **TL;DR:**
> Just like you can’t build a PDM without first having an LDM,
> you shouldn’t build architecture without a model behind it.
> The model defines what’s meaningful — the architecture just supports storing and moving it.
> This isn’t academic philosophy — it’s the foundation of a data strategy that doesn’t fall apart later.

---

## But Wait — Why Doesn’t Modeling Always Come First?
(And how can we still bring it back into focus?)

### 1. **Tech is already in place (Snowflake, Databricks, etc.)**
→ Modeling has to adapt after the fact.

**What to do:**
* Create a **conceptual map** on top of the current structures: map CDM ↔ LDM ↔ PDM.
* Bridge gaps through the semantic layer — `dbt metrics`, `LookML`, etc.

---

### 2. **“No time to model” — business wants data *yesterday***
→ Architecture is quicker to deploy than clarifying concepts.

**What to do:**
* Use **sprint-based modeling**: agile, minimum viable model first.
* Go **progressive**: start with the critical metrics, full CDM comes later.

---

### 3. **Different teams, no shared ownership**
→ Infra team owns architecture, BI team owns modeling → no shared vision.

**What to do:**
* Introduce a **“Model-as-a-Contract”** mindset.
* Treat the model definition as **input into infra specs** (model-driven provisioning FTW).

---

### 4. **Legacy architectures constrain you**
→ Already using Data Vault, SCD2, streaming ingestion, etc.

**What to do:**
* Use the model to **re-interpret your layers**
* Redefine the “gold layer” *through* the semantic layer.

---

## Quick Recap

| Perspective          | Model → Architecture     | Architecture → Model             |
| -------------------- | ------------------------ | -------------------------------- |
| Cost                 | Only build what’s needed | Risk of overengineering          |
| Flexibility          | Easy to change meaning   | Expensive to switch platforms    |
| Meaning & Context    | Clear, interpretable     | Risk of distortion or redundancy |
| Common in real life? | Rare, but growing        | Still the default unfortunately  |

> **Architecture is the body, the model is the meaning.**
> And data systems are only truly effective if they have **meaning — not just muscle.**

---
## (04) This Isn’t Just Theory — Modeling-First Can Actually Work
Now that we’ve talked about *why* starting with modeling makes sense,
let’s ask the next big question:

**Can you actually do this in the real world?**
Let’s look at what a modeling-first strategy might look like *in practice*.

Can you *really* start with modeling and pick the architecture later — all within a reasonable timeline?

**Short answer: yes, it’s absolutely doable.**
But only if the organization is willing to lead with **concepts, not platforms**, and consciously invest a little up front (just a *focused* bit, not months of overhead).
This isn’t a utopian dream — it’s a **realistic strategy**, especially for complex or greenfield initiatives.

---

### 1. **Conceptual modeling is about meaning, not mechanics**
You don’t need heavy entity lists or 900-row spreadsheets.
What you *do* need:

* Clear business goals
* Context + time dimensions
* Events vs. state representations
* Decision-making logic & feedback loops

*You can do this in 2–4 workshops. Not months. Not waterfall.*

---

### 2. **Test (or at least simulate) multiple architectures**

Take the *same conceptual model*, and try fitting it into different setups:

| Scenario                                | Architecture to Test            |
| --------------------------------------- | ------------------------------- |
| Event-driven logic + AI prediction      | Kafka + Iceberg + Feature Store |
| Slow change, retrospective analysis     | Snowflake + dbt + Power BI      |
| Real-time alerts + operational feedback | Flink + Materialize + Grafana   |
| Metadata-centric, controlled domains    | Data Vault + CDC + Looker       |

You’re not chasing “the perfect setup” — you’re aiming for **minimum viable compromise**.

---

### 3. **Choose based on *functional fit*, not industry hype**

When comparing options, use these real-life filters:

| Criteria                    | What to Compare                                      |
| --------------------------- | ---------------------------------------------------- |
| Model fit                   | Can it reflect the core concepts well?               |
| Performance vs. flexibility | Where do we need scale vs. nuance?                   |
| AI + BI compatibility       | How well can humans and machines co-interpret data?  |
| Governance complexity       | Where are the audit & compliance hotspots?           |
| Lock-in risk                | If we need to change tools, what’s the blast radius? |

The architecture you end up with may not be the trendiest,
but it will be the one that actually *makes sense*.

---

# Part 2: The Reis’s Law Distortion
(*A practical guide to managing modeling in a platform-first world*)

> **TL;DR:**
> Even if the architecture came first (it often does), it’s not game over.
> With a conceptual safety layer, modeling sprints, and tech-neutral framing,
> you can **recenter the model** — even in a vendor-led environment.

---

## (05) When the Order’s Already Reversed — How to Handle the Reis Effect (7 Tactics)
Here’s what you can do in an architecture-driven setting:

---

### 1. **Early conceptual safety layer (CDM or EAR-style pre-modeling)**

> *“Model meaning first, not data.”*

* Kick things off with a **non-technical conceptual model** — even a napkin sketch counts.
* Use an **EAR diagram, business object map, or semantic canvas** — *before* picking any tools.
* This flips the dynamic: the platform becomes *an instrument*, not *the author* of your data logic.

---

### 2. **Run modeling sprints in a platform-neutral space**

> *“Tech comes second.”*

* Build a **modeling backlog** — full of questions about meaning, not columns or tables.
* Run **iterative workshops** where SQL and dbt are *off the table*.
* Have a dedicated *"meaning-first sprint"* — no platform names allowed.

---

### 3. **Do architectural reflection mapping**

> *“Don’t swallow the architecture whole — interrogate it.”*

* Map out what the architecture is *forcing* onto you.
* Pair that with what you *actually want* to model.
* This gives you a **reflection matrix** — a visual to expose subtle distortions in meaning that creep in unnoticed.

---
### 4. **Semantic contrast design**

> *“Put the mapped world and the understood world side by side.”*

* Take a core concept (say, *“customer”*) and give it two different lenses:
  * “What does the platform see?” (e.g. 7 source systems, 14 attributes, 3 IDs)
  * “What does the business mean by it?” (e.g. context, lifecycle, relationships)
* This creates a **contrast pair** — and any mismatch *reveals distortion* you probably weren’t aware of.

---

### 5. **Data modeling personas — context-aware thinking**

> *“Who uses what — and why?”*

* Don’t model for architecture — model for **people’s goals** (BI user ≠ AI agent ≠ Ops team).
* Each element in the model should carry **intent, function, and value** behind it.
* This reframes the platform's constraints — and gives you a human compass.

---

### 6. **Dual modeling — logical & physical in parallel (not sequential)**

> *“Don’t model after the tech — model alongside it.”*

* The logical and physical model shouldn’t be in a hierarchy — they should **talk to each other**.
* For example: when defining a partitioning strategy in an Iceberg table, ask:

  *“Why are we partitioning by time?”*
  *“Why by customer?”*

  → These decisions feed back into the business logic itself.

---

### 7. **Human-in-the-loop AI model assistants**

> *“If we’re going to use AI, let’s make it ask questions — not just write code.”*

* Use copilots or agents to **generate model variants** — but make sure *humans* interpret them.
* These tools can function like a *Socratic modeler* — asking, nudging, exploring — **not dictating**.

---

## Still Worth Saying Out Loud:

The Reis-style distortion isn’t just technical — it’s *epistemological*.

> “The platform decides in advance what you’re even allowed to see.”

That’s why we need modeling practices that **start with meaning** — and only *then* look for technical implementation.

---

## (06) Inmon / Kimball / Data Vault / Anchor — What the Past Still Teaches Us

---

To really understand today’s modeling choices, it’s worth revisiting some of the classics.
They’re not just history — they still offer **practical lessons for modern data strategy**.

---

If we want to include these in a final modeling landscape or comparison table (as we did in Part 1), we need to ask:
Should they be standalone model types, or just design philosophies?

The short version:

> *Kimball* and *Inmon* aren’t model types — they’re **schools of thought**
> at the LDM/PDM boundary, with different ways of structuring and using the model.

---

### **Inmon** *(mid-to-late 1980s)*

* Originator of the “Corporate Information Factory”
* Strongly **normalized**, enterprise-wide integration focus
* Starts with a **3NF central warehouse**, then adds data marts
* Emphasizes **logical/physical separation**

---

### **Kimball** *(early-to-mid 1990s)*

* Response to Inmon’s perceived heaviness: **bottom-up, business-first**
* Works on the LDM/PDM edge (Star Schema, Fact + Dim tables)
* **Usage-optimized**, designed for query performance
* Strong dimensional modeling, denormalized, OLAP-friendly

---

### **Data Vault (Linstedt)** *(late 1990s, public in early 2000s)*

* Aimed at solving rigidities in Inmon/Kimball and capturing history
* Focuses on **auditability**, **historical tracking**, and **change resilience**
* Structure: **Hubs (business entities), Links (relationships), Satellites (attributes)**
* Still LDM-ish, but tightly coupled to **integration and traceability**
* Designed for schema evolution + governance compliance

---

### **Anchor Modeling** *(public since 2009, roots in early 2000s Scandinavia)*

* Academic origin, focused on **flexibility and abstraction**
* Built around **schema evolvability** and **atomization**
* Tables are **extremely granular** — every variation in its own entity
* Native support for **versioning**, like a time machine
* Highly **model-centric** and **abstraction-first**, but less “business-ready” out of the box

---
## (07) OLAP / MOLAP – A Historical Side Note, But Still Worth It?

This one's a spicy topic. When it comes to OLAP/MOLAP, we’re in a **liminal zone**:

**Not fully dead**
**But definitely not in the “live innovation” camp anymore**
**“MOLAP Never Died — It Just Dissolved Into Your Semantic Layer.”**
**“A Semantic Layer Without OLAP Is Just an Illusion of Governance.”**

---

### So… why should we still care?

---

### 1. Because it’s *still* a reference point for modeling practices

* The whole idea of **dimensional modeling** (Star Schema, hierarchies, pre-aggregates) comes straight out of this tradition.
* MOLAP was the **first real implementation of precomputed, governed metric logic** — and now it's resurfacing in tools like **Looker, dbt metrics, semantic layers**.


### 2. Because it's *still* alive — just in niches

* Finance, controlling, planning, structured low-granularity reporting
* Think: SAP BW, Oracle Essbase, TM1, Microsoft SSAS (Multidimensional)

### 3. Because it still *teaches us something*

* What does it mean when a system actually *contains business logic*, not just data storage?
* What happens when **model logic determines what can be asked** — not the other way around?

---

### Why isn’t it future-proof?

---

### 1. Because it’s *closed and rigid*

* Tough to scale for new use cases
* No schema-on-read, poor data fluidity
* AI, ad hoc querying, fuzzy questions? Nope. Not friends.

### 2. Because it’s *not born for distributed systems*

* Not cloud-native
* Heavy reliance on precomputes → long refresh cycles, high cost to reprocess

---

### So what should we do with it?

Let’s **include it in our modeling table**, but *with context*.
Why? Because OLAP/MOLAP is a **weird hybrid**:
* Part **modeling style**,
* Part **execution architecture**,
* Part **consumption optimization pattern**.

---

### Modeling Strategies and Implementation Philosophies Across the LDM/PDM Axis

Think of OLAP/MOLAP as a **cube-based, pre-aggregated logic layer** — ideal for:
* “OLAP-style PDM-centric consumption models”
* Very **client-facing**, **query-performance-driven**

It’s distinct from the more flexible Kimball Star Schema world, and that’s a good thing.
It **honors the historical legacy** without creating redundancy — and helps clarify the difference between:

> **“Models optimized for consumption” vs. “models optimized for structure.”**

---

| Modeling Approach     | Logical (LDM)    | Physical (PDM)                         | Why It’s Here                                                       |
| --------------------- | ---------------- | -------------------------------------- | ------------------------------------------------------------------- |
| Inmon (3NF)           | Strong focus     | Often implemented physically           | Clear split between logic and physical layer                        |
| Kimball (Star Schema) | Implicit         | Strong focus                           | Star schema is deeply physical, performance-oriented                |
| OLAP / MOLAP (Cube)   | Implicit logic   | Very strong PDM focus                  | Pre-aggregated, precomputed, cube-based. Highly consumption-focused |
| Data Vault            | Structure-driven | Implementable but logically formulated | Starts as LDM (hubs/links/sats), lives in physical conventions      |
| Anchor Modeling       | Extreme LDM      | Auto-generatable PDM                   | Philosophy is pure LDM, but meant to script out the physical model  |

---
## (08) Missing Architectures in Joe’s Chapters

---

### **Event-Driven Architecture (EDA)** – *Missing in name, but quietly present*
Joe talks quite a bit about **streaming systems** — Kafka, Flink, Pulsar, ksqlDB, and so on — but he never really names the underlying philosophy: **EDA – Event-Driven Architecture**.

That’s a bit of a blind spot, because:
* **Streaming** is a technical mechanism (*how*), while **EDA** is a conceptual and architectural stance (*why* and *what*): we think in *events*, not in *entities*.
* EDA is *not just data delivery* — it’s a full-blown logic for organizing systems and domains (CQRS, Event Sourcing, DDD).
* What's missing is the **modeling impact** of choosing *events* (rather than *states*) as the base unit of meaning.

> *"Data modeling is not just storage logic — it’s how we conceptualize the world."*
> EDA flips the script: an *event* is **not just a change** in state — it *is* the elemental reality.

---

### **Time Series Databases (TSDBs)** – Totally missing

Joe does emphasize the importance of time when discussing streaming: *event time vs. processing time*, etc.

But he skips over a whole family of systems designed **explicitly around time**, such as:
* **InfluxDB**
* **TimescaleDB**
* **Amazon Timestream**
* **OpenTSDB**
* Or *Prometheus* — on the metrics side

**Why does this matter?**
* In **TSDBs**, time is not metadata — it's the **primary index**, **query axis**, and **aggregation base**.
* This fundamentally changes the *modeling mindset*:
  You’re not modeling *entities* and *relationships*, but **measurements over time** and **query windows**.
* Architecturally, they also rely on **different storage optimizations**: time-based compression, rollups, interval chunking. So even the *physical model* is a whole different animal.

Maybe Joe sees this as too *operational*?
Still — it’s a major modeling implication, and worth mentioning.

---

### **Reverse ETL Architectures** – Reality in many orgs

This one’s creeping into the mainstream:
* Push data *back* from your PDM into operational systems (CRMs, marketing tools, support platforms)
* Often done **without any formal modeling**, or just with aggregated snapshots

---

### **Domain-Oriented Data Mesh** – I have to mention this. I’m a fan.

Even if it's controversial, Data Mesh is clearly reshaping how orgs think about *ownership and modeling*.
* Decentralized responsibility
* Domain-driven design
* Self-serve data infrastructure
* Product-oriented thinking over pipeline thinking

---
# Part 3: The New Horizons of Data Modeling — Beyond the Classical Three Levels
(*Not just about ordering — it’s about evolving what we mean by “model” itself*)

## (09) Semantic Layer ≠ Model? → Interpretive, Functional & Application-Layer Models

> **TL;DR:**
> Modern data modeling can’t stop at the CDM–LDM–PDM triad.
> We’re entering a new dimension of **semantic, functional, and application-layer models** — where *interpretation, intent*, and *reusability* take center stage instead of mere data structure.

---

Joe sometimes tries to draw a line between the **semantic layer** and what he calls “non-models.”
But let’s be honest — these things behave a *lot* like models:
* They **define things**,
* They **aggregate**,
* They support **slicing and dicing**,
* They enable **shared understanding**.

So… what if they *are* models — just of a **different kind**?
Aren’t we just using **modeling** in another form?
Maybe it’s time to *stop asking whether they’re “real models”* and instead ask:
* What kind of modeling are they?*
* Where do they sit on the modeling landscape?*
* Are they outliers — or signs of something new emerging?*

---

### So what are we really talking about here?

We’re talking about a type of modeling where:

* The **structure** isn’t primary — the **meaning** is.
* Instead of listing attributes, you **organize intent** and **define business logic**.
* The model isn’t always separated from the tech — it’s often embedded in the tool, the query, or even the AI prompt.

It’s **more than just an SQL view**,
Less than a full-blown CDM,
But in some ways, *more useful*.

---

## So what do we call this thing?

### **Interpretive Model**

→ The model’s job: **ensure consistent interpretation** across tools and contexts.
→ Not just structure, but **rules of meaning** and **semantic context**.
→ This is what the *semantic layer* *actually does*.

---

### **Functional Model**

→ Answers the question: *What are we doing with this, and why?*
→ It’s not about normalization — it’s about **purpose-driven usage**.
→ Example: An AI assistant’s prompt logic, or a dashboard’s filtering config — that’s a model if it’s **explicitly defined**.

---

### **Semantic Model**

→ Answers: *What does this mean to the business?*
→ A shared layer where **metrics, dimensions, and concepts** get formalized (e.g. LookML, dbt metrics).
→ This is not just about storage or logic — it’s **business meaning made reusable**.
→ It sits somewhere between CDM and query runtime — a *business-centric abstraction*.

---

### **Application-Layer Model**

→ Umbrella term for things like semantic layers, metrics layers, AI prompt schemas.
→ These behave like models: they define, abstract, and support reuse — but not in a classical ERD sense.
→ They often **only exist at runtime** (dynamic binding, just-in-time context injection).

---

## Where does this sit in the classical modeling landscape?

Here’s one way to place it on the map:

| Model Type                       | Focus                     | Example                         | Distinguishing Feature                |
| -------------------------------- | ------------------------- | ------------------------------- | ------------------------------------- |
| CDM (Conceptual)                 | Meaning, worldview        | EAR, business object map        | Human conceptual framing              |
| LDM (Logical)                    | Structure                 | ER diagrams, 3NF                | Entities, attributes, relationships   |
| PDM (Physical)                   | Storage structure         | Snowflake tables, indexes       | Performance, optimization             |
| Functional / Semantic            | Usage meaning             | LookML, dbt metrics, AI prompts | Aggregation logic, metric definitions |
| Interpretive / Application-Layer | Context-sensitive meaning | Metrics layer, AI DSLs          | Linking meaning to tools & users      |

---

## So… is it an outlier?

**It stands out — but not as an outsider.**
It’s not breaking away — it’s *pointing forward*.

* **Format-wise**: Yes, it doesn’t fit into a classical ERD.
* **Position-wise**: Yes, it lives *at runtime*, not at design-time.
* **Usage-wise**: Yes, it’s often touched by **end-users**, not data architects.

But this isn’t a break — it’s a *spectrum*.
Classic modeling (CDM/LDM) gives us **structural & conceptual maps**.
This new wave gives us **maps for everyday usage**. And we need both.

---

## Final Note

This isn’t about "replacing" the old way of modeling.
It’s about **adding a fourth dimension** to the stack:
➡️ *How meaning is applied and reused in dynamic contexts.*

> **Data modeling is no longer just about what we store —**
> **It’s about what we mean, how we reuse it, and how we keep it consistent across tools, teams, and time.**
> This new kind of modeling isn’t an alternative — it’s an *expansion* of the discipline into the realm of interpretation and application.

---
## (10) Is It Fair to Oppose Streaming Models vs. Normalized Models So Sharply?

---

Modeling is not just evolving in form — it’s also facing new *friction points*.
One of the sharpest: **how do we model in streaming environments where classic SQL and joins fall apart?**
This section breaks that down.

---

Joe makes a bold claim:

> “Classic dimensional models with numerous joins $are$ ill-suited for real-time models.”

He’s *technically* not wrong —
But *modeling-wise*, that framing might be throwing the baby out with the bathwater.
Are we seeing **Joe’s overcautious tech realism** sneak into his modeling philosophy?

---

### The Context: Streaming ≠ Dimensional Modeling?

Joe argues:

> “Classic dimensional models with numerous joins $are$ ill-suited for real-time models.”

## What’s he getting at?

He means:

* The classic **star schema** (fact + dim tables + foreign keys) **struggles in streaming**.
* Why? Because joins in a streaming system are technically hard:
  * Data doesn’t arrive all at once — it *trickles in* across time.
  * Joining two unbounded streams requires *massive state management* (see Flink’s state backend).
  * Late-arriving events can *break your aggregations* or throw off order.

So yeah, **technically valid**.

---

### But what’s the real issue?

The issue is that **he’s conflating a technical limitation with a modeling philosophy**.
Just because joins are hard, doesn’t mean we should ditch the *idea of relationships* in modeling.

Joe’s implicit message becomes:
→ *Streaming = denormalized, join-free, flattened data structures*
→ And therefore: *Dimensional modeling doesn’t belong here*

But that’s an **oversimplification**, because:

* **The relationships still exist** — they just manifest differently.
* You can still *think dimensionally*, even if the **implementation is different**.

---

### So what’s the alternative?

Let’s talk **new ways to express relationships** in modern, streaming-first architectures:

---

### 1. **Semantic Joins / Logical Joins**

* AI-driven or BI semantic layers can **interpret** connections without physical keys.
* Example: a streaming `event.customer_id` can be **understood in context** and tied to a `customer_profile` — not by SQL JOIN but by *semantic meaning*.

---

### 2. **Context Injection**

* Instead of runtime joins, you use **preloaded lookup containers** — snapshots, feature stores, or stateful caches.
* The system *knows* which metadata belongs to which ID, and **injects it** into the stream dynamically.
* Not a join — more like a **context overlay**.

---

### 3. **Event Enrichment Pipelines** (Materialized Join)

* Enrich your stream *upfront*, using batch lookups or CDC updates.
* Kafka stream + Flink = stream events **already contain** enriched dimension info.
* Think: pre-baked, forward-joined, live-ready.

---

### 4. **Feature-as-a-Service / Embedding-as-Context**

* Dimensions aren’t tables — they’re **precomputed features** like RFM score or predicted LTV.
* You attach those values to each event ahead of time.
* Here, the **function defines the connection**, not the ID key.

---

### Classic BI vs Streaming Model — Side-by-side

| Classic BI Model                                 | Streaming-Friendly Alternative                                       |
| ------------------------------------------------ | -------------------------------------------------------------------- |
| `JOIN orders o ON o.customer_id = c.customer_id` | `event.customer_name = getNameFromCache(event.customer_id)`          |
| `GROUP BY product_category`                      | `event.product_category = enriched_event.product_category`           |
| `SUM(revenue)`                                   | `calculate_revenue(event)` where `event` already contains price info |

---

### So what’s the philosophical takeaway?

Joe’s realism is fair — **joins are hard** in streaming.
But if we zoom out and ask what modeling *really* is, we’ll find:

* **Conceptual relationships aren’t defined by joins** — they’re defined by *meaning*.
* If meaning matters, then **the model must still be able to express relationships** — even if they’re technically implemented differently.

---

### In short:

* **Dimensional thinking isn’t dead** — it’s just *adapting*.
* Streaming doesn’t kill modeling — it *demands* a new modeling grammar.

---

### Final recap:

* Joe accurately highlights the **technical headaches** of real-time joins
* But at the **modeling level**, he **gives up too early** on the idea of dimensional structure
* **Interpretive modeling** can preserve relationships *without needing SQL JOINs*
* The new modeling toolkit? → **Semantic logic, enrichment flows, cache-based injection, and AI-enabled joins**

---

## (11) Feedback-Aware & Persona-Driven / Use-Case Modeling

**Are there other model types worth mentioning?**
Absolutely — especially ones that we *don’t usually call “models”* (but functionally are), or that might soon get *repositioned as models* in modern architectures.

---

### **Feedback-Aware Modeling**

(*A model that evolves based on how it’s used or interacted with.*)

| Model Type           | Core Focus                    | Example                                                 | Distinct Feature                                           |
| -------------------- | ----------------------------- | ------------------------------------------------------- | ---------------------------------------------------------- |
| Feedback-Aware Model | User feedback & usage signals | AI agent overrides a metric, user redefines a dashboard | The model *adapts* based on usage patterns or direct input |

**Why is this a new category?**
* Classic models are *static*: you build them once, and then just read from them.
* This model is *dynamic*, *reflexive*, and *interaction-driven*.
* Think: self-adjusting metrics, AI-tuned models, or data quality feedback loops.

*AI-Optimized Outlook:*
> *"A semantic layer is only truly smart if it can respond to how people actually use it."*

---

### **Persona-Driven / Use-Case Modeling**

(*Modeling based on roles and specific goals — not on data structure alone.*)

| Model Type           | Core Focus                              | Example                                             | Distinct Feature                                         |
| -------------------- | --------------------------------------- | --------------------------------------------------- | -------------------------------------------------------- |
| Persona-Driven Model | Mapping aligned with roles or use-cases | Ops dashboard vs. Sales dashboard vs. AI agent view | The structure and metrics are *tailored to each persona* |

**Why is this new?**
* This is **model segmentation** — not a “single source of truth,” but **custom views for different needs**.
* Kimball and Inmon didn’t go there — they aimed for one consistent enterprise model.
* But today? You *need* different models for the **AI assistant**, the **data analyst**, the **decision-maker**.
  This model is built not on *data types*, but on *functional requirements*.

---

### Wrap-Up

| Why treat these as new model types?                                                                                 |
| ------------------------------------------------------------------------------------------------------------------- |
| Because they follow **new modeling principles** (like feedback and role-centricity)                                 |
| Because they’re **not derivatives** of the traditional CDM–LDM–PDM hierarchy                                        |
| Because in today’s **AI-powered, context-rich environments**, these are emerging as **valuable new modeling forms** |
| Because in terms of *function and meaning*, they behave like models — even if they *look* different                 |

---
## (12) Intentional Model – and the Architecture That Doesn’t Exist Yet (But Should)

If I had to bet — not based on hype, but on actual *philosophical, architectural, and usage trends* — I’d say the next big modeling leap won’t be something we’re already talking about.
It’s already *brewing quietly*, but *we don’t yet have the right name or system for it*.

## **Intentional Model**
(*A model that doesn’t structure data — it structures human intent.*)

### What is this?
It’s a type of modeling that starts *not from the logic of the data*, but from the **intent of the user**.
Not just “persona-driven,” but something deeper:
**What was the actual goal of the person who created, queried, or consumed this data?**

---

### Why do I think this is coming?

#### 1. **LLM + Analytics fusion** → fuzzy queries, intent-laden language

We’re no longer querying columns like `SELECT customer_id`.
Now we ask:

> *"Why did churn drop in this segment?"*
> That’s not just a query — it’s an *intent-laden hypothesis*.

#### 2. **Actionable Data + AI agents** → not just *see*, but *do*

We’re moving from “insight” to *action triggers from prompts*.
So it becomes vital to track not just *what was done*, but *why it was done*.

#### 3. **Ethics & auditability** → who modeled what, and why?

If AI makes decisions, we’ll need:
* *“What intent models was it operating on?”*
* *“What kind of prompt logic or assumptions were embedded?”*

#### 4. **Product-led data** → the model is not a schema, but a *user journey lens*

In product usage, we don’t just model entities. We model:
* *“What did the user want?”*
* *“Which decision path were they on?”*

---

### Possible formats for this kind of model:
* **Prompt-type templates** (capturing query intent categories)
* **Intent graphs** (intent → metric → data lineage)
* **Interaction maps** (structured models of user goals)
* **Regret models** (what the user *should* have asked if they’d known better)

---

### How is this different from the semantic layer?

| Semantic Layer                | Intentional Model                     |
| ----------------------------- | ------------------------------------- |
| *What is this data?*          | *Why are you asking about this data?* |
| Structured metric definitions | Goal-driven querying logic            |
| Context for interpretation    | Context for *intent* and *decision*   |
| Query consistency             | Decision path awareness               |

---

### What’s the impact?
> **In the future, modeling won’t just shape *what* we calculate — it’ll shape *why* we calculate it.**
> The data model will begin to look more like an **intent map**, not just a data map.

That’s a whole new meta-layer — and likely **the generation that follows the semantic layer**.

---

### So how could we implement this?

Whoever figures this out won’t be thinking in:
* Classic ER diagrams,
* Or `metrics.yaml` files,
* But maybe in something like:
  * an **intention-graph DSL**,
  * or a schema for **classifying intent types** (like `ExplainIntent`, `CompareCause`, `ActNow`).

---

> **TL;DR:**
> The next generation of data models won’t just represent data — they’ll represent **human intent, goals, and decision logic**.
> The *intentional model* isn’t just a new kind of model — it’s a **whole new modeling dimension**: a way to formalize *the “why” behind every question or action*.

---
# Part-4: The Big Picture — Two Summary Tables

## (13) Data Modeling & Architecture Tables

By now, it’s probably clear that data modeling isn’t just about moving between levels — it’s about navigating a whole **spectrum of meaning and use**.

The following two tables aim to *sum up that spectrum* — by structuring both **model usage types** and **architectural behavior patterns** in a clean, cohesive way.

**These tables are designed to be: complete, coherent, and non-redundant.**

### Table 1: Analytical Architectures & Modeling Paradigms (2025)

Each row clearly separates:
* **Classic architectures** (e.g., DWH, Lakehouse)
* **Modeling layers** (Semantic Layer, Federated Layer)
* **Interfaces** (AI Interfaces)
* **Paradigms** (e.g., Data Mesh)

### Table 2: Comprehensive Data Modeling Usage Types (2025 Edition)

The *“Type”* column cleanly distinguishes between:
* **Classic models** (CDM, LDM, PDM)
* **Business logic layers**
* **Runtime interpretation techniques**
* **Contextual modeling practices**
* **Forward-looking modeling paradigms**

### Relationship Between the Two Tables
* They’re **not redundant** — they’re **complementary**
* They’re **interoperable** — e.g., *Intentional Model* flows into *AI-Augmented Interface* use
* They avoid: duplicate rows, conceptual overlap, or logical contradiction

---

### Comprehensive Data Modeling Usage Types (2025 Edition)

| Type                 | Model Kind                                  | Main Focus                          | Example                                             | Notable Characteristic                                                |
| -------------------- | ------------------------------------------- | ----------------------------------- | --------------------------------------------------- | --------------------------------------------------------------------- |
| Classic Layer        | CDM (Conceptual Data Model)                 | Conceptual world modeling           | EAR, business object mapping                        | Human-understandable logic, tech-agnostic                             |
| Classic Layer        | LDM (Logical Data Model)                    | Structural logic                    | ER diagrams, 3NF                                    | Entities, relationships, primary & foreign keys                       |
| Classic Layer        | PDM (Physical Data Model)                   | Storage-oriented structure          | Snowflake schema, Iceberg layout                    | Indexing, partitioning, storage-specific layout                       |
| Functional Layer     | Functional Model                            | Metric & business logic             | dbt metrics, LookML, ReisQL                         | Reusable business rules, slicing & dicing logic                       |
| Interface / Runtime  | Application / Interpretive Model            | Context-driven semantics            | Semantic Layer, Power BI, AI query protocol         | Runtime semantics, non-structural logic                               |
| Contextual Technique | Semantic Join                               | Interpretation-based joins          | AI-assisted linking `customer_id` to profile        | Logical, not SQL-based association                                    |
| Contextual Technique | Context Injection                           | External data injected into streams | Flink, Kafka, feature cache                         | Injected lookup instead of runtime JOINs                              |
| Contextual Technique | Event Enrichment Pipeline                   | Precomputed enrichment of stream    | Lookup joins, enrichment stages                     | Event streams enhanced with external dimensions                       |
| Contextual Technique | Feature-as-a-Service / Embedding-as-Context | Precomputed features and embeddings | RFM scores, AI embeddings                           | Relationship logic embedded via pre-calculated features               |
| Modeling Paradigm    | Event Model (EDA-native)                    | Events as primary modeling element  | `OrderPlaced`, `PaymentFailed` events               | Event sourcing, replay, causality, immutability                       |
| Modeling Paradigm    | Time-Series Model                           | Time as primary dimension           | `metric_value` over `timestamp`                     | Rolling windows, lag, trends, time-sensitive joins                    |
| Modeling Paradigm    | Feedback-Aware Model                        | Feedback-driven refinement          | AI fine-tuning a metric based on usage              | Usage-based learning, auditability, human or AI-driven feedback loops |
| Modeling Paradigm    | Persona-Driven Model                        | Role-specific modeling              | Metrics customized for marketing vs. ops dashboards | Model structures segmented by user intent or role                     |
| Modeling Paradigm    | Intentional Model                           | Human intent as a modeling input    | Prompt: “Why did AOV drop?”                         | Intent abstraction, decision logic, intention graph architecture      |

---
### Analytical Architectures & Modeling Paradigms (2025)

| Row Type           | Name                       | Short Description                                        | Typical Technologies               | Modeling Principle / Behavior                              | Typical Model Forms                       |
| ------------------ | -------------------------- | -------------------------------------------------------- | ---------------------------------- | ---------------------------------------------------------- | ----------------------------------------- |
| Architecture       | Data Warehouse (DWH)       | Centralized, relational, structured data store           | Snowflake, BigQuery, Redshift      | Pre-modeled, dimensional structures                        | Star schema, 3NF, OBT, Kimball            |
| Architecture       | Data Lake                  | Unstructured/semi-structured storage, cheap and flexible | S3, ADLS, HDFS                     | Minimal modeling, schema-on-read, structure comes later    | Flat raw data, event logs                 |
| Architecture       | Data Lakehouse             | Hybrid of lake + warehouse, structured querying on top   | Databricks, Delta Lake, Iceberg    | Modeling is optional; physical layout matters a lot        | Medallion model (bronze/silver/gold), OBT |
| Architecture       | Stream-native Architecture | Real-time processing of event data                       | Kafka, Flink, Materialize, ksqlDB  | Denormalized, window-based, append-only                    | Feature stores, enriched flat events      |
| Architecture       | Event-Driven Platform      | Event as the primary entity, with replay and idempotency | Pulsar, EventBridge                | Relationships modeled as causality chains, event sourcing  | Event model                               |
| Architecture       | TSDB Architecture          | Time-series data collection and analysis                 | InfluxDB, TimescaleDB, Prometheus  | Time = primary axis, windowed aggregations, lag handling   | Time-series model, rolling metrics        |
| Modeling Layer     | Semantic Layer-as-Core     | Abstract layer for metrics and dimensions                | Looker, Cube, dbt metrics, AtScale | Metric-based, reusable querying logic                      | Metric model, semantic model              |
| Modeling Layer     | Federated Query Layer      | Unified query across multiple data sources               | Trino, Starburst, Athena           | Logical mapping with minimal physical control              | Virtual model, logical mapping            |
| Architecture       | Reverse ETL Platform       | Push data back from DWH into operational tools           | Census, Hightouch                  | Output-focused; acts as a synthetic dimension export layer | Flat tables, synthetic keys               |
| Interface/Paradigm | AI-Augmented Interface     | Natural language querying and interpretation             | GPT, ThoughtSpot, MCP Protocol     | Prompt-driven interpretation, intent-centric querying      | Intentional model, semantic proxy         |
| Architecture       | Domain-Oriented Data Mesh  | Decentralized, domain-owned architecture                 | Platform + domain teams            | Local modeling, federated ownership and metric governance  | Domain models, mesh-scoped semantics      |

---
