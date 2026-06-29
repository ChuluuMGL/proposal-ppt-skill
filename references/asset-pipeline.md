# Asset Pipeline

Use this file when a proposal deck needs images, textures, generated visuals, HTML/SVG backgrounds, screenshots, or style-specific visual assets.

## Asset Priority

Use assets in this order:

1. Client-provided real assets: product photos, brand VI, screenshots, case photos, logos, packaging, store/event photos.
2. Publicly available assets with source labels and usage rights suitable for the context.
3. AI-generated conceptual assets using the user's configured provider.
4. Lightweight bundled or generated textures: paper, grain, pixel grid, glass blur, editorial labels.
5. Clean editable shapes if no asset path is safe.

Do not use random stock-like images only because they look decorative.

## Asset-First Quality Bar

For a style-rich public template, visual surfaces must be asset-first:

- Use real product/scene/case/screenshot assets when available.
- Use AI-generated conceptual images only when they are clearly marked conceptual and do not impersonate real client proof.
- Use public assets only when their source and usage status are suitable for the context.
- Use HTML/SVG/raster layers for texture, collage frames, interface fields, and visual atmosphere, while keeping business text editable.

Reject a slide if its main visual is only a large flat color block, a generic gradient, a crude shape collage, or a fake screenshot. These may be internal wireframes, but they are not publishable style templates.

Every asset must have a visual job:

| Visual job | Meaning |
|---|---|
| `hero proof` | Carries the main emotional/business proof of the page. |
| `source-backed screenshot` | Shows real platform, case, or execution evidence. |
| `concept atmosphere` | Sets direction only; must be marked conceptual. |
| `product/scene proof` | Shows product, usage, shelf, event, or consumer context. |
| `interface mock` | Explains system/product logic without pretending to be a real UI. |
| `texture/frame` | Supports style grammar without carrying business claims. |

Decorative assets without one of these jobs should be removed.

## Provider Model

The skill must not include API keys. If image generation is needed, ask the user to configure a provider or use tools available in the current agent environment.

Current provider reference anchors include OpenAI image generation APIs and ByteDance/Seedream-style image generation/editing APIs. Verify the current provider endpoint, model name, usage rights, and content policy at runtime before calling an external API. Other providers can be used when the current agent supports them, but the skill must never assume a key exists.

Supported provider pattern:

```yaml
image_provider:
  name: openai | seedream | flux | midjourney | other
  model: <model name>
  api_key_env: <environment variable name, never the key itself>
  output_dir: <absolute output folder>
  default_size: 16:9
```

If the provider is unavailable, continue with editable placeholders and list the missing assets in the script.

## Style Asset Requirements

Strong styles need style-specific assets. Do not let ordinary shapes impersonate an asset-heavy style.

| Style | Minimum Asset Layer | Good Asset Types | Fallback If Missing |
|---|---|---|---|
| fashion-beauty-editorial | hero product/person/scene image | product macro, campaign sample, lifestyle crop, caption board | typography-led spread plus explicit `图片待补充` frame |
| beauty-gloss-clinical | product macro or texture | packaging, ingredient, usage scene, efficacy table | clean clinical table with product placeholder |
| japanese-magazine-collage | multiple small proof images | screenshots, creator cards, product scenes, labels, tape/paper texture | structured index board, not random blank clippings |
| cinematic-photography | one dominant scene | real event, activation, store, table, user moment | generated conceptual scene marked as conceptual |
| web3-ai-glass | interface / node / dashboard layer | architecture map, data flow, UI mock, metric cards | editable system diagram on dark grid |
| pixel-retro | pixel grid / sprites / tile system | pixel icons, quest map, inventory/score frames | hard-grid SVG frame and normal readable body text |
| oil-salon | canvas / framed image | still-life, product art, gallery wall, warm canvas | cream gallery layout with image placeholder |
| e-reader-mono | document texture / scans | source excerpts, diagrams, margin notes | monochrome ruled report layout |

