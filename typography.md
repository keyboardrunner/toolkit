---
title: Typography
status: draft
applies_to: [web, mobile, landing]
last_reviewed: 2026-10-06
sources:
  - https://www.figma.com/resource-library/typography-in-design/
  - https://medium.com/@atnoforuiuxdesigning/typography-in-ui-design-10-rules-that-will-instantly-improve-your-interfaces-60604c8cb825
  - https://www.nngroup.com/topic/typography/
  - https://developer.apple.com/design/human-interface-guidelines/typography
  - https://m3.material.io/styles/typography/overview
---

# Typography

Baseline typography rules for any interface built from this toolkit. Values marked **(default)** are starting points the owner has not yet confirmed; change them here, not in individual projects.

## Platform precedence

Pick the section that matches the target platform. The platform's own guidelines override the generic web rules below wherever they conflict.

| Target | Source of truth |
| --- | --- |
| iOS / iPadOS | Apple Human Interface Guidelines, Typography: https://developer.apple.com/design/human-interface-guidelines/typography |
| Android | Material Design 3, Typography: https://m3.material.io/styles/typography/overview |
| Web, landing pages, cross-platform | This file (sections "Core rules" below) |

### iOS (Apple HIG)

**Rule:** Follow the HIG. Use the system text styles (e.g. body, headline, caption) instead of hard-coded sizes, and use the system font (SF Pro; NY for serif needs) unless the brand requires otherwise.
**Why:** Text styles bundle weight, size and leading, and scale with Dynamic Type and the larger accessibility sizes. Hard-coded sizes do not.
**Do:** Support Dynamic Type everywhere; make sure layouts do not clip or break at large sizes. If a custom font is required, scale it relative to a text style.
**Don't:** Go below the smallest system text style (caption styles are 11 pt). Do not use ultra-light weights for small text.
**Check at implementation time:** Exact style sizes and leading change between OS versions. Read the current HIG page instead of relying on numbers copied here.

### Android (Material Design 3)

**Rule:** Follow Material 3. Use the type scale roles (display, headline, title, body, label, each in large / medium / small) through the theme's typography tokens, not ad-hoc sizes.
**Why:** Roles describe purpose (e.g. body is for long-form text, label for buttons and small annotations), so hierarchy stays consistent and themeable.
**Do:** Map each text element to a role first, then set family/weight by overriding the role in the theme if the brand needs it.
**Don't:** Invent sizes outside the scale. Do not use display or headline roles for long text.
**Check at implementation time:** Read the current M3 typography pages for sizes and the Expressive variants.

## Core rules (web, landing, cross-platform)

### 1. Hierarchy first
**Rule:** Define the hierarchy before choosing styles: heading, subheading, body, supporting text (labels, captions, metadata). A screen must make its most important text obvious at a glance.
**Why:** Without hierarchy everything competes and users scan poorly.
**Do:** Form label small, medium weight, muted; input text regular, dark; error text small, error color with an icon.
**Don't:** Set everything to the same size, weight and color.

### 2. Use a type scale, not random sizes
**Rule:** All font sizes come from one modular scale. **(default)** Perfect Fourth (1.333) for general UI and landing pages; Major Third (1.25) for content-heavy reading; Major Second (1.125) for dense dashboards.
**Why:** Related sizes read as intentional. Arbitrary sizes read as noise.
**Do:** Base on body size (16px = 1rem) and derive the rest.
**Don't:** Add a one-off 17px or 19px for a single element.

### 3. Maximum two typefaces
**Rule:** At most two families per product (heading + body). One family with several weights is the preferred default.
**Why:** More families rarely help and quickly fragment the UI. Pairing works best when the fonts differ clearly in role and have multiple weights and distinct letterforms.
**Do:** Same family in different weights; or serif heading + sans body; or geometric sans + humanist sans.
**Don't:** Pair two serifs, mix two display fonts, or pick a font by looks without testing it at body size with real content.
**Also check:** The font covers every script the product needs (e.g. Cyrillic, Latin Extended). Monospace is allowed for code only.
**Default family:** TODO(owner).

### 4. Line height
**Rule:** **(default)** Body 1.5–1.6; headings 1.1–1.3; captions and labels 1.3–1.4. The larger the text, the tighter the line height.
**Why:** Too tight is claustrophobic, too loose breaks rhythm. Body text usually needs the most room.
**Note:** The Figma guide cites 1.125–1.2 as general readability leading. Treat that as the heading range, not the body range.

