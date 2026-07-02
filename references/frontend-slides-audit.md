# frontend-slides Reference Audit

Source:

- Repository: `https://github.com/zarazhangrui/frontend-slides`
- Inspected commit: `9906a34d640d2111f724544cbc50f7f130569ae1`
- License observed in source repo: MIT

## Judgment

`frontend-slides` is useful for improving proposal-ppt workflow because it treats slide generation as a staged visual-production system, not a one-shot prompt. Its value here is the method, not the exact layouts.

Proposal-ppt should borrow the production discipline and adapt it to commercial proposal logic: winning thesis, proof objects, budget boundaries, risk control, and presenter script stay above visual novelty.

## Transferable Practices

### Visual Discovery Before Production

When no client VI, approved reference, or chosen template family exists, create visual directions or a three-page sample set before scaling to a full deck. The samples must look like real proposal pages, not diagnostic cards.

### Fixed 16:9 Stage

For HTML demos, author each slide on a fixed 16:9 canvas, preferably `1920x1080`, and scale the whole stage in the browser. Do not let the slide composition reflow by viewport width.

### Progressive Template Loading

If a template library is available, shortlist using compact metadata first. Load full style rules only after a family is selected.

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

## Integration In proposal-ppt

Use this source as support for:

- `workflow.md` Stage 2.5 Template Selection Gate,
- `visual-system-card.md` Visual System Card Gate,
- `style-template-strategy.md` Visual Discovery Gate,
- `runtime-compatibility.md` HTML Demo Stage Contract,
- `quality-check.md` HTML Demo Visual QA Gate.

