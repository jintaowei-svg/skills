# Problem Formulation Rhetoric

Use this reference for full-section restructuring or when the user asks for a story-like formulation.

## Recommended section arc

1. **Opening bridge from system model.** State that the formulation follows from the modeled entities, time scale, demand, and resource constraints.
2. **Optimization goal.** State the high-level objective in words before the equation.
3. **Decision variables.** Define what the controller, user, BS, edge server, vehicle, satellite, or network operator decides.
4. **Objective equation.** Present the objective only after the core variables and metrics are clear.
5. **Constraint families.** Group constraints by function: domain, association, capacity, latency, energy, queue, reliability, flow conservation, stability, privacy/security, or policy.
6. **Complete problem.** Give the compact problem statement with `\mathbf{P1}` or the user's existing problem label.
7. **Handoff.** Explain the structural difficulty or coupling that motivates the next section without inventing unsupported theory.

## Paragraph roles

- Paragraph 1: `Why formulate this problem?`
- Paragraph 2: `What is controlled?`
- Paragraph 3: `What is optimized and why?`
- Paragraph 4: `What constraints make the solution feasible?`
- Final paragraph: `What makes the problem challenging, and what comes next?`

## Safe bridge sentences

Use conservative bridges when the draft implies but does not explicitly state a connection:

- `These constraints ensure that the decisions remain feasible under the resource model introduced above.`
- `The formulation therefore captures the tradeoff between service performance and resource consumption.`
- `Because the decisions are coupled across users and time slots, the problem cannot be decomposed directly without additional design.`
- `This motivates the algorithmic framework developed in the next section.`

Only use stronger claims, such as NP-hardness or nonconvexity, when the draft or user provides sufficient support.
