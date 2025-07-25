# The Thinking Machine Enters the Ring (AtCoder x IMO x AGI)

#### **Altenative Titles:**
* What If AGI Already Knows? (2025, AtCoder, IMO)
* Between the Prompt and the Proof
* 2025: Prompt and Conquer
* I Thought, Therefore I Prompted
* Debugging Meaning
* The AGI That Won’t Say Its Name
* Sleeping Models, Waking Minds

The Silent Layer (Semantic × Reasoning x AGI): I call it the Silent Layer. That part of our models that isn’t loud like code or fast like GPU — but holds the key to general reasoning: semantics. And not just semantics alone — but semantics in the service of reasoning. Call it what you want — this is where meaning stops whispering and starts thinking.

## **Part 00** – Confession and Recommendation

> **TL;DR:**
> 
> This piece is not a polished article in the classical sense. It’s more like a notebook of ideas: trying to grasp the philosophical, technical, and strategic layers of the AI–human rivalry sparked by the AtCoder 2025 and IMO 2025 competitions – from many angles, and in depth.
> 
> I’ll admit it: I simply don’t have the time, so aiming for an O’Reilly-quality peer-reviewed text, especially in two languages, is just not realistic.  
> What you’ll find here is a stream of thoughts, interspersed with tables, experiments, and broken down into structured parts.  
> 
> **My suggestion for reading:**  
> Don’t try to digest it all at once.  
> **Browse, pick and choose!**  
> Just open the paragraph, table, or section that really interests you.  
> That way, perhaps the complexity will become an enjoyable experience.


## **Part 01** – AtCoder 2025: what was known in advance?

> **TL;DR:** Let’s take a look at what kind of competition this was, what was new in 2025, and what could be anticipated in the duel between AI and humans.  
> A human victory was far from guaranteed — but it couldn’t be ruled out either.

### **What was the task?**
As part of the **AtCoder World Tour Finals 2025**, a _special exhibition match_ was organized — a direct clash between **AI and human participants**.  
The challenge fell into the category of **heuristic optimization problems** — typically **NP-hard** problems where finding the absolute best solution is practically impossible, but where various algorithms can search for good, near-optimal results.

Examples of such tasks include:
*   Route planning between cities (TSP)
*   Resource allocation optimization
*   Ranking combinatorial configurations
*   Timetable or graph structure optimization

### **What does “exhibition match” mean?**
An **“exhibition match”** is a type of contest that **does not count toward the official results**, and is held for **demonstration or experimental purposes**. Its goal is to **test new ideas**, or to **assess capabilities** in a new scenario — and it’s often designed to be a bit of a spectacle, too.

### **Exhibition match in the case of AtCoder 2025?**
The official AtCoder World Tour Finals (AWTF) championship match was **strictly between human competitors**, and the winner was decided based on that. However, **in parallel** or right after the finals, a separate **“human vs. AI” match** took place:

#### **Its purpose**
*   To test how well an **AI agent** could perform against the world’s top human algorithm developers.
*   To **demonstrate** what AI is currently capable of when facing a complex, real-time optimization task.
*   A kind of **technological showcase**: prestige for OpenAI, an innovation moment for AtCoder, and pure thrill for the audience.

#### **Its characteristics**
*   It did **not affect the official human rankings** in any way.
*   The task was the **same** as that of the finalists, but the AI’s performance was measured and evaluated **separately**.
*   It was **not a live duel**, but rather shown in parallel or after the main event.
*   It was a **specially designed** challenge: a heuristic, NP-hard optimization problem where AI’s strengths (speed, repetition, variation) could shine.

### **Why is this exhibition match format important?**
*   **Pushing technological boundaries**: It shows what today’s AI can do in problem spaces that traditionally required human creativity and iterative fine-tuning.
*   **Fair comparison**: Since it doesn’t count toward the official competition, it doesn’t interfere with the human players — yet it allows for direct benchmarking.
*   **A motivational platform**: It inspires developers, researchers, and AI labs to get involved in competitive optimization.
*   **A benchmark opportunity**: It’s a great way to map out areas where AI excels (e.g. speed, scalability), and where humans still lead (e.g. strategic adaptation, intuition).

### **What made this year special?**
*   For the **first time**, an artificial intelligence participated in the AWTF.
*   With the support of **OpenAI**, the AI competed alongside top human programmers.
*   The competition strongly focused on **speed** and **optimization**.

### **Who were the contestants and how did they perform?**
*   The **winner** was the brilliant human contestant **Psyho**.
*   The **OpenAI agent** came in second — it responded with **superhuman speed**, but in terms of solution quality, it didn’t clearly surpass the top human entries.
*   **Sakana AI** followed the event closely and later tested their prototype **ALE-Agent V2** **offline** after the contest ended.

### **What did Sakana AI’s ALE-Agent V2 achieve?**
*   According to their own measurements, it would have ranked **5th** unofficially, submitted as a simulated entry called _fishylene_.
*   Their agent leveraged the **collective intelligence** of multiple LLMs (Large Language Models).
*   The ALE-Agent was built based on the **ALE-Bench**, a new benchmark co-developed with AtCoder.

### **What were the challenges?**
*   These contests are extremely time-sensitive: solutions must be submitted within **short runtime windows**.
*   **Heuristic problems are non-deterministic**, so AI needs to generate and evaluate multiple solution variants.
*   The **OpenAI agent likely ran in a real-time** environment (online inference), while Sakana AI had the advantage of offline optimization.
*   **Model coordination**, **prompting technique**, **exploration-exploitation tradeoffs**, and **solution evaluation** were all critical.

### **Where might Sakana AI’s approach have been better than OpenAI’s?**
Hypotheses based on the post:
*   Sakana AI **combined multiple models**, which allowed for:
    *   _more diverse proposals_
    *   _ensemble-based filtering_ and selection
*   Without real-time pressure, they could try **more complex strategies** (e.g., iterative refinement, multiple initializations, re-ranking).
*   It’s likely that OpenAI’s method relied on a _single model_ or a real-time optimized strategy, which limited the complexity.

### **What comes next?**
*   Sakana AI promised a **detailed blog post** about the techniques they used and how they differed from OpenAI’s.
*   It will likely shed light on:
    *   heuristic uses of LLMs
    *   prompt engineering for AI-based optimization
    *   a comparison of real-time vs. offline competition architectures

### **TL;DR**
* This competition marked a major **milestone** in comparing AI and human problem-solving. While OpenAI's agent was lightning-fast, human contestants held their ground. Sakana AI’s post-analysis suggests that **collective LLM-based strategies** can yield competitive or even superior results — but only when time constraints are relaxed.


## **Part 02** – Why did AI "only" finish second at this year's AtCoder contest?

> **TL;DR:** OpenAI's model came in just behind the winner in a tight race. This section explores potential reasons: time constraints, lack of fine-tuning, and the nature of the problems, which may not always favor generative approaches.

### **One possible explanation: What can a human champion do better?**

*   **A fresh heuristic idea**:
    *   It's possible that the winner, _Psyho_, used a **novel, undocumented, or highly creative technique**—something no one has published, and the AI had no way to know about.
    *   Human contestants often apply **clever “twists”**: subtle greedy tricks or local optimizations that are effective only because of the specific quirks of the task.

*   **Rapid iteration and adaptation**:
    *   A human can **experiment during the contest**, try out partial strategies, and _instantly adapt_ if something seems promising.
    *   AI agents typically stick to **static strategies** or adapt only within a limited feedback loop and timeframe.

*   **Contest-specific know-how**:
    *   Psyho is a seasoned AtCoder veteran—familiar with the problem formats, scoring schemes, and hidden patterns of the platform.
    *   This is **meta-knowledge** that an AI can't easily learn unless it’s explicitly fine-tuned for that contest.

### **Why can't the AI do the same (yet)?**

*   **Limited creative bandwidth under time pressure**:
    *   The competition time is **extremely short** (~2–3 hours), which isn’t enough for the AI to explore hundreds of strategy branches or prompt variations.
    *   Modern LLMs rely heavily on **well-structured prompts**—without good prompting, they default to learned templates.

*   **Refined brute-force with basic fine-tuning**:
    *   OpenAI’s agent likely used an enhanced **brute-force + local search + simulated annealing / beam search** style approach—not a deeply creative prompt-hacking strategy.
    *   These work well across many problem types, but they may **miss domain-specific tricks** that can make the difference.

*   **Lack of tuned intuition or precedent**:
    *   If the human contestant had _intuition_ built from past contests—e.g., sensing which inputs or scoring features to target—the AI likely didn't have that kind of foresight unless it was manually hardcoded.

### **TL;DR (again)**

*   It’s **not that the AI was “bad” or “dumber”**—rather:
    *   The **human adapted better to the actual contest conditions**,
    *   may have had a **creative spark** that AI couldn’t mimic fast enough,
    *   and likely found **better trade-offs** between speed, points, and submission quality.

*   What this event shows is not some grand **“AI vs. human” showdown**, but rather a **real-world stress test** for what today’s AI can truly handle in terms of **reasoning and problem solving**—beyond just memorizing facts.

*   **Bottom line**: On the _live_ leaderboard of competitive programming, AI is catching up fast. But in contests like this, especially in the realm of creative, ad hoc problem solving, **humans will likely remain in the lead for a few more years**.


