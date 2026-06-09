# Quality Checklist

Before finalizing a substantial problem formulation rewrite, check the following.

## Technical preservation

- All original variables, parameters, indices, sets, objective terms, constraints, and labels are preserved or explicitly flagged.
- No new assumptions, tractability claims, convergence claims, or complexity claims are introduced without support.
- The optimization variable list matches the variables that actually appear in the problem.
- Equation references and labels remain consistent.

## Narrative quality

- The formulation starts from the system goal rather than from unexplained symbols.
- Each objective term has a prose interpretation.
- Each constraint family has a prose role.
- The final paragraph explains why the following algorithm or analysis is needed.

## LaTeX readiness

- LaTeX environments are balanced.
- Citations and labels are preserved.
- The output is in a fenced code block when the user asks for LaTeX source.
- The polished text can be pasted into a manuscript with minimal cleanup.
