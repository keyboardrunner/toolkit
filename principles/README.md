# Design Principles

This directory contains reusable defaults for how interfaces should look, behave, and communicate. Principles guide decisions; they are not rigid rules that override explicit requirements or a project's established design system.

## How to use these files

1. Identify the target platform and type of interface.
2. Read the principle files relevant to the decisions being made.
3. Check the active project's design system and requirements.
4. Apply principles as defaults, adapting them to the actual content and context.
5. Use catalog entries elsewhere in the toolkit to find implementation resources.
6. Review the implementation against the criteria in the relevant principles.

Do not read every file for every task. Do not treat planned topics below as existing guidance.

## Source-of-truth order

1. Explicit user requirements.
2. Active project's design system, architecture, and instructions.
3. Relevant principle files in this directory.
4. Toolkit catalog entries.
5. General agent defaults.

For current technical facts, official documentation takes precedence over copied examples or remembered details.

## Current principles

| File | Use when |
| --- | --- |
| [typography.md](typography.md) | Choosing type hierarchy, fonts, sizing, line height, line length, and text accessibility. |

Only files listed in this table are confirmed as current principles. Add a row when a new principle file is created.

## Platform guidance

- **Web / landing pages:** use applicable toolkit principles and the active project's design system.
- **iOS / iPadOS:** follow Apple's Human Interface Guidelines for platform-specific behavior and conventions.
- **Android:** follow Material Design 3 for platform-specific behavior and conventions.

Prefer current official guidance when it is more specific or has changed since a principle was reviewed.

## Creating or updating a principle

Create a new file when a recurring design decision deserves reuse across projects. Prefer updating an existing file when the topic already belongs there.

A useful principle should include:

- a clear rule and the reason behind it
- practical guidance, not just adjectives such as “clean” or “modern”
- defaults distinguished from confirmed project requirements
- good examples and anti-examples where they clarify the rule
- observable checks that an agent or reviewer can apply
- platform differences and exceptions
- authoritative sources for claims that need them
- a review date or note when details may become stale

Avoid duplicating the same rules across multiple principle files. Keep the index synchronized with the files that exist.

## Planned topics

These are candidates, not active rules. Create them only when their guidance is sufficiently developed and reusable.

- `spacing-and-layout.md` — spacing scale, grids, alignment, density, responsive composition.
- `color.md` — palette roles, semantic color, contrast, surfaces, and themes.
- `motion.md` — duration, easing, transitions, feedback, and reduced motion.
- `accessibility.md` — keyboard behavior, focus, semantics, contrast, scaling, and assistive technology.
- `antipatterns.md` — recurring UX and visual failures, with explanations and alternatives.
- `content-and-language.md` — UI copy, labels, terminology, and error messages.
- `forms.md` — input behavior, validation, and error recovery.
- `data-display.md` — tables, lists, metrics, charts, and information density.
- `icons-and-imagery.md` — iconography, imagery, and illustration.
- `navigation.md` — hierarchy, wayfinding, and navigation behavior.

## Agent checklist

- [ ] Relevant current principle files were read.
- [ ] The active project's design system and user requirements were checked.
- [ ] Platform-specific guidance was considered.
- [ ] Defaults were adapted to real content and context.
- [ ] Claims and technical details were verified where necessary.
- [ ] The implementation was reviewed against observable criteria.
