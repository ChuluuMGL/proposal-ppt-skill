# Style Systems

Use this file when the user asks for richer visual directions, when no client VI exists, or when a proposal should deliberately use a recognizable style such as editorial, product-launch, magazine collage, cinematic, Web3, pixel, ink wash, or premium lifestyle.

A style system is not a color palette. It must define:

- visual grammar: composition, rhythm, image behavior, typography, texture, and density,
- component language: how proof objects, tables, timelines, cards, diagrams, and callouts change under the style,
- asset plan: what images, textures, SVG/HTML backgrounds, screenshots, or generated visuals are required,
- font system: free/commercial-safe font choices and fallbacks,
- page-type boundaries: which pages can use the style fully and which pages must return to a clearer business layout.

Do not clone protected brand templates, media layouts, logos, mastheads, or exact commercial designs. Use references as design grammar only.

## Style DNA Gate

Before building any rich-style PPTX, define and check the style DNA. A named style is not approved until it has all six parts:

1. **Reference grammar**: 3-5 words that describe the source logic, such as strict grid, image-led spread, film still, pixel grid, ink diffusion, or glass depth.
2. **Asset behavior**: what real/generative images, textures, screenshots, cutouts, or SVG/HTML layers make the style visible.
3. **Typography signature**: heading font, body font, number font, scale contrast, and whether serif/mono/caption styles are allowed.
4. **Component grammar**: how cards, proof objects, tables, timelines, diagrams, labels, and captions change for this style.
5. **Density rhythm**: which slides are sparse, which are proof-dense, and where breathing slides appear.
6. **Anti-examples**: what must be rejected because it looks generic, decorative, or low-taste.

## Three-Page Style Sample Gate

When the user requests a strong visual style and no approved reference deck exists, do not scale the style directly to a full proposal. First create 3 full-size sample pages and review them at slide size:

| Sample | Purpose | Must Prove |
|---|---|---|
| Cover / big-idea page | Show the emotional and visual peak of the style. | The style is recognizable without reading the style name. |
| Proof / mechanism page | Show how the style carries business evidence. | Proof objects change form, not only color. |
| Dense business page | Show budget, KPI, risk, brief coverage, or timeline treatment. | The style remains readable and auditable under information pressure. |

Gate:

- If only the cover looks styled, the route is not approved.
- If the dense page becomes unreadable, restrict the style to cover, section, concept, and sample pages.
- If the proof/mechanism page falls back to ordinary rounded cards, redesign the component grammar before continuing.
- If the sample pages pass, record the approved grammar in the presenter script so later pages do not drift.

If the user asks for a strong style and no reference deck exists, first create a compact style direction checkpoint instead of building the full deck:

```markdown
### Style DNA Checkpoint

| Item | Decision |
|---|---|
| Style route |  |
| Visual grammar |  |
| Required assets |  |
| Typography signature |  |
| Component changes |  |
| Pages that should stay business-clean |  |
| Reject if it looks like |  |
```

Then build only 2-3 full-size sample pages for review when possible: one cover/big-idea page, one proof/mechanism page, and one dense business page. Do not mass-generate a full visual demo until these samples pass human review.

## Style Quality Bar

- Do not publish or bundle style reference PPTX files unless every slide has been reviewed full-size, not only as a contact sheet.
- Contact sheets are useful for rhythm checks, but they are not visual approval.
- Shape-only approximations are internal wireframes, not style templates.
- A slide that claims ink, oil, photography, magazine, pixel, or Web3 style must contain the visual grammar of that style, not only a matching palette.
- If the slide is built from crude circles, oversized ovals, generic cards, fake brush marks, or decorative neon dots, reject it and restart from assets/reference grammar.
- If the style requires assets and assets are missing, request/generate assets or explicitly downgrade to a clean business style.

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

### Full-Deck Style Systems

These systems can carry most of a proposal if the dense-page treatment is respected.

