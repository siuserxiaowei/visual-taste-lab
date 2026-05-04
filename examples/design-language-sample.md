# Design Language Sample

This is a fictional example of the kind of output Visual Taste Lab can produce before implementation.

## Brand

**Northstar Pantry** is a fictional planning tool for small hospitality teams that need clear purchasing lists, weekly menus, and supplier notes in one workspace.

## Site Type

Product website with a calm operational tone.

The page should show what the product does quickly, but it should avoid feeling like a loud growth landing page. The audience needs trust, clarity, and a sense that the tool will reduce daily coordination work.

## VI Anchors

- Wordmark: simple title-case wordmark with a small compass mark.
- Personality: organized, practical, warm, and quietly capable.
- Visual direction: clean workspace, paper list clarity, restrained interface previews.

## Color Roles

- Primary: deep pine green for navigation, primary actions, and selected states.
- Secondary: muted brass for highlights, dividers, and small emphasis.
- Accent: tomato red used sparingly for alerts or urgent inventory states.
- Neutrals: warm off-white background, soft gray surfaces, dark ink text.
- Semantic: green for ready, amber for attention, red for blocked, blue for informational notes.

## Typography

- Headings: confident sans serif with compact line height.
- Body: readable sans serif, medium contrast, generous line height.
- Data labels: smaller, slightly heavier text for scanability.
- Avoid oversized hero type inside operational UI panels.

## Layout And Spacing

- Use a 12-column desktop grid and a single-column mobile flow.
- Keep page sections unframed; use cards only for repeated items or contained tools.
- Prefer dense but breathable spacing: compact controls, clear section rhythm.
- Radius should stay modest, around 6px to 8px.

## Components

- Buttons: one primary action per section; secondary actions should be quiet.
- Cards: use for menu plans, supplier notes, and status summaries.
- Tables: compact rows, sticky headers when useful, clear status badges.
- Forms: labels above fields, direct validation, no decorative containers.
- CTAs: specific verbs such as "Create weekly plan" or "Review stock list."

## Imagery

Use real product screenshots or precise interface mockups. Avoid vague desk photos, abstract gradients, and images that do not explain the workflow.

## Motion

Motion should support state changes: drawer open, row update, filter apply, save confirmation. Avoid looping decorative animation.

## Anti-Patterns

- Loud neon startup styling.
- Generic hero sections with no product signal.
- Nested cards.
- Claims without proof.
- Decorative gradients that fight the product UI.

## Implementation Order

1. Define color tokens and type scale.
2. Update navigation, buttons, cards, tables, and forms.
3. Rework the hero around a real interface preview.
4. Tighten mobile spacing and prevent horizontal overflow.
5. Run build and visual checks.
