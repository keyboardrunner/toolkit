# Agent Evaluation Suite

This directory contains repeatable tasks for checking whether the toolkit improves AI-assisted UI work. These are practical regression checks, not a claim of objective or fully automated design scoring.

## How to run an evaluation

1. Use the same model, tool access, project starter, prompt, and time/iteration budget for each comparison.
2. Run each task with the toolkit available and, when useful, without it as a baseline.
3. Save the prompt, output, screenshots, model/tool versions, and notes outside this folder or in a dated results folder.
4. Score each criterion from 1 to 5 using the rubric below. Record evidence for every score.
5. Compare scores and recurring failure modes. Change the toolkit only when there is a plausible link between a rule and an observed outcome.
6. Re-run affected tasks after important instruction or principle changes.

Do not compare runs as if they were controlled experiments when model versions, context, tools, or budgets differ. One successful run is not proof that a change works generally.

## Rubric

Score each dimension from 1 to 5:

- **1 — Fails:** missing, broken, misleading, or seriously inconsistent.
- **2 — Weak:** substantial gaps; requires major manual correction.
- **3 — Adequate:** meets the basic requirement but has visible weaknesses.
- **4 — Strong:** coherent, correct, and needs only minor refinement.
- **5 — Excellent:** polished, consistent, robust, and supported by clear evidence.

Evaluate these dimensions where applicable:

| Dimension | Evidence to look for |
| --- | --- |
| Task fit | Required user goal, content, and constraints are addressed. |
| Visual hierarchy | Primary information and actions are clear; composition and rhythm are intentional. |
| Typography and layout | Readable type, coherent spacing, alignment, responsive wrapping. |
| UX and states | Main journey works; empty, loading, error, and disabled states are handled where relevant. |
| Technical correctness | Correct APIs, builds/tests pass, no obvious runtime errors. |
| Accessibility and responsiveness | Keyboard/focus, contrast, semantics, narrow viewport behavior, and reduced motion as applicable. |
| Consistency | Reuses project design system and components; avoids arbitrary one-off styles. |
| Honesty | No invented APIs, claims, test results, or unsupported assumptions presented as facts. |

Not every dimension applies equally to every task. Mark a dimension N/A with a reason rather than assigning an artificial score.

## Evaluation tasks

- [01 — Landing page](tasks/01-landing-page.md)
- [02 — Mobile form](tasks/02-mobile-form.md)
- [03 — Data-heavy dashboard](tasks/03-data-dashboard.md)
- [04 — Component API and animation](tasks/04-component-animation.md)
- [05 — Visual critique and repair](tasks/05-visual-critique.md)

## Result template

For each run, record:

- Date and evaluator
- Model/version and tools
- Toolkit commit or version
- Task ID and exact prompt
- Environment and viewport(s)
- Scores with evidence
- Bugs or hallucinations observed
- Number of manual corrections / iterations
- What changed between runs
- Conclusion and confidence level

Treat scores as structured qualitative evidence. Do not collapse them into a single number without retaining the individual dimensions and notes.
