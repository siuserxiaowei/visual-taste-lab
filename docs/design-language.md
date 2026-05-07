# Visual Taste Lab Design Language

This document defines the current Visual Taste Lab direction. It learns from Impeccable's disciplined workflow without borrowing its brand, palette, typography, page composition, commands, or case-study identity.

## Direction

- Name: VI-first taste lab
- Archetype: Technical Product Console + Editorial Brand System
- Site type: product website for a coding-agent skill
- Audience: developers, coding-agent users, and builders who need a reusable visual brief before UI implementation
- Impression in 5 seconds: thoughtful, methodical, visual, and practical
- What must feel true: the skill turns taste into implementable design constraints, not generic polish advice
- Primary user task: understand the workflow, inspect generated case images/screenshots, and copy a starter prompt
- Main risk if the design is wrong: it reads like another generic design-skill landing page instead of a VI-first method

## Brand / VI Audit

- Existing logo or wordmark: circular four-quadrant mark plus "Visual Taste Lab" wordmark in the header
- Logo shape language: compact audit seal, color-role quadrant, precise circular mark
- Logo constraints: keep the mark simple, high contrast, and small enough for docs, nav, and social preview use; do not turn it into Impeccable's editorial wordmark or magenta identity
- Existing primary color: `#203447`, deep blue used as the serious system anchor
- Existing secondary color: `#6F825F`, olive support for softer system states and secondary proof
- Existing accent color: `#C14E31`, brick red used for active emphasis, eyebrows, numbering, and high-signal moments
- Existing neutral palette: `#F7F5EF` paper, `#FFFDF7` surface, `#EEF3EF` alternate surface, `#15212B` ink, `#53616C` secondary text, `#7A858C` muted text
- If missing, proposed VI direction: not missing; refine the current warm paper, brick, blue, and olive system
- Why this VI fits the product: it feels like a design notebook, audit sheet, and working lab rather than a glossy SaaS launch page
- What this site must not be mistaken for: the Impeccable brand, a generic AI design marketplace, or a real-client agency portfolio
- Reference inputs used: current `index.html`, `visual-taste-lab/SKILL.md`, `references/archetypes.md`, design-language template, and the local Impeccable reference files
- Reference inputs rejected and why: Impeccable's magenta accent, Renaissance editorial layout, floating bottom nav, specific anti-pattern branding, and Neo Mirai event visual system are reference material only

## Company Site vs Product Site Decision

- Primary subject: product skill and reusable workflow
- Main visitor question: "Can this help my agent make coherent visual decisions?"
- Main credibility proof: explicit VI audit flow, color-role tokens, archetype previews, public screenshots, and verification requirements
- Main conversion action: copy/use the skill prompt
- Product role on this site: central subject
- Investor/partner role on this site: none
- Navigation priority: Method, Cases, Reference, Archetypes, Verify, Use it
- Above-fold priority: product name, VI-first promise, workbench preview, and prompt/workflow CTAs

## Tokens

### Color

- Background: `#F7F5EF`
- Background alternate: `#EEF3EF`
- Surface: `#FFFDF7`
- Surface raised: `#FFFDF7` with restrained shadow
- Surface subtle: `#F3EADF`
- Text primary: `#15212B`
- Text secondary: `#53616C`
- Text muted: `#7A858C`
- Border: `rgba(21, 33, 43, .14)`
- Border strong: `rgba(21, 33, 43, .32)`
- Brand primary: `#203447` / trust, system anchor, company-style demos
- Brand secondary: `#6F825F` / support, softer proof, secondary status
- Accent: `#C14E31` / active emphasis, section labels, numbered proof
- Accent soft: `rgba(193, 78, 49, .12)` / low-emphasis highlights only
- Success: `#286B57` / verified, ready, accepted states
- Warning: `#A96D19` / caution, pending, partial states
- Error: `#A13B35` / failed validation or unusable contrast
- Chart palette: `#203447`, `#C14E31`, `#6F825F`, `#D2A234`, `#2F6F9F`, `#53616C`
- Contrast notes: keep body text on warm surfaces dark; avoid gray text on saturated accents

### Typography

- Display: `Literata`, Georgia fallback
- H1: `Literata`, 86px desktop, 70px tablet, 44px mobile, compact line-height
- H2: `Literata`, 52px desktop, 42px tablet, 34px mobile, short editorial phrases
- H3: `Literata` for page/card headings; `IBM Plex Sans` for compact operational panels
- Body: `IBM Plex Sans`, 16-18px depending on prominence
- Metadata: `IBM Plex Mono`, uppercase only for short labels and command context
- Data/number: serif for big index numbers; monospace for token values and command lines
- Link: inherits text color by default; hover uses underline or border, not random color changes
- Line-height rules: display 1.04-1.25, body 1.6-1.75, metadata 1.4-1.7
- Max text width: body copy 55-70ch; hero lead about 680px; mobile copy must wrap without horizontal scroll

### Geometry

- Page width: `min(1180px, calc(100% - 40px))`
- Content width: use the shared `.wrap`; reduce to 32px/24px side gutters on tablet/mobile
- Grid: two-column hero, 2-column workbench internals, 3/4-column proof grids, one-column mobile collapse
- Section spacing: 82px desktop, 62px tablet, tighter mobile with preserved rhythm
- Card padding: 20-22px desktop, 16px mobile for tool panels
- Radius: `8px` default; pills only for real buttons, labels, and small mark treatments
- Border: 1px warm hairline; stronger borders only for active or primary states
- Shadow: one restrained warm shadow for raised previews, not every card
- Sticky/fixed elements: sticky top navigation only; no floating bottom nav by default
- Mobile breakpoints: around 1100px, 920px, and 640px, with explicit text wrapping and single-column cards

