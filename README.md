# IEEE TON System Model Polisher

`ieee-ton-system-model-polisher` is a Codex skill for polishing, rewriting, and restructuring system model sections in IEEE/ACM Transactions on Networking style manuscripts and related networking papers.

It is designed for drafts that already contain the author's technical model, notation, assumptions, equations, and problem formulation, but need clearer academic English and a more coherent section-level narrative.

## What It Does

This skill helps turn a rough system model into a LaTeX-ready section that reads in a natural technical progression:

1. Operational scenario
2. Entities, topology, sets, and indices
3. Time, demand, channel, traffic, or task model
4. Decision variables and controlled actions
5. Costs, constraints, and performance metrics
6. Handoff to the optimization problem, algorithm, analysis, or simulations

The skill focuses on preserving technical meaning while improving readability, flow, and IEEE-style academic expression.

## When To Use

Use this skill when you have:

- A draft system model section for a networking, edge computing, wireless, caching, routing, scheduling, or resource allocation paper
- LaTeX paragraphs that need clearer structure without changing the math
- Chinese technical notes that should be rewritten into polished academic English
- Equations that need better lead-in text and interpretation
- A mechanically organized variable list that should become a coherent narrative
- A system model that needs to connect more naturally to the problem formulation

## Key Principles

- Preserve all original entities, assumptions, notation, equations, labels, citations, and technical dependencies.
- Do not invent new assumptions, claims, algorithms, parameters, or constraints.
- Define notation close to first use and keep it consistent.
- Introduce each equation before it appears and explain its role after it appears.
- Use formal, direct academic English suitable for IEEE/ACM networking manuscripts.
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
|-- assets/
|   `-- icon.svg
`-- references/
    |-- example-patterns.md
    |-- quality-checklist.md
    |-- source-notes.md
    |-- style-principles.md
    `-- system-model-rhetoric.md
```

## Reference Files

- `SKILL.md`: Main skill instructions, trigger description, workflow, and output contract.
- `references/style-principles.md`: Target voice, sentence patterns, tone controls, and anti-patterns.
- `references/system-model-rhetoric.md`: Section-level organization for story-like system model writing.
- `references/example-patterns.md`: Example-driven rewriting patterns for common system model cases.
- `references/quality-checklist.md`: Final review checklist for meaning preservation, notation consistency, and IEEE/TON style.
- `references/source-notes.md`: Additional notes used by the skill.

## Installation

Clone this repository into your Codex skills directory, or copy the `ieee-ton-system-model-polisher` folder into the local skills folder used by your Codex environment.

Example:

```bash
git clone https://github.com/jintaowei-svg/skills.git ieee-ton-system-model-polisher
```

If your Codex environment expects each skill to live under a skills root, place the cloned folder there so that `SKILL.md` is at:

```text
<skills-root>/ieee-ton-system-model-polisher/SKILL.md
```

## Example Request

```text
Please polish the following system model section for an IEEE TON manuscript.
Keep all LaTeX notation and equations unchanged, but improve the narrative flow.
```

The skill will map the original meaning, rebuild the narrative order, polish the prose at section level, preserve the technical content, and return a LaTeX-ready version with revision notes when useful.

## License

No license has been specified yet. Add a license before public reuse or redistribution if needed.
