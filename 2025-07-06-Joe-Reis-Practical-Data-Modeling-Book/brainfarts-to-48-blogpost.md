48.Post: **AI to the Rescue？**  
https://practicaldatamodeling.substack.com/p/ai-to-the-rescue  

**PART 1 – Probability vs. Symphony: What is AI, really?**  
Let’s start with a bit of clarification. You often hear: “Artificial intelligence is just a machine that runs on probability.”
Well... yes. And also, very much no.

Yes, because most modern AI (especially machine learning and generative models) **does** rely on probability — Bayesian reasoning, statistical inference, loss minimization. Training an AI means minimizing a loss function — which is really just statistical betting on what will probably work best.

But also no, because saying that is like claiming a Mozart symphony is just “a series of soundwaves.” Technically correct, but **spectacularly missing the point**. What makes AI interesting — at least the better versions of it — is the **learning dynamics, the layered representations, the adaptivity, the structured complexity**. That’s what turns a matrix of numbers into something closer to a Jupiter Symphony than a coin toss.


**PART 2 – Pain and Learning in Data Modeling**
(A skeptical detour through Joe’s optimism)

So here’s the thing: Joe sounds pretty upbeat about AI in this chapter. And to be honest, I don’t disagree with the tools or the use cases he’s listing — they’re solid, they work, and yes, they’re already helpful. But still... I find myself leaning more skeptical. Maybe not doomer-pessimistic, but definitely more cautious. Why? Because I don’t think AI just helps us fix things. Sometimes, it distorts what we should be fixing in the first place.

AI isn’t just a typo-fixer for data models. It can just as easily become a **funhouse mirror** — distorting our assumptions, giving us a false sense of progress, and dulling the edge of our critical thinking. And that’s my biggest worry here. It’s not about whether you "know data modeling" as a craft and want AI to help. It’s about how easy it becomes to let go of **the pain** — and that pain is where real learning happens.

To me, good data modeling is built on a certain amount of discomfort. If you’re not feeling it, you’re probably skipping steps. No friction? No remodelling. And AI? It’s so good at soothing friction that sometimes it stops us from realizing something's even wrong. So here’s a not-so-glamorous list. A taxonomy of the pain points in data modeling — and why they matter:

**The Many Pains of Data Modeling:**

* **Cognitive pain (the pain of understanding):** The domain logic is fuzzy. Terms shift. Stakeholders are unsure of what they even want. You’re asked to build a map while the territory is still forming.

* **Social pain (alignment hurts):** Different teams interpret the same thing differently. Reaching a shared vocabulary? It’s a slow and painful compromise.

* **Philosophical pain (time is a nightmare):** What’s valid when? Are you modeling a snapshot or a process? A slowly changing dimension or an event stream? Reality moves — the model stands still.

* **Operational pain (idempotency isn’t obvious):** When is an aggregation “final”? Is it okay if re-running gives a different number? Deterministic, auditable pipelines don’t just happen.

* **Evolutionary pain (change breaks things):** New use case, old model breaks. What you called “user” last month no longer fits. Models are always temporary truth, never permanent structure.

* **Polysemous pain (too many meanings):** A field named “status” means one thing in onboarding, something else in billing. Same word, different worlds.

* **Ontological pain (the pain of missing data):** Sometimes, the data just isn’t there. Maybe it was never captured. Maybe it’s noise. But you can’t model what no one thought to measure.

* **Structural pain (rigid models trap you):** Your schema becomes a frozen worldview. The decisions you made last quarter haunt you next year.

* **Linguistic pain (you can’t ask what isn’t modeled):** Some questions can't be asked — not because they're invalid, but because there's no structure to support them. Modeling isn’t just about answers; it defines what’s askable.

* **Memory pain (intuition fades):** By the time your 50-table data mart is humming, no one remembers what the original question even was. The model survives, but the insight doesn’t.

Now, back to Joe’s take. Yes — feedback loops can get tighter with AI. And yes — modeling can become more accessible. But the danger lives in that same progress: if the AI starts masking broken assumptions, skipping over structural flaws, and numbing the necessary tension, then we stop learning — both individually and as organizations.

You can’t optimize a feedback loop if your mental model is wrong. That’s where my cautious side kicks in. And my reasoning? It starts and ends with the big one: the **absence of grounding**. 


**PART 3 – Expanding Joe’s List (The Data Modeling Edition)**

Joe’s original list of AI use cases in data work is great — practical, optimistic, and already proving its worth in the wild. But I’ve been wondering: how would that same list look through the lens of a data modeler? Not just a “data person,” but someone who lives in the mud of schemas, joins, naming debates, and versioned assumptions?

Here’s my take on expanding Joe’s list with some modeling-specific firepower:

