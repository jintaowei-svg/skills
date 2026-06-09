# IEEE TON Algorithms Polisher

`ieee-ton-algorithms-polisher` is a Codex skill for polishing, rewriting, and restructuring algorithm sections in IEEE/ACM Transactions on Networking style manuscripts and related networking papers.

It is designed for drafts that already contain the author's algorithmic logic, pseudocode, update rules, variables, assumptions, complexity discussion, or proof sketches, but need clearer academic English and a more coherent procedural narrative.

## What It Does

This skill helps turn a rough algorithm section into a LaTeX-ready section that reads in a natural progression:

1. Motivation from the formulated problem
2. Algorithm overview
3. Inputs and outputs
4. Initialization
5. Main loop, stages, or update rules
6. Termination and returned solution
7. Complexity, convergence, guarantee, or implementation discussion

The skill focuses on preserving algorithm behavior while making the method easier to follow.

## When To Use

Use this skill when you have:

- A draft algorithm section for a networking, edge computing, wireless, caching, routing, scheduling, or resource allocation paper
- LaTeX algorithm environments that need clearer surrounding prose
- Pseudocode whose variables should be aligned with the problem formulation
- Complexity or convergence statements that need careful wording
- Chinese technical notes that should be rewritten into polished academic English
- Reviewer-facing explanations of algorithm design or implementation details

## Key Principles

- Preserve all original inputs, outputs, steps, update rules, stopping criteria, variables, and guarantees.
- Do not invent algorithmic steps, proofs, convergence guarantees, approximation ratios, complexity orders, or optimality claims.
- Keep prose and pseudocode notation consistent.
- Explain what each stage achieves, not only what line number executes.
- Preserve LaTeX algorithm environments, captions, labels, and line references unless they are clearly broken.
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
    |-- algorithm-section-rhetoric.md
    |-- complexity-and-guarantee-handling.md
    |-- pseudocode-handling.md
    |-- quality-checklist.md
    `-- style-principles.md
```

## Reference Files

- `SKILL.md`: Main skill instructions, trigger description, workflow, and output contract.
- `references/style-principles.md`: Target voice, sentence patterns, tone controls, and anti-patterns.
- `references/algorithm-section-rhetoric.md`: Section-level organization for procedure-style algorithm writing.
- `references/pseudocode-handling.md`: Guidance for LaTeX algorithm environments and prose around pseudocode.
- `references/complexity-and-guarantee-handling.md`: Guidance for complexity, convergence, optimality, and proof-sketch language.
- `references/quality-checklist.md`: Final review checklist for preserving steps, variables, notation, and claims.

## Installation

This skill is one folder inside the `skills` repository:

```bash
git clone https://github.com/jintaowei-svg/skills.git
```

Install this folder into your Codex skills root so that `SKILL.md` is at:

```text
<skills-root>/ieee-ton-algorithms-polisher/SKILL.md
```

## Example Request

```text
Please polish the following algorithm section for an IEEE TON manuscript.
Keep the LaTeX algorithm environment and variable names unchanged, but improve the explanation and flow.
```

## License

No license has been specified yet. Add a license before public reuse or redistribution if needed.
