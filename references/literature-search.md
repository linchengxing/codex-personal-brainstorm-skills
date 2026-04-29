# Literature Search Guide

Use this reference when the user asks for papers, related work, SOTA context, novelty checks, or literature-grounded idea discovery.

## Search Triggers

Search the web when:

- The user asks for literature, papers, citations, SOTA, related work, or "有没有人做过".
- The user explicitly asks to discover ideas and the idea space depends on prior art.
- A novelty claim would change the recommendation.
- The area is fast-moving, especially LLMs, diffusion, agents, VLMs, robotics, retrieval, benchmarks, or recent conference work.
- Exact facts matter: paper year, venue, benchmark name, architecture detail, dataset, or result.

## Source Priority

Prefer primary and stable sources:

1. arXiv pages or PDFs
2. OpenReview submissions and reviews
3. official conference or workshop pages
4. official project pages and code repos
5. publisher pages such as ACM, IEEE, Springer, Nature, Science
6. Semantic Scholar, Papers With Code, Google Scholar snippets, or lab pages only as discovery aids

For technical claims, rely on primary sources whenever possible.

## Early Exploration Literature Use

In early exploration, use references to expand thinking rather than to close the discussion.

Prefer:

- "this paper gives a useful lens"
- "this line of work suggests a tension"
- "this related area may be worth reading"
- "this result might challenge your assumption"

Avoid:

- turning references into a final method
- claiming novelty is settled too early
- building a full related-work section
- proposing experiments unless the user asks for validation or convergence

## Literature-Grounded Idea Discovery

When the user explicitly asks for ideas after a multi-turn discussion:

1. Start from the conversation state: accepted constraints, rejected branches, current focus, and open uncertainties.
2. Search only the literature needed to resolve novelty, baseline, or mechanism uncertainty.
3. Use papers to expose gaps, constraints, and tensions before proposing candidates.
4. Generate ideas only as responses to the literature map, not generic combinations of methods.
5. For each idea, state which paper or gap motivated it and what would make it fail.

If the user is still in normal Q&A mode, use literature to answer the current question or surface one insight. Do not turn a literature check into unsolicited idea generation.

## Search Strategy

Start broad, then narrow:

```text
<core mechanism> <task> arxiv
<method family> <failure mode> OpenReview
<benchmark/dataset> <mechanism> paper
survey <area> <year>
```

Track synonyms. For example:

- routing: gating, selection, conditional computation, mixture-of-experts
- memory: retrieval, cache, external memory, episodic memory
- robustness: OOD, distribution shift, stress test, adversarial, long-tail
- adaptation: test-time training, online adaptation, continual learning, personalization

## Reading Pass

For each relevant paper, extract only what matters for the user's idea:

```text
Paper: title, year, venue/source
Source/link: verified URL
Core idea: one sentence
Relation: supports / overlaps / competes / contrasts
Key detail: method, assumption, benchmark, or limitation
Implication: what it changes about the user's idea
```

If a paper is only weakly related, say so and avoid overfitting the discussion to it.

## Synthesis

After reading, organize by conceptual role:

- **Direct prior art**: closest methods that may threaten novelty.
- **Supporting evidence**: papers that make the idea more plausible.
- **Contradictory evidence**: papers or results that weaken the idea.
- **Methods/resources**: useful methods, datasets, or tools. Discuss baselines only when the user asks for validation or convergence.
- **Open gaps**: what the literature still does not answer.

End with the consequence for the idea:

```text
This literature suggests the idea should be reframed as ...
The novelty is probably not ...
The defensible angle may be ...
The first experiment should compare against ...
```

## Citation Discipline

- Include links for searched sources.
- Use exact paper titles only after verifying them.
- Distinguish "the paper shows" from "this suggests".
- Do not cite a source for a claim that was not checked in that source.
- If search results are thin or ambiguous, say what was searched and what remains uncertain.

## Output Template

```text
Literature map
- Closest prior art: title, year, source/link, relevance
- Adjacent useful work: title, year, source/link, relevance
- Baselines/tools: title or resource, source/link, why it matters

What this means for your idea
- ...

Next searches
- ...
```