## **Part 03** – AI is _likely_ to win soon. But not _necessarily_, and not under every condition.

> **TL;DR:** This section anticipates that it’s only a matter of time before AI starts winning. Meta-knowledge, optimized prompting, and increasing compute power will gradually push human competitiveness aside — but for now, the challenge is still alive.

### **YES, because...**
*  **Meta-knowledge _can_ be learned**
    * Today’s AI agents don’t yet “think like contestants,” but **this can be explicitly taught** (e.g. RLHF tuned for contest logic, a “contest curriculum”).
    * Fine-tuning on real competition tasks and ALE-Bench-type benchmarks (like at Sakana AI) aim exactly for this.

*   **Speed and iteration capacity strongly favor AI**
    * A well-scaled AI agent can try out **1000+ versions in seconds**, while a human might manage 3–4.
    * This is especially true for **multi-agent systems** (like Sakana AI used), where several models run in parallel with different strategies.

*   **Prompting and fine-tuning are getting better**
    * Today, prompt engineering is still a key human strength. But the next-gen AI models will **optimize their own prompts**.
    * That means the future AI contestant will be _better at prompt engineering itself_ than a skilled human today.

*   **Hybrid AI architectures are emerging**
    * More AI agents will combine:
        * LLMs (for general knowledge),
        * specialized search algorithms (like Tabu Search, Simulated Annealing, Beam Search),
        * and reinforcement learning-based, self-rewarding adaptive mechanisms.
    * This “holy trinity” is getting very close to _superhuman performance_.

### **BUT STILL: Why isn't it guaranteed that AI wins next year?**
*   **Optimization contests often reward ad hoc tricks**
    * Many tasks hide some “twist”: an edge case or input structure that AI agents struggle to _generalize_.
    * Human contestants often intuitively _feel_ the puzzle-like patterns that AI still _doesn't_ learn well.

*   **Hard stop: time and compute limits**
    * In real contests, AI agents **can’t run endlessly**. If you've only got 2 hours and no GPU cluster, executing your best plan becomes hard.
    * If the AI misprioritizes strategy — time’s up. Tactical thinking _optimized for contest time_ isn’t perfect yet.

*   **AI’s ceiling still depends on the search space**
    * In NP-hard problems, the **explosion of the search space** means even AI has limits.
    * If the best solution _can’t be approximated_ within 20–30 seconds of iteration, human ingenuity still has a chance.

### **Verdict: When will AI dominate?**
| Year | Likely AI victory? | Why |
| --- | --- | --- |
| 2025 | 50-50 | Humans still think more creatively; AI dominates in speed |
| 2026 | 70% | Tuned, multi-model AI agents deployed |
| 2027+ | >90% | AI trained specifically for contests, adaptive and self-prompting |

### **Closing note**
> **AI will win – not because it’s “smarter,” but because it learns faster and generalizes better.**
* The future of these contests isn’t “human vs. AI,” but rather:
    * **Human + AI** (as coach and agent)
    * or **AI vs. AI**, where even prompting becomes a learned competition tactic.


## **Part 04** – Algorithmizing Creativity

> **TL;DR:** This is where the classic "chess analogy" falls apart: here, the rules change every year. Creativity doesn’t mean combinatorial genius — it’s about the ability to adapt to shifting goal functions.  
> That’s a human strength — but for how long?

> **“Can creativity be algorithmized to the point where an AI can beat humans in general-purpose optimization contests — just like it happened in chess and Go?”**
That’s a **very deep question**, and the answer can only be nuanced. So let’s take a **structured approach**.

### **Comparison: Chess/Go vs. AtCoder Heuristic Optimization**
| Property | Chess / Go | AtCoder Heuristic Challenges |
| --- | --- | --- |
| State space | Well-defined, closed, finite | Often enormous, combinatorially explosive |
| Rule set | Fixed, fully known | New and ad hoc every contest |
| Objective function | Clear: you must win | Specific scoring system, often complex and nonlinear |
| Fully solvable? | In theory yes (though Go is too large) | No, NP-hard or NP-complete problems |
| AI advantage comes from | Search + self-play + value network | Search + LLM + heuristics + meta-learned intuition |
| Human creativity's role | Shrinking | Still highly present |

So yes, **the pattern looks similar**, but **AtCoder-style problems are still not deterministic, not "closed-world games"**. That’s why **AI can’t yet dominate them** as easily as it did in chess or Go.

### **So is creativity algorithmizable?**
**Yes — gradually, more and more so.** But not by "coding creativity," rather by:
* Learning **meta-heuristics** (e.g. “this kind of input → this kind of solution is worth trying”).
* Automating **prompt generation and evaluation**: models can **prompt themselves**, “creatively”.
* Using **diversity-based AI collaboration**: multiple models run in parallel → multiple ideas → comparative evaluation.
* **Competition-specific fine-tuning**: an AI can learn from what worked well in past contests, and what the winning tricks were.

### **So when will AI start to dominate?**
* In **chess** and **Go**, AI dominance came from:
    * → closed systems
    * → strong feedback (self-play)
    * → billions of simulation loops
* In **AtCoder-type problems**:
    * → _every task is new_, no pre-learned loops
    * → varied input structures, many rule types
    * → short contest window: **2–3 hours, no billion-round self-play**

**So we’re not there yet.** But the **trend is clear**: as models get better at _learning general creative heuristics_, and better at _prioritizing in solution space_, **the tipping point will come**.

### **Conclusion**

We started with the question:

> **“If creativity is algorithmizable, are human contestants doomed?”**

* **Yes, if**:
    * contests keep using algorithmically accessible structures,
    * AI models learn to operate at the _meta level_ (not just solving, but understanding, classifying, adapting),
    * and sufficient compute becomes available _within_ contest time.
* **But no, if**:
    * contests start demanding **intuitive creativity and unformalizable patterns** (like "competitive poetry" for AIs),
    * or if organizers write **intentionally anti-AI tasks**, designed to confuse learned patterns.

### TL;DR
> **Creativity _can_ be algorithmized — but not linearly, not quickly, and not in every context.**
* In chess, the AI takeover has happened.  
* In optimization contests — **not yet — but it’s coming.**
* And these **in-between years** are the most fascinating.  
  Right now, **humans and AIs amplify each other’s creativity**, not replace it.


## **Part 05** – Well-known Prompting Techniques with ChatGPT

> **TL;DR:** A quick overview of free-running, vine.coding, and other popular LLM usage styles.  
> They’re intuitive and fast – but simply not enough when tackling NP-hard problems. That’s when you need a different approach.

### **Free-running**

Prompting within ChatGPT’s conversational context

> This refers to a **freeform, unstructured, iterative dialogue**, where the user doesn't start with a specific prompt but explores interactively alongside the AI.
*   Key traits:
	*   No predefined prompt or template involved
	*   The conversation evolves organically – often branching in different directions
	*   The user reacts to the AI’s ideas and fine-tunes things on the fly
	*   Often used for learning, brainstorming, philosophical exploration, or creative writing
* Example: “I don’t really know what I want yet – I’ll just start chatting with ChatGPT and see where it goes…”

### **Vine.coding**

Sometimes written as vine-coding or vine-prompting in the community

> A **coding (or prompting) style** where the user builds **step-by-step**, like a growing vine – starting with a small request, then expanding, modifying, or branching off as needed.
*   The core idea:
	*   You don’t write a _perfect prompt_ right away – instead, the solution grows over time
	*   Lots of “Now add this…” or “Can you rewrite it in this style…” type requests
	*   In coding: you begin with a scaffold, then enrich it, then refactor – but all of this happens through live interaction with the AI
*   Why the name “vine”?
	*   A vine is a creeping plant that **grows organically and spreads sideways** – unlike a “waterfall” or “pipeline”-style prompting workflow.

### **How It Connects to Other Ideas**
*   These techniques are closely related to **conversational programming** or **collaborative coding**.
*   And they stand in contrast to **one-shot prompting** or **structured chain-of-thought prompting**.

### **TL;DR**

| Concept | What It Means | When You Use It |
| --- | --- | --- |
| Free-running | Freeform, unstructured, exploratory dialogue | Learning, creativity, idea generation |
| Vine.coding | Organic, stepwise, iterative coding with AI | Prototyping, refactoring, fine-tuning |


## **Part 06** – Prompting the OpenAIAHC Model

> **TL;DR:** Here's a likely take on OpenAI’s strategic approach during the AtCoder finals: a beam search-based, structured prompting pipeline — fast, general, but not easy to fine-tune.

* In the 2025 AtCoder World Tour Finals showcase match — where the **OpenAI Atcoders Heuristic Competition** model competed against human challengers in an **NP-hard heuristic optimization task** — evidence suggests that OpenAI **did not rely on free-running or vine.coding styles**, but rather on **a much more structured approach**:  
* **OpenAI’s likely style: “Prompt pipeline + Heuristic core”**. This means **precisely constructed, well-scripted interactions**, closer to:

    * **Structured Prompt Chains / System Prompting**
        * The system used **predefined prompts** like:
            * "You are solving a resource allocation problem..."
            * "Generate 10 greedy heuristics for minimizing overlap under constraint X..."
        * Instead of organically growing ideas ("vine" style), it **strategically embedded** them.

    * **LLM-as-module paradigm**
        * The LLM acted as **one component** within a larger system:
            * LLM → idea generation / heuristic synthesis  
            * → then combined with classical algorithms (e.g., beam search, local search)  
            * → followed by evaluation, selection, and iteration (likely offline)

    * **Time-boxed multi-agent strategy**
        * Most likely, **multiple strategies ran in parallel** (similar to Sakana AI’s approach), competing for the best score. This was essentially an **auto-promptor ensemble**.