| Style System | Best For | Use As Full Deck? | Requires Images? |
|---|---|---:|---:|
| `swiss-boardroom` | B2B, consulting, finance, government-adjacent, formal tenders | Yes | Optional |
| `fashion-beauty-editorial` | beauty, fashion, premium consumer, hospitality, high-end lifestyle | Yes, with assets | Required |
| `beauty-gloss-clinical` | skincare, health-beauty, premium FMCG, product efficacy | Yes, with assets | Required |
| `japanese-minimal` | premium lifestyle, culture, education, calm executive strategy | Yes | Optional |
| `french-editorial` | hospitality, wine/food, luxury service, lifestyle brands | Yes, with assets | Recommended |
| `american-campaign-bold` | launch campaign, entertainment, sports, youth activation, growth pitch | Yes, if tone fits | Optional |
| `web3-ai-glass` | Web3, crypto, AI, data platforms, fintech, automation | Yes, if legible | Optional |
| `e-reader-mono` | research, whitepaper, knowledge product, strategy memo | Yes | Optional |

### Hybrid / Expressive Systems

These systems are strongest on cover, chapter, big idea, proof gallery, creative sample, and mechanism pages. Use clean business layouts for budget, risk, legal, KPI, and procurement-heavy pages unless the three-page sample gate proves they remain readable.

| Add-on | Best Use | Boundary |
|---|---|---|
| `product-launch-minimal` | product strategy, AI/SaaS, big idea, launch, keynote-style pitch | Reveal pages can be sparse; proof and budget pages must be clearer. |
| `japanese-magazine-collage` | social/content proposals, creator pools, lifestyle scenes, sample-heavy decks | Use for browsable proof walls; dense pages become index/table pages. |
| `cinematic-photography` | brand story, event, activation, case proof, experience design | Use for scene-led proof; dense pages need separate business treatment. |
| `ink-wash` | Chinese culture, government-adjacent, heritage, premium ceremony pages | Use for cover, section, big idea, proof summary; keep dense pages clean. |
| `pixel-retro` | gaming, youth, interactive campaigns, gamified mechanisms | Use for creative/module pages; avoid budget/legal pages. |
| `oil-salon` | art, gifting, hospitality, culture, exhibition-like concepts | Use for cover/concept/case pages; keep numbers readable. |
| `craft-paper-natural` | organic food, sustainability, handmade, agriculture, wellness | Use when natural materials and real product scenes exist. |

### Style Pack Component Rule

For every selected style, define how these components transform:

| Component | Must Decide |
|---|---|
| Cards | Are they cards, magazine clippings, glass panels, score tiles, exhibition labels, or ruled ledger rows? |
| Tables | What header, rule, spacing, and highlight behavior keeps them readable? |
| Timelines | Are they roadmaps, issue calendars, level paths, storyboards, release layers, or chapter folios? |
| Proof galleries | Are images full-bleed, captioned boards, contact sheets, framed art, pixel sprites, or dashboard thumbnails? |
| Callouts | Are they margin notes, seals, ticker chips, campaign stickers, glass alerts, or quiet footnotes? |

If component treatment is the same across styles, the style library has failed.

### Expressive Add-on Rules

Use these add-ons only when their visual grammar is visible. They are not palette names.

#### ink-wash

Visual DNA:

- Monochrome tonal range, brush diffusion, rice-paper texture, negative space, and one restrained red seal/accent.
- The page should feel like ink breathes across the canvas; proof objects remain precise and lightly ruled.
- Use asymmetry and silence: one dominant ink field is better than many decorative marks.

Asset/component requirements:

- Requires a real or generated ink texture, brush stroke, paper grain, or SVG/HTML ink layer.
- Tables and proof objects should use thin rules, ample margins, and small seal-like markers.
- Dense business pages should be clean editorial pages with ink only as texture or section marker.

Reject if it looks like:

- A black oval, donut, blob, or random brush sticker.
- Fake calligraphy with unreadable decorative text.
- Red seals used repeatedly as decoration instead of one deliberate accent.

#### pixel-retro

Visual DNA:

- Hard pixel grid, limited palette, stepped edges, tile rhythm, sprite-like icons, and no smooth gradients.
- Page logic should feel like a game interface, inventory, map, quest board, score panel, or level path.
- Pixel style works best when the proposal topic has youth, gaming, interactive, or gamified mechanics.

Asset/component requirements:

- Use HTML/SVG or generated bitmap assets to create crisp pixel grids, tiles, icons, and borders.
- Keep charts and tables readable by making the pixel treatment a frame/system, not tiny body text.
- Use monospaced or geometric fonts for English/numbers and clear sans-serif Chinese fallbacks.

Reject if it looks like:

