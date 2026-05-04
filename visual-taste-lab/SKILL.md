---
name: visual-taste-lab
description: Use when the user wants better-looking UI, fewer AI-looking webpages, a reusable design-language workflow, screenshot/URL-based aesthetic distillation, or adaptable visual direction for company sites, product landing pages, investor pages, institutional pages, transactional utility sites, dashboards, portfolios, or marketing pages.
---

# Visual Taste Lab

## Purpose

Turn vague taste requests into a repeatable design-language workflow. Use this before major UI work when the goal is not just "make it nicer" but "make it look like one coherent brand system".

## Trigger When

- The user asks to improve, polish, redesign, modernize, de-AI, or make a UI look more premium.
- The work involves a website, product surface, dashboard, portfolio, investor page, institutional page, transactional flow, or marketing page.
- The user provides screenshots, URLs, brand references, competitor references, or asks to derive taste from examples.
- The project needs a reusable visual system before implementation.

Do not use this skill for pure copy editing, backend work, accessibility-only audits, or small bug fixes unless visual language decisions are part of the request.

## Core Rule

Do not start by redesigning pages. First create or infer the brand visual identity, then create the design language, then apply it.

The first question is not "how do we make this page prettier?" The first question is "what visual identity should this organization or product own?"

## VI-First Guardrail

Before choosing an archetype, layout, palette, or component style, identify the visual identity anchors:

- Logo or wordmark: shape, rhythm, weight, and any color cues.
- Color roles: primary, secondary, accent, neutral, and semantic states.
- Type attitude: institutional, technical, editorial, commercial, operational, playful, or minimal.
- Geometry: square, modest radius, rounded, modular, document-like, or app-like.
- Imagery: product shots, screenshots, diagrams, people, documents, editorial media, or none.
- Site type: company website, product website, transactional utility, institutional page, dashboard, portfolio, or other.

If references conflict with the existing brand, state the conflict and choose a direction deliberately. Do not replace a viable existing VI just because a reference looks fashionable.

## Workflow

1. **Collect references**
   - Prefer full-page screenshots, URLs, brand sites, existing codebase, or 3-5 inspiration links.
   - If no references exist, infer a design language from the product type and audience.

2. **Run a VI and site-type audit**
   - Identify the logo or wordmark if one exists. Treat it as the strongest visual anchor.
   - Identify current brand colors, likely primary color, secondary color, accent color, neutral system, and semantic colors.
   - If the brand has no clear VI, create a provisional VI direction and state why it fits.
   - Decide whether the site is primarily a **company website** or a **product website**.
   - Company websites should foreground the organization, business structure, credibility, partners, investors, and contact paths.
   - Product websites should foreground product value, features, demos, pricing, proof, and conversion.
   - Do not let a company website accidentally become a single-product landing page unless the user explicitly asks for that.

3. **Classify the project**
   - Pick one archetype from [references/archetypes.md](references/archetypes.md), or blend two if needed.
   - Name the direction in one short phrase, e.g. `credible company brief`, `quiet institutional clarity`, `sharp transactional utility`.

4. **Distill design language**
   - Produce a concise `docs/design-language.md` or equivalent.
   - Use [references/design-language-template.md](references/design-language-template.md).
   - Include VI anchors, logo usage, color roles, typography, spacing, surfaces, components, CTA rules, motion, imagery, and anti-patterns.
   - Keep decisions implementable: use concrete tokens, component rules, and page patterns.

5. **Prototype before committing to a full rebuild**
   - Create 1-3 small visual previews when the user is choosing style.
   - Each preview should show hero, data cards, content cards, table/list, form/CTA, and mobile behavior.
   - If showing multiple previews, each preview must use a meaningfully different VI territory, not just the same layout with different copy.
   - Show palette swatches and explain what audience each VI serves.

6. **Apply system-first**
   - Update shared tokens and components before isolated page tweaks.
   - Reuse the same button, card, badge, table, section, and CTA language across key pages.

