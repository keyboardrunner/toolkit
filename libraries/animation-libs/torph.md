# Torph

## Purpose

Torph is a focused text-morphing animation library for React, Vue, Svelte, and vanilla JavaScript. It animates transitions between text values by matching and moving text segments instead of simply replacing the whole string.

- Repository: https://github.com/lochie/torph
- Documentation and demos: https://torph.lochie.me/
- npm package: https://www.npmjs.com/package/torph
- License: MIT (verify the current repository license before production use)

## When to use Torph

- Animated headlines that rotate between short messages.
- Dynamic numbers such as prices, counters, scores, and dashboard metrics.
- Short labels and status text that change between states.
- Text transitions that need more character than a simple fade.
- Projects using React, Vue, Svelte, or vanilla JavaScript.

## When not to use it

- The animation concerns a whole component, page, image, or layout rather than text.
- A direct text update is clearer or less distracting.
- The project already has a text-animation utility that should be reused.
- Rapid or frequent motion would make important content harder to read.
- The active project's framework or runtime is incompatible.

Torph is a specialized text-animation tool, not a general-purpose animation framework.

## Installation

Install the dependency in the **active product project**, not in this toolkit repository. Check the official source for the current package instructions and framework entry points.

```bash
pnpm add torph
# or
npm install torph
# or
yarn add torph
```

## React examples

Use the official React entry point and confirm the current API against the repository before implementation.

### Morph between two labels

```tsx
import { useState } from "react";
import { TextMorph } from "torph/react";

export function BillingLabel() {
  const [annual, setAnnual] = useState(false);

  return (
    <button onClick={() => setAnnual((value) => !value)}>
      <TextMorph>
        {annual ? "Billed annually" : "Billed monthly"}
      </TextMorph>
    </button>
  );
}
```

### Animate a changing price

```tsx
import { TextMorph } from "torph/react";

export function Total({ amount }: { amount: number }) {
  return (
    <TextMorph>
      {amount.toLocaleString("en-US", {
        style: "currency",
        currency: "USD",
      })}
    </TextMorph>
  );
}
```

Use the product's actual locale and currency. Ensure the animation does not obscure the value or imply a change that has not occurred.

### Customize easing

```tsx
import { TextMorph } from "torph/react";

export function AnimatedLabel({ label }: { label: string }) {
  return (
    <TextMorph
      duration={400}
      ease="cubic-bezier(0.19, 1, 0.22, 1)"
      as="span"
    >
      {label}
    </TextMorph>
  );
}
```

Treat these snippets as implementation starting points, not a substitute for checking the current API. Verify available props, defaults, and framework-specific imports in the official documentation.

## API topics to verify

The project documentation describes configuration for animation duration and easing, scaling, locale-aware text segmentation, rendered element, styling, animation callbacks, and caret-aware matching for editable text. It also documents a React hook and framework-specific APIs for Vue, Svelte, and vanilla JavaScript.

Do not assume every option is available in every framework or that the API remains unchanged. Check the official repository before coding.

## Instructions for AI agents

When implementing a text transition:

1. Check the active project's framework, package manager, and existing dependencies.
2. If Torph fits, use the official framework-specific API; do not create a custom character-diff animation unnecessarily.
3. Prefer it for short labels, headlines, counters, prices, and status changes—not long paragraphs or rapidly changing body copy.
4. Preserve semantic HTML, accessibility, and existing project styles.
5. Follow the project's motion principles and honor reduced-motion preferences. Verify the library's current behavior and provide a reduced-motion or immediate-update path where needed.
6. Keep changing values legible, formatted, and visible long enough to understand.
7. Test initial render, repeated and rapid updates, responsive behavior, and editable text if applicable.
8. If the library is unsuitable or unsupported, use the project's existing motion tools or a simple text update.

### Discovery triggers

Consider Torph when the user asks for:
- text morphing or character-level text transitions
- rotating or animated headlines
- animated labels or status changes
- animated prices, counters, scores, or metrics
- spring-based text transitions

Example agent instruction:

> When a changing text value should morph rather than simply update, read `libraries/animation-libs/torph.md`. Check whether the active framework is supported, verify the current API, and use Torph if it fits the design and accessibility requirements.

## Source of truth

- Repository: https://github.com/lochie/torph
- Demos: https://torph.lochie.me/
- npm: https://www.npmjs.com/package/torph

The official repository and package documentation take precedence over this catalog entry if technical details change.

## Related

- Category: libraries
- Type: text animation / motion
- Path: `libraries/animation-libs/torph.md`