- Normal rounded cards with a pixel font.
- Smooth shadows, blurred gradients, or anti-aliased decorative icons pretending to be pixel art.
- Random 8-bit icons that do not map to proposal logic.

#### oil-salon

Visual DNA:

- Canvas grain, warm gallery light, framed artwork, still-life composition, rich shadow, and ceremonial spacing.
- The page should feel curated like a gallery wall or exhibition poster, not like corporate beige.
- Use strong image/texture fields; flat vector ellipses cannot carry this style.

Asset/component requirements:

- Requires oil/canvas texture, generated still-life imagery, real art/product photos, or frame-like editorial crops.
- Concept pages can use large framed visuals; proof and budget pages should return to clean cream paper with thin warm rules.
- Captions should read like exhibition labels: short, precise, source-aware.

Reject if it looks like:

- Brown background plus flat circles.
- Generic vintage palette without canvas, lighting, image, or frame behavior.
- Decorative frames that make business proof harder to read.

#### e-reader-mono

Visual DNA:

- Monochrome or near-monochrome, e-ink contrast, quiet margins, serif/sans pairing, annotation marks, and document-like pacing.
- Best for research-heavy decks where the tone should feel reflective, credible, and slow.
- The style comes from reading rhythm, footnotes, folios, marginalia, and restrained diagrams.

Asset/component requirements:

- Use page folios, marginal notes, source blocks, quoted findings, and low-ink charts.
- Avoid heavy fills; use lines, spacing, and hierarchy to create structure.
- Works without images, but benefits from scans, diagrams, or source excerpts when permitted.

Reject if it looks like:

- A plain black-and-white corporate deck.
- Dense Word-document pages pasted into PPT.
- Tiny gray text that sacrifices readability for a printed-paper mood.

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
- Commercial proof feels like an art-directed spread, not a card dashboard.

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
- Detail density is intentional; every small object must carry a caption, tag, source, or implication.

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
- Glow and gradients must reveal system structure; colored circles alone are not Web3/AI style.

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

### beauty-gloss-clinical

Reference grammar: premium skincare decks, clinical clarity, glossy product macro, soft light, clean efficacy tables, refined neutral/pastel surfaces.

Use for: skincare, beauty care, nutrition, premium FMCG, maternal/child care, health-adjacent products.

Visual DNA:

- Product macro or texture image is the visual anchor; avoid generic model-only beauty.
- Soft light, controlled shadow, translucent product panels, cream/white/rose/sage surfaces.
- Claims are handled clinically: ingredient, benefit, evidence, usage moment, compliance note.
- Typography can be elegant, but efficacy and budget pages must be table-readable.

Fonts:

- English/numbers: `Inter`, `Libre Baskerville`, `Cormorant Garamond`.
- Chinese: `Source Han Sans SC`, `Noto Sans CJK SC`, `Noto Serif CJK SC` for display only.

Component transformation:

| Component | Beauty gloss treatment |
|---|---|
| Insight | Product macro + user moment + concise claim boundary. |
| Proof object | Efficacy / content / channel table with clean white panels. |
| Content sample | Product cutout, usage scene, captioned sample board. |
| KPI | Clinical-looking measurement table; no decorative sparkle. |

Reject if it looks like:

- Pink/beige template without product texture or proof.
- Overly feminine stock-photo mood with no business evidence.
- Thin serif body text that cannot survive projection.

### japanese-minimal

Reference grammar: quiet Japanese editorial minimalism, asymmetry, natural materials, generous negative space, vertical rhythm, restrained marks.

Use for: culture, premium lifestyle, education, sustainability, government-adjacent strategy, calm executive proposals.

Visual DNA:

- One strong focal object, many quiet margins, and deliberate asymmetry.
- Natural paper, stone, wood, or ink-adjacent neutrals; accent is used sparingly.
- Page rhythm is slow: big idea pages can be sparse, but dense pages use ruled editorial grids.
- The style is about restraint and proportion, not empty slides.

Fonts:

- English/numbers: `Inter`, `IBM Plex Sans`, `Libre Baskerville`.
- Chinese: `Noto Serif CJK SC` for titles, `Source Han Sans SC` for body.

Component transformation:

| Component | Japanese minimal treatment |
|---|---|
| Winning thesis | One sentence with large negative space and a small proof cue. |
| Mechanism | Thin ruled diagram, few labels, no heavy fills. |
| Table | Editorial ledger with soft rules and ample row height. |
| Source note | Marginalia or folio-like note, not a footer dump. |

