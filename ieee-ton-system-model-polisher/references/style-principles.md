# Style Principles for IEEE/TON System Model Polishing

## Target voice

Write like a careful IEEE/ACM Transactions on Networking author explaining a model to a technically strong but busy reader. The voice should be:

- formal but not stiff;
- precise but not over-compressed;
- confident but not promotional;
- explanatory without sounding like a textbook;
- mathematically disciplined while still readable.

A strong system model does not merely list variables. It guides the reader from the real networking scenario to the abstraction used by the paper.

## The narrative contract

Each paragraph should have one job:

1. **Scene paragraph:** identify the considered network, entities, and purpose of the model.
2. **Granularity paragraph:** specify time slots, regions, flows, requests, packets, users, tasks, channels, or other units of analysis.
3. **State paragraph:** define stochastic processes, queues, demand, mobility, cache state, topology, or channel state.
4. **Decision paragraph:** define control variables and who chooses them.
5. **Cost/constraint paragraph:** define latency, throughput, energy, storage, reliability, stability, privacy, or other constraints.
6. **Handoff paragraph:** connect the model to the optimization problem, algorithm design, theorem, or performance analysis.

Do not force all six paragraphs if the model is short, but keep the logic in this order unless the original paper requires a different order.

## Preferred sentence moves

Use these as patterns, not mandatory wording.

- Opening the model: “We consider a [network/system] consisting of ...”
- Giving purpose: “The model captures the interaction between ... and ... under ... constraints.”
- Introducing time: “Time is divided into slots indexed by ..., where each slot corresponds to ... .”
- Introducing entities: “Let ... denote the set of ..., indexed by ... .”
- Explaining a decision: “At the beginning of each slot, the controller determines ... .”
- Explaining a variable: “The binary variable ... indicates whether ... .”
- Explaining an assumption: “This assumption allows the model to focus on ... while keeping ... tractable.”
- Moving to cost: “Given these decisions, the resulting ... is measured by ... .”
- Moving to formulation: “The objective is therefore to choose ... so as to minimize/maximize ... subject to ... .”

## Readability rules

- Put the main subject early in the sentence.
- Avoid long noun stacks such as “user task service caching decision optimization problem.” Break them into clauses.
- Avoid starting many consecutive sentences with “where.” Vary with “Here,” “Specifically,” “The term ... represents,” or “This constraint ensures that ... .”
- Use “respectively” only when it truly improves clarity.
- Avoid overusing “which” clauses; split long sentences when a definition and an implication are mixed.
- Prefer one clear sentence over two cryptic compact sentences.

## IEEE-like technical tone

Good tone:

- “To capture the limited storage capacity at each edge node, we impose ... .”
- “The queue evolves according to ..., where the first term represents ... .”
- “This model abstracts away packet-level scheduling and focuses on the time scale of caching updates.”

Weak tone:

- “It is obvious that the storage is very important.”
- “We can easily know that the delay is bad.”
- “The system model is shown below and the variables are introduced one by one.”

## Handling assumptions

When polishing assumptions, make them neither apologetic nor hidden. A good assumption sentence has three parts when space allows:

1. the assumption;
2. its modeling role;
3. its scope or consequence.

Example pattern:

“Following the time scale of service placement, we model user requests at the region level rather than at the individual-user level. This abstraction preserves the spatial demand pattern relevant to caching decisions while avoiding unnecessary short-term mobility details.”

## Handling equations

Use the “lead-equation-interpret” pattern.

1. **Lead:** explain what is being quantified.
2. **Equation:** present the expression.
3. **Interpret:** define non-obvious symbols and explain the meaning of the constraint or metric.

Avoid placing an equation immediately after a heading with no prose. Avoid explaining only syntax while leaving the modeling role unclear.

## Chinese-to-English polishing patterns

Common transformations:

- “本文考虑了一个...” → “We consider a ... in which ... .”
- “为了方便分析，假设...” → “For analytical tractability, we assume that ... .”
- “可以得到...” → “It follows that ...” or “The resulting ... can be written as ... .”
- “需要注意的是...” → “It is worth noting that ...” only when the note is genuinely important; otherwise use “Here,” “In this model,” or remove it.
- “因此，问题可以建模为...” → “The resulting design problem can therefore be formulated as ... .”

Do not translate Chinese logical connectors mechanically. Rebuild the relation: contrast, cause, consequence, scope, or handoff.

## Anti-patterns to fix

- Variable inventory without context.
- Multiple definitions of the same notation.
- Equations introduced before the quantities are motivated.
- Assumptions stated after the formula that depends on them.
- Paragraphs that begin with a symbol before the reader knows what the symbol represents.
- Unsupported claims about novelty or optimality inside the model section.
- “Story-like” rewritten as informal prose. Keep it academic.
