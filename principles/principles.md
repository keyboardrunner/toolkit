# Principles

`principles/` is the design-decision layer of the toolkit.

It defines reusable rules for how interfaces should look, behave, and communicate. These are defaults for AI agents and designers, not rigid requirements. Apply them with judgment and respect the precedence rules below.

## How to use this directory

When working on UI, interaction, visual design, or product experience:

1. Identify the platform and type of interface.
2. Read the relevant principle files before making design decisions.
3. Apply the principles as the default baseline.
4. Check the project's own design system for more specific rules.
5. Follow explicit user requirements over all toolkit principles.
6. Use catalog entries in other directories to find implementation resources that help realize the chosen design.

Do not read every principle file for every task. Read the files relevant to the decision being made.

## Precedence

When rules conflict, use this order:

1. User request
2. Project's own design system
3. `principles/`
4. Catalog entries in other toolkit directories

A principle is a default, not an excuse to override explicit project requirements.

## Platform rules

### Web and landing pages

Use the relevant files in this directory as the primary design baseline.

### iOS / iPadOS

Follow Apple's Human Interface Guidelines for platform-specific behavior and conventions.

### Android

Follow Material Design 3 for platform-specific behavior and conventions.

When a principle file contains platform-specific guidance, follow the platform's official documentation if it is more current or more specific.

## Principle map

### `typography.md`

Typography decisions:
- type scale
- font families and pairing
- font weights
- line height
- letter spacing
- line length
- responsive type
- platform typography
- typographic accessibility

Read when choosing or reviewing typography.

### `spacing-and-layout.md`

Layout decisions:
- spacing scale
- grid
- alignment
- containers
- density
- responsive layout
- composition
- whitespace

Read when defining page structure, component layout, or responsive behavior.

### `color.md`

Color decisions:
- palette roles
- semantic colors
- contrast
- surfaces
- text colors
- borders
- dark mode
- state colors

Read when creating or reviewing a color system or visual hierarchy.

### `motion.md`

Motion decisions:
- animation duration
- easing
- transitions
- interaction feedback
- entrance and exit behavior
- choreography
- reduced motion

Read when designing or implementing animation and interaction.

### `accessibility.md`

Accessibility baseline:
- keyboard interaction
- focus
- semantics
- contrast
- touch targets
- text scaling
- screen readers
- reduced motion
- inclusive interaction

Read for every interface, with particular attention to interactive components.

### `antipatterns.md`

Things to avoid:
- common UI mistakes
- misleading interaction patterns
- unnecessary visual complexity
- accessibility failures
- generic or low-quality design patterns

Read when reviewing existing work or making important design decisions.

## Decision model

Use principles to answer:

> "What should this interface look and behave like?"

Use catalog entries elsewhere in the toolkit to answer:

> "What resource or implementation approach can help me build it?"

For example:

1. `typography.md` defines the typographic direction.
2. `spacing-and-layout.md` defines the layout system.
3. `motion.md` defines the interaction behavior.
4. `libraries/` or `components/` provides implementation resources.
5. The project's own design system determines the final implementation.

Do not select a library first and then bend the design principles around it.

## When creating a new principle

Add a new file only when a recurring design decision deserves to be reusable across projects.

A principle should:
- describe a decision or rule
- explain why it exists
- distinguish defaults from confirmed decisions
- identify platform-specific differences where relevant
- link to authoritative sources when appropriate
- include practical guidance for AI agents
- avoid duplicating rules from other principle files

Prefer updating an existing principle over creating a new file when the topic already belongs there.

## Status

Principles may be marked as:

- `active` — currently applies
- `draft` — being developed
- `deprecated` — retained for reference but should not be used

Agents should not apply deprecated principles.

## Current structure

```
principles/
├── principles.md
├── typography.md
├── spacing-and-layout.md
├── color.md
├── motion.md
├── accessibility.md
└── antipatterns.md
```

Some files may not exist yet. Do not invent rules from files that are not present.

## Future principle areas

Potential future areas include:

- `content-and-language.md` — UI copy, tone, labels, errors, terminology
- `responsive.md` — responsive behavior and breakpoint philosophy
- `interaction.md` — interaction states, feedback, affordances
- `forms.md` — form structure, validation, errors, and input behavior
- `data-display.md` — tables, lists, metrics, charts, and information density
- `icons-and-imagery.md` — iconography, imagery, illustration, and visual assets
- `components.md` — component-level design rules
- `navigation.md` — navigation hierarchy and wayfinding

Only create these files when their rules become sufficiently developed and reusable.

## Agent checklist

Before finalizing a UI decision:

- [ ] Relevant principle files were checked.
- [ ] Platform-specific rules were considered.
- [ ] Project design-system rules were checked.
- [ ] User requirements were respected.
- [ ] Principles were treated as defaults, not absolute constraints.
- [ ] Implementation resources were selected after the design decision.