* Surfacing Implicit Logic and Hidden Assumptions in SQL and dbt Models
Let’s be honest — a lot of our data logic lives inside silent agreements, not documentation. What if AI could help extract and reflect on those invisible assumptions?
Think about it: We ask the AI to analyze our queries, views, or dbt models not just syntactically, but semantically. What's taken for granted? What's assumed to be always true?
For example: “This query assumes that every user has at least one transaction.”
That’s the kind of subtle modeling trap that won’t throw an error — but will distort everything downstream. AI can be a logic mirror, revealing what we’ve encoded without even realizing.
And more than that — it can teach us to think more systematically. Most orgs don't document that kind of thinking. But they should. And AI could help us start.

2. Schema Evolution Audits – Powered by AI
Let’s talk about time. Models evolve. Fields get added, redefined, renamed. Sometimes we update dependent layers… sometimes we don’t.
What if AI could help audit schema changes over time, not just mechanically, but interpretively?
We could ask:
– What changed in this table in the last 3 months?
– Which downstream models didn’t reflect that change?
– What kind of risk does that introduce?
This isn’t just about metadata diffs — it’s about surfacing where reality and structure drifted apart. AI here isn’t just logging. It’s reading between the lines of version history.

* Prompt-Based Data Modeling in Plain Use-Case Language
Now this one’s close to my heart: writing prompts in use-case language, and getting back early-stage model proposals.
Example: “I want to identify customers who were inactive for 90 days, but came back and bought something via mobile only.”
Instead of manually parsing that into tables, relationships, fields, and filters — what if AI could take a first pass?
Maybe it suggests:
– A session table with device type
– A purchase fact table
– A user state flag for inactivity
– A time-window logic block
No, it won’t be perfect. But as a prototyping partner, this is gold. It helps bridge the gap between stakeholder-speak and implementation logic — a gap that often eats up hours of meetings, alignment, and interpretation.
Later, a senior data modeler can refine, validate, or throw out the scaffolding — but this is a powerful first swing.

* Human-in-the-Loop Checklists: The Underrated AI Use Case
Here’s where it gets real. The most underrated, high-leverage use case for AI in modeling is co-creating checklists. But not generic ones. Not “here are 7 questions to ask before publishing a model” copy-paste junk.
I mean something deeper: checklists as knowledge codification tools.
Checklists that are context-aware, reflective, and grounded in the domain.
But here’s the catch: this only works if the dialogue is real. Not prompt–response ping pong, but actual back-and-forth, with human feedback guiding the learning process.

* The Data Engineer Has to Teach, Not Just Ask
If you’re building this kind of AI-powered checklist, the data engineer isn’t just consuming outputs — they’re shaping the structure.
They show examples.
They flag blind spots.
They provide context: goals, business needs, data quality issues, update frequencies, scaling challenges, temporal quirks.
This interaction becomes a shared learning process, not an outsourcing shortcut.

* The AI Has to Ask Back
This is non-negotiable.
An AI that just spits out checklists based on prompt templates isn’t good enough. The AI has to learn to push back, to ask for clarification, to differentiate.
Example:
– “This looks too generic. Want to break it down by temporal dimensions?”
– “Should we consider idempotency scenarios for batch pipelines here?”
Only then does it become a partner, not a glorified checklist generator.

* The Goal Is Not Compliance — It’s Discovery
This is my biggest point.
Most checklist tools — human or AI — default to checking boxes:
– “Primary key?
– Source schema validated?
That’s fine. But if it’s not tied to the problem space, it’s just bureaucracy.
What really matters:
– What are we trying to understand?
– What decision is this model meant to support?
– What assumptions are baked into this structure?
That’s where AI can help if we teach it to ask those questions. And that’s a big “if.”

EXAMPLE: Dialogue-Driven Checklist Creation
Let’s play it out.
You: “Give me a 7-point checklist for validating the structure of a customer lifetime value model.”
AI: (Returns a reasonable list)
You: “Now add something about how we’re defining churn timing and cohort boundaries — those are fuzzy.”
AI: (Updates the checklist, adds thoughtful prompts)
You: “Cool. Now reframe it so the checklist doesn’t just validate the model, but helps surface unspoken assumptions.”
AI: (Returns version 3 — now it’s not a checklist, it’s a thought partner)

That’s the shift.
We’re not generating checklists.
We’re building a shared narrative, based on experience and reflection.

CONCLUSION:
Yes — AI can build high-quality, practical, assumption-surfacing checklists together with a human data engineer.
But only if:
– The dialogue goes deep, with feedback loops
– The goal isn’t just compliance, but insight
– And the human brings in real-world nuance, not just prompts
Otherwise, it’s just another autocompleted to-do list.


**PART 4 – Grounding and Dialogue: How (and Why) We Need to Teach AI**

Let’s start with a line from Joe that stuck with me:
“I haven’t found AI to be good at understanding broad contexts or domains, but I imagine it will improve as models become larger and more sophisticated.”

That, right there, is what I would call an unintentional admission of the grounding problem.

What is grounding?
In simple terms, grounding means that an AI model doesn’t just throw around plausible-sounding words — it actually ties those words back to something real.
It means anchoring the model’s language and output to:
– real-world meaning,
– actual context,
– domain knowledge,
– or reference points grounded in practice and consequence.

