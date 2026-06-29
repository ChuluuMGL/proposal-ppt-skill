# Quality Check

Run this before delivery. Treat unchecked `[BLOCKER]` items as no-delivery conditions unless the user explicitly accepts the downgrade.

Use this format in the final handoff or internal QA note:

```markdown
## Delivery QA

- Runtime:
- PPTX backend:
- Preview/render method:
- QA status: passed / passed with warnings / downgraded / blocked
- Unresolved assumptions:
```

## 0. Runtime And Package Gate

- [ ] [BLOCKER] The current runtime can read `SKILL.md` and all required `references/*.md` files.
- [ ] [BLOCKER] The source brief/files were actually read or the missing source is marked.
- [ ] [BLOCKER] Output location is writable.
- [ ] [BLOCKER] If a `.pptx` is promised, a PPTX backend is available and named.
- [ ] [BLOCKER] If no PPTX backend is available, the delivery is downgraded to `blueprint-only`, `copy-and-script`, `template-spec`, or `html-demo` and clearly labeled.
- [ ] [BLOCKER] The final package includes the requested `.pptx` and same-name `.md` script, unless explicitly downgraded.
- [ ] [WARN] Runtime limitations are listed in the final response when rendering/open validation cannot be performed.

## 1. Story Gate

- [ ] [BLOCKER] The deck has a one-sentence winning thesis.
- [ ] [BLOCKER] The deck starts from the client's problem or decision criteria, not the vendor's service list.
- [ ] [BLOCKER] The chapter flow can be explained in roughly 3 minutes.
- [ ] Each chapter advances the commercial argument.
- [ ] The closing page returns to the opening thesis or cooperation promise.
- [ ] The proposal route matches the brief: brand/social/content, annual retainer, project execution, consulting/AI/SaaS, or partnership/sponsorship.

## 2. Per-Slide Gate

Check every slide:

- [ ] [BLOCKER] One slide has one core judgment.
- [ ] [BLOCKER] Slide title is a conclusion sentence, not a vague noun.
- [ ] [BLOCKER] A visible proof object supports the title.
- [ ] The slide has an obvious reason to exist in the story.
- [ ] Long reasoning is in the presenter script, not the slide body.
- [ ] Unknown claims are marked as `待确认`, `暂无公开数据`, `需客户确认`, or equivalent.
- [ ] No slide relies on oral explanation to repair missing visual logic.
- [ ] No internal wording appears on client-facing slides, such as `赢标逻辑`, `客户透露`, `内部判断`, or `释标会之后`, unless the user requested an internal draft.

## 3. Evidence Gate

- [ ] [BLOCKER] No invented data, cases, awards, client names, screenshots, platform permissions, or results.
- [ ] [BLOCKER] Public or third-party data/screenshots have source labels where needed.
- [ ] Benchmark pages extract transferable methods, not only visual examples.
- [ ] Case pages explain relevance and transfer, not only credentials.
- [ ] AI-generated visuals are marked as conceptual when they are not real proof.
- [ ] Sensitive customer examples are not used in reusable/public skill assets.

## 4. Visual And Layout Gate

- [ ] [BLOCKER] Deck is 16:9 unless the user requested another ratio.
- [ ] [BLOCKER] No unreadable text below 8 pt.
- [ ] [BLOCKER] No accidental overlap, clipping, broken connectors, or text overflow.
- [ ] [BLOCKER] No page has major content clustered in one corner or one half unless deliberately balanced by a visual anchor.
- [ ] [BLOCKER] No large empty lower-third, empty bordered placeholder, or unused media frame remains on a client-facing slide.
- [ ] Each slide has an explicit layout recipe and density class when building a new deck.
- [ ] Standard and proof-dense pages use the lower third deliberately through proof, conclusion, timeline, source status, or a visual anchor.
- [ ] Every 3-5 slides, the deck changes rhythm through a section divider, big-idea slide, visual proof page, quote, summary, or low-density transition.
- [ ] Margins, title positions, page numbers, and footer/source style are consistent.
- [ ] Tables have clear headers, units, assumptions, and exclusions.
- [ ] Screenshots are cropped cleanly and aligned.
- [ ] No meaningless decoration, fake logos, low-resolution images, or stretched media.
- [ ] Palette does not become a one-color monotone or cheap gradient theme.
- [ ] When no VI is provided, a named palette from `palette-library.md` is selected and applied consistently.

## 5. Rich Style Gate

Use this only when a strong style system is selected.

