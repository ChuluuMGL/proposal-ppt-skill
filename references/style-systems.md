# Style Systems

Use this file when the user asks for richer visual directions, when no client VI exists, or when a proposal should deliberately use a recognizable style such as editorial, product-launch, magazine collage, cinematic, Web3, pixel, ink wash, or premium lifestyle.

A style system is not a color palette. It must define:

- visual grammar: composition, rhythm, image behavior, typography, texture, and density,
- component language: how proof objects, tables, timelines, cards, diagrams, and callouts change under the style,
- asset plan: what images, textures, SVG/HTML backgrounds, screenshots, or generated visuals are required,
- font system: free/commercial-safe font choices and fallbacks,
- page-type boundaries: which pages can use the style fully and which pages must return to a clearer business layout.

Do not clone protected brand templates, media layouts, logos, mastheads, or exact commercial designs. Use references as design grammar only.

## Reference Anchors

Use these sources as visual-grammar anchors, not as templates to copy:

- Swiss/grid systems: Poster House's Swiss Grid overview and The Vignelli Canon.
- Product-launch minimalism: Apple Human Interface typography/layout guidance and keynote-style one-idea slide practice.
- Fashion editorial: fashion typography/editorial discussions around high-contrast serif, white space, and image-led spreads.
- Japanese magazine collage: Japanese lifestyle/editorial magazine coverage around highly specific, browseable, image-caption dense spreads.
- Ink wash: ink wash painting principles such as monochrome tonal range, brushwork, red seals, spirit over literal imitation, and negative space.
- Web3/AI glass: contemporary dark UI, glassmorphism, dashboard, node-flow, and high-contrast interface patterns.

## Selection Rule

Use client VI or a user-provided reference deck first. Use these style systems only when the user requests a visual direction or no stronger visual source exists.

| Style System | Best For | Use As Full Deck? | Requires Images? |
|---|---|---:|---:|
| `swiss-boardroom` | B2B, consulting, finance, government-adjacent, formal tenders | Yes | Optional |
| `product-launch-minimal` | product strategy, AI/SaaS, big idea, launch, keynote-style pitch | Partial | Strongly recommended |
| `fashion-beauty-editorial` | beauty, fashion, premium consumer, hospitality, high-end lifestyle | Yes, with assets | Required |
| `japanese-magazine-collage` | social/content proposals, creator pools, lifestyle scenes, sample-heavy decks | Partial | Required |
| `cinematic-photography` | brand story, event, activation, case proof, experience design | Partial | Required |
| `web3-ai-glass` | Web3, crypto, AI, data platforms, fintech, automation | Yes, if legible | Optional |

Expressive add-ons:

| Add-on | Best Use | Boundary |
|---|---|---|
| `ink-wash` | Chinese culture, government-adjacent, heritage, premium ceremony pages | Use for cover, section, big idea, proof summary; keep dense pages clean. |
| `pixel-retro` | gaming, youth, interactive campaigns, gamified mechanisms | Use for creative/module pages; avoid budget/legal pages. |
| `oil-salon` | art, gifting, hospitality, culture, exhibition-like concepts | Use for cover/concept/case pages; keep numbers readable. |
| `e-reader-mono` | research, whitepaper, knowledge product, strategy memo | Can be full deck if the goal is calm reading. |

## Blueprint Output Requirement

When recommending a style, include this block in the proposal blueprint:

```markdown
### 视觉风格系统

- 推荐风格：
- 为什么适合本 brief：
- 不适合使用该风格的页面：
- 必需资产：
- 可由 AI 生成的资产：
- 字体建议：
- 缺少资产时的 fallback：
```

## Style Systems

### swiss-boardroom

Reference grammar: International Typographic Style, modular grids, asymmetry, sans-serif hierarchy, left-aligned precision, disciplined whitespace.

Use for: formal tenders, consulting decks, B2B service retainers, finance/government-adjacent proposals.

Visual DNA:

- 6/12-column grid, strict margins, flush-left typography.
- Large numeric markers, small labels, clear hierarchy.
- Mostly white/light grey canvas with black/navy text and one sharp accent.
- Minimal decoration; proof objects feel auditable.

Fonts:

- English/numbers: `Inter`, `IBM Plex Sans`, `Aptos`.
- Chinese: `Source Han Sans SC`, `Noto Sans CJK SC`, `Microsoft YaHei`.

Component transformation:

| Component | Swiss treatment |
|---|---|
| Brief translation | Audit table with row numbers and red/black status marks. |
| Decision criteria | Numbered grid, one criterion per cell, no illustration. |
| Proof object | Tables, bars, matrices, source notes, acceptance columns. |
| Timeline | Thin linear roadmap with phase numbers. |
| Budget | Audit-style table plus one decision callout. |

Page-type coverage:

- Full style: cover, brief audit, strategy, proof, budget, risk, team, closing.
- Avoid: overly expressive creative concept pages unless paired with a clear proof page.

### product-launch-minimal

Reference grammar: product-launch/keynote minimalism, one idea per slide, large dark or light canvas, hero visual, very short text.

Use for: AI/SaaS product strategy, launch proposal, big idea reveal, executive pitch.

Visual DNA:

- One sentence dominates the page.
- Product/idea hero occupies the visual center or one side.
- Extremely low density on reveal pages.
- Proof follows reveal: after every dramatic page, add a grounded evidence page.

Fonts:

- English/numbers: `Inter`, `SF Pro` when available, `Aptos`.
- Chinese: `Source Han Sans SC`, `Noto Sans CJK SC`, `PingFang SC`.

Component transformation:

| Component | Launch treatment |
|---|---|
| Winning thesis | One-line reveal page with hero image/object. |
| Module explanation | Three-step system, large labels, minimal copy. |
| Proof object | One chart/table only; no dense dashboard on reveal pages. |
| Roadmap | Big milestone cards, not Gantt-like detail. |
| Risk | Separate clean business page; do not hide under launch drama. |

Page-type coverage:

- Full style: cover, chapter divider, big idea, product value, closing.
- Hybrid style: proof, budget, KPI, risk pages must become clearer business pages.

### fashion-beauty-editorial

Reference grammar: high-fashion editorial typography, high-contrast serif headings, large photographic fields, white space, captions, product detail, glossy but restrained color.

Use for: beauty, fashion, premium consumer goods, hospitality, lifestyle campaigns.

Visual DNA:

- Image-led spread: product/person/scene carries the page.
- Editorial headline, caption, page folio, and narrow text columns.
- High contrast between large title and tiny credits/captions.
- Soft surfaces for beauty; sharper black/cream/red for fashion.

Fonts:

- English/numbers: `Playfair Display`, `Cormorant Garamond`, `Libre Baskerville`, `Inter`.
- Chinese: `Noto Serif CJK SC`, `Source Han Serif SC`, `Source Han Sans SC`.

Component transformation:

| Component | Editorial treatment |
|---|---|
| Cover | Magazine-spread style, oversized title, hero image. |
| Insight | Pull quote + product/person/scene image + short caption. |
| Proof object | Editorial proof board: image, caption, source, implication. |
| Content sample | Moodboard/sample spread, not generic cards. |
| Budget/KPI | Return to clean tables with editorial typography and restrained rules. |

Asset requirements:

- Product cutouts, product macro shots, lifestyle images, campaign mockups, creator/scene samples.
- Without images, use this style only for typography-led cover/divider pages.

### japanese-magazine-collage

Reference grammar: Japanese lifestyle magazines such as highly specific topic spreads, browsing density, image/caption clusters, stickers, small labels, and organized clutter.

Use for: social media proposals, creator pools, lifestyle/FMCG content, sample-heavy decks.

Visual DNA:

- Many small assets, each with a label, caption, and purpose.
- Grid exists, but objects may rotate or overlap slightly.
- Page feels browsable, not corporate.
- Rich proof-wall layouts for screenshots, samples, creator cards, product scenes.

Fonts:

- English/numbers: `Inter`, `IBM Plex Sans Condensed`, `Space Grotesk`.
- Chinese/Japanese-compatible: `Source Han Sans SC`, `Noto Sans CJK SC`, `LXGW WenKai` for warm captions.

Component transformation:

| Component | Collage treatment |
|---|---|
| Content pillars | Magazine board with image cards, captions, tags. |
| Creator pool | Catalog grid with headshots/samples and labels. |
| Platform strategy | Side-by-side screenshot/editorial notes. |
| Timeline | Issue-planning calendar or content map. |
| Budget | Keep as clean table; add small "included/not included" tags. |

Asset requirements:

- Screenshots, sample thumbnails, product/scene photos, creator examples.
- If assets are missing, request or generate placeholders before using the style deeply.

### cinematic-photography

Reference grammar: cinematic stills, dark/light contrast, wide crops, scene-first evidence, one strong commercial caption.

Use for: brand story, event, offline activation, case proof, experience design, product usage scenes.

Visual DNA:

- One dominant image or wide scene controls the page.
- Text sits on a dark band, quiet side panel, or image-safe area.
- Proof comes from real scene, not abstract cards.
- Color grading is part of the style: warm film, muted shadows, controlled highlights.

Fonts:

- English/numbers: `Inter`, `IBM Plex Sans`, `Libre Franklin`.
- Chinese: `Source Han Sans SC`, `Noto Sans CJK SC`.

Component transformation:

| Component | Cinematic treatment |
|---|---|
| Cover | Full-bleed or split scene with one claim. |
| Case proof | Photo + caption + transferable method. |
| Execution flow | Storyboard strip / shot list / scene sequence. |
| Risk | Clear business table; do not bury in image. |
| Closing | Hero image + cooperation promise. |

Asset requirements:

- Real scene/product/event photos or generated cinematic scenes.
- Always mark AI-generated visuals as conceptual unless the user says otherwise.

### web3-ai-glass

Reference grammar: dark data UI, neon accents, glass cards, nodes/flows, dashboards, technical trust signals.

Use for: Web3, crypto, AI, data platforms, fintech, automation, technical transformation.

Visual DNA:

- Dark structured canvas with subtle grid or depth.
- Neon accent is used for nodes, flows, risk, or active state.
- Glass cards are controlled; contrast must remain high.
- Components should explain architecture, asset flow, governance, and risk.

Fonts:

- English/numbers: `Space Grotesk`, `IBM Plex Mono`, `Inter`.
- Chinese: `Source Han Sans SC`, `Noto Sans CJK SC`.

Component transformation:

| Component | Web3/AI treatment |
|---|---|
| Architecture | Node map, system layers, data/asset flow. |
| KPI | Dashboard cards with clear units and deltas. |
| Risk | Risk-control matrix with triggers and owners. |
| Roadmap | Layered technical release path. |
| Budget | Transparent table; avoid neon overuse on numbers. |

Page-type coverage:

- Full style: strategy, architecture, dashboard, roadmap, risk, proof.
- Keep text at readable contrast; never use glow behind small body text.

## Asset-Heavy Style Rule

If the chosen style requires images and the user did not provide them:

1. Create an asset list by slide.
2. Ask whether to use user assets, AI-generated conceptual images, or placeholders.
3. If proceeding automatically, generate conceptual assets or use abstract editable backgrounds.
4. Mark generated images as conceptual in the presenter script when they are not real proof.

Do not pretend a deck has a photographic, editorial, ink, or product style if the only change is color and generic shapes.