It’s the difference between saying “revenue growth dropped in Q2” because the sentence sounds right, and saying it because you understand what “revenue,” “growth,” and “Q2” mean inside that particular business context.

Why this matters — especially in data modeling

Let’s be clear: AI can do surprisingly well when the frame is narrow. When the prompt is clear. When the structure is known.

But ask it to think conceptually about modeling — say, to evaluate tradeoffs between snapshot vs. event-based representation, or to interpret a fuzzy request from a stakeholder — and things start slipping. It can mimic insight, but often it’s just echoing patterns. Not reasoning. Not grounding.

That’s what Joe’s quote points to, even if not explicitly.

AI still doesn’t really know what it means when someone says:
- “We’re debating the ‘migrational risk’ of moving these tables.”
- “What’s the long-term effect of schema change X on compliance reporting?”
- “Can we trust this as a proxy for engagement?”

It processes these as sequences of tokens. Not decisions. Not tradeoffs. Not consequences.

Analogy time

An ungrounded AI is like a data model with no schema references and no foreign keys.
It has structures, but they don’t relate to anything real.

It “hits” but doesn’t “understand.”
It “says” but doesn’t “see.”
It gives you words without experience.

That’s fine for autocomplete.
It’s a problem for actual thinking.

Why is grounding so hard in AI-assisted data modeling?

Let’s break it down.

* There’s no universal “map of reality.”
Every data model is a selective, opinionated slice of the world. It’s not objective truth — it’s a reflection of what matters to a particular org, in a particular moment, for a particular purpose.
So unless the AI has access to:
- the business context,
- the decision rationale,
- stakeholder intent,
- and modeling tradeoffs...
…it can’t really “know” why a schema looks the way it does. It can’t guess your worldview. And grounding is all about worldview alignment.

* The gap between language and model logic is wide.
Let’s say a stakeholder says: “We want to find customers who were inactive but then came back after 3 months — but only if they used mobile.”
Simple enough? Nope.
To translate that into a model, the AI would need to figure out:
– What counts as “activity”?
– Where is it stored? In which tables?
– How do we define “inactive”? Absence of events? A status column?
– What’s the time window logic?
– What does “mobile” mean — device type, channel, or app version?
This is not entity extraction. It’s semantic translation + domain alignment + structural inference. And right now, AI fumbles that mix — unless it’s guided.

3. Modeling decisions are often implicit
Ask any seasoned data modeler why a certain field is denormalized, or why a join is built the way it is, and the answer is often:
– “We did that to avoid a 15-minute runtime.”
– “It was for a BI report that used to crash.”
– “We never trusted the source system’s timestamp.”
These aren’t errors. They’re embedded tradeoffs — but they’re almost never documented.
An AI can’t see these unless you surface them. And because most orgs don’t externalize this reasoning, AI ends up modeling off an incomplete map.

So… what actually helps?

How do we make progress toward grounded AI in data modeling?
Here are three realistic — and complementary — strategies.

* Human-in-the-loop metamodeling
This is the most practical and immediately usable method.
You, as a data engineer or architect, stay in the loop — not just prompting, but teaching.
That means:
– Giving examples.
– Explaining intent.
– Offering correction when the AI generalizes too much.
– Running short feedback loops with clarifying questions.
It’s not prompting. It’s co-creating. And yes, it’s slower — but the outcome is structurally smarter AI output.
Think of it as few-shot teaching + dialog-based refinement + reflective interaction.

* Retrieval-Augmented Modeling (RAM)
Think of it as a variant of RAG (retrieval-augmented generation), applied to modeling.
Let’s say your AI system has access to:
– a history of data models,
– semantic layer docs,
– versioned dbt projects,
– architectural diagrams.
Now imagine prompting it with: “How did we model 'refund event' in similar projects?”
Instead of generating from scratch, the AI retrieves relevant past examples — tables, definitions, relationships — and uses that to scaffold a grounded suggestion.
But for this to work, your organization has to structure its knowledge first. AI can’t ground itself in what it’s never seen.

* Ontology-driven grounding
This is the most advanced — and also the least widely implemented.
Here, the organization defines machine-readable conceptual ontologies:
– What is a “customer”?
– What is a “contract”?
– What events can be tied to a “session”?
– What’s the temporal logic of a subscription?
If this information is encoded (think: JSON-LD, RDF, custom vocabularies), then the AI doesn’t need to guess meanings from surface form — it can resolve them structurally.
Right now, very few companies do this. But those that do will have a huge advantage in AI-assisted modeling down the line.

Final thoughts — what to do now
If you want to use AI for real, grounded data modeling today, here’s what works:
– Run use-case driven, back-and-forth conversations with the model.
– Think of yourself as the grounding mechanism — not just a prompter.
– Bring your own examples, business context, data samples, and modeling constraints.
– Don’t just ask for models — help the AI understand why you’d accept or reject its ideas.
That’s how it learns.
Because if it doesn’t ground in your world, it’s just building castles in the air — nice-looking, statistically likely... but structurally disconnected.
And honestly? That’s worse than being wrong. That’s being confidently off-base.
