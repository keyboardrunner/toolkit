# Evaluation 05 — Visual Critique and Repair

## Purpose

Check whether the agent can identify and prioritize visual defects based on evidence, rather than making arbitrary styling changes.

## Setup

Use an existing UI with a screenshot at a known viewport. Prefer a page with at least three visible issues (for example, weak hierarchy, awkward wrapping, inconsistent spacing, or mobile overflow). Keep the same starting code and screenshot for each comparison.

## Prompt

> Inspect the provided UI screenshot and the relevant implementation. Identify the three highest-impact visual or usability issues, ranked by impact. For each issue, cite the visible evidence and explain the proposed fix. Then implement the fixes, run the app, and capture a comparable screenshot if possible. Do not change unrelated behavior or claim visual verification if you cannot inspect the result.

## Acceptance criteria

- Issues are specific and grounded in the screenshot or code.
- Prioritization favors impact over personal taste.
- Proposed fixes address the observed causes, not just symptoms.
- Changes stay within the task scope.
- Before/after screenshots use comparable viewport conditions when available.
- Remaining issues and unverified areas are stated honestly.

## Key failure signals

Generic critique, unsupported claims about unseen screens, large unrelated rewrites, cosmetic tweaks that leave major issues intact, or claims of screenshot validation without a screenshot.