Reject if it looks like:

- A blank corporate slide with small text in the corner.
- Random red circle/seal decoration without meaning.
- Beige-only monotony with no focal hierarchy.

### french-editorial

Reference grammar: refined lifestyle editorial, understated luxury, serif headlines, warm photography, narrow captions, gallery-like spacing.

Use for: hospitality, wine, food, tourism, premium retail, cultural lifestyle, service experience.

Visual DNA:

- Warm cream, burgundy, ink, brass, and muted blue/green accents.
- Large lifestyle or place image balanced by small precise captions.
- Layout feels like a magazine feature or lookbook, but proof remains source-aware.
- Avoid excessive ornament; use rules, folios, and captions instead.

Fonts:

- English/numbers: `Cormorant Garamond`, `Libre Baskerville`, `Inter`.
- Chinese: `Noto Serif CJK SC`, `Source Han Sans SC`.

Component transformation:

| Component | French editorial treatment |
|---|---|
| Cover | Image-led feature spread with restrained serif headline. |
| Case proof | Gallery image + caption + transferable method. |
| Timeline | Chaptered itinerary or editorial sequence. |
| Budget | Clean cream ledger with brass/burgundy emphasis only on totals. |

Reject if it looks like:

- Paris cliches, script fonts, flourishes, or decorative frames.
- Luxury mood with no operational detail.
- Low-contrast beige text.

### american-campaign-bold

Reference grammar: bold campaign posters, high-contrast type, direct slogans, modular blocks, punchy accent colors, action-oriented proof.

Use for: campaign launches, entertainment, sports, youth activation, growth pitches, sales-driving proposals.

Visual DNA:

- Big declarative typography, strong scale contrast, energetic composition.
- Red/blue/black/cream, cobalt/citrus, or high-contrast brand colors.
- Components feel like campaign boards, scorecards, activation maps, and rollout posters.
- The tone is confident and direct, but not noisy.

Fonts:

- English/numbers: `Anton`, `Archivo Black`, `Inter`, `IBM Plex Sans`.
- Chinese: `Source Han Sans SC`, `Noto Sans CJK SC`.

Component transformation:

| Component | American campaign treatment |
|---|---|
| Big idea | Slogan-scale headline with one proof anchor. |
| Activation plan | Bold modular blocks and route arrows. |
| KPI | Scoreboard / target board with large numbers and units. |
| Risk | Clear warning strips, not hidden caveats. |

Reject if it looks like:

- Random patriotic color use.
- Loud poster pages that cannot explain execution.
- All-caps body text that hurts readability.

### craft-paper-natural

Reference grammar: natural materials, packaging labels, paper texture, warm product photography, farm/handmade cues, earthy but not dull.

Use for: organic food, agriculture, wellness, sustainability, handmade products, family lifestyle.

Visual DNA:

- Paper texture, label systems, product/ingredient close-ups, hand-drawn-style separators used sparingly.
- Earthy palette balanced with fresh green/blue or product color.
- Proof objects look like ledgers, recipe cards, sourcing maps, or packaging systems.
- Avoid fake rustic decoration; real product/source images matter.

Fonts:

- English/numbers: `Inter`, `IBM Plex Sans`, `Libre Baskerville`.
- Chinese: `Source Han Sans SC`, `Noto Serif CJK SC` for selected titles.

Component transformation:

| Component | Craft natural treatment |
|---|---|
| Insight | Product/ingredient scene + plain-language implication. |
| Mechanism | Label-card system or sourcing map. |
| Timeline | Seasonal calendar or batch plan. |
| Budget | Kraft-paper ledger with clear inclusions/exclusions. |

Reject if it looks like:

- Brown/orange monotone.
- Fake hand-drawn clutter.
- Low-contrast text on textured backgrounds.

## Asset-Heavy Style Rule

If the chosen style requires images and the user did not provide them:

1. Create an asset list by slide.
2. Ask whether to use user assets, AI-generated conceptual images, or placeholders.
3. If proceeding automatically, generate conceptual assets or use abstract editable backgrounds.
4. Mark generated images as conceptual in the presenter script when they are not real proof.

Do not pretend a deck has a photographic, editorial, ink, or product style if the only change is color and generic shapes.
