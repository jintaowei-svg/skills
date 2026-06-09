# Algorithm Section Rhetoric

Use this reference for full-section restructuring or when the user asks for a story-like algorithm section.

## Recommended section arc

1. **Motivation from the problem.** Explain which coupling, discreteness, nonconvexity, stochasticity, large scale, or online information issue prevents direct solution, but only if supported by the draft.
2. **Design principle.** State the algorithmic idea in one or two sentences.
3. **Inputs and outputs.** Make clear what data are known and what decisions are returned.
4. **Main procedure.** Explain the stages in the same order as the pseudocode.
5. **Step rationale.** For non-obvious updates, explain what each step optimizes, approximates, relaxes, projects, or repairs.
6. **Termination and returned solution.** State the stopping criterion and final decision.
7. **Complexity or guarantee discussion.** Add only if the draft supports it.

## Paragraph roles

- Paragraph 1: `Why is this algorithm needed?`
- Paragraph 2: `What is the high-level algorithmic idea?`
- Paragraph 3: `What are the main steps?`
- Paragraph 4: `Why are the steps valid or useful?`
- Final paragraph: `What does the algorithm return, and how costly/reliable is it?`

## Safe bridge sentences

Use conservative bridges when the draft implies but does not explicitly state a connection:

- `The algorithm is designed to handle the coupling among the decision variables in \mathbf{P1}.`
- `Each iteration alternates between updating ... and refining ... while keeping the remaining variables fixed.`
- `The procedure terminates once the objective variation becomes sufficiently small or the preset iteration budget is reached.`
- `The obtained decisions are then used in the performance evaluation in Section ... .`

Only use stronger claims, such as monotonic improvement or convergence to a stationary point, when the draft or user provides sufficient support.
