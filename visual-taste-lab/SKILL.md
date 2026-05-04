---
name: visual-taste-lab
description: Use when the user wants better-looking UI, fewer AI-looking webpages, a reusable design-language workflow, screenshot/URL-based aesthetic distillation, or adaptable visual direction for company sites, product landing pages, investor pages, institutional pages, transactional utility sites, dashboards, portfolios, or marketing pages.
---

# Visual Taste Lab

## Purpose

Turn vague taste requests into a repeatable design-language workflow. Use this before major UI work when the goal is not just "make it nicer" but "make it look like one coherent brand system".

## Core Rule

Do not start by redesigning pages. First create or infer the brand visual identity, then create the design language, then apply it.

The first question is not "how do we make this page prettier?" The first question is "what visual identity should this organization or product own?"

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
- Build/test results.
- A short final note with what changed and what still needs real assets/content.

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
- Do not delete unrelated files.
- Keep mobile clean with no horizontal overflow.
- Run build/tests when applicable.
- Commit and deploy if this project normally deploys from git.
```
