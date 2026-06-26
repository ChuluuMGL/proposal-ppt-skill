# Asset Pipeline

Use this file when a proposal deck needs images, textures, generated visuals, HTML/SVG backgrounds, screenshots, or style-specific visual assets.

## Asset Priority

Use assets in this order:

1. Client-provided real assets: product photos, brand VI, screenshots, case photos, logos, packaging, store/event photos.
2. Publicly available assets with source labels and usage rights suitable for the context.
3. AI-generated conceptual assets using the user's configured provider.
4. Lightweight bundled or generated textures: paper, grain, pixel grid, ink wash edges, glass blur, editorial labels.
5. Clean editable shapes if no asset path is safe.

Do not use random stock-like images only because they look decorative.

## Provider Model

The skill must not include API keys. If image generation is needed, ask the user to configure a provider or use tools available in the current agent environment.

Current provider reference anchors include OpenAI image generation APIs and ByteDance/Seedream-style image generation/editing APIs. Verify the current provider endpoint, model name, usage rights, and content policy at runtime before calling an external API.

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

## Asset Plan Output

Before building an asset-heavy deck, output:

```markdown
### 视觉资产计划

| 页码 | 资产类型 | 用途 | 来源 | 状态 |
|---|---|---|---|---|
| 01 | 产品主图 | 封面 hero | 客户提供 / AI 生成 / 待补充 |  |
```

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

- ink wash: brush-edge masks, ink diffusion, red seal blocks,
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

## Asset QA

Before delivery:

- No fake client logos, fake platform icons, fake award badges, or fake screenshots.
- No generated image is presented as a real case or real product photo.
- Images are not stretched or blurred.
- Product/people/case images have clean crop and text-safe zones.
- Third-party/public assets have source labels where appropriate.
- The same generic image is not reused across unrelated pages.
- Generated visuals are marked as conceptual in the script if needed.

## Missing Asset Fallback

If required images are missing and generation is not available:

- use a clean editorial placeholder with `图片待补充`,
- show the intended crop ratio and caption structure,
- keep the business argument readable without the missing image,
- list each missing asset in the presenter script.
