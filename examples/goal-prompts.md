# Goal Prompts

Copy one of these prompts into Codex, Claude Code, or another coding agent that supports local skills. Replace bracketed fields with your project context.

## 1. Full Website Visual Refresh

```text
/goal Use $visual-taste-lab to improve the visual quality of this website.

First audit the existing visual identity from the logo, colors, typography, layout, screenshots, and codebase. Do not start redesigning immediately.

Then classify the site type, distill a reusable design language, and apply it to the main pages/components.

Constraints:
- Do not use a generic SaaS template.
- Do not invent customers, claims, metrics, or proof.
- Keep all existing product facts accurate.
- Keep mobile layouts free of horizontal overflow.
- Run build or tests when applicable.
- Summarize the design language and changed files.
```

## 2. Landing Page With Existing Brand

```text
/goal Use $visual-taste-lab to redesign the landing page for [fictional product name].

Use the existing logo and palette as the strongest visual anchors. Start with a VI audit, then define color roles, typography, spacing, buttons, cards, imagery, and CTA behavior.

After the audit, update the landing page so it feels specific to the brand and audience.

Do not add fake testimonials, fake partners, fake usage numbers, or fake press quotes.
```

## 3. Dashboard Polish

```text
/goal Use $visual-taste-lab to make this dashboard calmer, clearer, and more professional.

First classify the dashboard's job: what should users scan first, compare second, and act on third?

Then define a compact design language for tables, filters, stats, status badges, empty states, forms, and navigation.

Implementation constraints:
- Preserve current data structure and routes.
- Improve density without making the UI cramped.
- Keep controls predictable and accessible.
- Verify desktop and mobile breakpoints.
```

## 4. Portfolio Direction

```text
/goal Use $visual-taste-lab to create a distinctive portfolio direction.

Infer a visual identity from [references / screenshots / current site]. Before editing, explain the intended personality, typography direction, palette roles, imagery style, motion level, and anti-patterns.

Then apply the direction to the homepage and project list.

Avoid generic gallery grids, vague claims, and decorative effects that hide the work.
```

## 5. Design Language Only

```text
/goal Use $visual-taste-lab to produce a design-language brief only.

Do not edit files yet. Review the current project and output:
- VI anchors
- site type
- audience assumptions
- color roles
- typography direction
- spacing and radius rules
- component rules
- imagery direction
- motion rules
- anti-patterns
- recommended implementation order
```

## 6. Small Scoped UI Pass

```text
/goal Use $visual-taste-lab for a focused UI pass on [page or component].

Run a brief VI audit first, then improve only this scope:
- [target page/component]

Keep the existing information architecture. Tighten hierarchy, spacing, color roles, component consistency, and responsive behavior.

Do not modify unrelated files. Run the smallest relevant verification step.
```
