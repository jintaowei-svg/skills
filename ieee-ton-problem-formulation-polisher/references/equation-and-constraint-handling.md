# Equation and Constraint Handling

Use this reference when the input contains optimization problems, dense equations, or multiple constraint families.

## Equation introduction

Every major equation should be preceded by a sentence that tells the reader what the equation does. Avoid presenting an equation as a surprise.

Good pattern:

```latex
To capture the tradeoff between delay and energy consumption, we minimize the weighted system cost
\begin{equation}
...
\end{equation}
where ...
```

## Constraint explanations

After a complete problem statement, explain constraints by family rather than repeating every symbol mechanically:

- domain constraints: identify binary, integer, continuous, nonnegative, or probability-simplex variables;
- resource constraints: name the capacity or budget being protected;
- latency constraints: identify which delay components are included;
- energy constraints: identify transmission, computation, propulsion, sensing, or circuit energy if present;
- flow/queue constraints: identify conservation, stability, or causality;
- association constraints: identify one-to-one, one-to-many, or many-to-one restrictions.

## Preservation rules

- Do not change mathematical meaning for stylistic smoothness.
- Do not normalize notation unless the user asks for notation revision.
- Do not remove a constraint because it seems redundant.
- Do not invent missing definitions for unexplained symbols. Add `author check needed` if the symbol cannot be inferred.
- Keep user-provided problem labels such as `P0`, `P1`, `OP1`, and `\mathcal{P}` unless a clear typo exists.