### **Why not vine.coding?**

* **Vine.coding** is all about **human-AI interaction** — you gradually build up the prompt:  
"Now add this", "Try with that", "Let's tweak this..." — it's a live co-building process. But in the AtCoder match, **there was no human in the loop**. The AI ran **fully autonomously** — not in a back-and-forth conversation, but with a **predefined strategy**.

### **Why not free-running?**

* **Free-running** works best when you're not under time pressure and optimization isn't the main goal. In a 2–3 hour, score-based, rigorously measured competition, there's simply **no room for wandering exploration**.

### **TL;DR – So what was OpenAI’s style, really?**

* **"Structured AI-agent with prebuilt heuristics and fixed strategy paths"**.  
It didn’t chat, didn’t vine, didn’t roam freely — it just **executed what had been built in beforehand**. Fast, effective, almost robotic.


## **Part 07** – A tangible demo example for all three steps of the "Prompt-pipeline + Heuristic core", illustrated with an NP-hard problem

> **TL;DR:** Here’s a concrete example of how an AI problem-solving system is built from three components: prompting, heuristics, and feedback. Iteration is its superpower – and also its bottleneck.

### **Problem (NP-hard): Maximum Coverage Problem (MCP)**
> **Input**: We have a list of sets (S₁, S₂, ..., Sₙ), each a subset of a universal set.  
> **Goal**: Pick k sets such that their union covers as many elements from the universe as possible.
*   This is NP-hard because we’d have to try **all k-element combinations**, and that explodes fast.
*   **OpenAI-style approach: 3 steps**

#### **Step 1:**
* Prompt: **"Generate heuristic strategies"** from an LLM
```plaintext
You are solving the Maximum Coverage Problem.
Input: A list of subsets S = [S1, S2, ..., Sn] from a universe U.
Goal: Pick k subsets to cover as many elements of U as possible.

Generate 5 different heuristic strategies for selecting the k sets, each using a distinct principle (e.g., greedy, probabilistic, diversity-based).
Output each heuristic as a short pseudocode description.
```

* Imaginary LLM response:
```plaintext
1. Greedy by Coverage: At each step, pick the set that adds the most new elements to the current union.
2. Weighted Density: Pick the set with the highest ratio of new elements to total size.
3. Randomized Greedy: With 80% probability pick greedy-best, otherwise pick randomly.
4. Diversity-aware: Choose sets that cover elements not only many times, but also rare ones.
5. Local Swap: Start with a random k-collection, then swap sets if the coverage improves.
```

#### **Step 2:**
**Heuristic Core: implementation and evaluation**
* Input:
```python
U = {1, 2, 3, 4, 5, 6, 7, 8, 9}
S = [
    {1, 2, 3},
    {4, 5},
    {1, 4, 7},
    {6, 8},
    {2, 5, 9},
    {3, 6},
    {7, 8, 9}
]
k = 3
```
Heuristic #1: Greedy by Coverage
*   **Steps:**
    *   Start with `selected = []`, `covered = set()`
    *   Repeat k times:
        *   For each set, calculate how many new elements it adds to `covered`
        *   Choose the set with the highest number of new elements

```python
selected = []
covered = set()

for _ in range(3):
    best = max(S, key=lambda s: len(s - covered))
    selected.append(best)
    covered |= best
    S.remove(best)
```

*   Result (one run):
    1.  pick: `{1, 2, 3}` → new = 3 elements  
    2.  pick: `{4, 5}` → new = 2 elements (1,2,3 already covered)  
    3.  pick: `{6, 8}` → new = 2 elements  
*   Total coverage: 7 elements  

#### **Step 3:**
**Iteration / another prompt pipeline**

If the result isn’t good enough, new prompt:
```plaintext
Given that "Greedy by Coverage" produced only 7/9 coverage, generate 3 hybrid heuristics that combine Greedy with Randomization or Swapping to improve performance.
Each heuristic must be described in short pseudocode.
```

LLM response:
```plaintext
1. Greedy+Swap: Run greedy, then perform local swaps to improve coverage.
2. Beam-Greedy: Keep top 2 partial solutions at each step, not just best.
3. Probabilistic Greedy: Assign probabilities to candidates based on coverage gain, sample one.
```

The system then feeds this back into the Heuristic Core and re-runs it.

### **So what is the AI doing here?**
*   It’s not “free thinking,” not “vine.coding,” not “chat-style”
*   **Prompts are used to generate heuristics** (via LLM)
*   **Low-level evaluation code** (Python, C++, Rust, etc.) measures performance
*   Prompts are **iterated**, but not by human dialogue – by an automated feedback loop

### **TL;DR – Prompt-pipeline + Heuristic Core, in one iteration**
| Phase | Tool | Example |
| --- | --- | --- |
| 1. Prompting | LLM | “Give me 5 heuristics for MCP” |
| 2. Code + execution | Heuristic Core (e.g., Python) | Greedy heuristic runs in 3 steps |
| 3. Iteration | New prompt or strategy shift | “Give hybrid methods with swap or randomness” |


## **Part 08** – Is this “Prompt-pipeline + Heuristic core” just a temporary phase or the final form? Could a radical, paradigm-shifting evolution come?

> **TL;DR:** It’s a fair question: is this method only good for contest problems? The answer: no.  
> This section explores where and how this strategy might be useful in business or other real-world domains.

*   In short: **Yes, it could happen.** What we’re seeing now is most likely a **temporary hybrid**, not the final shape. And there are at least **3 major future directions**, which could be either **evolutionary refinements** or actual **paradigm shifts**.

### **Autonomous Prompt-Agents: prompt loop as intelligence**
* Vision: Instead of a human (or system) iterating the prompts, the **AI itself “thinks” in prompts**.
* The AI’s inner prompt game:
```plaintext
(1) It generates a strategy,
(2) Then asks itself: “Where could this fail? What edge cases?”
(3) It generates a counter-prompt → a new heuristic
(4) It pits them against each other and learns from the result
```
* Paradigm shift?  
    *   **Yes!** Because here the **prompt becomes the unit of learning**, not just a tool.  
    → This is something like “LLM creativity with internal iteration.”  
    *   Preconditions:  
        *   Internal “critical thinking” (self-reflection)  
        *   Meta-analysis of prompts and heuristics  

### **Neuro-symbolic or structure-aware LLMs**
* Vision: Instead of text-based heuristics, the model directly does **structure manipulation**:
    *   It generates, evaluates, and modifies graphs
    *   It formalizes constraints (e.g., via Z3 or SAT logic)
    *   It “thinks” mathematically, natively
* Paradigm shift?
    *   **Yes.** Today’s LLMs work with **linguistic constructs**, not abstract structures.  
    An **LLM that “understands” graph structure** could directly solve something like a vertex cover problem using **graph transformations**, not just pseudocode.

### **End-to-end NeuroHeuristics (i.e., heuristic-learning models)**
* Vision: A model doesn’t just generate a strategy from prompts, it **learns the entire optimization workflow**:
    *   Input: problem specification (natural language or formal)
    *   Output: step sequence (choices, mutations, estimates)
    *   Learning: Based on RL or imitation learning (trained on contest data)
* Example:
```plaintext
Model: “This problem reminds me of task 4 from AWTF 2023. The Swap+Diversity strategy worked well there. I’ll try that first.”  
→ The model taps into its own “heuristic memory.”
```
* Paradigm shift?
    *   **Yes.** It doesn’t build from prompts anymore, but **learns directly on the strategy/code level**.  
    *   This is the “AlphaZero for combinatorial problems” vision.

### **Subtle, evolutionary improvements (if no paradigm shift occurs)**
* Even without a big leap, the current pipeline could evolve significantly:
    *   **Automatic prompt prioritization** (deciding which ideas to try under time pressure)
    *   **Heuristic auto-ensembling** (like weak learners → boosting)
    *   **Input profiling → strategy selection** (“if lots of overlap, then choose diversity-based approach”)
    *   **Plug-in solver architectures**: LLM + SAT-solver + constraint propagator, all in one runtime

### **Summary: What’s next – evolution or revolution?**
| Direction | Degree | Example | Paradigm shift? |
| --- | --- | --- | --- |
| Prompt prioritization, benchmark learning | 🟡 Refinement | “Run top 3 heuristics based on time budget” | No |
| Auto-promptor agent | 🟠 Mid-level | Internal LLM-loop on itself | Yes |
| Structural reasoning | 🔵 Strong | Graph-manipulating LLMs | Yes |
| End-to-end neuroheuristic solver | 🔴 Powerful | AlphaZero for optimization | Yes |


## **Part 09** – Scope of Prompt-pipeline + Heuristic core

> **TL;DR:** Turns out this method isn’t just for NP-hard problems — it can be broadly useful if you're intentional enough about how you structure your questions.  
> It’s about a new kind of “thinking style.”

> Does this _Prompt-pipeline + Heuristic core_ method **go beyond NP-hard problems**?  
> Can it **still be useful**, even when the task itself **isn't hard** — maybe even _trivial_?  
> Can it replace _free-running_ or _vine.coding_ styles in **everyday human iterative workflows**?

