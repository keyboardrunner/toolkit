# UI Implementation Workflow

Use this workflow for non-trivial UI design or frontend implementation when the active environment supports the relevant steps. Scale it to the task; do not add ceremony to a one-line change.

## 1. Understand the task

Capture:
- user goal and audience
- target platform and viewport(s)
- primary user journey
- required content and states
- explicit constraints and acceptance criteria
- supplied references and what they demonstrate

Do not infer product requirements solely from visual inspiration. If a critical decision is missing, ask; otherwise state a reasonable assumption.

## 2. Inspect before choosing

- Read the active project's instructions and inspect its framework, components, styles, dependencies, and design tokens.
- Search the toolkit for relevant principles, patterns, components, libraries, and references.
- Read only applicable resources.
- Verify APIs, versions, and installation details against official sources.
- Prefer existing project components and conventions unless they prevent meeting the task.

## 3. Decide the design direction

Before implementation, define briefly:
- information hierarchy and page/screen structure
- visual direction and its relationship to references
- typography, spacing, color, and layout decisions
- interaction states and responsive behavior
- accessibility requirements

For a substantial page, establish a coherent visual system rather than styling each element independently. Avoid generic filler sections and decorative effects that do not support the task.

## 4. Implement

- Build the core user journey first.
- Use semantic, reusable components where they reduce inconsistency.
- Include relevant loading, empty, error, disabled, hover, focus, and success states.
- Support keyboard interaction, readable contrast, text scaling, and reduced motion where relevant.
- Keep the implementation aligned with the active project's architecture.

## 5. Run functional checks

Use available checks appropriate to the project:
- formatter, linter, type checker, and build
- unit or integration tests
- key interaction flows
- console/runtime errors
- links, forms, navigation, and state changes

Report unavailable checks honestly.

## 6. Inspect visual output

When the environment allows it, run the app and inspect screenshots at the primary viewport and at least one narrow viewport when responsive behavior matters.

Review:
- hierarchy: can the primary action and key information be found quickly?
- composition: alignment, balance, whitespace, and visual rhythm
- typography: scale, line lengths, wrapping, and legibility
- spacing: consistent relationships, not merely identical gaps everywhere
- color: contrast and meaningful use of semantic colors
- components: consistent variants, borders, radii, and states
- content: realistic copy, no unexplained placeholders, awkward truncation, or invented claims
- responsiveness: overflow, layout collapse, and touch target usability
- accessibility: focus visibility, semantics, keyboard operation, and reduced motion where relevant
- reference fidelity: preserve the intended qualities of supplied references without copying irrelevant details

Do not claim visual verification if screenshots or a running app were not available.

## 7. Critique and iterate

Write down the three most important defects, ranked by impact on usability or visual quality. Fix the highest-impact issues first. Re-run relevant checks and inspect the updated result.

Avoid endless cosmetic tweaking. Stop when acceptance criteria are met, no high-impact defects remain, and further changes have low expected value.

## 8. Final report

Summarize:
- what was implemented
- important design decisions and relevant toolkit resources
- checks actually run and their results
- visual viewports/states inspected, if any
- known limitations and anything not verified

## Quality gate

Before calling a non-trivial UI task complete, confirm:

- [ ] The implementation meets the stated user goal and acceptance criteria.
- [ ] Existing project conventions and design system were respected.
- [ ] Relevant toolkit guidance and technical sources were checked.
- [ ] Functional checks appropriate to the project were run or limitations stated.
- [ ] Visual output was inspected when the environment allowed it.
- [ ] No high-impact usability, responsive, accessibility, or visual defects remain unaddressed.
- [ ] The final report distinguishes verified facts from assumptions.
