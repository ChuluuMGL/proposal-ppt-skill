# Quality Check

Run this before delivery.

## Story QA

- Is there a one-sentence winning thesis?
- Does the deck start from the client problem instead of the vendor service list?
- Can the main story be explained in 3 minutes?
- Does each chapter advance the commercial argument?
- Is the closing page connected to the opening thesis?

## Slide QA

For each slide:

- One core point only.
- Title is a conclusion sentence.
- A proof object is visible.
- The proof object supports the title.
- The slide has an obvious reason to be in this deck.
- Long explanations are in the script, not the slide body.
- Unknown data is marked as `待确认` / `暂无公开数据` / `需客户确认`.

## Evidence QA

- No invented data, cases, awards, client names, screenshots, or results.
- Sources are noted where public data or third-party screenshots are used.
- Benchmark pages extract transferable methods, not just visual examples.
- Case pages explain relevance and transfer, not only credentials.

## Visual QA

- 16:9 ratio.
- Consistent margins, title positions, page numbers, and footer/source style.
- No unreadable text below 8 pt.
- No accidental overlap, clipping, or broken connectors.
- No page has all major content clustered in one corner or one half unless the layout is deliberately asymmetric and balanced by a visual anchor.
- No large empty lower-third, empty bordered placeholder, or unused media frame remains on a client-facing slide.
- Each slide has an explicit layout recipe and density class when building a new deck.
- Standard and proof-dense pages use the lower third deliberately through proof, conclusion, timeline, source status, or a visual anchor.
- Every 3-5 slides, the deck changes rhythm through a section divider, big-idea slide, visual proof page, quote, summary, or low-density transition.
- Tables have clear headers, units, assumptions, and exclusions.
- Screenshots are cropped cleanly and aligned.
- No meaningless decoration, fake logos, low-resolution images, or stretched media.
- The palette does not become a one-color monotone or cheap gradient theme.
- When no VI is provided, a named palette from `palette-library.md` is selected and applied consistently.
- If a rich style is selected, the deck changes more than color: typography, layout grammar, components, proof-object forms, and asset treatment all match the chosen style system.
- If no approved reference deck exists, strong visual styles pass the three-page sample gate: cover/big idea, proof/mechanism, and dense business page.
- Components are not identical across different style routes. A magazine collage page, Web3 dashboard, pixel quest path, and editorial proof board should not share the same generic card grid.
- Asset-heavy styles have real client assets, sourced assets, AI-generated conceptual images, or explicit placeholders; the deck does not fake photographic/editorial/ink/product quality with generic shapes alone.
- Review style-rich pages full-size before delivery or bundling; contact sheets only prove macro rhythm, not quality.
- Reject slides where the claimed style is represented by crude primitive shapes, oversized generic circles, decorative dots, or ordinary cards with a new palette.
- Reject any public skill asset or reusable template that has not passed human full-size visual review.
- HTML/SVG-generated style layers do not turn core business text, tables, budgets, KPI, or risk controls into uneditable screenshots unless the user accepts that tradeoff.
- Free/commercial-safe fonts or documented fallbacks are used; no unlicensed commercial font dependency is required.

## PPTX Compatibility QA

- The final `.pptx` passes ZIP integrity check and XML well-formedness checks.
- The deck can be rendered or converted by an Office-compatible tool before delivery when available.
- For bundled skill assets or reusable templates, do not rely on ZIP validity alone; validate that PowerPoint/Keynote/LibreOffice or the local preview pipeline can actually open/render the file.
- If a generated PPTX is valid XML but fails to open in PowerPoint, rewrite it through an Office-compatible exporter and deliver the repaired copy.

## Commercial QA

- Brief requirements are mapped to proposal responses.
- Budget is split into base service, project modules, optional items, media/third-party costs, and client-provided resources where relevant.
- Exclusions and assumptions are visible.
- KPI are layered and measurable.
- Team page shows operating responsibility, not only titles.
- Risk page has triggers, responses, and owners.

## Common Failure Modes

- Generic table of contents with no winning thesis.
- Market analysis that does not change the strategy.
- Competitor screenshots with no transferable learning.
- Creative concept with no production cadence.
- Budget number without deliverables and acceptance criteria.
- KPI list that mixes exposure, conversion, and brand asset metrics without hierarchy.
- Presenter script that merely repeats slide text.
- Deck that looks good but cannot answer why the client should choose this vendor.
