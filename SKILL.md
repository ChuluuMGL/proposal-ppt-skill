---
name: proposal-ppt
description: Create, write, design, edit, or audit commercial proposal presentations and presenter scripts. Use when the user asks for a proposal PPT, business proposal deck, pitch deck, bid/RFP deck, client proposal, tender presentation, annual operation plan deck, marketing/social/content proposal, execution plan deck, budget proposal, or a PPT plus逐字稿 from briefs, research, brand assets, budgets, cases, timelines, or existing PPTX files.
---

# Proposal PPT

Use this skill to turn client briefs, tender files, research, brand materials, budgets, cases, and execution plans into a commercial proposal package:

- an editable `.pptx`
- a same-name presenter script `.md`
- a missing-information list when inputs are incomplete

The goal is not to decorate information. The goal is to help the client decide why this proposal should win: it understands the business problem, makes a clear judgment, proves execution ability, explains budget boundaries, and controls risk.

## Required Output

When creating a proposal, produce both deliverables unless the user explicitly asks for only one:

1. `*.pptx` with the full proposal deck.
2. `*.md` with presenter script. Include presentation logic, slide-by-slide talking points, transition notes, and exact speaker script. Do not put long oral explanation into slide bodies.

If information is missing, continue with a working draft and mark unknowns as `待补充`, `待确认`, `暂无公开数据`, or `需客户确认`. Do not invent data, results, awards, client cases, pricing, permissions, or platform rules.

## Reference Loading

Load only the references needed for the current task:

- For guided execution modes, stage gates, and user-option handling, read `references/workflow.md`.
- For story structure and proposal type routing, read `references/proposal-routes.md`.
- For page planning and proof objects, read `references/page-types.md`.
- For slide rhythm, whitespace balance, layout density, and page-to-page pacing, read `references/layout-rhythm.md`.
- For visual direction, palette, typography, and PPT template use, read `references/visual-system.md`.
- For default high-taste palette presets when no client VI is provided, read `references/palette-library.md`.
- For final file and script format, read `references/output-contract.md`.
- For delivery QA and failure modes, read `references/quality-check.md`.

Use `assets/minimal-proposal-template.pptx` only as a fallback visual asset when no client VI, reference deck, or stronger design direction is provided.

## Operating Modes

Default to `guided` mode unless the user explicitly asks to generate everything directly.

- `guided`: Use staged checkpoints. First return brief audit, winning thesis, chapter structure, page plan, proof objects, and visual direction for confirmation. After confirmation, build the PPTX and script.
- `auto`: If the user says to proceed directly or is under time pressure, make reasonable assumptions, mark unknowns as待确认, and produce the full `.pptx` plus `.md`.
- `edit`: If the user provides an existing PPTX, audit and modify the deck instead of rebuilding from scratch unless the user asks for a rebuild.
- `audit`: If the user asks for review only, do not generate a new deck. Return findings, page-level issues, and revision recommendations.

In guided mode, ask only high-impact routing questions. Do not block on details that can be marked待确认.

## Workflow

Follow `references/workflow.md` for the full stage-gate process. The high-level workflow is:

1. **Start and route the work**
   - Identify mode, proposal route, page-depth range, visual source, and required deliverables.
   - If the user has not specified these, infer defaults and show them in the first checkpoint.

2. **Collect and audit inputs**
   - Read the real brief, tender, deck, research, brand assets, budget, cases, and chat notes the user provides.
   - Separate confirmed facts from assumptions.
   - Extract client goal, audience, decision criteria, scope, timeline, budget, deliverables, KPI, exclusions, and approval risks.

3. **Define the winning thesis**
   - Write one sentence explaining why this proposal should be selected.
   - Define 3-5 client evaluation standards such as business fit, strategy judgment, execution certainty, proof, budget clarity, team response, and risk control.

4. **Select a proposal route**
   - Pick the closest route from `references/proposal-routes.md`.
   - Use the route to decide chapter order, proof emphasis, visual style, and required page types.
   - Do not force every deck into the same structure.

5. **Create the page plan before authoring slides**
   - For every slide, specify: slide title, page purpose, key message, proof object, visual form, required source, and presenter-script intent.
   - Each slide must answer one commercial question.
   - Each slide title should be a conclusion sentence, not a vague noun.

6. **Write slide copy**
   - Slides contain judgment, structure, proof, and key examples only.
   - Speaker notes / script contain oral reasoning and transitions.
   - Keep bullets short and action-oriented.
   - Remove internal wording such as `赢标逻辑`, `客户透露`, `内部判断`, `释标会之后`, unless the user explicitly wants an internal working draft.

7. **Build or edit the PPTX**
   - If the user provides a template/reference deck, follow it as the visual source.
   - If the client has VI, use client brand colors and typography first.
   - If no visual source exists, use `references/visual-system.md` and the minimal template as fallback.
   - When creating a PowerPoint deck, follow the active PowerPoint/presentations skill requirements, including deck rendering and overlap QA.

8. **Write the presenter script**
   - The `.md` must be usable by a presenter, not just a slide outline.
   - For each slide, include slide objective, why it appears here, exact talk track, transition sentence, and notes about numbers or claims that need confirmation.

9. **Run final QA**
   - Use `references/quality-check.md`.
   - Verify story continuity, slide-title quality, proof objects, source labels, visual alignment, text size, budget boundaries, KPI logic, and risk controls.
   - Do not claim the deck is ready until the PPTX and script are both present and checked.

## Hard Rules

- Do not fabricate data, awards, clients, case outcomes, screenshots, platform permissions, or third-party endorsements.
- Do not use customer-sensitive examples in reusable templates or public skill assets.
- Do not default to a service-list deck. Start from the client problem and decision criteria.
- Do not let budget pages hide exclusions or uncertain costs in unreadable footnotes.
- Do not make a PPT that requires the presenter to explain missing logic verbally. The visual argument must stand on its own.
- Do not leave large empty placeholder frames or a visually dead lower third. If evidence is missing, mark the item compactly as `待确认` and rebalance the layout.
- Do not make every slide dense. Insert deliberate breathing slides, section dividers, big-idea pages, or visual proof pages every 3-5 slides.
- Do not insert the skill author's company information into user decks unless the user explicitly asks to present under that company identity.
