# Quality Checklist

Use this checklist before returning a polished system model.

## Meaning preservation

- Are all entities from the original draft still present?
- Are all indices, sets, variables, parameters, and functions preserved or clearly renamed with reason?
- Are assumptions preserved without strengthening or weakening them?
- Are stochastic models, distributions, independence assumptions, and time scales unchanged?
- Are claims about optimality, convergence, novelty, or complexity unchanged unless the user requested substantive revision?

## Narrative completeness

- Does the section open with the considered system and modeling scope?
- Does each variable appear after the reader knows what object it describes?
- Are decisions introduced before the costs or constraints they influence?
- Does each equation have a lead-in and an interpretation?
- Does the final paragraph connect to the next section or problem formulation?

## IEEE/TON style

- Is the prose formal, direct, and free of exaggerated adjectives?
- Are sentences readable without oversimplifying technical meaning?
- Are paragraphs organized by modeling role rather than by a raw list of variables?
- Are abbreviations defined at first use?
- Are LaTeX commands, labels, citations, and equation references intact?

## Common author-check flags

Add an “author check needed” note if any of these occur:

- the original draft uses the same symbol for two different meanings;
- a variable appears in an equation but is never defined;
- a constraint is written but its physical meaning is unclear;
- a distribution or independence assumption is implied but not stated;
- the optimization objective does not match the prose description;
- the text says a decision is made “online” while requiring future information;
- time scales are inconsistent, such as per-packet scheduling combined with per-hour caching updates without explanation.

## Final reader test

After polishing, a reader should be able to answer:

1. What system is being modeled?
2. What are the main entities and indices?
3. What is random, time-varying, or controlled?
4. What decisions are made and under what constraints?
5. What performance metric or objective follows from the model?
6. Why does the next section naturally follow?