### **Short answer**  
**Yes — but only if your thinking space is more complex than the task itself.**

* The strength of this method isn’t that the problem is hard. It’s that you **don’t know in advance what to do**. That’s why even “hello world”-type problems **can justify the pipeline** — but only when:
   * you don’t know what kind of “hello world” is needed;
   * or you’re unsure about **the style**, the framework, or the purpose of that “hello world”;
   * or you’re picking from a thousand “hello worlds,” not knowing which one truly fits your goal.

### **Extended example: Prompt-pipeline on a “too simple” task**
*   **The task:**  
> “I need a simple table that shows the difference between batch and streaming processing.”
*   A **trivial** task for a pro. But then the person adds:  
> “But I want one that a junior data handler can understand. And I’d like to send it to my boss in Excel, who doesn’t like to see English words. Also, I’d love it to be expandable with Spark examples later.”
*   Whoa. Suddenly not so trivial. Because:
		*		there are **multiple criteria** you have to balance at once,  
		*		there’s **no single ‘correct’ answer** — several could work,  
		*		and you need a **structured iteration** process.  
*   So what does the prompt-pipeline do here?
		*		**Prompt 1: “Give me 3 different table formats that clearly show the difference between batch and streaming.”**  
		*		**Heuristic core: a human or script picks the best — or merges them.**  
		*		**Prompt 2: “Translate this into clear Hungarian, avoiding technical jargon.”**  
		*		**Prompt 3: “Suggest how this could be extended with Spark examples in a non-distracting way.”**  
*		The task is trivial. **But building the answer is complex.**

### **Conclusion: when is the pipeline not worth it?**
*   This method **isn’t for** you if:
		*		you know exactly what to ask for, and it’s deterministic (e.g., “Print numbers from 1 to 10 in Python”);  
		*		there’s only one way to answer it, no style choice, no decision space;  
		*		or you do 1–2 iterations in your head and you’re done.  
*   It **is for you** when the task is simple — but the goal is complex or fuzzy. Like when you’re asked to make “just” a PowerPoint slide, but you also want it to carry a political message.

### **Free-running / vine.coding vs. pipeline**
| Style | When does it shine? | How does it work? |
| --- | --- | --- |
| Free-running | For exploration, open-ended thinking | The answer “wanders into place” |
| Vine.coding | For building iteratively in small blocks | Step-by-step, organically grows |
| Prompt-pipeline | Structured, multi-step goal optimization | One prompt generates, core evaluates, new prompt kicks in |
*   Pipeline **doesn’t replace** free-running — but it **summarizes**, systematizes, and makes it reusable.

### **TL;DR**  
> “Prompt + heuristics” is not just a way to **muscle through hard tasks**,  
> it can also serve as a **skeleton for unstructured thinking**.
>
> It helps even when the problem isn’t hard — it’s just that **your brain sees too many ways to solve it**.
*   It’s **not the complexity of the problem** that decides whether you need an _AI strategy_ — it’s whether your own approach is structured or not.
*   And sometimes even a **“Hello World”** is like a political speech: it’s not about what you say — it’s about _to whom, how, with what intention, and what worldview it supports_.

> **Could this method be a framework for structuring our thinking — even if the task doesn’t demand it?**
*   The answer: **Yes, if the uncertainty lives not in the answer, but in us.** And honestly, **that’s a beautiful idea — not just a practical one.**


## **Part 10** – The 2025 AtCoder World Tour Finals Heuristic Contest is Over

> **TL;DR:** In this post, I’ll walk you through the actual contest task.  
> I’ll clarify what the problem was, why it's NP-hard, and how heuristic strategies were used to tackle it.  
> This was the heart of the competition.

Let me briefly and clearly summarize the challenge called  
**“A – Command Centers and Wall Design”**.

### **The task in plain English**
Imagine a **30×30 grid map**, where:
*   there are **K robots** (between 10 and 100), each with a start and a goal position,
*   there are some **walls** between the cells (some are pre-generated, and we can build new ones too),
*   the goal is to **get all robots to their destination** with as few moves as possible.

### **The solution has three phases**
*   **1. Preparation:**
*   You can **build walls** anywhere (between neighboring cells).
*   You can also **assign robots into groups** (to move several at once).
    *   A robot can only belong to one group.
*   **2. Movement:**
*   Two types of commands are allowed:
    *   **Group command**: move all robots in a group in one direction (U/D/L/R), **at once**.
        *   Important: if there’s a wall or another robot blocking the way, it won’t move.
        *   Execution order matters too: “the farthest robot moves first.”
    *   **Individual command**: move one specific robot in one direction.
*   **3. Evaluation (Scoring):**
*   The goal: **fewer total commands**, and robots as **close as possible to their goals**.
*   **Scoring formula**: Score = T + 100 × Σd_k  
    *   `T`: number of total commands issued,  
    *   `d_k`: the **Manhattan distance** between the `k`-th robot and its goal at the end.  
*   The **lower**, the better. The system also applies **relative scoring** compared to other participants.

### **Why is this task difficult?**
*   Robots can **collide** and **block each other**.
*   Strategic **wall placement** is critical: too many walls limit movement, too few cause chaos.
*   **Group assignment**: poor grouping leads to poor coordination.
*   The **order and tactics** of movement commands is complex: one wrong step can mess up the whole squad.

### **Types of heuristic approaches AI might use**
*   **Initial reachability analysis**: pre-simulating shortest paths from start to goal.
*   **Wall optimization**: graph-based clustering to figure out where to “close” the traffic.
*   **Group generation**: clustering based on goals, routes, or geography.
*   **Movement planning**: greedy or beam search to minimize the combined T + Σd_k score.

### **TL;DR**
*   **Task**: Guide robots to their goals on a grid, with the help of walls and group commands.  
*   **Goal**: Fewer commands, smaller remaining distances.  
*   **Challenge**: Smart coordination, collision avoidance, and command sequencing.


## **Part 11** – Proof: The AtCoder 2025 problem is NP-hard

> **TL;DR:** Here's the math to back it up — this problem really is NP-hard.  
> We'll show there’s no known polynomial-time algorithm, and why only heuristics stand a chance.

> The proof is done by **reduction** — that is, by **transforming the current task into a known NP-hard problem**. This is the classic way to demonstrate the hardness of a new problem.

### **Goal: Prove that the **AtCoder 2025 Heuristic A problem** is NP-hard**  
*   **Strategy:**  
    *   We'll reduce the task to a **known NP-hard** problem.  
    *   That means: if our problem *could* be solved in polynomial time, then we *could also* solve a problem that's already known to be *not* solvable in polynomial time (assuming P ≠ NP).  

### Chosen NP-hard problem: **Multi-Agent Path Finding (MAPF)**
*   In the **Multi-Agent Path Finding (MAPF)** problem:
    *   we’re given a grid (or graph),
    *   with several robots, each having a start and a goal position,
    *   each robot can move one cell per time step,
    *   **they can’t collide**, share a cell, or swap places,
    *   goal: get all robots to their goals in the **fewest possible steps**.
