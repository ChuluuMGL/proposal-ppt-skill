# Visual System

Use client VI first. Use a user-provided reference deck before any fallback style. Use this guide only when no stronger visual source exists. For page density and rhythm, use `layout-rhythm.md`. For richer default color choices, use `palette-library.md`. For style-rich routes, use `style-systems.md`, `asset-pipeline.md`, and `font-system.md`.

## Visual Style Families

Choose one primary family, then pick a specific palette from `palette-library.md`. If the user asks for a specific style such as magazine, launch, cinematic, Web3, pixel, ink, or beauty, choose a style system from `style-systems.md` instead of merely changing colors. Do not reuse the same green/gold palette for every proposal.

### corporate-trust

Use for consulting, B2B, finance, government-adjacent, annual service, and formal tenders.

- Base: `#FFFFFF`, `#F7F8FB`, `#EEF2F7`
- Text: `#0B1220`, `#172033`, `#5C667A`
- Primary: `#123C69`, `#0E5E43`
- Accent: `#C6A15B`, `#2F80ED`
- Feel: restrained, precise, evidence-led.

### brand-growth

Use for brand marketing, social media, content, creative campaigns, and growth proposals.

- Base: `#FFFFFF`, `#F8FAFE`, `#F2F6FF`
- Text: `#101828`, `#344054`, `#667085`
- Primary: `#0052D9`, `#0E5E43`
- Accent: `#FF7A45`, `#6C5CE7`
- Feel: energetic but not decorative; enough room for samples and screenshots.

### consumer-lifestyle

Use for FMCG, food and beverage, beauty, fashion, home, and lifestyle scenes.

- Base: `#FFFFFF`, `#FBF8F1`, `#FAF7F0`
- Text: `#101814`, `#4F5B52`, `#77746A`
- Primary: `#0E5E43`, `#8A4B2D`
- Accent: `#CDA34B`, `#D86D55`, `#3D83A5`
- Feel: warm, product-friendly, real-scene oriented.

### tech-intelligence

Use for AI, SaaS, digital platforms, automation, data, and productized services.

- Base: `#FFFFFF`, `#F6F8FC`, `#ECF3FF`
- Text: `#0A1020`, `#27364A`, `#637083`
- Primary: `#143D8F`, `#0B6B78`
- Accent: `#3B82F6`, `#16A34A`, `#F59E0B`
- Feel: structured, clear, architecture-driven.

## Layout Standards

- Use 16:9 widescreen.
- Use stable margins. Suggested safe area: left/right 56-72 px, top 36-48 px, bottom 32-44 px.
- Keep title zone, content zone, footer, and page numbers consistent.
- Align title, cards, tables, and diagrams to a grid.
- Use at most three information levels on normal slides: title, key content, support note.
- Break complex pages instead of shrinking core text.
- Distribute content through the intended content field. Avoid clustering all objects in the top half while leaving the lower third visually dead.
- Use empty space deliberately. A page may be sparse only when it is a title, section divider, big idea, quote, transition, or visual focus slide.
- Never place a large empty bordered placeholder on a client-facing slide. If an asset is missing, use a compact `待确认` note or restructure the slide.
- Do not use more than two consecutive pure tables or pure matrices without a strategy/sample/mechanism page.
- Use page numbers as two digits when appropriate: `01`, `02`, `03`.

## Typography

Preferred fonts:

- Chinese: PingFang SC, Microsoft YaHei, Source Han Sans
- English/numbers: Arial, Helvetica, Inter, Aptos

For style-specific and open-source font pairings, use `font-system.md`.

Suggested PPT sizes:

- Cover title: 48-64 pt
- Chapter title: 40-56 pt
- Normal slide title: 30-40 pt
- Lead/subtitle: 16-22 pt
- Body: 12-18 pt
- Dense table text: 10-13 pt
- Notes/source: 8-10 pt

When using the PowerPoint/presentations skill with no template, follow its minimum font-size requirements unless the deck has a stronger template or explicit compact business style.

Rules:

- Do not use text below 8 pt.
- Do not use negative letter spacing.
- Use no more than two font families and three weights.
- Keep title size, footer position, page number position, and table style stable across the deck.

## Graphics and Charts

- Prefer editable shapes, tables, and charts over blurry screenshots.
- Every chart needs a conclusion, not only a label.
- Prefer direct labels over complex legends.
- Keep flow diagrams to 3-6 major steps.
- Keep matrices to 2x2, 3x3, or up to 5 columns unless using an appendix.
- Use 1-1.5 pt lines for dividers and connectors.
- Keep icon style consistent. Use text labels when platform/logo use is not authorized.

## Images and Screenshots

- Use images only when they prove a commercial judgment or show real execution.
- Prefer real products, real scenes, platform screenshots, case screenshots, sample boards, and data dashboards.
- Crop screenshots cleanly.
- Use consistent frame style for screenshot groups.
- Do not stretch images.
- Do not rely on stock-looking dark, blurred, decorative images to carry the argument.
- Cite or label third-party sources when needed.
- For AI-generated images, HTML/SVG backgrounds, or texture assets, follow `asset-pipeline.md`.
- Keep commercial text, tables, budgets, KPI, and risk controls editable whenever possible. Use generated/HTML assets mainly as background, texture, collage, or hero visual layers.

## Minimal Template Asset

`assets/minimal-proposal-template.pptx` is a fallback starter only. Use it when:

- no client VI exists,
- no reference deck is supplied,
- the user still needs an editable PPTX quickly.

Do not force this template when the client has an established style.
