# 45.Post：*Example - Building a Traditional Data Model*
**(Using the levels to build a traditional conceptual, logical, and physical data model)**  
→ [Original Joe Reis post](https://practicaldatamodeling.substack.com/p/example-building-a-traditional-data)

* * *

**Teaser**
----------

_Could you explain the difference between CDM, LDM, and PDM to a business stakeholder—in just three sentences—and make them actually want to become a data modeler afterward?_

* * *

**TL;DR – What This Post Covers**
---------------------------------

*   Part-1: A slick little demo of CDM–LDM–PDM using coffee
    
*   Part-2: Why the ER model doesn’t work well as a conversation starter
    
*   Part-3: What Béla Halassy taught us about attributes (still relevant in 2025)
    
*   Part-4: How to unlock Dana’s worldview in an interview
    
*   Part-5: 10 classic CDM-level modeling mistakes, ranked by how much pain they’ll cause later
    

* * *

**PART 1 – The Demo**
---------------------

If I could, I’d launch a global competition:  
_How do you demo CDM → LDM → PDM in 2025 so that people actually want to stick around and not just zone out after the second bullet point?_

Here’s what I’d be looking for:

*   Use _as few words as humanly possible_. People scroll fast, they skim even faster.
    
*   Doesn’t matter if it’s a bit shallow—_make it bingeable_.
    
*   Prioritize _clarity over cleverness_.
    
*   The demo should take _zero mental effort_ to absorb.
    
*   Deliver an **AHA moment**—the kind that makes someone want to become a data modeler, _right now_.
    
*   In other words, the demo should be:  
    **elegant, punchy, micro-crafted, and irresistibly smooth.**
    

Alright, let’s fire up a double shot of _data modeling espresso_.

* * *

**The Coffee Order Demo** ☕️
----------------------------

**Why this works:**

*   Everyone gets the context (no need for backstory)
    
*   There are just a few entities
    
*   It naturally includes relationships, attributes, and events
    
*   And it scales beautifully from CDM to LDM to PDM
    

* * *

### **The AHA version (as tight as it gets)**

#### **CDM – Conceptual Level**

> A **Customer** orders **Coffee**.

That’s it.  
Two nouns, one verb.  
Two entities, one relationship. Pure business logic.  
_A model Dana would actually nod at._

* * *

#### **LDM – Logical Level**

```text
Customer (name, phone)
Order (time, size, milk_type)
Coffee (type)

Order → Customer (many-to-1)  
Order → Coffee (many-to-1)
```

Now we’re adding detail—attributes, cardinalities, structure.  
No keys yet. Still technology-neutral.  
But _you’re already seeing the skeleton of the real system_.

* * *

#### **PDM – Physical Level**

```sql
CREATE TABLE customer (
  customer_id SERIAL PRIMARY KEY,
  name TEXT,
  phone TEXT
);

CREATE TABLE coffee (
  coffee_id SERIAL PRIMARY KEY,
  type TEXT
);

CREATE TABLE orders (
  order_id SERIAL PRIMARY KEY,
  customer_id INT REFERENCES customer(customer_id),
  coffee_id INT REFERENCES coffee(coffee_id),
  time TIMESTAMP,
  size VARCHAR,
  milk_type VARCHAR
);
```

Now we’re grounded in real-life implementation:  
Data types, keys, references. This is where **SQL meets semantics**.

* * *

### **And the final punchline:**

> **CDM is why we sell coffee.**  
> **LDM is how we think about it.**  
> **PDM is how the barista finds your name.**

* * *

All of that?  
Less than 50 lines of text.  
And yet, we just walked through the full lifecycle:  
From _business intention_ to _logical structure_ to _physical implementation_.

Clean. Relatable. No fluff.

You don’t need a PhD in data architecture to get it—you just need to have ever ordered a cappuccino.

* * *

Let me know if you'd like to proceed with the next part (why ER modeling might not be the best tool for business discovery). I'm ready to keep the tone, clarity, and rhythm going.

* * *

**PART 2 – ER Modeling as CDM in 2025?**
----------------------------------------

So… I have a few reservations about this.

That Dana coffee-ordering demo?  
It’s a **classic, IT-driven, ER-style CDM**. And don’t get me wrong: it’s perfect for _teaching_, for _onboarding technically-minded folks_.  
But I don’t think it really captures **how meaningful business modeling actually happens in 2025**, at least not in the smoothest, lowest-friction way.

Let me explain.

* * *

### **ER Models Are Rigid Tools for Fluid Conversations**

Here’s the problem:  
The **ER model is an ontological tool**, but it’s _not_ a great _conversational instrument_.

When Dana starts telling her story, is that how she wants to think?  
In “entities” and “relationships”?  
Does she want to freeze the world into static boxes?

Not really.

Why not?

*   Because **ER models struggle with processes, states, transactional narratives**, and the _dynamics of real-world interactions_.
    
*   In 2025, **business complexity isn’t just about “what exists” but “how it evolves.”**
    
*   ER captures _structure_. But Dana speaks _flow_.
    

That’s why, as a demo, it works. But as a representation of business reality?  
It feels... a bit _flat_.

The _form_ can stay — sure. But we need a **semantic overlay**, something more dynamic.

* * *

**What Would I Do Differently?**
--------------------------------

Let me be direct: I’d separate two layers within the CDM.

*   **Structural CDM** — your classic entity-relationship view.
    
*   **Behavioral CDM** — what happens, when, why, and to whom.  
    (_Think of it as a “Business Event Map.”_)
    

But most importantly:

**I wouldn’t model too early.**  
Instead, I’d **facilitate structured dialogue**, where the model is a _byproduct_, not the goal.

* * *

**Ask Better Questions, Get Better Meaning**
--------------------------------------------

Let’s say Dana mentions “active customer.”  
Now, is that just a data point?

Nope. That’s a **state**, triggered by a **business rule** or **event**.

So here’s how I’d frame it:

*   **Not** as an attribute in the CDM.
    
*   But as a **status transition**:  
    _“Customer becomes active after their first payment is confirmed.”_
    

That’s **business logic**, not a field in a table.

Which brings us here:  
**Status isn’t a CDM or LDM thing.**  
It’s a **modeling mindset** question:  
_What exactly are we trying to represent?_  
Is it an attribute? A rule? An event? A derived relation?

* * *

**More Than Modeling — It’s Meaning Extraction**
------------------------------------------------

To be honest, when I’m modeling at the CDM level, I’m not just designing a data structure.  
I’m _searching for meaning_ — through questions, not boxes.  
It’s way closer to **product discovery or design thinking** than to classical ER work.

Let’s go back to Dana.

Her CDM is structurally clean.  
But I wonder if we’re **conflating structural relationships with business meaning**.

When she says “active customer,” she’s not pointing to a column.  
She’s pointing to a **lifecycle**.  
A status transition.  
An embedded set of rules.

Maybe what we need is a **second layer** of modeling.  
Not ER-style.  
But **event-state mapping** — as a conversational _bridge_ before LDM.

* * *

**So... Is “Status” CDM or LDM?**
---------------------------------

Well — it depends _how_ it emerges:

*   If Dana says: _“An active customer is someone who has paid”_ →  
    That’s a **CDM-level business rule**, a behavioral insight.
    
*   If someone says: _“There’s a field called ‘active’ in the customer table”_ →  
    That’s an **LDM-level implementation choice**.
    

**Same word. Entirely different worlds.**  
The difference?  
It’s all about _how you approach the modeling conversation_.

And that leads us to a new dimension:  
**CDM-level meta-modeling.**  
Before any key or column even appears.

* * *

**TL;DR – Big Takeaways**
-------------------------

*   **Can “time” enter the room?**  
    Status changes, events, triggers — they’re not second-class citizens.
    
*   **Can we challenge what’s implicit?**  
    Whose definition of “active” are we even using?
    
*   **It’s not just entities — it’s narratives.**  
    What story does this model want to tell?
    

* * *

This isn’t about rejecting ER modeling. It’s about **seeing where it stops being helpful** — and **knowing when to invite in another language**.

And sometimes, all that starts with a simple question:  
_“When exactly does someone become active?”_

Because that’s not a field.  
That’s a story.  
And stories are where models _begin to matter_.

* * *

Let me know when you're ready for **Part 3** — Halassy Béla, attributes, and the deep philosophical divide between ER and EAR.

* * *

## **PART 3 – Dr. Béla Halassy and EAR Modeling**

Alright, time for a sentimental moment.

Dr. Béla Halassy — a fellow Hungarian — was working as a database administrator at Chase Manhattan Bank in the 1970s. Back then, being a "DBA" meant something entirely different than it does today: it meant being a *data modeler in the wild west of computing*. And he wasn't just any modeler — he soaked up a mountain of knowledge in the US, and then brought it home to Hungary.

I remember cold-calling him — completely out of the blue — around 1987. I was a part-time IT lecturer at a polytechnic school, showing up in a suit and tie, asking if he'd give a guest lecture to my students on data modeling. He welcomed me warmly — and immediately began "examining" me to size me up. Not pushy, but I was sweating.

He said yes.

The big day came. My class? 100% women — they were training to become production engineers in the garment industry. 20+ students, all beautifully dressed for the occasion (not quite formal, but definitely elegant), honoring both me and the guest speaker. Faculty members showed up too. And what followed was the most *unforgettable* lecture I've ever witnessed — and I've got two BScs, an MSc, and have taken 100+ exams.

Halassy never lectured *at* them — he *asked* them, constantly. The girls were fully engaged, answering, laughing, feeling smart and seen. It was 90 minutes of brilliance. They even surprised him with a gift, unprompted. To this day, just thinking about it gives me an adrenaline rush.

---

## **So what exactly is EAR modeling, according to Halassy?**

**EAR modeling** is built on a few core beliefs:

- *Attributes are not optional extras* when mapping reality.
- They already appear — and **should** appear — in the **Conceptual Data Model (CDM)**.
- An attribute is **not** just an implementation detail — it's a **semantic carrier**. ("Birthdate" ≠ just a "date" type.)
- **Explicitly modeling attributes** helps clarify concepts, boost consistency, and sharpen meaning.

So EAR modeling is **not a technical formalism**. It’s a **modeling philosophy** — one that doesn’t *banish* attributes from the conceptual level, but *embraces* them.

---

## **Is this approach still valid in 2025?**

### *Mostly: YES — but context matters.*

**To exclude attributes from CDM entirely is now an artificial constraint.**
Given the complexity of modern digital systems, domain-driven design, policy-centric logic, and even AI-trainability — we *need* to think in terms of **conceptual attributes**, not just entities and relationships.

### A few quick examples:

- `Customer is active` → Not just a relationship status, but a **semantic attribute** implying **business rules**.
- `Order.created_at` → Not just a timestamp. It's the anchor for **SLA calculations**, **audit trails**, **event-based logic**.

---

## **Why EAR still makes sense**

### **1. CDM ≠ Minimalism**

Classical ER models give us abstract structures — but they often fail to express **rules, context, and meaning**. They’re dry blueprints. We need more than that.

### **2. Attributes = Vocabulary of the Domain**

Attributes aren't just fields — they are *words in the domain language*. If we don’t model them *conceptually*, we lose out on clarity and business dialogue.

### **3. Compatible with AI / ML / Rule Engines**

A well-structured EAR model provides **direct semantic inputs** to machine learning models. "Field-level meaning" becomes not just nice-to-have — but critical.

---

## **But where can EAR modeling backfire?**

### **1. If it overformalizes CDM**

If you obsess over attributes and neglect relationships, the model becomes **LDM-lite** — too concrete, not conceptual.

### **2. If attributes are treated as final**

In CDM, everything is still *fluid*. An attribute isn’t a spec — it’s a narrative fragment. Over-fixing them too early stifles flexibility and dialogue.

---

## **So how do we apply Halassy’s wisdom in 2025?**

✅ *Don’t fear attributes in the CDM.* Fear losing their **conceptual depth**.

✅ *Don’t exclude them.* Just **handle them well** — name them clearly, tie them to business rules, link them to statuses.

✅ The EAR model gets new relevance — especially when CDM is used for:

- **Business meaning**
- **AI compatibility**
- **Navigating between stories, events, and rules**

---

So here’s to Dr. Halassy — a Hungarian data modeling pioneer — and to keeping the **semantic richness** alive in our models.

Because an attribute isn’t just a column. Sometimes, it’s the *essence of what we’re trying to understand.*

* * *

## **PART 4 – How to Extract Dana’s Worldview: Interviewing for Meaning**

So how exactly should we be doing things differently?
Can a more practical, empathetic, human-centered approach improve the way we model business reality?

Let’s explore how to get Dana talking—really talking. How do we guide her into surfacing the right stories, and ideally, all of them? Is it better to rely on (1) our modeling assumptions, or (2) steer the conversation with pre-built prompts based on experience, while focusing entirely on making Dana feel safe and inspired—*so much so that she tells stories even seasoned data modelers have never heard before*?

And how do we *know* when it’s time to wrap the interview—when there’s no more energy to squeeze out meaningful insights?

Do we go for a “catalog-style” story sweep first (in-order tree traversal)? Or dive deep into the very first one (depth-first), because that depth might unlock the rest?

---

## **How Should We Get Dana to Speak?**

### **Not a “briefing.” A dialogue.**

We’re not just trying to extract data—we’re trying to *unravel a web of meaning*. So the goal isn’t “answers,” but *trust-based storytelling*. Inspired. Reflective. Sometimes messy. Always real.

### **A Two-Hemisphere Strategy**

- **Left-brain (structure):** Yes, I bring preconceptions and pattern recognition with me. They’re my internal **mental models** — they help me go: *“Oh, this is clearly a payment state transition.”*

- **Right-brain (connection):** But I don’t *ask* those patterns. I **listen for metaphors**, **tensions**, **thresholds**. That’s where Dana’s worldview really surfaces.

---

### **I’d structure the conversation in 3 phases:**

#### _PHASE 1: The “safe zone” – Dana’s narrative turf_

> “When you came in to work this morning, what’s the first thing that crossed your mind about your customers?”

Goal: **Don’t speak modeling language yet. Speak from experience.** This is where we’ll hear *archetypal stories* — “the client didn’t pay,” “the system rejected the order,” etc.

#### _PHASE 2: Anchoring and expanding the zone_

> “When did this story begin? And when did you realize it would go well or badly?”  
> “Who else was involved?”  
> “Was there something you didn’t understand at the time?”

Now we’re exploring **time, people, and context**. Slowly, we begin to *surface relationships, states, processes* — **from inside her reality**, not from our system diagram.

#### _PHASE 3: Tension map and blind spots_

> “What’s something the system *doesn’t* help with today?”  
> “If you could magically change anything about this flow tomorrow, what would it be?”

This is where we hear about **“non-modelled reality”** — transient states, workarounds, shadow IT, emotional friction.

---

### **When (and How) to Stop**

**The conversation doesn’t end when the data runs out. It ends when the patterns stop evolving.**

You’ll feel it: Dana begins **repeating herself metaphorically**. You hear the *same narrative arcs* wrapped in different surface examples. That’s a **signal** — you’ve mapped the dominant mental structures.

---

## **In-order or depth-first? A map of Dana’s story-tree**

It’s **not a binary question**, but a **dynamic switching strategy**. The key is:

> **Start broad, but when something “dances,” go deep.**

So:

- **Begin with an in-order pass**: Ask Dana to share a few *different types* of stories — complaints, payments, orders, handovers, etc.  
Goal: **Sketch a wide map** — understand the cast of characters and the stage.

- **But when a story carries latent tension or emotional charge**, switch to **depth-first**:

> “How does that usually go in other cases? Is this typical? What makes it exceptional?”

That’s when the stories start **generating each other**. You’re no longer interviewing — *Dana’s stringing the beads*, and you’re just holding the thread.

---

## **Meta-question: Is This Already Data Modeling?**

By the end of it, **your CDM won’t be a structure of entities — it’ll be an imprint of stories.**

And when you later add “active status” into the LDM, you’ll realize: it’s not just a field. It’s *a tension, a threshold, an event, a rule — and a lived experience.*

And you’ll thank Dana for showing you how to see it.

* * *

## PART-5: Mapping CDM Modeling Pitfalls (Because Space is Limited)

### GOAL:
Can you really make **structural or pattern-based mistakes** at the CDM level?

Let’s list the most common structural/patterning mistakes one can make in a **Conceptual Data Model (CDM)**.

For each, we’ll assign a **damage rating from 1 to 9** — depending on how far the issue could travel undetected through the data modeling pipeline, and how much cost it would incur in rework, misimplementation, or architectural debt. 

**The later a CDM mistake is caught, the more it hurts.** That’s what the score reflects.


---

Honestly, this feels **more relevant than ever in 2025** — because we’re no longer modeling just systems, we’re modeling how people make sense of systems.  

**Spoiler alert:** Yes, you *can absolutely* make CDM-level modeling mistakes that later cost millions, or lock you into conceptual dead ends — because *fundamental misunderstandings* often start right here.

---

### Possible CDM Structural / Pattern-Based Mistakes
_(with a 1–9 impact score, where 9 = nightmare cost if detected late)_

---

### 1. **Missing Entity (e.g., there's "Order" but no "Payment")**
🔴 **Impact Score: 9**
> An entire business process gets ignored. Later patched into LDM/PDM using sketchy workarounds (like a `payment_status` flag).

---

### 2. **Fake Aggregation (e.g., "Customer–Product" directly)**
🔴 **Impact Score: 8**
> Modeler misses that an intermediate entity (e.g., "Order") is required. Logical relationships become misleading, queries fall apart.

---

### 3. **Double Meaning (e.g., "Order" as both transaction + template)**
🟠 **Impact Score: 7**
> One entity carries two distinct concepts. Auditing, versioning, and transactional tracking become painful. Data quality bleeds out.

---

### 4. **Premature Concretization (e.g., `is_active` as an attribute)**
🟠 **Impact Score: 6**
> A business rule is modeled as a static field instead of logic or state. Changing the definition later is hell.

---

### 5. **Missing Role Modeling (e.g., no distinction between "Payer" and "Recipient")**
🟠 **Impact Score: 6**
> One entity (like "User") plays multiple roles but they’re not differentiated. Business logic and permissions unravel.

---

### 6. **Junk Box Entity (e.g., a generic "Event" catch-all)**
🟡 **Impact Score: 5**
> Over-abstracted placeholder that turns into a black hole. Hard to split out later. Traceability and usability tank.

---

### 7. **Lost Directionality (e.g., "Customer–Order" with no hint of direction)**
🟡 **Impact Score: 4**
> “Who’s doing what to whom?” is unclear. Weakens AI-based interpretation, auto-documentation, and rule engine logic.

---

### 8. **Over-Normalization at the CDM Level (e.g., phone/email as separate entities)**
🟡 **Impact Score: 3**
> Focus is lost. The CDM becomes tech-y schema design instead of a business modeling conversation.

---

### 9. **Naming Confusion, Non-Domain Language (e.g., “Cust”, “Prod”, “Txn”)**
🟡 **Impact Score: 2**
> Blocks shared understanding. Poor naming flows into LDM/PDM and hurts automation, mapping, and communication.

---

### 10. **No Time Dimension or Status Logic (e.g., no timestamps or "active" state)**
🔴 **Impact Score: 8**
> Auditability, lifecycle modeling, and analysis break. You can’t track events, and reporting becomes contextless.

---

### In Short:
A solid CDM is your **first map of the narrative reality**. 
If this map is distorted, every downstream artifact — analytics, ingestion, governance, AI training, business rules — inherits that distortion. 

A few misplaced lines can cost you a year.

* * *
