---
name: ieee-ton-algorithms-polisher
description: polishes, rewrites, and restructures algorithms sections for ieee/acm transactions on networking style manuscripts and related networking papers. use when the user provides algorithm descriptions, pseudocode, latex algorithm environments, complexity analysis, convergence/proof sketches, implementation steps, chinese/english technical writing, or reviewer-facing explanations that need clearer academic english, consistent variables with the problem formulation, step-by-step narrative, pseudocode-friendly wording, and a natural link to analysis or evaluation.
---

# IEEE TON Algorithms Polisher

## Purpose

Transform an already drafted networking-paper algorithm section into clear, complete, and publication-appropriate academic writing. Preserve the author's technical meaning, variables, pseudocode logic, update rules, assumptions, and stated guarantees while making the section read like a guided procedure: why the algorithm is needed, what information it uses, how each step progresses, and how the final solution connects back to the problem formulation.

## Default workflow

1. **Map the algorithm before editing.** Identify inputs, outputs, initialization, iteration index, state variables, update rules, stopping criteria, subproblems, feasibility repairs, complexity claims, and links to the formulated problem.
2. **Rebuild the narrative order.** Prefer the sequence: motivation from problem difficulty -> algorithm overview -> inputs/outputs -> initialization -> main loop or stages -> update rationale -> termination -> complexity/convergence/implementation discussion.
3. **Polish at section level, not only sentence level.** Merge repetitive step descriptions, add bridge sentences between pseudocode and prose, and keep definitions close to first use.
4. **Preserve all technical content.** Do not invent algorithmic steps, proofs, convergence guarantees, approximation ratios, complexity orders, or optimality claims. If a missing link is necessary, write a conservative bridge using existing content or mark it as `author check needed`.
5. **Make pseudocode readable.** Introduce the algorithm before the environment, explain non-obvious steps after the environment, and ensure prose uses the same variables as the pseudocode.
6. **Return a LaTeX-ready polished version.** Keep LaTeX commands, labels, citations, algorithmic environments, line references, equation references, and notation intact unless the user asks for plain text.
7. **Add concise revision notes when useful.** After the polished text, include short notes on major structural improvements and any technical ambiguities that require author verification.

## Output format

For a normal polishing request, use:

```markdown
### Polished version
[latex-ready revised text]

### Revision notes
- [1-4 concise notes about structure, clarity, or author-check items]
```

For a long section, polish subsection by subsection and preserve headings. For a request that only asks for rewriting without commentary, provide only the polished version. When the user asks for LaTeX source, put the source in a fenced code block so it can be copied safely.

## Style principles

Use `references/style-principles.md` for the target voice, sentence patterns, tone controls, and common anti-patterns. The preferred style is formal, direct, and explanatory: precise enough for experts, but not needlessly compressed.

Key defaults:

- Prefer simple present tense for algorithm descriptions: “the algorithm initializes,” “the controller updates,” “the iteration terminates,” “we solve.”
- Use active, controlled prose where possible: “we decompose the problem into two subproblems” is often clearer than “the problem is decomposed,” unless passive voice improves focus.
- Keep algorithm variables consistent with the problem formulation. Do not rename variables unless the user asks for notation revision.
- Explain what each stage achieves, not only what line number executes.
- Avoid unsupported claims such as “optimal,” “globally convergent,” “polynomial-time,” or “low-complexity” unless the original text establishes them.
- Avoid turning a paper algorithm into software documentation. The tone should explain mathematical logic, not implementation trivia.

## Algorithm-section rhetoric

Use `references/algorithm-section-rhetoric.md` when the user asks for full-section restructuring, a stronger story, or major coherence improvements. The algorithm section should usually answer these reader questions in order:

1. Why does the formulated problem need a dedicated algorithm?
2. What design idea is used: decomposition, relaxation, alternating optimization, matching, Lyapunov optimization, DRL, federated learning, game theory, graph methods, heuristic search, or another method?
3. What information is required as input, and what decision variables are produced as output?
4. How are variables initialized and updated?
5. What makes each update feasible or beneficial with respect to the original problem?
6. When does the algorithm terminate, and what is returned?
7. What complexity, convergence, or implementation discussion is supported by the draft?

## Pseudocode handling

Use `references/pseudocode-handling.md` when the user provides LaTeX algorithm environments, line-by-line descriptions, or mixed prose and pseudocode. Follow these defaults:

- Preserve the user's algorithm environment unless there is a clear syntax issue.
- Keep algorithm labels, captions, line references, and variable names consistent.
- If the input uses `algorithm`, `algorithmic`, `algorithm2e`, or custom macros, keep that style.
- Do not add new lines of pseudocode that change algorithm behavior.
- Convert vague line comments into concise, technical comments only when they clarify existing steps.
- Explain the algorithm in prose before and after the pseudocode; do not force all explanation into comments.

## Complexity and guarantee handling

Use `references/complexity-and-guarantee-handling.md` when the draft mentions complexity, convergence, optimality, approximation, stability, or proof sketches.

Defaults:

- Preserve any stated order such as `O(NK)`, `O(TN^3)`, or `\mathcal{O}(...)` unless it is clearly inconsistent.
- Do not derive a new complexity order without enough algorithmic detail.
- If the algorithm has nested loops, describe complexity in terms of the user's existing dimensions and iteration counts.
- If convergence is claimed, state the required conditions only if present in the draft.
- If the guarantee is heuristic or empirical, do not make it sound theoretical.

## Handling Chinese input

When the user provides Chinese technical prose or Chinese explanations of the intended algorithm, produce polished English unless the user asks for Chinese output. Translate meaning rather than word order. Keep the Chinese author’s intended emphasis, but rewrite into conventional IEEE-style academic English.

Use bilingual reasoning internally when necessary: first infer the intended technical relation in Chinese, then express it as clean English. Do not expose unnecessary translation notes unless ambiguity remains.

## Quality check before finalizing

Use `references/quality-checklist.md` before answering substantial requests. Confirm that:

- every original algorithmic step, variable, input, output, stopping criterion, and claim is preserved, merged with an equivalent object, or flagged;
- every new transition is logically implied by the original draft;
- prose and pseudocode use consistent notation;
- complexity and guarantee statements are not strengthened beyond the draft;
- the polished section naturally connects the problem formulation to analysis, implementation, or simulations.

## Safety against over-editing

If a sentence or pseudocode block is already clear and technically precise, keep it close to the original. The goal is not to make the algorithm ornate; it is to make the method easy to follow. “Like telling a story” means coherent procedural progression, not casual language.
