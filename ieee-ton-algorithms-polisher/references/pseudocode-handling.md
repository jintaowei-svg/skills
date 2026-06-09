# Pseudocode Handling

Use this reference when the input contains a LaTeX algorithm environment or a draft pseudocode block.

## Supported LaTeX styles

Preserve the user's existing style when possible:

- `algorithm` with `algorithmic` or `algpseudocode`;
- `algorithm2e`;
- custom IEEE-style pseudocode macros;
- enumerated steps when the user does not use an algorithm environment.

## Pseudocode editing rules

- Keep the algorithm caption, label, input, output, and line references unless the user asks for revision.
- Do not change the order of steps unless the user explicitly asks for restructuring and the change is logically safe.
- Do not add algorithmic operations that change behavior.
- Convert vague comments into short functional comments if they clarify existing logic.
- Use consistent verbs: `Initialize`, `Update`, `Solve`, `Compute`, `Select`, `Project`, `Return`.
- Keep notation consistent with the surrounding prose.

## Prose around pseudocode

Before the environment, explain the design idea and what the algorithm returns. After the environment, explain the main stages, termination, and any supported complexity or guarantee. Avoid mechanically restating every line.

## Author-check flags

Flag issues such as:

- an input appears in pseudocode but is never defined;
- an output is missing from the return line;
- a loop index or stopping criterion is ambiguous;
- a subproblem is referenced but not specified;
- the pseudocode and prose use different symbols for the same quantity.
