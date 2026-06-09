# Style Principles

Use this reference when polishing the voice, paragraph flow, or sentence-level academic style of an algorithm section.

## Target voice

- Write in formal IEEE/ACM transactions style.
- Be precise, direct, and procedural.
- Explain why each stage exists, not only what it computes.
- Keep the author's technical claims within the evidence supplied by the draft.
- Use simple present tense for standing algorithm descriptions.

## Useful sentence patterns

- `To solve \mathbf{P1}, we develop an iterative algorithm that ... .`
- `The algorithm takes ... as input and returns ... as output.`
- `At the beginning of each iteration, the controller updates ... according to ... .`
- `Given the current ..., the subproblem with respect to ... can be solved by ... .`
- `The iteration terminates when ... or when the maximum number of iterations is reached.`
- `The resulting solution is then used to ... in the original problem.`

## Tone controls

- Do not overclaim optimality, convergence, or complexity.
- Avoid casual expressions such as `firstly`, `secondly`, `obviously`, `just`, or `simply`.
- Replace vague verbs like `deal with`, `make`, and `do` with precise verbs such as `initialize`, `update`, `solve`, `select`, `associate`, `allocate`, `schedule`, `rank`, `project`, `normalize`, or `terminate`.
- Keep the writing mathematical rather than software-oriented unless the paper is explicitly about implementation.

## Common anti-patterns

- Describing pseudocode line by line without explaining the design idea.
- Introducing new variables in prose that never appear in the algorithm.
- Using different names for the same variable in the problem and the algorithm.
- Claiming convergence or low complexity without conditions or derivation.
- Hiding essential feasibility restoration or projection steps behind vague wording.
