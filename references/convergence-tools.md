# Convergence Tools

Use this reference only when the user explicitly asks to converge, critique, prioritize, design validation, plan experiments, or prepare implementation.

Do not use this reference during early exploration.

## Critique Rubric

Score informally, not numerically unless the user asks:

- **Novelty**: is the contribution more than a recombination of familiar blocks?
- **Causal story**: is there a plausible reason the mechanism affects the metric?
- **Ablatability**: can the core claim be isolated from incidental engineering?
- **Baseline pressure**: would strong existing baselines make the improvement hard to show?
- **Resource fit**: can the user test it with available compute, data, and code?
- **Paper shape**: can the work become a clear claim, method, experiment, and limitation section?

When an idea is weak, identify the weakest link and propose one repair:

```text
Weakest link: ...
Repair path: ...
Cheap test: ...
```

## Experiment Planning

For a selected idea, produce:

- **Minimal prototype**: the smallest implementation that tests the mechanism.
- **Baselines**: current repo baseline, strongest known baseline, and one simple control.
- **Ablations**: remove or vary only the proposed mechanism.
- **Diagnostics**: measure the intermediate behavior the idea claims to improve.
- **Failure cases**: cases where the idea should not help or may hurt.
- **Stop rule**: what result would justify stopping, revising, or scaling up.

Keep the plan implementation-aware but do not write code unless asked.

## Output Shape

```text
Verdict
- ...

Strongest version
- ...

Main risks
- ...

Validation path
- ...

What to check in literature
- ...
```