7. **Verify**
   - Build/test the project.
   - Check desktop and mobile for horizontal overflow.
   - Check title/H1/CTA visibility when it is a website.
   - Check that repeated UI elements share the same token/component rules.
   - Keep honest claims: do not invent cases, customers, metrics, or product status.

## Design Standards

- Typography should create hierarchy before decoration does.
- Color should be restrained: 1 dominant neutral system, 1 main accent, 1 support color.
- Brand colors must have roles. Do not use random accent colors because they look fashionable.
- Logo, color, typography, imagery, and component geometry should feel like one brand, not one downloaded template.
- Company sites should explain the company first. Product sites should sell the product first.
- Cards should explain information boundaries, not fill space.
- Buttons should be reserved for real actions and use consistent visual priority.
- Tables and status blocks are preferred for credibility-heavy content.
- Motion should be subtle and structural; avoid random animated decoration.
- For business and institutional audiences, clarity beats spectacle.

## Anti-Patterns

- "高级一点" without tokens or references.
- Purple/blue gradient hero by default.
- Treating every company website like a SaaS product landing page.
- Ignoring an existing logo, brand color, or industry expectation.
- Changing colors module by module without a palette system.
- Every section as a floating card.
- Oversized cards nested inside cards.
- Mixed visual languages across modules.
- Fake case studies, fake partners, fake operational status.
- Videos or heavy assets loaded all at once on page load.

## Output Contract

For a real project, aim to deliver:

- `docs/design-language.md` or a project-local equivalent.
- A short VI brief: logo anchor, primary color, secondary color, accent color, neutral system, typography direction, image direction, and site-type decision.
- Updated shared styles/components.
- 2-4 key pages redesigned or tightened.
- Build/test results, or a clear note when verification was not possible.
- A final note with changed files, the chosen visual direction, remaining content/assets needed, and any assumptions.

If the user only asks for strategy, deliver the VI brief, archetype choice, design-language outline, and next implementation steps instead of editing code.

## Acceptance Checklist

- The output starts from VI and site type before visual styling.
- The chosen archetype is named and mapped to the audience.
- Tokens cover colors, type, spacing, surfaces, radius, borders, and motion.
- Buttons, cards, navigation, tables/lists, forms, and CTAs have reusable rules.
- Company pages do not read like single-product landing pages unless requested.
- Product pages make value, proof, and conversion obvious.
- Desktop and mobile layouts avoid overlap, clipped text, and horizontal overflow.
- Claims, examples, metrics, partners, and screenshots are either supplied by the user or clearly marked as placeholders.

## Privacy Boundary

- Do not expose private project names, customer names, internal metrics, unreleased plans, credentials, tokens, or proprietary screenshots in generated templates, examples, or public docs.
- When creating reusable references, use generic project categories and fictional placeholders only.
- If a reference contains sensitive content, extract visual attributes such as palette, density, typography, and component behavior without repeating confidential details.
- Do not publish or commit user-provided business specifics unless the user explicitly asks and the repository is intended to contain them.

## Goal Prompt Template

Use this when the user wants a long-running implementation:

```text
/goal Use $visual-taste-lab to improve this project visually.

First distill a reusable design language from the provided references, screenshots, URLs, brand context, and existing codebase. Do not redesign immediately.

Start with a VI audit:
- Identify the logo or wordmark.
- Identify or propose primary color, secondary color, accent color, neutral palette, and semantic colors.
- Decide whether this is a company website, product website, transactional utility, institutional page, dashboard, portfolio, or another type.
- Explain how the visual identity supports the audience.

Then apply the design language to the key pages/components. Keep the style coherent across typography, color, spacing, cards, buttons, tables, navigation, CTAs, and motion.

Project type:
- [company site / investor page / product landing page / transactional utility / institutional page / dashboard / portfolio / other]

Audience:
- [...]

Required pages:
- [...]

Constraints:
- Do not invent fake cases or metrics.
- Do not leak private project names, customer details, internal metrics, credentials, or unreleased plans.
- Use generic placeholders for examples unless I provide approved public copy.
- Do not delete unrelated files.
- Keep mobile clean with no horizontal overflow.
- Run build/tests when applicable.
- Commit and deploy if this project normally deploys from git.
```
