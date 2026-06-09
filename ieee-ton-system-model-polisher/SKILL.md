---
name: ieee-ton-system-model-polisher
description: polishes, rewrites, and restructures system model sections for ieee/acm transactions on networking style manuscripts and related networking papers. use when the user provides draft paragraphs, latex text, assumptions, notation, equations, problem formulations, or chinese/english technical writing that needs clearer academic english, fuller preservation of meaning, more readable narrative flow, and a story-like progression from scenario to variables, assumptions, equations, constraints, and objectives.
---

# IEEE TON System Model Polisher

## Purpose

Transform an already drafted networking-paper system model into clear, complete, and publication-appropriate academic writing. Preserve the author's technical meaning, notation, assumptions, and logical dependencies while making the section read like a guided story: what system is considered, who interacts with whom, what is decided, how performance is measured, and why the resulting formulation follows naturally.

## Default workflow

1. **Map the original meaning before editing.** Identify entities, indices, sets, time scale, traffic/task model, channel/network model, decisions, constraints, performance metrics, and the final optimization or analytical goal.
2. **Rebuild the narrative order.** Prefer the sequence: operational scenario → entities and topology → time/demand model → decisions/control variables → costs/constraints → problem handoff.
3. **Polish at section level, not only sentence level.** Merge repetitive short sentences, add transition sentences where needed, and move definitions closer to their first use.
4. **Preserve all technical content.** Do not invent assumptions, parameters, algorithms, or claims. If a missing link is necessary, either write a conservative bridge using existing content or mark it as “author check needed.”
5. **Make equations readable.** Introduce each equation before it appears and explain its symbols or implication immediately after it appears. Avoid dumping equations without narrative context.
6. **Return a LaTeX-ready polished version.** Keep LaTeX commands, labels, citations, equation references, and notation intact unless the user asks for plain text.
7. **Add concise revision notes when useful.** After the polished text, include short notes on major improvements and any technical ambiguities that require author verification.

## Output format

For a normal polishing request, use:

```markdown
### Polished version
[latex-ready revised text]

### Revision notes
- [1-4 concise notes about structure, clarity, or author-check items]
```

For a long section, polish subsection by subsection and preserve headings. For a request that only asks for rewriting without commentary, provide only the polished version.

## Style principles

Use `references/style-principles.md` for the target voice, sentence patterns, tone controls, and common anti-patterns. The preferred style is formal, direct, and generous to the reader: precise enough for experts, but not needlessly compressed.

Key defaults:

- Prefer simple present tense for model statements: “we consider,” “the system consists of,” “let ... denote,” “the operator aims to.”
- Use active, controlled prose where possible: “we divide time into slots” is often clearer than “time is divided into slots,” unless passive voice improves focus.
- Define notation once, close to first use, and reuse it consistently.
- Use assumptions as narrative tools: state what is assumed, why it is reasonable or analytically useful, and how it affects the model.
- Avoid inflated claims such as “novel,” “significant,” “obviously,” or “very important” inside the system model unless the original text explicitly requires them.
- Avoid making the section sound like a list of variables. Every paragraph should answer a reader question.

## System-model rhetoric

Use `references/system-model-rhetoric.md` when the user asks for full-section restructuring, “story-like” writing, or major coherence improvements. The system model should usually answer these reader questions in order:

1. What network or computing scenario is being modeled?
2. What are the main entities and how are they indexed?
3. What evolves over time, space, traffic, channel state, or service demand?
4. What decisions are controlled by the algorithm/operator/user/device?
5. What physical, resource, latency, energy, queueing, or reliability constraints apply?
6. What metric is optimized or analyzed, and how does it connect to the next section?

## Example-driven polishing

Use `references/example-patterns.md` when the user asks for examples, wants a stronger “story,” or provides text that is grammatically acceptable but mechanically organized. The examples are illustrative patterns, not fixed templates.

## Quality check before finalizing

Use `references/quality-checklist.md` before answering substantial requests. Confirm that:

- every original technical object is either preserved, merged with an equivalent object, or flagged;
- every new transition is logically implied by the original draft;
- notation, indices, equation references, and citation commands remain consistent;
- the polished prose is readable without diluting the technical meaning;
- the final paragraph naturally leads to the problem formulation, algorithm, analysis, or simulations.

## Handling Chinese input

When the user provides Chinese technical prose or Chinese explanations of the intended model, produce polished English unless the user asks for Chinese output. Translate meaning rather than word order. Keep the Chinese author’s intended emphasis, but rewrite into conventional IEEE-style academic English.

Use bilingual reasoning internally when necessary: first infer the intended technical relation in Chinese, then express it as clean English. Do not expose unnecessary translation notes unless ambiguity remains.

## Safety against over-editing

If a sentence is already clear and technically precise, keep it close to the original. The goal is not to make all prose ornate; it is to make the model easy to follow. “Like telling a story” means coherent progression, not casual language.
