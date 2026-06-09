# Style Principles

Use this reference when polishing the voice, paragraph flow, or sentence-level academic style of a problem formulation section.

## Target voice

- Write in formal IEEE/ACM transactions style.
- Be precise, direct, and explanatory.
- Prefer reader-guiding prose over compact variable dumps.
- Keep the author's technical claims within the evidence supplied by the draft.
- Use simple present tense for standing definitions and formulation statements.

## Useful sentence patterns

- `Based on the above model, we formulate the joint ... problem as follows.`
- `The objective in \eqref{...} captures ..., where the first term represents ... and the second term penalizes ... .`
- `Constraint \eqref{...} guarantees that ... .`
- `Constraints \eqref{...} and \eqref{...} restrict ... within the available ... budget.`
- `The binary variable ... indicates whether ... .`
- `The resulting problem couples ... with ..., which motivates the algorithmic design in the next section.`

## Tone controls

- Do not oversell the method in the formulation section.
- Avoid casual expressions such as `obviously`, `it is easy to see`, or `a lot of`.
- Avoid unsupported labels such as `optimal`, `efficient`, `tractable`, or `low-complexity`.
- Replace vague verbs like `deal with`, `make`, and `do` with precise verbs such as `allocate`, `schedule`, `associate`, `route`, `cache`, `offload`, `minimize`, `bound`, or `satisfy`.

## Common anti-patterns

- Listing variables without explaining the operational decision they represent.
- Presenting an objective before explaining what the decision variables control.
- Saying a constraint is `for resource limitation` without naming the actual resource.
- Using different symbols for the same quantity across text and equations.
- Introducing an algorithm claim inside the problem statement before the problem is fully defined.
