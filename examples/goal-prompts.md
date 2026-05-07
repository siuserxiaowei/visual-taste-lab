# Goal Prompts

Copy one of these prompts into Codex, Claude Code, or another coding agent that supports local skills. Replace bracketed fields with your project context.

## 1. Autonomous Visual Implementation

Use this when you want a long-running agent to inspect the project, define the design language, implement the changes, and verify the result.

```text
/goal Use $visual-taste-lab to improve this project visually from audit through implementation.

Work autonomously, but do not redesign immediately. First read the existing codebase, visible UI, screenshots, logo/wordmark, brand notes, and any references I provide.

Start with a VI audit:
- Identify the strongest visual anchors in the logo, wordmark, colors, typography, layout, imagery, and existing components.
- Classify the project type: company site, product website, transactional utility, institutional page, dashboard, portfolio, or other.
- Explain the audience, trust model, and what the interface should make obvious within the first few seconds.
- Name the visual direction in one short phrase.

Then create or update a reusable design-language brief before editing UI:
- color roles: primary, secondary, accent, neutral, semantic
- typography direction and scale
- spacing, radius, borders, surfaces, and shadow rules
- navigation, buttons, cards, forms, tables/lists, CTAs, imagery, and motion
- anti-patterns this project must avoid

After that, implement the design language system-first:
- Update shared tokens/styles/components before isolated page polish.
- Apply the direction to the key pages/components: [list pages/components].
- Preserve accurate product facts, routes, data structures, and existing working behavior.

Constraints:
- Do not invent customers, case studies, testimonials, partners, usage numbers, metrics, press quotes, screenshots, or proof.
- Do not leak private project names, customer details, credentials, internal metrics, unreleased plans, or proprietary screenshots.
- Use generic placeholders only when real approved copy/assets are missing.
- Do not delete unrelated files or perform destructive git operations.
- Keep desktop and mobile layouts free of clipped text, overlap, and horizontal overflow.
- Run build/tests when applicable, and add the smallest useful verification if the project has no test command.
- Stop and ask before making a brand direction choice if the references conflict with the existing VI.

Finish with:
- chosen visual direction
- design-language summary
- changed files
- verification results
- remaining assumptions or assets needed
```

## 2. Full Website Visual Refresh

```text
/goal Use $visual-taste-lab to improve the visual quality of this website.

First audit the existing visual identity from the logo, colors, typography, layout, screenshots, and codebase. Do not start redesigning immediately.

Then classify the site type, distill a reusable design language, and apply it to the main pages/components.

Constraints:
- Do not use a generic SaaS template.
- Do not invent customers, claims, metrics, partners, screenshots, or proof.
- Keep all existing product facts accurate.
- Keep mobile layouts free of horizontal overflow.
- Run build or tests when applicable.
- Summarize the design language, changed files, verification, and remaining assumptions.
```

## 3. Landing Page With Existing Brand

```text
/goal Use $visual-taste-lab to redesign the landing page for [fictional or approved public product name].

Use the existing logo and palette as the strongest visual anchors. Start with a VI audit, then define color roles, typography, spacing, buttons, cards, imagery, and CTA behavior.

After the audit, update the landing page so it feels specific to the brand and audience.

Constraints:
- Do not add fake testimonials, fake partners, fake usage numbers, fake press quotes, or fake case studies.
- Do not replace a viable existing VI just because a reference looks fashionable.
- Keep the mobile layout readable and free of horizontal overflow.
- Run the smallest relevant build/test command.
```

## 4. Dashboard Polish

```text
/goal Use $visual-taste-lab to make this dashboard calmer, clearer, and more professional.

First classify the dashboard's job: what should users scan first, compare second, and act on third?

Then define a compact design language for tables, filters, stats, status badges, empty states, forms, and navigation.

Implementation constraints:
- Preserve current data structure and routes.
- Improve density without making the UI cramped.
- Keep controls predictable and accessible.
- Do not invent operational metrics, customer names, or status data.
- Verify desktop and mobile breakpoints.
- Run build/tests when applicable.
```

## 5. Portfolio Direction

```text
/goal Use $visual-taste-lab to create a distinctive portfolio direction.

Infer a visual identity from [references / screenshots / current site]. Before editing, explain the intended personality, typography direction, palette roles, imagery style, motion level, and anti-patterns.

Then apply the direction to the homepage and project list.

Avoid generic gallery grids, vague claims, fake client work, and decorative effects that hide the work.

Verify mobile behavior and run build/tests when applicable.
```

## 6. Design Language Only

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

Constraints:
- Mark assumptions clearly.
- Do not invent customers, metrics, case studies, or proof.
- Do not include private or unreleased business details unless I explicitly provide approved public copy.
```

## 7. Small Scoped UI Pass

```text
/goal Use $visual-taste-lab for a focused UI pass on [page or component].

Run a brief VI audit first, then improve only this scope:
- [target page/component]

Keep the existing information architecture. Tighten hierarchy, spacing, color roles, component consistency, and responsive behavior.

Constraints:
- Do not modify unrelated files.
- Do not invent examples, metrics, or proof.
- Keep mobile free of horizontal overflow.
- Run the smallest relevant verification step.
```
