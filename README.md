# toolkit
My personal toolkit for AI-assisted product design and development.

## Contents

- `principles/` — design decisions and rules for how interfaces should look and behave
- `libraries/` — useful external libraries and tools
- `components/` — UI components and component references
- `animations/` — animation references and implementations
- `patterns/` — UX and product patterns
- `references/` — visual and product references
- `workflows/` — workflows for AI-assisted development

## Principles

`principles/` holds the toolkit's design decisions: rules for how interfaces should look and behave. Principles are reusable defaults for AI agents, not project-specific implementation details.

Typical principle files include:

- `typography.md` — type scale, fonts, line height, measure/line length, and platform typography rules
- `spacing-and-layout.md` — spacing, grid, density, alignment, and layout rules
- `color.md` — palette roles, contrast, semantic color, and dark-mode rules
- `motion.md` — durations, easing, interaction motion, and reduced-motion behavior
- `accessibility.md` — accessibility baseline and inclusive interaction requirements
- `antipatterns.md` — patterns and decisions to avoid, with reasons

### Precedence

When rules conflict, use this order:

1. User request
2. Project's own design system
3. `principles/`
4. Catalog entries in other toolkit directories

### Platforms

General web and landing-page rules live in the relevant principle files. For native platforms, follow the platform's official guidance: iOS uses Apple's Human Interface Guidelines; Android uses Material Design 3. Relevant principle files should link to the current official guidance.