### 5. Letter spacing
**Rule:** **(default)** Large headings (32px+): slightly negative, about -0.5px to -2px. Body: 0 (up to +0.2px). ALL CAPS, small caps and tiny labels: positive, 0.05em–0.15em.
**Why:** Large text looks loose at default spacing; capitals need air to stay legible.
**Don't:** Apply one tracking value everywhere. Do not track out lowercase body text.

### 6. Line length
**Rule:** **(default)** Long-form body text: max-width about 65ch, never above 75ch. Short UI copy (labels, descriptions): 40–50 characters is fine.
**Why:** Lines that are too long make readers lose their place; too short breaks reading flow. The sources differ slightly (40–60 vs 60–75 characters), so this default sits at the overlap and the owner may tighten it.
**Do:** Constrain the text container with `max-width: 65ch`. If lines must be longer, increase line height.

### 7. Size, units and responsiveness
**Rule:** **(default)** Body text is at least 16px on web, including mobile web. Define sizes in rem so user browser settings are respected. Use fluid sizing (`clamp()`) instead of many breakpoints for large headings.
**Why:** Small text on phones is painful to read, and users must be able to scale text.
**Do:** Adjust more than size on small screens: check line height and weight too.
**Don't:** Just scale desktop sizes down. Native iOS/Android use their platform rules above.

### 8. Weight and color carry hierarchy, not only size
**Rule:** **(default)** Use weights 400 (body), 500 (labels), 600 (emphasis), 700 (primary headings). Avoid 200 and below, and 800 and above, in UI. Use three text colors: primary, secondary (muted), disabled/placeholder.
**Why:** Weight and color create hierarchy without inflating size.
**Don't:** Make hierarchy levels too similar (e.g. 20px bold vs 18px semibold). Differences should be obvious: roughly 2:1 in size, or 700 vs 400 in weight.

### 9. Contrast and accessibility
**Rule:** Body text meets WCAG AA contrast (4.5:1 minimum; large text 3:1). Check weight, size and style contrast too, not only color.
**Why:** Low contrast is the most common legibility failure, and it is not fixed by font choice.
**Do:** Test text on every real background, including brand-color backgrounds and dark mode.
**Note:** NN/g reports large differences in reading speed between fonts and slower reading with age, so never block or fight user text scaling.

### 10. Whitespace around text
**Rule:** **(default)** Paragraph spacing ≈ body font size. More space above a heading than below it. Keep text off container edges (at least 16px padding on mobile, 24px on desktop). The gap between a heading and its body is smaller than the gap between sections.
**Why:** Spacing groups content and is part of the typography.

### 11. Case and alignment
**Rule:** Use sentence case for UI text. ALL CAPS only for short labels, with positive tracking. Never use all caps in chat or conversational interfaces. Left-align long text; center only short headings and quotes. Avoid fully justified text on the web.
**Why:** Caps lose word shape in long text and read as shouting in conversation. Justified text creates uneven spacing.
**Do:** Avoid single-word last lines ("danglies") by adjusting widths. On the web, `text-wrap: balance` for headings and `pretty` for body help.

### 12. Data, numbers and glanceable text
**Rule:** In tables and anywhere characters must be told apart (IDs, codes), use a typeface that passes the I-L-1 test (capital I, lowercase l and digit 1 are visibly different). Use tabular figures for aligned numbers (`font-variant-numeric: tabular-nums`). For text read at a glance (signage-like UI, dashboards on wall displays), use larger, non-condensed type.
**Why:** NN/g findings on distinguishable characters and glanceable reading.

### 13. Choose and test with real content
**Rule:** Evaluate typefaces with real content, at small and large sizes, on the actual brand colors. Do not decide from a specimen page.
**Why:** Letterform details (x-height, counters, ascenders) show up only in use.

## Quick checklist for agents

Before finishing any interface, confirm:
- [ ] Platform check done: iOS → HIG text styles, Android → M3 roles, else this file
- [ ] Hierarchy is visible; every size comes from the scale
- [ ] No more than two typefaces; font covers the needed scripts
- [ ] Body ≥ 16px (web), line height 1.5–1.6, line length ≤ 65–75ch
- [ ] Text contrast meets WCAG AA in every theme
- [ ] Text scales (rem on web, Dynamic Type on iOS, sp-based roles on Android)
- [ ] Numbers in tables use tabular figures; confusable characters are distinguishable

## Open decisions (owner)

- Default font family and pairing
- Default scale ratio per product type
- Whether line length target should be tighter (e.g. 60ch)
- Whether to pin a house style for headings (tracking, weight)
