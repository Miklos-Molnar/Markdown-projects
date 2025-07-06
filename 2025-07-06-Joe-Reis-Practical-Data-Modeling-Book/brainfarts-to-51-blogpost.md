51.Post: **What is Analytical Data Modeling?**  
https://practicaldatamodeling.substack.com/p/what-is-analytical-data-modeling

(1) Analytical processing usually requires **replication**, the (optional) daily closure of OLTP systems & after backup. This results in extra overhead in terms of time and performance. Often, it is not even possible to fit it into a 24-hour day. Especially if any errors occur during the process.

(2) There is a saying that **“you can't ride two horses with one ass”**. This seems to have been the primary motivation behind Oracle RAC. If I look at it from here, it's OLTP, if I look at it from there, it's Analytical DB. It's without extra operational overhead, but it's damn expensive.

(3) The **Reverse ETL aspect**. When we feed the results of analytical processing back into OLTP. For example, after campaign management sorting, marking the affected customers in OLTP.

(4) **Controlling Data Warehouse** / data mart as "oxymoron"?  
* Analytical systems (historically even more so) are designed to work with loose consistency and a “big picture” view. Controlling, on the other hand, demands absolute financial accuracy: not a penny must be missing and the numbers must be auditable and traceable. Big data, approximate, good enough is not really in play here. Data governance and data quality aspects play a tough role.  
* Unlocking can also come from the Data Vault, SCD Type 2, and the design of reconciliation logics.  

Beyond historical precedents, here are **some newer ideas**. These aren’t ideas that must be implemented right away or at all costs, but as part of thoughtful design, it might be worth considering which ones are worth exploring further — and which ones might ultimately be set aside.  

(5) The **intelligent question model** as a data model supplement   
* The post talks about how the goal of analytical data modeling is to support human questions. What if the analytical data model also included explicit modeling of typical, expected questions and decision-making situations? (In connection with the “ontology of questions” or “decision taxonomies”.)  
* In other words, not only tables and relationships, but also the “question map” would be a design artifact:  
– What types of questions are there (What/Why/When/How)?  
– What decision points is the data consumed for?  
This would bring the data model closer to the true “human-centric” principle: the model would contain not only the query structure, but also the user's intent.  

(6) **“Exploratory Design”:** the data model as a living prototype  
* The post emphasizes that analytical questions are often exploratory and ad hoc in nature.  
* Shouldn't the data model itself be designed to be “exploratory”?  
– A model that can be versioned, iterated, and treated as a “prototype.” How often does a field that was previously optional become mandatory later on?  
– Not a final design, but one that continuously learns from user questions and is modified  
* This is in line with the spirit of “Lean” or “Design Thinking” in product development: the model is never finished, but learns from real questions.  

(7) **Temporality as a primary dimension**  
The article discusses how OLAP models are often time-oriented.  
Why don't we explicitly consider time to be a “first-class citizen” in data modeling?  
We should not think of time as just a passive dimension, but rather as something that the data model actively contains in the form of temporal patterns, state changes, and trends. Time shapes and organizes the structure of the model as a native entity, not just a label.  
This idea brings the predictive and historical approaches closer to classic descriptive analyses.  

(8) **The data model as a narrative framework**  
Post: analytics → people → decision. The structure of the data model can also convey a narrative. So that the “story” appears not only at the dashboard level, but also at the data model level. In many cases, this story is not so changeable that it needs to be dealt with at the dashboard level first. It is part of the idea of “understanding our company.”  

(9) How misguided is the idea of “fit for purpose” instead of “fit for question” (in relation to the principle of “fit for use case” in the post)? Would it be better to optimize the data model not for specific purposes, but for specific question classes?  
For example, **descriptive, diagnostic, predictive, and prescriptive questions** would get separate layers in the model.  
This could also structure the analytical model, helping with transparency.  

(9) **The tooling lens:** the impact of the tool on the model. Does the way we query the model distort or shape its design? Notebook, BI tool, LLM interface, etc.? The “query affordance” of the tool has a strong impact on how we model. This is already at the meta-level, but it is an exciting and fresh perspective.  
