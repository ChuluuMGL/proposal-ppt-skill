# Font System

Use this file when choosing typography for a proposal deck, especially style-rich decks.

## License Rule

Prefer open-source fonts from Google Fonts, Adobe open-source font projects, IBM Plex, Inter, and Noto/Source Han families. Check the current license before bundling fonts into a public package. Do not bundle commercial fonts unless the user provides a license.

Most Google Fonts are open source and can be used commercially under their listed licenses. SIL Open Font License fonts can generally be used and bundled subject to OFL conditions.

Reference anchors: Google Fonts FAQ, SIL Open Font License, Inter license, IBM Plex license, Noto/Source Han open-source font projects. Re-check licenses before bundling font binaries into a public skill release.

Runtime rule:

- Do not assume a preferred font is installed on the user's machine.
- Do not download or install fonts unless the user approves it or the runtime already has a safe font-install workflow.
- If a preferred font is unavailable, use the fallback stack and keep the layout intact.
- Do not fail a proposal build only because a display font is missing.
- If a public template or demo requires a non-system font for its appearance, document the font name, license, source, and fallback.

## General Fallback Stack

Use installed system fonts when the target machine may not have custom fonts.

| Role | Preferred | Fallback |
|---|---|---|
| Chinese sans | `Source Han Sans SC`, `Noto Sans CJK SC` | `PingFang SC`, `Microsoft YaHei` |
| Chinese serif | `Source Han Serif SC`, `Noto Serif CJK SC` | `Songti SC`, `SimSun` |
| UI/business sans | `Inter`, `IBM Plex Sans` | `Aptos`, `Arial`, `Helvetica` |
| Mono/data | `IBM Plex Mono`, `Space Mono`, `JetBrains Mono` | `Courier New` |
| Editorial serif | `Playfair Display`, `Cormorant Garamond`, `Libre Baskerville` | `Georgia` |
| Pixel accent | `Press Start 2P`, `Pixelify Sans`, `DotGothic16` | `Courier New` |
| Bold campaign | `Anton`, `Archivo Black`, `Bebas Neue` | `Arial Black` |

## Style-Specific Pairings

| Style | Heading | Body | Numeric/Data | Notes |
|---|---|---|---|---|
| swiss-boardroom | `Inter` / `IBM Plex Sans` | `Source Han Sans SC` | `IBM Plex Mono` | Use few weights, strict hierarchy. |
| product-launch-minimal | `Inter` / `Aptos` | `Source Han Sans SC` | `Inter` | Large titles, very short copy. |
| fashion-beauty-editorial | `Playfair Display` / `Cormorant Garamond` | `Noto Serif CJK SC` or `Source Han Sans SC` | `Inter` | Use serif for mood, sans for proof. |
| beauty-gloss-clinical | `Cormorant Garamond` / `Inter` | `Source Han Sans SC` | `Inter` | Keep efficacy and table copy sans-serif. |
| japanese-minimal | `Noto Serif CJK SC` / `Libre Baskerville` | `Source Han Sans SC` | `Inter` | Sparse titles, quiet body, generous line height. |
| japanese-magazine-collage | `IBM Plex Sans Condensed` / `Inter` | `Source Han Sans SC` | `IBM Plex Mono` | Many small labels need high legibility. |
| cinematic-photography | `Inter` / `Libre Franklin` | `Source Han Sans SC` | `Inter` | Avoid thin weights on photos. |
| french-editorial | `Cormorant Garamond` / `Libre Baskerville` | `Noto Serif CJK SC` / `Source Han Sans SC` | `Inter` | Use serif for display and captions, sans for tables. |
| american-campaign-bold | `Anton` / `Archivo Black` | `Source Han Sans SC` | `IBM Plex Sans` | Bold headings only; body must remain readable. |
| craft-paper-natural | `Libre Baskerville` / `Inter` | `Source Han Sans SC` | `Inter` | Use serif sparingly for label-like headings. |
| web3-ai-glass | `Space Grotesk` / `Inter` | `Source Han Sans SC` | `IBM Plex Mono` | Mono for metrics and IDs. |
| pixel-retro | `Press Start 2P` / `Pixelify Sans` | `Source Han Sans SC` | `IBM Plex Mono` | Pixel fonts only for labels/headings. |
| e-reader-mono | `Noto Serif CJK SC` | `Noto Serif CJK SC` | `IBM Plex Mono` | Use book-like line height and narrow measure. |

## Typography QA

- [ ] Preferred fonts are free/commercial-safe or user-provided.
- [ ] No commercial font is bundled without a license.
- [ ] Missing fonts fall back without text overflow or layout breakage.
- [ ] Display/serif/pixel fonts are not used for dense body copy.
- [ ] Font choices are documented in the presenter script or final handoff when they materially affect the visual system.
- Do not use more than two font families per deck unless a style system explicitly needs an accent font.
- Keep body text readable; avoid thin weights on dark or image backgrounds.
- Use serif/display fonts for mood, not for dense tables.
- Use mono fonts for code, metrics, IDs, asset ledgers, and technical dashboards.
- Do not use negative letter spacing.
- If a required font is unavailable, use the fallback stack and keep layout intact.
