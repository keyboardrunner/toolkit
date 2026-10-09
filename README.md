# toolkit

A curated knowledge base for AI-assisted product design and frontend development.

The toolkit helps agents find relevant principles, implementation resources, UX patterns, references, and repeatable workflows. It is not a package to install wholesale, and its entries do not replace the active project's code, design system, or official documentation.

## Start here

1. Read [AGENTS.md](AGENTS.md) for the agent workflow and operating rules.
2. Identify the platform, task, and constraints.
3. Read only the relevant principle and resource files.
4. Verify changing technical facts against official sources.
5. Implement, inspect the result, and validate it using available checks.

## Directory map

- `principles/` — reusable rules for visual design, interaction, accessibility, and content.
- `libraries/` — external libraries and tools, grouped by category (for example, `icons/` and `animation-libs/`).
- `components/` — reusable UI components and component references.
- `patterns/` — repeatable UX and product patterns.
- `references/` — visual/product references with notes about what to learn from them.
- `workflows/` — repeatable processes for design, implementation, and review.
- `evals/` — representative tasks and rubrics for checking whether agent output meets the intended quality bar.

### Animation content

Document third-party animation libraries under `libraries/animation-libs/`. Reserve a top-level `animations/` directory for original, reusable animation recipes or implementation patterns only if such material actually exists. Do not duplicate the same entry in both places.

## Source-of-truth order

When guidance conflicts, use this order:

1. Explicit user requirements.
2. The active project's design system, architecture, and instructions.
3. Relevant toolkit principles.
4. Toolkit catalog entries and examples.
5. The agent's general defaults.

For technical facts such as package APIs, versions, installation, and licensing, the current official source takes precedence over toolkit notes.

## Principles

See [principles/README.md](principles/README.md) for the index of current principles and planned topics. Only files that exist in the repository are active references; planned topics are not rules.

## Quality loop

Use the workflow in [workflows/ui-implementation.md](workflows/ui-implementation.md) for UI tasks when the environment supports running the app and inspecting screenshots. Use `evals/` to compare outputs against explicit criteria instead of relying on a vague impression that an agent has improved.