## Visual Identity Rules

- Logo usage: keep the circular quadrant mark paired with the wordmark; never replace it with an Impeccable-style wordmark
- Palette usage: warm neutral base first, deep blue for system authority, brick red for emphasis, olive/gold for support states
- Icon style: minimal line icons only when they clarify controls; avoid decorative icon tiles above headings
- Image/video style: prefer screenshots, generated workflow case images, visual audits, token swatches, and rendered previews; no unrelated stock imagery
- Illustration style: abstract diagrams can be geometric and token-driven, but must explain workflow
- Data visualization style: small, labeled, chart-safe palette; no decorative charts or unsourced metrics
- What should repeat across pages: token swatches, audit rows, modest cards, command panels, section kickers, proof/process rows
- What should never repeat: fake customer logos, fake performance numbers, nested cards, purple-blue gradient heroes, Impeccable branding cues

## Components

### Navigation

- Structure: sticky header with brand left, compact primary links center, and CTA actions right
- Active state: underline or current-color border; no animated bottom dock
- CTA placement: primary CTA appears in header, hero, and final "Use the Skill" section
- Mobile behavior: hide secondary nav before crowding; keep brand visible
- Scroll behavior: smooth anchors are acceptable; no scroll-jacking

### Buttons

- Primary: ink or context-specific dark fill with warm surface text; reserved for the main action
- Secondary: warm surface fill with hairline border
- Tertiary: text link or underline for low-emphasis navigation
- Disabled: muted text, no shadow, cursor/default state
- Loading: inline text change or small spinner only if real async behavior exists
- Icon usage: optional, small, and meaningful; text must remain readable

### Cards

- Default: one-level surface block with 1px border and `8px` radius
- Proof/data: numbered or labeled; use compact copy and a visible hierarchy
- Product/status: can use darker contextual panels inside the workbench and archetype previews only
- CTA: should not look like another proof card; clear action hierarchy
- Media: framed preview with stable aspect ratio and accessible labels
- Empty/loading: honest placeholder language; no fake metrics or clients

### Tables / Lists

- Header: concise label row, often monospace or uppercase
- Row rhythm: 50px minimum for audit rows, 10-14px internal gaps
- Density: scannable and compact, not dashboard-cramped
- Status cells: semantic colors only, always with text labels
- Mobile collapse: one-column row stack with label above value
- Empty/loading: state the missing input, not a fictional result

### Forms

- Label: visible, short, and above the field
- Input: warm surface, 1px border, 44px minimum touch height
- Error/help: message below field, error color plus clear text
- Submit: one primary action per form
- Success state: confirmation text with optional olive status
- Field grouping: use dividers and headings before extra card chrome

### Badges / Status

- Neutral: muted text on warm surface with hairline border
- Active: brick accent text or border
- Success: green/olive text and border with clear label
- Warning: gold with dark text
- Error: deep brick/red with explicit recovery copy
- Size and placement: small labels near the thing they describe; avoid badge confetti

## Page Patterns

- Hero: product name/promise, short VI-first explanation, primary and secondary CTA, visual audit preview
- First viewport must show: "Visual Taste Lab", the VI-first promise, and enough of the preview panel to signal the product visually
- Proof section: four-step workflow or audit checklist; no invented adoption metrics
- Product/offer section: generated case images and archetype previews must be clearly fictional and show different site jobs
- Case/progress section: use method examples, not customer case studies unless provided
- FAQ/compliance section: emphasize honest claims, privacy boundaries, and screenshot verification if added later
- Final CTA: command/prompt panel plus best-input checklist
- Footer: public-demo disclaimer, repo links, and fictional-demo disclosure
- Case gallery: use generated workflow images only when they teach the method; never frame them as customer outcomes
- Mobile-specific changes: single-column flow, full-width buttons, no clipped long words, no horizontal overflow

## Motion

- Page reveal: optional subtle fade/translate for sections; content must be readable without animation
- Hover: small color, border, or translate changes; no bounce or elastic easing
- Focus: visible outline with sufficient contrast
- Loading: only for real async states; static site should not fake progress
- Reduced motion: disable transforms and long transitions under `prefers-reduced-motion`
- Avoid: random decorative motion, cursor-follow effects, heavy canvas backgrounds, and motion that hides content

## Copy Rules

- Voice: clear, practical, design-literate, and agent-oriented
- Claim boundaries: describe what the workflow does; do not claim market adoption, customer results, or performance metrics
- CTA verbs: `View`, `Use`, `Copy`, `Start`, `Read`
- Placeholder rules: fictional demos must stay clearly marked; replace only with approved real inputs
- Forbidden language: "AI-powered magic", "future of design", fake client wins, fake partner logos, and reference-project brand claims

## Anti-Patterns

Do not:

- Copy Impeccable's magenta/rose identity, Cormorant/Instrument/Space Grotesk stack, floating nav, split-comparison branding, or case-study framing
- Use purple-to-blue gradients as a default signal of "AI"
- Turn every section into a floating card or put cards inside cards
- Add decorative icon tiles above headings
- Use gray body text over colored backgrounds
- Invent customers, metrics, testimonials, screenshots, or product status
- Let demo brands look real without a fictional disclosure
- Add visual complexity before the VI audit and token roles are clear

## Implementation Checklist

- Shared tokens are defined before one-off page styling.
- Repeated components use the same geometry, type scale, and state rules.
- Desktop and mobile screenshots show no clipped text, overlap, or horizontal overflow.
- CTAs have clear hierarchy and do not compete.
- Every metric, customer, partner, quote, or proof point is supplied or marked as placeholder.
- Private names, internal numbers, credentials, and unreleased details are not included in reusable docs.
- Reference projects are credited as inspiration only and never treated as Visual Taste Lab branding.
