# IEEE TON Problem Formulation Polisher

`ieee-ton-problem-formulation-polisher` is a Codex skill for polishing, rewriting, and restructuring problem definition and formulation sections in IEEE/ACM Transactions on Networking style manuscripts and related networking papers.

It is designed for drafts that already contain the author's objective, constraints, variables, notation, equations, and modeling intent, but need clearer academic English and a stronger derivation from the system model.

## What It Does

This skill helps turn a rough mathematical formulation into a LaTeX-ready section that reads in a natural progression:

1. Modeling goal
2. Decision variables
3. Objective construction
4. Constraint families
5. Complete problem statement
6. Tractability or solution handoff

The skill focuses on preserving the mathematical structure while making every objective term and constraint easier to understand.

## When To Use

Use this skill when you have:

- A draft problem definition or optimization formulation section
- Dense LaTeX equations that need better lead-in prose
- Constraints that need clearer physical, resource, latency, queueing, or policy explanations
- Decision variables that need more consistent notation
- Chinese technical notes that should be rewritten into polished academic English
- A formulation that should connect more naturally to the algorithm section

## Key Principles

- Preserve all original decision variables, parameters, constraints, objective terms, labels, citations, and technical dependencies.
- Do not invent objectives, constraints, convexity claims, complexity claims, relaxations, or solution methods.
- Define notation close to first use and reuse it consistently across the objective, constraints, and algorithm handoff.
- Explain what each constraint enforces.
- Keep problem labels, equation references, and theorem/problem environments intact.
- Flag unresolved technical ambiguity with concise author-check notes.

## Typical Output

For a normal polishing request, the skill returns:

```markdown
### Polished version
[LaTeX-ready revised text]

### Revision notes
- [Concise notes about structure, clarity, or author-check items]
```

For requests that ask only for rewriting, it can return only the polished version.

## Repository Structure

```text
.
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- equation-and-constraint-handling.md
    |-- problem-formulation-rhetoric.md
    |-- quality-checklist.md
    `-- style-principles.md
```

## Reference Files

- `SKILL.md`: Main skill instructions, trigger description, workflow, and output contract.
- `references/style-principles.md`: Target voice, sentence patterns, tone controls, and anti-patterns.
- `references/problem-formulation-rhetoric.md`: Section-level organization for derivation-style formulation writing.
- `references/equation-and-constraint-handling.md`: Guidance for objectives, constraints, labels, domains, and dense LaTeX.
- `references/quality-checklist.md`: Final review checklist for meaning preservation, notation consistency, and IEEE/TON style.

## Installation

This skill is one folder inside the `skills` repository:

```bash
git clone https://github.com/jintaowei-svg/skills.git
```

Install this folder into your Codex skills root so that `SKILL.md` is at:

```text
<skills-root>/ieee-ton-problem-formulation-polisher/SKILL.md
```

## Example Request

```text
Please polish the following problem formulation for an IEEE TON manuscript.
Keep all LaTeX notation and constraints unchanged, but improve the explanation and flow.
```

## License

No license has been specified yet. Add a license before public reuse or redistribution if needed.
