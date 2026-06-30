# frontend-slides Reference Audit

Source:

- Repository: `https://github.com/zarazhangrui/frontend-slides`
- Inspected commit: `9906a34d640d2111f724544cbc50f7f130569ae1`
- License observed in source repo: MIT

## Judgment

`frontend-slides` is useful for improving proposal-ppt page design workflow, especially for HTML-based style demos. Its value is not a ready-made commercial proposal template. The useful part is the visual production method:

1. show visual directions before building the full deck,
2. author slides on a fixed 16:9 stage,
3. use compact metadata before loading a large template library,
4. reject generic AI-looking slides,
5. separate low-density speaker-led pages from dense reading-first pages.

Proposal-ppt should borrow the method, not copy the demo layouts, screenshots, copy, or protected visual compositions.

## Transferable Practices

### Visual Discovery

When no client VI, approved reference, or chosen template family exists, create 2-3 visual directions or a three-page sample set before scaling to a full deck. The samples must look like real proposal pages, not diagnostic cards.

### Fixed Stage

For HTML demos, author each slide on a fixed 16:9 canvas, preferably `1920x1080`, and scale the whole stage in the browser. Do not let the slide composition reflow by viewport width.

### Progressive Template Loading

If a template library is available, shortlist using compact metadata first. Load full design rules only after a family is selected.

### Anti-Generic Design

Reject one-color recolors, generic rounded-card dashboards, decorative circles, and templates where different styles share the same component grid.

### Density Modes

Use breathing pages for live-pitch emphasis and proof-dense pages for tender, budget, KPI, risk, and brief-coverage evidence. If proof pages become cramped, split the page instead of shrinking text or removing gutters.

## Do Not Transfer Directly

- Do not import browser-presentation categories as proposal strategy categories.
- Do not depend on browser-only interactivity for a PPTX deliverable.
- Do not use motion or visual novelty as a substitute for commercial proof.
- Do not bulk-import all template styles before they pass proposal-specific sample gates.
- Do not copy screenshots, exact compositions, demo wording, or protected images.

## Integration In Proposal-ppt

Use this source as support for:

- `style-template-strategy.md` Visual Discovery Gate,
- `runtime-compatibility.md` HTML Demo Stage Contract,
- `quality-check.md` HTML Demo Visual QA Gate.

