# Font System

Use this file when choosing typography for a proposal deck, especially style-rich decks.

## License Rule

Prefer open-source fonts from Google Fonts, Adobe open-source font projects, IBM Plex, Inter, and Noto/Source Han families. Check the current license before bundling fonts into a public package. Do not bundle commercial fonts unless the user provides a license.

Most Google Fonts are open source and can be used commercially under their listed licenses. SIL Open Font License fonts can generally be used and bundled subject to OFL conditions.

Reference anchors: Google Fonts FAQ, SIL Open Font License, Inter license, IBM Plex license, Noto/Source Han open-source font projects. Re-check licenses before bundling font binaries into a public skill release.

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

## Style-Specific Pairings

| Style | Heading | Body | Numeric/Data | Notes |
|---|---|---|---|---|
| swiss-boardroom | `Inter` / `IBM Plex Sans` | `Source Han Sans SC` | `IBM Plex Mono` | Use few weights, strict hierarchy. |
| product-launch-minimal | `Inter` / `Aptos` | `Source Han Sans SC` | `Inter` | Large titles, very short copy. |
| fashion-beauty-editorial | `Playfair Display` / `Cormorant Garamond` | `Noto Serif CJK SC` or `Source Han Sans SC` | `Inter` | Use serif for mood, sans for proof. |
| japanese-magazine-collage | `IBM Plex Sans Condensed` / `Inter` | `Source Han Sans SC` | `IBM Plex Mono` | Many small labels need high legibility. |
| cinematic-photography | `Inter` / `Libre Franklin` | `Source Han Sans SC` | `Inter` | Avoid thin weights on photos. |
| web3-ai-glass | `Space Grotesk` / `Inter` | `Source Han Sans SC` | `IBM Plex Mono` | Mono for metrics and IDs. |
| ink-wash | `Noto Serif CJK SC` / `Source Han Serif SC` | `Source Han Sans SC` | `Inter` | Serif for titles, sans for proof. |
| pixel-retro | `Press Start 2P` / `Pixelify Sans` | `Source Han Sans SC` | `IBM Plex Mono` | Pixel fonts only for labels/headings. |
| e-reader-mono | `Noto Serif CJK SC` | `Noto Serif CJK SC` | `IBM Plex Mono` | Use book-like line height and narrow measure. |

## Typography QA

- Do not use more than two font families per deck unless a style system explicitly needs an accent font.
- Keep body text readable; avoid thin weights on dark or image backgrounds.
- Use serif/display fonts for mood, not for dense tables.
- Use mono fonts for code, metrics, IDs, asset ledgers, and technical dashboards.
- Do not use negative letter spacing.
- If a required font is unavailable, use the fallback stack and keep layout intact.
