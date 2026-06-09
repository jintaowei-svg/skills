# System Model Rhetoric Guide

## The story arc

A polished system model should feel like a controlled walk through the paper’s world. The reader should never feel that notation appears randomly. Use the following arc as the default structure.

### 1. Scenario and modeling scope

Start with the system being studied and the level of abstraction. Mention the network type, participating entities, and the operational goal.

Good questions to answer:

- Is this a wireless, wired, edge-computing, satellite, IoT, datacenter, or multi-hop network?
- Is the model about routing, scheduling, caching, offloading, resource allocation, learning, security, reliability, or inference?
- What is intentionally abstracted away?

### 2. Entities and indices

Define sets, indices, and relationships before defining decisions. Typical entities include users, devices, base stations, edge servers, links, flows, services, files, tasks, regions, queues, and time slots.

Preferred order:

1. set and index;
2. physical/logical meaning;
3. relation among entities;
4. any capacity or state associated with each entity.

### 3. Time, traffic, and state evolution

Introduce time and stochastic dynamics before decisions that depend on them. Clarify whether decisions are per slot, per frame, per request, per packet, or long-term.

Useful distinctions:

- long-term decisions: caching, placement, model deployment, pricing, topology planning;
- short-term decisions: scheduling, association, offloading, power allocation, routing;
- random state: arrivals, channels, mobility, failures, demand, queue length.

### 4. Control decisions

Explain what is chosen, who chooses it, and when. A decision variable should not be only syntactic; it should have an operational interpretation.

Example logic:

“Given the predicted demand at the beginning of slot t, each edge server first selects the services to cache. After requests arrive, the server determines the fraction of tasks processed locally and forwards the remaining tasks to the cloud.”

### 5. Performance metrics and constraints

Define metrics after the decisions that influence them. Use intuitive motivation before formulas.

Metrics may include:

- delay, age of information, deadline violation probability;
- throughput, utility, revenue, cost;
- energy, power, spectrum, storage, CPU cycles;
- queue stability, reliability, privacy leakage, fairness.

Constraints should be interpreted after being written. For example, do not only write “s.t. ...”; also explain what the constraint prevents or enforces.

### 6. Problem formulation handoff

End the system model by telling the reader what the model enables. The final sentences should naturally prepare the next section.

Possible handoff patterns:

- “Based on the above model, the operator seeks to ... .”
- “The resulting problem couples ... across ..., which motivates the online algorithm developed in the next section.”
- “This formulation reveals two main challenges: ..., and ... .”
- “We next derive ... under this model.”

## Paragraph-level blueprint

Use this blueprint for substantial rewrites.

### Paragraph 1: considered system

State the network and its main components. Keep notation light unless the notation is essential.

### Paragraph 2: indexing and states

Introduce sets and variables. Keep related definitions together.

### Paragraph 3: demand or interaction

Explain how traffic, tasks, packets, flows, users, services, or channels interact with the system.

### Paragraph 4: decisions

Define decision variables and their constraints. Explain operational timing.

### Paragraph 5: cost and objective

Define cost, utility, or performance. Interpret equations.

### Paragraph 6: formulation and challenge

State the objective and constraints. Mention coupling, nonconvexity, stochasticity, incomplete information, scalability, or other challenges only if present in the original.

## Coherence repairs

When the original draft is hard to follow, apply these repairs:

- Move all definitions of a symbol to the first paragraph where the symbol is used.
- Group variables by semantic role rather than by the order the author invented them.
- Introduce a transition sentence before switching from physical topology to optimization variables.
- Convert isolated statements into cause-effect relations: “Because ..., the controller must ... .”
- Replace repeated “we assume” openings with varied structures: “Under this model,” “For each ...,” “To capture ...,” “Following ... .”

## How to preserve meaning while improving flow

Use three tiers of editing:

1. **Light polish:** grammar, concision, and word choice; keep sentence order mostly intact.
2. **Narrative polish:** reorder sentences within a paragraph, add transitions, merge duplicated definitions.
3. **Structural rewrite:** reorganize subsections, split or merge paragraphs, and add a problem-handoff paragraph.

Default to narrative polish unless the user asks for heavy rewriting or the original section is clearly disordered.

## What “like telling a story” means here

It means the section has progression and motivation:

- from physical scene to abstraction;
- from abstraction to variables;
- from variables to decisions;
- from decisions to metrics;
- from metrics to the problem or algorithm.

It does not mean informal wording, dramatic language, or excessive explanation.
