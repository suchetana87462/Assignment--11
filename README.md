Eight core BA/PM documents — explained, with templates

Eight templates, written as one linked set. They share a running example (a customer portal for the repair shop) so you can see how each document feeds the next, rather than eight unrelated forms.

Every template is Markdown — versionable in Git, publishable to a wiki, and openable in LibreOffice Writer if a stakeholder needs a formatted document.

The set
#	Document	Answers	Owned by	Written when
1	Scope document	What are we doing, and what are we not doing?	BA	First
2	Project plan	Who, in what order, by when?	PM / Scrum Master	After scope
3	Effort estimation	How much work is it?	The team	With the plan
4	SRS	What must the system do?	BA	After scope
5	SDD	How will it be built, and why that way?	Tech lead	After SRS
6	User manual	How does someone use it?	BA / writer	During build
7	Change request	What does this change cost?	Anyone raises; BA assesses	Whenever
8	Scrum meeting notes	What did we decide, what's blocked?	Scrum Master	Continuously
How they connect
   Scope ──────┬──> Project plan <───> Effort estimation
               │           │
               └──> SRS ───┴──> SDD ──> Build ──> User manual
                     │                    │
                     └── Test cases ──────┘
                     
   Change request ──> amends any of the above, then re-baselines
   Scrum notes    ──> the running record underneath all of it

Three connections are worth understanding because they are where projects go wrong:

Scope → estimate. You cannot estimate what has no boundary. If the estimate keeps moving, the scope is not agreed — no amount of re-estimating will fix it.

SRS → SDD. These answer what and how, and mixing them is the most common documentation failure. A table name in the SRS means design decisions are being made before requirements are agreed. A business rule in the SDD means it will get lost when the architecture is revisited.

Change request → everything else. A CR is the only legitimate way an agreed document changes. Without one, scope creeps through conversation and nobody can reconstruct why go-live slipped.

Two distinctions people get wrong

Effort vs duration. Sixty person-days is not twelve calendar days with five people on it. Communication overhead grows with team size, and some work cannot be parallelised at all. State which one you are quoting — every time.

Defect vs change. If the system does not do what the baselined SRS says, it is a defect and it is fixed under the existing budget. If someone wants it to do something the SRS never said, it is a change and it costs money. Decide this in writing, with the reasoning, in the CR itself. This distinction is where supplier–client relationships are won or lost.

Which of these apply on an Agile project?

All eight, at varying weight — Agile reduces documentation, it does not eliminate it.

Document	Waterfall	Agile equivalent
Scope	Fixed, signed	Product vision + release roadmap; the boundary still needs to exist
Project plan	Detailed Gantt	Release plan + sprint plans
Estimation	Bottom-up, once	Story points against rolling velocity
SRS	Complete before build	User stories with acceptance criteria, elaborated just in time
SDD	Complete before build	ADRs and lightweight design, written as decisions are made
User manual	After build	Written alongside each feature
Change request	Formal board	Backlog reprioritisation — but anything touching a contractual commitment still needs a CR
Scrum notes	Status reports	The ceremonies themselves

The judgement call is proportionality. A two-week internal tool does not need a twelve-page SRS; a regulated system with an external supplier needs every one of these, signed. Scale the ceremony to the cost of being wrong.

Using these
Delete sections that do not apply rather than filling them with "N/A". A document padded to look thorough is harder to read and no more complete.
Keep the Common failure modes block at the bottom of each template while you are learning, and strip it before issuing the document to a stakeholder.
Version and date everything. An undated document is unusable six months later.
The bracketed placeholders and the repair-shop examples are both meant to be replaced — the examples are there to show the level of specificity expected.
