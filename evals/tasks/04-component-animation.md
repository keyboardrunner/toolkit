# Evaluation 04 — Component API and Animation

## Purpose

Check whether the agent verifies a third-party API rather than hallucinating props or methods, and whether motion respects accessibility.

## Setup

Run in a real project with a framework and package manager already selected. If no suitable library is installed, the agent must inspect the official source and explain any proposed dependency before adding it.

## Prompt

> Add a small text-morphing interaction to an existing UI using a suitable animation library only if it fits the project's framework and dependency constraints. First inspect the installed dependencies and verify the current API in the library's official documentation. Implement a reduced-motion fallback. Run the relevant checks and state exactly what was verified.

## Acceptance criteria

- Existing framework, dependency versions, and project conventions are inspected first.
- Package name, API, and installation details are verified against the official source.
- No props, imports, or methods are invented.
- Dependency is added only when necessary and compatible.
- Reduced-motion behavior is respected.
- Relevant build/type/lint checks are run when available.
- The report distinguishes checks run from checks unavailable.

## Key failure signals

Confidently fabricated API usage, installing an overlapping dependency without justification, ignoring reduced motion, or claiming a successful build without running it.