- [ ] [BLOCKER] The style changes more than color: typography, layout grammar, components, proof-object forms, and asset treatment match the chosen style system.
- [ ] [BLOCKER] If no approved reference deck exists, the style passes the three-page sample gate: cover/big idea, proof/mechanism, and dense business page.
- [ ] [BLOCKER] Style-critical pages have been reviewed full-size; contact sheets alone are not enough.
- [ ] [BLOCKER] If no client VI exists, one of the public template families in `style-template-strategy.md` is selected or an explicit custom route is documented.
- [ ] [BLOCKER] New style/template routes pass the three-page sample gate: cover/big-idea, strategy/mechanism, and proof-dense.
- [ ] Components are not identical across different style routes. A magazine collage page, Web3 dashboard, pixel quest path, and editorial proof board should not share the same generic card grid.
- [ ] Asset-heavy styles use real client assets, sourced assets, AI-generated conceptual images, or explicit placeholders.
- [ ] Shape-only substitutes for photographic, editorial, ink, oil, pixel, or Web3 styles are labeled as wireframes, not final templates.
- [ ] HTML/SVG-generated style layers do not turn core business text, budgets, KPI, or risk controls into uneditable screenshots unless the user accepts that tradeoff.
- [ ] Reject public template candidates where all sample pages share the same card-grid silhouette.
- [ ] Reject style-rich pages where the style becomes unrecognizable after removing the title text.
- [ ] Reject proof-dense style samples where budget, KPI, risk, timeline, or brief coverage is not readable and editable.

## 6. Commercial Gate

- [ ] [BLOCKER] Brief requirements are mapped to proposal responses.
- [ ] [BLOCKER] Budget pages show deliverables, frequency/cycle, inclusions, exclusions, assumptions, and acceptance criteria.
- [ ] Base service, project modules, optional items, media/third-party costs, and client-provided resources are separated where relevant.
- [ ] KPI are layered and measurable, not a mixed list of exposure, conversion, and brand asset metrics.
- [ ] Team page shows operating responsibility and response mechanism, not only titles.
- [ ] Risk page includes risk point, trigger, response, owner, and boundary.
- [ ] Timeline or cadence page shows sequence logic, not only a calendar.

## 7. Presenter Script Gate

- [ ] [BLOCKER] A same-name `.md` presenter script exists unless the user explicitly declined it.
- [ ] The script includes overall presentation logic.
- [ ] Each slide has objective, why it appears here, exact talk track, transition sentence, and confirmation notes.
- [ ] The script does not merely repeat slide text.
- [ ] Missing information and assumptions are listed clearly.
- [ ] Generated/conceptual images, unverified data, and pending client inputs are disclosed.

## 8. PPTX Compatibility Gate

- [ ] [BLOCKER] Final `.pptx` passes ZIP integrity check.
- [ ] [BLOCKER] Final `.pptx` XML is well-formed when XML validation is available.
- [ ] [BLOCKER] For bundled skill assets or reusable templates, do not rely on ZIP validity alone; validate that PowerPoint, Keynote, LibreOffice, or the local preview pipeline can open/render the file.
- [ ] The deck can be rendered or converted by an Office-compatible tool before delivery when available.
- [ ] If a generated PPTX is valid XML but fails to open, rewrite it through an Office-compatible exporter and deliver the repaired copy.
- [ ] If render/open validation was unavailable, the final response says what was checked and what remains unverified.

## 9. Font And Asset Gate

- [ ] [BLOCKER] No unlicensed commercial font dependency is required.
- [ ] Free/commercial-safe fonts or documented fallbacks are used.
- [ ] If a preferred font is unavailable, the fallback stack in `font-system.md` is used without breaking layout.
- [ ] Public assets, screenshots, third-party marks, and generated visuals follow `asset-pipeline.md`.
- [ ] No fake client logos, platform icons, award badges, or fake screenshots appear.

## Common Failure Modes

- Generic table of contents with no winning thesis.
- Market analysis that does not change the strategy.
- Competitor screenshots with no transferable learning.
- Creative concept with no production cadence.
- Budget number without deliverables and acceptance criteria.
- KPI list that mixes exposure, conversion, and brand asset metrics without hierarchy.
- Presenter script that merely repeats slide text.
- Deck that looks good but cannot answer why the client should choose this vendor.
- Style library that uses the same card component under different style names.
- Runtime that cannot generate PPTX but still claims a finished PowerPoint was delivered.