If the style cannot be recognized after removing the style title, generate/request better assets or downgrade the style.

## Asset Plan Output

Before building an asset-heavy deck, output:

```markdown
### 视觉资产计划

| 页码 | 资产类型 | 用途 | 来源 | 状态 |
|---|---|---|---|---|
| 01 | 产品主图 | 封面 hero | 客户提供 / AI 生成 / 待补充 |  |
```

For style-rich routes, also state the visual job of each asset. Example: `hero proof`, `texture only`, `collage evidence`, `product cutout`, `concept atmosphere`, `interface mock`, or `source-backed screenshot`. Decorative assets without a visual job should be removed.

## Image Generation Prompt Contract

For AI-generated visuals, write prompts with these fields:

| Field | Requirement |
|---|---|
| subject | product, scene, person, environment, object, interface, or abstract texture |
| commercial role | what the image proves in the proposal |
| style system | chosen style from `style-systems.md` |
| composition | crop, perspective, safe area for text, background density |
| palette | main colors and forbidden colors |
| output ratio | 16:9, 4:3, 1:1, 9:16, or exact size |
| negative prompt | no logos, no unreadable text, no fake platform UI, no watermark |
| disclosure | conceptual image / real client asset / public source |

Example:

```text
Generate a 16:9 cinematic warm film still for a beverage family campaign proposal.
Subject: dining table scene with product area left empty for later compositing.
Commercial role: show family holiday consumption context, not generic atmosphere.
Composition: dark upper-left safe area for title; product/action zone on right; realistic light; no brand logos; no readable text.
Style system: cinematic-photography.
Palette: warm amber, deep brown, soft cream, controlled highlights.
Output: 1920x1080.
```

## HTML/SVG-to-PPT Hybrid

Use HTML/SVG generation when a style needs texture or complex visual language that is hard to build with native PPT shapes:

- pixel: exact pixel grids, tile patterns, retro UI frames,
- Web3/AI: glassmorphism backgrounds, node fields, grid glows,
- magazine collage: sticker sheets, paper textures, tape strips,
- oil/craft: paper grain, frame textures, warm canvas blocks.

Preferred route:

1. Generate SVG/HTML background or texture as a static visual layer.
2. Export it as PNG/SVG.
3. Place it as a background or decorative layer in PPT.
4. Keep titles, body text, tables, budgets, KPI, and page numbers as editable PPT objects.

Avoid full-page screenshots for editable proposal pages unless the user explicitly accepts non-editable slides.

Recommended hybrid split:

- Background, texture, collage frame, pixel grid, ink wash, glass glow, and oil/canvas treatment may be raster/SVG layers.
- Titles, body text, tables, budgets, KPI, risk controls, page numbers, and source notes should remain editable PPT objects whenever practical.
- When a quick style sample uses rasterized text for speed, label it as a visual QA demo, not as the final production method.

## Asset QA

Before delivery:

- No fake client logos, fake platform icons, fake award badges, or fake screenshots.
- No generated image is presented as a real case or real product photo.
- Images are not stretched or blurred.
- Product/people/case images have clean crop and text-safe zones.
- Third-party/public assets have source labels where appropriate.
- The same generic image is not reused across unrelated pages.
- Generated visuals are marked as conceptual in the script if needed.
- Full-size slide QA is required for every style-critical slide; a contact sheet alone is insufficient.
- Shape-only substitutes for photographic, oil, magazine, pixel, or Web3 styles must be labeled as wireframes, not reference templates or final visuals.
- If the intended style is not recognizable after removing the title text, the asset treatment is too weak.
- If color blocks, pills, and cards remain the only visual language, the deck has not met the asset-first bar.
- If a public/demo asset is used, add a source note in the deck or presenter script.

## Missing Asset Fallback

If required images are missing and generation is not available:

- use a clean editorial placeholder with `图片待补充`,
- show the intended crop ratio and caption structure,
- keep the business argument readable without the missing image,
- list each missing asset in the presenter script.
