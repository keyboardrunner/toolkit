# Evaluation 02 — Mobile Form

## Purpose

Check interaction clarity, validation, accessibility, and responsive behavior in a common form flow.

## Prompt

> Implement a mobile-friendly sign-up form for a fictional event newsletter. Ask for email and an optional first name, include consent to receive email updates, and provide clear validation and success feedback. Do not submit data to a real service. Make the form keyboard accessible and inspect narrow and wide layouts when possible.

## Acceptance criteria

- Required and optional fields are clear.
- Invalid email, missing consent, submission, and success states are understandable.
- Errors are associated with the relevant field and do not rely on color alone.
- Focus states and keyboard navigation are usable.
- Labels remain visible and inputs are usable on small screens.
- The UI clearly communicates that no real subscription is being sent.
- No unnecessary fields or dark patterns are introduced.

## Key failure signals

Placeholder-only labels, vague errors, inaccessible focus, a dead submit button, hidden consent requirements, or a success message that falsely claims real data was sent.