*   This is a **well-studied, proven NP-hard** problem.  
    *   Source: [Yu and LaValle, 2013](https://ieeexplore.ieee.org/document/6645806), among many others.

### **Reduction: the AtCoder problem is at least as hard as MAPF**  
*   **The AtCoder task embeds MAPF as a subproblem**
    *   Robots have **start and goal positions**.
    *   No collisions, no overlapping → **same collision rules**.
    *   Goal: move all robots to their targets in **as few steps as possible** → **same objective**.
*   **Group commands make things even harder**
    *   In MAPF, robots move individually → more control.
    *   Here: **group commands limit your freedom**, so it's more complex.
    *   “Individual command” is allowed only K times per round, so group commands can’t be avoided in the long run.
*   So: **even just the robot control part matches MAPF-level difficulty**, and the wall-building and group assignments **only expand the search space further**.

### **Logical sketch of the argument**  
*   **Claim**: The AtCoder problem is at least as hard as MAPF.
*   **Why**:
    *   MAPF can be *reduced* to the AtCoder task: put each robot in its own group, don’t build walls, use only individual commands → same rule system.
    *   If the AtCoder task were solvable in polynomial time, then so would MAPF be → but MAPF is NP-hard ⇒ contradiction.
*   **Conclusion**: The AtCoder task is **NP-hard**.

### **TL;DR – Proof in short**
*   The robot control part of the task **embeds a classic NP-hard problem** (MAPF).
*   Group commands and wall-building even **increase** the difficulty.
*   Via reduction, we showed: **if we could solve this efficiently, we could solve MAPF too** — but we can't, so this one is NP-hard too.


## **Part 12** – Psyho’s Commentary on the AtCoder 2025 Finals

> **TL;DR:** The winner’s post offers a glimpse into what really matters in a contest like this: sleep deprivation, compute budget, and the surprising fact that beam search wasn’t even necessary in the finals.

* The winner, Psyho, posted the following on X:
   * My comment on people betting on humans vs AI aspect. It's silly, because the result depends on: - problem itself - compute budget - testing budget - variance in human performance (non-JP will be sleep deprived) - amount of work put towards finetuning agent for AHCs 
   * I think my good TCO performance comes from the fact that none of the finals' problems ever required beam search. Not sure if was too obvious about that

* This comment is quietly powerful — especially considering that **he beat OpenAI’s AI agent as a human**, in an NP-hard, heuristics-driven optimization task. Let’s take a closer look at it, unpacking both technical and strategic context.

### **“My comment on people betting on humans vs AI aspect.”**

* _“It's silly...”_ — In other words: this whole “human vs. AI” framing is **misleading**.
Psyho’s saying: it’s **nonsense to oversimplify** the contest into a man-versus-machine duel, because **the outcome is shaped by many external factors**. And he lists them:

* **“- problem itself”**
The **type and structure of the problem** greatly influences **who has the upper hand — human or AI**.
* If the task is highly structured with many learnable patterns → it **favors AI**.
* If it’s ad hoc and rewards clever tricks → it **favors humans**.
This particular problem (robot control, group coordination, wall building) was **a one-of-a-kind combo**, where creativity played a big role.

* **“- compute budget”**
For the AI, it makes a huge difference how much **machine time**, parallelization, GPU power, or fine-tuning is allowed.
* More compute → more heuristics can be tested
* Beam search, reinforcement learning, auto-looping prompts → **only work well when there’s enough time and compute**
It’s possible that OpenAI’s agent **ran in real-time inference mode**, not with days-long training or tuning — which clearly **limited** its performance.

*   **"- testing budget"**  
To do well in this kind of competition, it's not enough to just develop your agent—you have to **test it a lot**. Different random seeds, input variants, edge rules... you name it.  
*   Testing and benchmarking AI agents is also **compute-intensive**.  
*   As a human, Psyho could **interactively fine-tune** his strategy based on temporary test results.

*   **"- variance in human performance (non-JP will be sleep deprived)"**  
This one's very human—but absolutely valid: the **contest was held on Japanese time**, so non-Japanese competitors (like Europeans or Americans) had to **stay up all night** to focus.  
That's a **real disadvantage** that distorts the “human vs AI” narrative even more:  
*   the AI doesn’t get tired,  
*   but humans do—especially near the end of a long contest.

*   **"- amount of work put towards finetuning agent for AHCs"**  
This might be the **most important point**:  
*   AI performance **heavily depends** on how **specifically it was fine-tuned** for this exact kind of problem.  
*   AHC = AtCoder Heuristic Contest (a family of contests like this)  
If the AI agent is designed as a _general problem solver_, it might be **at a disadvantage** compared to a human who’s seen **hundreds of AHC problems** and has developed their own “metaheuristics.”

### **"I think my good TCO performance comes from the fact that none of the finals' problems ever required beam search."**
* This is probably the **deepest technical message** in the whole thread—a clear statement on AI and algorithmic style.  
   * What is **beam search**?  
      - It's a **heuristic search algorithm** that:  
      - keeps multiple “most promising” partial solutions **in parallel** (this is called the “beam width”),  
      - expands from those while keeping only the most promising ones,  
      - **doesn't explore everything** like brute force, but explores **more paths** than greedy.  
   * It’s often used in AI agents, language models, game trees, pathfinding, and so on.  

* What is Psyho saying?  
> In the TopCoder Open (TCO) finals where he performed well, **not a single task required beam search as an optimal strategy**.  
   * Meaning: he’s **not the kind of contestant** who cracks open the whole search tree with brutal compute.  
   * He’s more into **precise, minimalist, optimized, ad hoc strategies**.  
   * And this is **key** in the AI vs human showdown:  
      * AI **loves beam-search-like strategies**, where you can learn or evaluate from a wide search space.  
      * Psyho **dominates in contests** where there’s no room for beam search → that is, where the **search tree is small, but you need insight and intuition**.

### **TL;DR – What is Psyho really saying?**  
*   The question “who wins, human or AI?” is **shallow and misleading**.  
*   The outcome of a contest depends on many things: the task itself, compute budget, human exhaustion, AI tuning depth.  
*   His edge came from the fact that **the problem didn’t need hardcore AI-style tricks** (like beam search), but could be solved with **intuitive, simple, elegant ideas**.  
*   So: **human intuition still works**—as long as the task is written in a way that’s **not “AI-compatible.”**


## **Part 13** – Technical comparison table for the competition strategies**

> **TL;DR:** This section shows how Sakana AI’s agent approached the challenge.  
> A follow-up post will compare it with OpenAI and Psyho strategies.  
> It turns out that the collective LLM-based strategy worked surprisingly well — even if not within the contest time limit.  
> A detailed, aspect-by-aspect table will help us understand how OpenAI, Psyho, and Sakana AI thought through the problem — phase by phase, subproblem by subproblem, with strengths and weaknesses.

* Goal: How would a **Beam Search-based AI**, **Psyho**, and **Sakana AI’s strategy (ALE-Agent v2)** approach the challenge?  
* The example task is the classic _robot-coordination wall-building_ type (AWTF2025), a notoriously NP-hard heuristic problem.  
* Here's how **Sakana AI (ALE-Agent v2)** tackled the AtCoder World Tour Finals 2025 NP-hard challenge — using the same table structure as before. This approach is **experimental and innovative**, especially because it relies on **multiple LLMs collaborating as a team**, instead of just one pre-optimized model.

### **AI (Beam Search) vs Psyho (Human Metaheuristics) vs Sakana AI**

| Phase / Subproblem | AI Beam Search Agent | Psyho (Human Thinking) | Sakana AI Strategy (ALE-Agent v2) |
| --- | --- | --- | --- |
| Search Strategy | Runs thousands or millions of partial solutions in parallel, scores them, and expands the most promising ones | Identifies strategic key ideas: manual rules, local tweaks, quick iterations | Multi-agent sampling & voting – Several LLM prompt attempts run in parallel, best one is picked (consensus model or "swarm prompting") |
| State Space Representation | Generic graph-based structure, where each step adds a new node | Compact, goal-driven representation, e.g. “wall equilibrium zones”, “bottlenecks” | Program structure + logical state space: LLMs represent strategic choices in text, like “left-to-right wall building for bottleneck” |
| Type of Heuristics | Predefined value functions (e.g. wall length, collision-free, synchronized), refined with a prompt loop | Dynamically shifting, intuitive goal-function tweaking (e.g. if stuck, new goal: “build center first”) | Several types of LLM-based implicit heuristics: different agents weigh objectives differently (e.g. risky, fast, stable strategies) |
| Parameter Tuning | Grid search / random search / genetic tuning → time-consuming, hard to adapt quickly | “Psychological” locality-sensitive tuning (“Halve it. No? Then double it.”) | Iterative changes to prompt parameters and code templates: one LLM proposes, another judges, third evaluates (co-evolutionary prompt shaping) |
| Time Usage | Pre-allocated CPU/GPU runs, often in parallel | Interactive testing, asymmetric time use: brutal tuning in the last hour | Post-hoc optimization – They ran after the contest, so no real-time strategy; but used compute time super efficiently |
| Handling Unstable Inputs | Clunky – new seed → new world, often needs retraining | “Inner model” switching: Psyho recognizes seed traits (e.g. sparse, dense) | Relied on LLMs' self-reflective skills: if a seed has a different structure, it's mirrored in prompt response variation (meta-adaptation) |
| Backup Strategies | Several versions run, mostly optimized for ranking → no manual re-planning | Manually crafted backup strategies: “If type A fails, I’ll try a completely different B…” | Simultaneous strategies, not sequential: multiple strategic LLM pipelines ran together and voted |
| Level of Fine-tuning | Pretrained + fine-tuned, but with generic architecture | Fully problem-specific codebase, tailored to seed-specific quirks | No dedicated fine-tuning, but taught many “template strategies” via prompts (zero/few-shot generalization) |
| Source of Creativity | Prompt design and reward shaping | Internal analogies, recycled template ideas from past contests | Emerged from model diversity – different LLMs interpreted prompts differently; this variation sparked novel ideas |
| Debug / Diagnostics | Logging, metrics, automatic traces → delayed feedback | Direct, visual and quick evaluation (“Why’s the wall piling up on the right?”) | Automatic metrics + log analysis, but no human intuition – instead used statistical selection: “These versions were 10% better” |
| Final Hours | Limited, unless fine-tuning loop was automated | Psyho’s legendary “post-midnight edits” – +5% score even in last 10 mins | Didn’t participate live, only optimized for final result (like an “offline agent”) |
| Resource Needs | Heavy compute, many tests, slow refactoring | Low compute, high cognitive agility | Moderate compute, but several LLM instances ran in parallel, a few hundred LLM calls + comparative scoring for one final score |
| Style | Heavily static, probabilistic modeling | Heuristic, minimal combinatorics, meta-level decision-making | Collaborative LLMs like a council of many heads: not a single algorithm, but a fusion of ideas and strategies |
| Strength | Persistent, scalable, low error rate | Flexible, creative, adaptive | Flexible, generalizable, able to “learn” from patterns in its own answers – surprisingly strong strategies emerged through consistent prompt iteration |
| Weakness | Struggles with changing context or “tricky” rule edges | Gets tired, limited time capacity, prone to focus slips | Not real-time capable yet, lacks inner world model – doesn’t “understand” the contest, only reacts; decision sequences may be inconsistent |

### **Notes:**
* In the contest, OpenAI’s Beam Search-like strategy came **very close** to Psyho’s solution (2nd place), but it **couldn’t dynamically shift** its search patterns when Psyho made a breakthrough with **new, untested ideas** during the **final hour**.
* **Main takeaway**: Beam Search is powerful if you have enough time and compute — but when the task is **anti-beam**, **human intuition and creative variation still hold a decisive edge**.
* Sakana AI’s method is like a “mini artificial analyst team” debating strategies and picking the most promising one. It’s **metaheuristic prompt tuning inside the prompt**, ending with code generation. This method is **less deterministic but possibly much more robust** against "diversity" — and that’s why it might be a **relevant leap forward in creative AI thinking**.


## **Part 14** – Psyho’s task plan before the contest

> **TL;DR:** Let's dive into Psyho’s preparation notes.  
> From these, we can see where he built in safety nets, where he optimized for speed, and what those “fine vibrations” are that set a human approach apart from an AI’s.

| #  | Tasks | 
|----|-------| 
| 01 | short python script that copies content of a file to clipboard | 
| 02 | windows, fix problem with not passing sys.argv when run without python.exe (does work in .bat files) | 
| 03 | psytester, clean tests dir before running (option?) | 
| 04 | psytester, add option to override exec name | 
| 05 | psyrunner, fix it? | 
| 06 | psybatch, probably not happening | 
| 07 | psyopt, is it resistent to snoozing? | 
| 08 | psyopt, try using pruning (a bit risky but should speed up drastically?) | 
| 09 | psyopt, add parallel runs (considering compiling might be the bottleneck?) | 
| 10 | psyopt, extract number of errors and/or fix errors remembering prev score (clear test dir?) | 
| 11 | [?] psyopt, sometimes it hangs on killall repeatedly, why? | 
| 12 | [?] psyopt, sometimes breaks after a run (what's the state, maybe test on super short runs) | 
| 13 | psyopt, add run names | 
| 14 | [?] psyopt, delete temporary files | 
| 15 | psyopt, research method types | 
| 16 | [?] psyopt, add check if run is broken (stuck for too long) & restart | 
| 17 | practice on AHC 049? | 
| 18 | [done] look at screen sharing doc | 
| 19 | [done] aws, test c7a multithreading | 
| 20 | [nope] gcp, test ssh connection | 
| 21 | [nope] gcp, contact support to get ALL CPU quota (in Japan) | 
| 22 | [done] gcp, setup account, set key, try to get high cpu machine | 
| 23 | [nope] test cline? | 
| 24 | [done] psyopt, optimize all calls for speedup | 
| 25 | [done] look at confession room from AWTF 2024 | 
| 26 | [done] slack, fill questionairre | 
| 27 | [done] slack, ask questions   | 

This task list is a hidden gem for understanding **how a top-level competitive programmer thinks, prepares, and works**—especially in the context of a heuristic optimization contest.  

The fact that this list was created **beforehand** (not as a post-hoc explanation) gives us a rare peek into how someone **systematizes their own workflow and tools**.  
Now let’s walk through it and **analyze** what it reveals about Psyho’s competition mindset—and how it **reinforces everything** we’ve said before (human vs AI, beam search, and so on).

### **The list structure: 3 main themes**  
* **Technical tooling and environment setup**  
Examples: `psytester`, `psyrunner`, `psyopt`, `.bat file` fixes, AWS/GCP prep  
This is about getting the infrastructure and developer environment ready.

* **Development of the optimizer system (psyopt)**  
Examples: pruning, parallel runs, error handling, watchdogs  
This section holds the core ideas to test and refine competition strategies.

* **Practice, metainfo, contest context**  
Examples: testing old problems (AHC 049), filling out forms, being active on Slack  
This is about being embedded in the competition community, metacommunication, and the human side of things.

### **Detailed analysis: What can we learn about Psyho?**

**(1) “It’s not about solving the task first — it’s about the _environment and the runtime framework_.”**  
   *   **`psytester`, `psyrunner`, `psybatch`** → he doesn’t just “write code”, he’s building a **test and batch system** right from the start.  
   *   **Highlights**: `clean tests dir`, `override exec name`, `fix argv when missing`  

This shows that he wants to **automate dozens of variants**, with _fast retries_.  
_This behavior aligns with the logic of AI-style pipelines — but it’s driven by human intelligence._

**(2) "`psyopt`: his own heuristic _meta-optimization_ framework"**  
This is the most fascinating part:
| Line | Feature | What it means |
| --- | --- | --- |
| 8 | “resistant to snoozing?” | Avoiding slow or exhausted search strategies (e.g., local optima) |
| 9 | “try pruning” | Cutting down the search space for quicker decisions → beam search light |
| 10 | “parallel runs” | Running several processes in parallel, with different random seeds or strategies |
| 11–17 | “restart if broken”, “detect hangs” | Watchdog-like behavior, self-repair, stability checks |
| 25 | “optimize all calls for speedup” | Full-code profiling, not just algorithmic but also runtime optimization |

These show that Psyho:  
   *   **isn’t just running a fixed algorithm**, but works with a **dynamically tunable experimental engine**, similar to a **modular AI agent**.  
   *   And this _"agent"_ isn’t an LLM — it’s a **heuristic agent**, which he **built, understands, and tunes himself**.  
_What’s “finetuning” for an AI model is “psyopt config” for him. The analogy holds beautifully._

**(3) No beam search → _a conscious strategy of minimalism_**  
Here’s where Psyho’s now-famous X comment gets proven:
> “...none of the finals' problems ever required beam search.”
And what do we see on the list?
   *   **No beam search.**
   *   Instead: _pruning_, _error monitoring_, _score tracking_, _restarts_.

This tells us:
   *   He **deliberately avoids wide branching search trees**.
   *   He aims for **lean, fast, and robust algorithms**.
   *   He wants to **solve problems with narrow, targeted strategies**.
_This is the kind of thing an AI agent struggles with: decision-loops instead of prompt-loops._

**(4) Meta-knowledge: he knows what kind of tasks to expect**  
   *   Line 18: “Practice on AHC 049?” → _adapting to a specific seed pattern_  
   *   Line 26: “confession room from AWTF 2024” → _learning from last year’s strategies_  
   *   Line 27: Slack, survey → _using meta-info, watching community knowledge_  

These **aren’t algorithms**, but they’re clearly **winning human behaviors**.  
AI could only learn this if it were **prompted to**, or if it were **explicitly finetuned for the AtCoder context**.

### **TL;DR – What does this solution plan prove?**

It shows that Psyho:  
*   **Built his own mini AI-like framework**, just not with LLMs, but with his own code modules.  
*   Consciously **avoided “beam search” type strategies**, preferring lean, fast, retry-friendly tactics.  
*   Took **meta-information**, **runtime stability**, and **competition hygiene** very seriously.  
*   Throughout, he **acted as a human**, but geared up with tools to the point where he **competed head-on with OpenAI’s fine-tuned AI agent**.


## **Part 15** – What can we really conclude after the contest?

> **TL;DR:** Here’s a carefully weighed summary: OpenAI’s beam search strategy nearly caught up with Psyho’s performance.  
> But human experiential knowledge (aka metaheuristics) still gave the edge—even in the very final hour.  
> That said, this won’t stay true forever.

### **“Did OpenAI almost catch up to Psyho using just a generic beam search?”**

* **Yes, it’s highly likely.**  
  Multiple signals point to OpenAI’s agent being a **general-purpose, beam-search-style, multi-strategy explorer** rather than a contest-specific fine-tuned one.
   * Sakana AI’s retrospective approach (multi-agent + ensemble + offline search) followed a similar flavor.
   * OpenAI’s “superhuman-speed” response suggested **automated search**, rather than creative decision-making.
* And even with all that—they still ended up “only” in second place.

### **“Psyho won with a clever, anti-beam-search strategy”**

* **Fully confirmed.**
* He wrote himself that he _never needed beam search_ in the finals.
* His prep list didn’t just skip beam search—it actively leaned into **alternative human-style techniques**:
    * pruning
    * watchdogs
    * seed strategies
    * restarts and restart monitoring
* This wasn’t brute-force. It was a **deliberate, experience-driven strategy**.

### **“The victory came down to the very last 10th hour”**

* Psyho didn’t explicitly say this—but if you know the AtCoder landscape, it’s a safe assumption.
   * Final tuning and submissions usually happen in the last hour.
   * Whoever was **measuring constantly, tweaking, and reacting in real-time** could gain a clear edge.
   * In past years, Psyho often found his winning strategy in the final day’s final moments.

### **“There’s still hope for AI to learn human-style metaheuristics”**

* This is a **key idea** worth highlighting.
   * What Psyho did wasn’t **exclusively human knowledge**—it was just **not yet formalized** human knowledge.
   * Metaheuristic behavior (seed handling, fallback strategies, watchdog logic, restart flows, “intuitive pruning”) showed **learnable patterns**.
* A _RL-based agent_ with an LLM-style prompt module could eventually reach similar tactics, provided:
   * it’s trained on competition-style data,
   * it tracks the objective function over time,
   * and it can internalize the dynamic nature of experience-based heuristics.

### **Final takeaway – stated precisely**

> OpenAI’s general beam-search-based agent came **very close** to winning, but was ultimately outperformed by Psyho’s **unique, well-structured, anti-beam approach**—rooted in **human experience, strategic simplification, and frequent measurements**.  
>  
> This doesn’t disprove AI progress—on the contrary:  
> it **confirms** that the **“tacit knowledge” of human optimization strategy** is **learnable** and **valuable**.  
>  
> The next frontier won’t be human vs. AI, but:  
> **human strategies vs. their formalized, AI-learned representations**.


## **Part 16** – What is tacit knowledge?

> **TL;DR:** Through the lens of recent competitions, we can grasp what "tacit knowledge" really means: it's a kind of professional instinct that's hard to verbalize—and that's exactly where human advantage still lies over AI.

* **Tacit knowledge** refers to **non-formalized, often subconscious knowledge** that we gain **through practice**, and which is **hard to put into words or rules**.

### **Key characteristics**
*   It’s not explicitly taught → **you can’t learn it from a book**.
*   It’s hard to code or explain → runs on **intuition and experience**.
*   Often only becomes conscious when asked: “Why do you do it this way?”

### **Examples**
*   A seasoned programmer *feels* when a solution will be slow—even before benchmarking it.
*   A contestant just *knows* certain types of seeds need fallback strategies—though nobody taught them that.
*   A chef knows when the dough is perfect—not by recipe, but through **hands-on instinct**.

### **Why does it matter for AI?**
*   Current AI models learn mostly from **explicit examples**.
*   Tacit knowledge doesn’t come in examples—it’s found in **continuous context, subtle perception, and feedback loops**.
*   AI will only truly level up once it can **internalize** these **non-rule-based patterns**.

*   **Psyho’s victory was partly due to tacit knowledge that went beyond the AI’s explicit heuristics.**

### **TL;DR – Quick summary**
* **Tacit knowledge**:
   *   Human experience and intuition that’s hard to formalize.
   *   A key ingredient in Psyho’s win.
   *   AI might learn it someday—but _we’re still at the doorstep_ of reliable imitation.

### **Comparison matrix**

* This shows **which types of knowledge work best under which competition formats—and who has the upper hand: human or AI**. On the left: knowledge types. On top: competition traits. Columns also hint at the likely winner.

* **Knowledge Type vs. Competition Format Comparison Matrix**

| Knowledge Type / Competition Trait | 🧠 Fixed rules, lots of pretraining (e.g. chess) | 🔀 Unknown tasks, long time (e.g. open contest) | ⏱ Unknown tasks, time-limited (e.g. AHC) | 🧪 Multiple seeds, hidden tests (AtCoder heur.) | 🧬 Changing input, adaptive pressure | 🧩 Complex combinatorics, heuristic space |
| --- | --- | --- | --- | --- | --- | --- |
| Explicit algorithmic knowledge | ✅ AI | 🤝 Even (humans generalize better) | ✅ AI | 🤝 Mostly AI | ❌ Slow to adapt | 🤝 AI is fast, but may be off-target |
| Tacit (implicit) knowledge | ❌ AI can't access it | ✅ Human (experience-based tuning) | 🤝 Human edge | ✅ Human picks what to sacrifice | ✅ Human intuition shines | ✅ Human instinct may be the key |
| Prompting skill (meta-AI control) | ❌ (no prompt field) | 🤝 AI scales better | ✅ AI (prompt pipelines are faster) | ✅ AI improves with more agents | 🤝 AI is catching up | 🤝 AI can search, but humans grasp faster |
| Metaheuristic strategy thinking | ❌ Not relevant | ✅ Human (wide strategy range) | 🤝 AI is a fast searcher, human is better selector | ✅ Human (adapts strategy by seed) | ✅ Human “feels” things | 🤝 AI explores, human combines creatively |
| Heavy compute support | ✅ AI (like AlphaZero) | ✅ AI (can catch up with time) | ✅ AI (if no token limits) | ✅ AI (offline Sakana-style runs) | 🤝 Humans fast, AI massive | ✅ AI can run at insane speed |
| Spotting creative new ideas | ❌ AI lacks “creativity” | ✅ Human (with experience) | ❌ AI beam-search often generic | ✅ Humans like Psyho can win here | 🤝 AI might learn (if not restricted) | ❌ AI can’t tell a new gem in time |

* **Takeaway:**
   *   In **rule-based contests** (like chess), **AI dominates**—given enough time and compute.
   *   In **AtCoder-style hidden-seed, NP-hard problems**, **human experience and strategy (tacit + metaheuristics) still win out**.
   *   **AI thrives when it’s well-prompted and scaled up massively.**
   *   The future will be **hybrid**: **humans prompt, machines optimize, and slowly but surely learn our tacit patterns too**.


## **Part 17** – Commentary on the AtCoder 2025 Competition Rules

> **TL;DR:** The rules are not just a formal necessity – they’re a strategic factor. This part sheds light on why the *last* successful submission matters, how this invites tactical thinking, and how the rules may even serve as an implicit anti-AI safeguard.

* The goal of the rules is to create a **fair, individual, and technically meaningful competition environment**. Here are some thoughts on key points:

### **“There’s one problem. Any AtCoder programming language is allowed.”**

* **Flexible and fair.**
   *   Everyone can use the language they’re strongest in.
   *   AI agents are welcome too (e.g. Python + C++, or their own custom toolchain).

* _But this opens an asymmetrical advantage for AI_, since code generation can mix languages easily, while for us humans, that’s a whole different story.

### **“No penalty for resubmitting, but there’s a 5-minute cooldown.”**

* **This encourages experimentation**, but:
* It has a **serious impact on strategy**:
* Both AI agents and human players rely heavily on **tight tuning** – meaning they optimize their response to seed values or parameters _during runtime_.
* The 5-minute pause makes it **non-trivial** to calculate how many retries you can afford → whoever has a good automated test system **has an edge**.
* _This indirectly rewards those who’ve built psyops-style custom runners._

### **“It’s an individual competition. Sharing solutions is not allowed.”**

* Totally understandable and necessary.  
* This **also bans collaborative AI agents running together** during the competition.
* Fair use of AI agents is only possible if:
   *   they’re trained beforehand,
   *   and they **don’t learn on the fly** from public feedback on seed data (which the rules clearly prohibit).

### **“Only the last non-CE submission is judged in the system test.”**

* This is strategically crucial.
   *   **System test inputs are hidden**, so you can’t overfit to them.
   *   But **only your final submission counts** → which puts pressure on you to decide: _which one do you trust as your final answer?_

* For humans, this becomes a **psychological factor** (will I mess it up at the last second?), while an AI agent might resolve this through stochastic choice or voting – *if* it were allowed.

### **“Why is the last submission counted, not the best one?”**

* This rule – **“only your final non-CE (Compilation Error) submission counts in the system test”** – is a **deliberate and thoughtful competition design choice**. Here’s why it exists, and what might happen if it didn’t.

* **Short answer:** The point of only counting the final submission is to **force you to make a responsible endgame decision.**  
It’s a **metaheuristic tactical challenge**: it’s not enough to write a good algorithm – **you also need to know when you trust it enough to make it _the one_**. It’s a **psychological and strategic game mechanic**, designed to **balance luck, automation, and trial-and-error.**

* **What if only your _best submission_ counted?**
   * ➕ Pros:
      * Contestants could **experiment freely**, knowing that their best score would be preserved.
      * AI agents and meta-tuning systems could **keep sending trial runs**, and the “golden shot” would secure all the benefits.
   * ➖ Cons:
      * **System overload chaos** – Everyone would submit endlessly → overload, DDOS-like behavior.
      * **Overfitting risk** – Contestants could learn to **game the public tests** with a lucky submission that performs well – but doesn’t generalize.
      * **Metaheuristics would dominate too much** – The “try a hundred times and keep the best” tactic would become **too effective** → the contest becomes a tuning lottery instead of an algorithm challenge.
      * **It would break seed-agnostic design** – The current system pushes contestants toward _seed-independent general algorithms_ (especially on system tests). A "best-of" strategy would _bias generalization_.

* **Why is the “last submission counts” rule actually great?**

   * **It reduces the luck factor**
      * If you try 50 times and get one magical result → that’s not fair.
      * This way it’s **not about whether you got a lucky seed**, but whether your algorithm performs **consistently well**.

   * **It forces you to build an optimized tuning pipeline**
      * Random trial-and-error isn’t enough.
      * You have to solve this: **how will you choose your final submission?**
      * That’s a serious strategic question:
         * → _“Should I risk the fresh but unstable version?”_
         * → _“Or stick with the stable but slightly weaker one?”_

   * **It brings time management into play**
      * A new experiment submitted in the final 5 minutes can **overwrite** your previous good result.
      * So everyone needs to **calculate**: _“How long can I develop? When is stop time?”_

* **Appendix:**
   * **Analogies – It's like...**
      * **Chess Analogy:** In chess, not all your brilliant moves matter – only the **last one** that gives or receives checkmate.
      * **Sports Analogy:** It's not your prettiest goal that wins the game, but the one that’s **still on the board** when the clock runs out.

   * **Bonus tidbit:**
      * The system **doesn’t count a CE (compilation error) submission** as your last one, because that would **technically break** the contest results.
      * Instead, the **last valid, executable submission** is what gets system-tested – which **reflects the contestant’s actual intent**.

### **TL;DR – Contest Rule Summary**
*   Overall, it’s fair – but it **especially rewards those who build a solid runtime and evaluation framework**.
*   The playing field isn’t closed for AI agents, but **the tuning and submission strategy still gives humans an edge – for now**.

| Why does only the last count? | Because... |
| --- | --- |
| 🎯 It forces responsible decisions | No “I’ll just submit everything I can think of” |
| ⚖️ It lowers luck and brute-force impact | Flooding the system isn’t enough |
| 🧠 Tuning pipeline quality is key | Who can pick their best run the smartest way? |
| ⏳ Time management is strategic | When should I submit the final one? |

* So this rule creates a competition space at the crossroads of knowledge, strategy, and self-control. Exactly the kind of arena where – _for now_ – humans and AI still don’t function quite the same.


## **Part 18** – How many KB of source code are we talking about in Psyho’s case?

We can’t know an _exact number_ for what Psyho had on their machine — but we can make a pretty good estimate of what to expect from a contestant like this in an AtCoder Heuristic Contest.

### How much Python code did Psyho bring to the contest?

* Psyho is a **seasoned contestant** and tooling builder. Based on previously published lists (e.g., `psyopt`, `psytester`, `psyrunner`, `setup.py`, etc.):

| Module | Estimated size |
| --- | --- |
| psyopt.py (metaheuristics framework) | ~15–25 KB |
| psytester.py (testing, scoring) | ~5–10 KB |
| psyrunner.py (automated running) | ~2–5 KB |
| setup scripts, .bat, .sh files | ~1–3 KB |
| Total at arrival | ~25–40 KB Python code |

* This is mainly **tooling**, not the problem-specific logic itself.

### How much code could he have written during the 10-hour contest?

* Now we enter the domain of **problem-dependent optimization strategies**, experimentation, and re-installations. We know that:
   * Psyho **didn’t use beam search**, so he likely tried several ideas.
   * In the optimization phase, he often made _small tweaks_, switching parameters or heuristics.
   * His prebuilt tools let him test tiny changes (1–2 lines) over and over.

| Aspect | Estimate |
| --- | --- |
| Typical problem-specific code (e.g., main.py) | 5–10 KB |
| Iterative versions (not deleted) | 10–30 KB |
| Temporary / unused experiments | 10–15 KB |
| Total new code during contest | ~20–40 KB Python code |

### Altogether, in Psyho’s folder:

* By the end of the contest, there were likely about **60–80 KB** of Python code in his project — but only **a portion was active** (`main.py`, `params.yaml`, `runner.py`). The rest was tooling, discarded attempts, or profiling logs.

### Visual analogy:

* Psyho-style competing isn’t about writing one big, long codebase — it’s more like a **heuristic patchwork**, guided by _profiling_ and _meta-testing_.


## **Part 19** – IMO, International Mathematical Olympiad 2025?

> **TL;DR:** For a thoughtful, rounded closing, let’s bring in the IMO contest too — even if just for a few reflections.

### **IMO Gold Medals**

* **Google DeepMind** – officially recognized with a **gold medal**. The Gemini Deep Think model solved 5 out of 6 problems, scoring 35/42 points. The IMO organizers validated the result. [LessWrong](https://www.lesswrong.com/posts/RcBqeJ8GHM2LygQK3/openai-claims-imo-gold-medal?utm_source=chatgpt.com) [Reuters](https://www.reuters.com/world/asia-pacific/google-clinches-milestone-gold-global-math-competition-while-openai-also-claims-2025-07-21/?utm_source=chatgpt.com).

* **OpenAI** – also scored 35 points but **did not officially enter** the contest. Independent IMO medalists assessed the result. [Reuters](https://www.reuters.com/world/asia-pacific/google-openais-ai-models-win-milestone-gold-at-global-math-competition-2025-07-21/?utm_source=chatgpt.com)

* Both models solved the tasks in **natural language**, **without using Lean or any formal proof language**. [Hacker News](https://news.ycombinator.com/item?id=44637191&utm_source=chatgpt.com)

### **What happened technically at OpenAI?**

* **Maximizing CoT chains**: “test-time compute scaling,” parallel reasoning paths, multiple iterations, and a metaconsensus strategy — all aiming for more structured and less brittle chains of thought. [Reuters + LessWrong](https://www.reuters.com/world/asia-pacific/google-clinches-milestone-gold-global-math-competition-while-openai-also-claims-2025-07-21/?utm_source=chatgpt.com)

* This made **natural language problem-solving** possible with a more advanced reasoning model behind it.

### **What happened technically at DeepMind / Gemini (DeepThink)?**

A summary of Gemini/DeepMind’s (DeepThink) technical strategy for IMO 2025 — side by side with OpenAI’s "test-time scaling" method:

* **Implicit world-model planning**:  
   * DeepThink doesn’t primarily rely on CoT chains. Instead, it follows the principle of **“inner simulation”** — building internal representations of the world to mentally model the problem, and exploring **“state evolution”** pathways to test reasoning alternatives.

* This strategy includes a few key ingredients:
   * **Model-based search**: exploring the inner dynamics of the problem itself, rather than maximizing linguistic chains.
   * **Intuitive representations**: the LLM doesn’t learn explicit reasoning steps — it follows implicit patterns in its internal token-space, enabling **“sketch-level planning”**.

* **Self-consistency tuning**: it runs multiple independent reasoning threads and uses their **dynamic coherence** to weigh the final answer.

### **The DeepThink advantage**

* This approach **avoids relying on explicit CoT chains**, steering clear of the trap of hallucinated, overcomplicated reasoning steps. Instead, it aims to _understand the structure_ of a math problem from within — based on a sort of **hidden "reasoning landscape."**

### **IMO 2025 in action:**

* DeepThink’s strengths shine in **complex geometry or number theory problems**, where success depends less on linear logic and more on **planned exploratory thinking** — something closer to discovery than deduction.

* The AI doesn’t just answer — it **“thinks about how to think toward an answer,”** modeling this with deep internal network weight patterns.

### Summary:

| Model | Method | Core Strength | Analogy |
|    
| OpenAI (GPT-4+) | CoT + metaconsensus | Structured reasoning, iterative corrections | “Playing chess move by move” |
| DeepMind (Gemini / DeepThink) | Implicit world model + internal planning | Intuitive discovery, planned insight | “A geometry experiment imagined in the mind” |


## **Part 20: FINALE** – Is the hidden AGI already here, after the 2025 AtCoder and IMO competitions?

> **TL;DR:** A thought-provoking finale about how some closed-source models are already performing at a quasi-AGI level. If these ever get released, the real question won’t be *whether* AI wins competitions – but *when* it gets banned from them.

### **Corpus Size and Learning**

* There are currently **398 IMO problems** (1959–2025, 6 per year, except 1960 and 1962). That’s **relatively small** compared to a typical LLM training corpus – so we’re not talking about brute memorization, but actual **abstract reasoning**.

### **AtCoder and Programming**

* The 2025 **AtCoder Heuristic Finals** were a major milestone: a human programmer (Psyho) actually **defeated an OpenAI model**, although the model **still reached second place** [Google DeepMind](https://deepmind.google/discover/blog/advanced-version-of-gemini-with-deep-think-officially-achieves-gold-medal-standard-at-the-international-mathematical-olympiad/?utm_source=chatgpt.com) [Ars Technica+7thetimes.co.uk+7pcgamer.com+7](https://www.thetimes.co.uk/article/human-programmer-beats-ai-model-coding-psyho-3qv070q2w?utm_source=chatgpt.com).

* This shows that **AI models excel more in programming** (thanks to LLM-compatible patterns) than in tasks like chess or the IMO, where **lookahead-based, stateful reasoning** is required.

### **General LLM Progress in 2025**

* Both IMO and AtCoder demonstrate that **general-purpose LLMs have caught up significantly** with human performance by 2025 – in some competitions, they’re even neck and neck.

* They’re **getting close even to chess engines like AlphaZero**, especially when competing **without external tools like search engines**.

### **AGI Timing: Already here, but unpublished?**

* These results, combined with the **non-public but increasingly advanced LLMs**, suggest that by **mid-2025**, we might already be seeing **AGI-level performance** in some cases.

* But due to **geostrategic and economic reasons**, many of these models remain closed – the focus now is not on publishing, but on **accelerating development**.

* Still, it’s worth noting: these breakthroughs are happening even though LLMs still **don’t perceive the world** – in other words, **there is still no grounding**. These models **don’t see, don’t sense, don’t act in the physical world**, and their concepts are **not anchored in real-world interactions** – only in **textual logical consequences**. That’s what still separates them from the **embodied idea of AGI** – no matter how powerful they’ve become in math or programming.

### **TL;DR Recap**

* ✅ **DeepMind**: officially validated IMO gold medalist.  
* ✅ **OpenAI**: IMO gold-worthy, but unofficial.  
* ✅ Both: **solutions written in fluent English**, **no Lean used**.  
* ✅ **OpenAI**: new techniques for deeper CoT chains and toxicity prevention.  
* ✅ IMO corpus ≈ 398 problems → **thinking is a must, memorization won’t cut it**.  
* ✅ **FAQ**: general LLMs in 2025 are **breathing down the necks** of the best humans (IMO, AtCoder), sometimes tied.  
* ✅ **AGI**: technically here, but unpublished; it’s all about speed, not disclosure.  
* ✅ **Still no grounding** – these are **textual reasoners**, not **world-rooted intelligences**.


