# IEEE TON Writing Skills

This repository contains three sibling Codex skills for polishing major technical sections in IEEE/ACM Transactions on Networking style manuscripts.

The skills are organized as independent directories because each one targets a different manuscript section:

1. `ieee-ton-system-model-polisher`: system model writing
2. `ieee-ton-problem-formulation-polisher`: problem definition and formulation writing
3. `ieee-ton-algorithms-polisher`: algorithm section writing

Together, they support a common paper flow:

```text
System Model -> Problem Formulation -> Algorithms
```

Each skill can also be used independently when only one section needs revision.

## Repository Structure

```text
.
|-- ieee-ton-system-model-polisher/
|   |-- SKILL.md
|   |-- README.md
|   |-- agents/
|   |-- assets/
|   `-- references/
|-- ieee-ton-problem-formulation-polisher/
|   |-- SKILL.md
|   |-- README.md
|   |-- agents/
|   `-- references/
`-- ieee-ton-algorithms-polisher/
    |-- SKILL.md
    |-- README.md
    |-- agents/
    `-- references/
```

## Skills

### System Model

Use `ieee-ton-system-model-polisher` to rewrite and restructure system model sections. It focuses on scenario description, entities, topology, time and demand models, decisions, constraints, metrics, and the transition toward formulation.

### Problem Definition / Formulation

Use `ieee-ton-problem-formulation-polisher` to polish optimization problem definitions and mathematical formulations. It focuses on decision variables, objective construction, constraint explanations, notation consistency, and the transition from system model to algorithms.

### Algorithms

Use `ieee-ton-algorithms-polisher` to polish algorithm sections, pseudocode explanations, complexity discussion, convergence or guarantee statements, and the connection from the formulated problem to solution procedure.

## Installation

Clone the repository:

```bash
git clone https://github.com/jintaowei-svg/skills.git
```

Then install the specific skill folders you need into your Codex skills root. For example:

```text
<skills-root>/ieee-ton-system-model-polisher/SKILL.md
<skills-root>/ieee-ton-problem-formulation-polisher/SKILL.md
<skills-root>/ieee-ton-algorithms-polisher/SKILL.md
```

Do not install the repository root as a single skill. Install or copy the individual skill directories.

## Typical Use

For a full manuscript pipeline, use the skills in this order:

1. Polish the system model.
2. Polish the problem definition and formulation.
3. Polish the algorithm section.

For targeted revision, use only the skill that matches the section being edited.

## License

No license has been specified yet. Add a license before public reuse or redistribution if needed.
