# proposal-ppt-skill

> **Business Proposal Presentation Skill for AI Agents**
> An open-source skill that helps AI agents create stage-gated commercial proposal decks, editable PowerPoint files, and presenter scripts from client briefs, research, budgets, cases, timelines, and execution plans.

[Simplified Chinese](./README.zh-CN.md) | English

[![Skill](https://img.shields.io/badge/AI%20Skill-proposal--ppt-0E5E43)](./SKILL.md)
[![Version](https://img.shields.io/badge/version-0.1.2-green)](./skill.json)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](./LICENSE)
[![Template](https://img.shields.io/badge/template-PPTX-blue)](./assets/minimal-proposal-template.pptx)
[![Workflow](https://img.shields.io/badge/workflow-stage--gated-purple)](./references/workflow.md)

---

## What This Skill Does

`proposal-ppt` turns messy proposal inputs into a structured commercial presentation package:

| Output | What It Contains |
|---|---|
| Editable `.pptx` | A business proposal deck with a coherent storyline, slide-by-slide proof objects, visual system, and QA-ready layout. |
| Presenter script `.md` | The proposal logic, section rhythm, slide-by-slide talk track, transition lines, and assumptions to confirm. |
| Missing-information list | A clear list of unknowns that should be marked instead of invented. |

The purpose is not to make slides decorative. The purpose is to help the client understand why this proposal should be selected.

---

## Use Cases

| Scenario | Typical Request |
|---|---|
| Business proposal deck | "Create a proposal PPT from this client brief." |
| Bid / RFP / tender presentation | "Turn this tender document into a pitch deck and script." |
| Annual operation plan | "Create an annual social/content operation proposal." |
| Brand and social marketing proposal | "Build a brand campaign or social media proposal deck." |
| Live commerce / event / activation plan | "Create an execution proposal with budget, SOP, risk, and KPI." |
| AI / SaaS / digital consulting proposal | "Create a solution deck with roadmap, architecture, and value model." |
| Partnership / sponsorship proposal | "Create a cooperation proposal with packages and activation scenarios." |
| Existing deck revision | "Improve this PPT's logic, titles, proof objects, and presenter script." |

---

## Workflow

This skill uses a stage-gated workflow inspired by professional proposal production:

| Stage | Gate | Deliverable |
|---|---|---|
| 0. Start and route | Choose mode, proposal type, depth, visual source, and deliverables. | Startup judgment |
| 1. Brief intake | Separate confirmed facts from missing information. | Brief audit |
| 2. Proposal blueprint | Build the winning thesis, chapter flow, page plan, and proof objects. | Blueprint for approval |
| 3. Slide copy | Write concise slide copy and proof-object content. | Slide-level copy draft |
| 4. PPT build | Create or edit the PowerPoint deck. | Editable `.pptx` |
| 5. Presenter script | Write the proposal logic and slide-by-slide talk track. | `.md` script |
| 6. Final QA | Check logic, evidence, visual layout, budget, KPI, and risk. | Delivery-ready package |

Default mode is `guided`: the agent stops after the blueprint and waits for confirmation before building the PPTX. If you ask it to proceed directly, it uses `auto` mode and marks missing information as "to be confirmed."

---

## Work Modes

| Mode | When to Use | Behavior |
|---|---|---|
| `guided` | You want to review the strategy before slides are built. | Produces the audit and blueprint first, then waits for confirmation. |
| `auto` | You need a complete first draft quickly. | Builds the full PPTX and script with assumptions clearly marked. |
| `edit` | You already have a PPTX. | Preserves the deck's visual system unless you ask for a redesign. |
| `audit` | You only want review feedback. | Reviews the deck and returns findings, risks, and revision suggestions. |

---

## Proposal Routes

The skill does not force every proposal into the same template. It routes the project into one primary proposal type:

| Route | Best For |
|---|---|
| Brand, social, and content marketing | Brand campaigns, social operation, creative concepts, content systems. |
| Annual operation and retainer service | Always-on operations, account management, B2B content assets, customer operations. |
| Project execution, live commerce, and activation | Live commerce, event execution, production-heavy work, complex project delivery. |
| Consulting, digital, AI, SaaS, and tooling | Transformation, AI tools, SaaS platforms, workflow automation, consulting proposals. |
| Partnership, sponsorship, and resource integration | Sponsorship, channel cooperation, joint marketing, investment packages. |

See [`references/proposal-routes.md`](./references/proposal-routes.md) for the full routing logic.

---

## Included Files

| File / Folder | Purpose |
|---|---|
| [`SKILL.md`](./SKILL.md) | Core skill metadata and instructions. |
| [`references/workflow.md`](./references/workflow.md) | Guided workflow, stage gates, recommended prompts. |
| [`references/proposal-routes.md`](./references/proposal-routes.md) | Proposal type routing and chapter structures. |
| [`references/page-types.md`](./references/page-types.md) | Page-type library and proof-object standards. |
| [`references/layout-rhythm.md`](./references/layout-rhythm.md) | Slide density, whitespace balance, and deck pacing rules. |
| [`references/visual-system.md`](./references/visual-system.md) | Visual families, typography, layout, chart, and screenshot rules. |
| [`references/palette-library.md`](./references/palette-library.md) | Default high-taste palette presets when no client visual identity exists. |
| [`references/output-contract.md`](./references/output-contract.md) | Required PPTX and presenter-script output format. |
| [`references/quality-check.md`](./references/quality-check.md) | Final QA checklist and common failure modes. |
| [`assets/minimal-proposal-template.pptx`](./assets/minimal-proposal-template.pptx) | Neutral fallback PowerPoint template. |
| [`agents/openai.yaml`](./agents/openai.yaml) | Codex/OpenAI-style skill UI metadata. |
| [`skill.json`](./skill.json) | Machine-readable metadata for directories and marketplaces. |

The fallback template is used only when there is no client visual identity, no reference deck, and no stronger design direction.

---

## Installation

### Ask an AI Agent

You can ask your AI coding agent:

> Install the proposal-ppt skill from https://github.com/ChuluuMGL/proposal-ppt-skill

### Manual Install

| Agent / IDE | Suggested Skill Directory |
|---|---|
| Codex | `~/.codex/skills/proposal-ppt/` |
| Claude Code | `.claude/skills/proposal-ppt/` |
| Cursor | `.cursor/skills/proposal-ppt/` |
| Qoder | `.qoder/skills/proposal-ppt/` |
| Trae | `.trae/skills/proposal-ppt/` |
| Windsurf | `.windsurf/skills/proposal-ppt/` |
| Generic agents | `.agents/skills/proposal-ppt/` |

Example:

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  ~/.codex/skills/proposal-ppt
```

Restart your agent after installation so the skill metadata is reloaded.

---

## Recommended Prompts

### Guided Blueprint First

```text
Use $proposal-ppt to create a business proposal from the brief below.

Do not generate the PPTX yet. First return:
1. Brief audit
2. Winning thesis
3. Chapter structure
4. Slide-by-slide titles, page purpose, and proof object
5. Visual system recommendation
6. Questions that need my confirmation

Brief:
...
```

### Direct PPTX and Presenter Script

```text
Use $proposal-ppt to directly generate:
1. an editable PowerPoint deck
2. a same-name presenter script in Markdown

Requirements:
- infer the proposal route and slide count
- mark missing information as to be confirmed
- do not invent data, cases, pricing, or performance results
- use the fallback business template if no client visual identity is available
- save outputs to the current project's outputs folder

Brief:
...
```

### Existing Deck Revision

```text
Use $proposal-ppt to revise this existing proposal PPTX.

Goals:
- preserve the current visual style
- improve the winning thesis and chapter logic
- convert slide titles into conclusion sentences
- add proof-object recommendations
- output a matching presenter script in Markdown

File:
...
```

---

## Design Principles

- Start from the client's business problem, not the vendor's service list.
- Every slide should make one judgment and show one proof object.
- Use conclusion-style slide titles.
- Put reasoning and oral explanation into the presenter script, not dense slide text.
- Do not invent data, cases, awards, platform permissions, pricing, or performance results.
- Mark unknowns clearly instead of hiding them.
- Make budget, KPI, ownership, acceptance criteria, and risk boundaries visible.

---

## FAQ

**Is this a PowerPoint template or an AI skill?**  
It is an AI skill. The included PPTX is only a neutral fallback template. The main value is the workflow, page planning, proof-object logic, and presenter-script structure.

**Does it create the PPTX automatically?**  
Yes, when used inside an agent that can create or edit PowerPoint files. In Codex, it should be used together with the local presentation tooling available in the environment.

**Does it require an MCP server?**  
No. This is a local skill package, not an MCP server.

**Can it use a client's existing PPT template?**  
Yes. User-provided templates, existing PPTX files, or client visual identity always take priority over the fallback template.

**Will it invent market data or case results?**  
No. The skill explicitly requires unknown data to be marked as missing or to be confirmed.

**Can other agents use it?**  
Yes, if they support skill folders or can read `SKILL.md`-style packages. Installation paths differ by client.

---

## Technical Specs

| Item | Description |
|---|---|
| Skill name | `proposal-ppt` |
| Repository | `ChuluuMGL/proposal-ppt-skill` |
| Format | Local skill folder with `SKILL.md`, references, assets, and metadata |
| Primary output | `.pptx` + `.md` |
| Bundled asset | Neutral fallback PowerPoint template |
| License | MIT |
| Author | YUEYU TECH |

## Directory Structure

```text
proposal-ppt-skill/
├── SKILL.md
├── README.md
├── README.zh-CN.md
├── LICENSE
├── skill.json
├── agents/
│   └── openai.yaml
├── assets/
│   └── minimal-proposal-template.pptx
└── references/
    ├── output-contract.md
    ├── page-types.md
    ├── layout-rhythm.md
    ├── palette-library.md
    ├── proposal-routes.md
    ├── quality-check.md
    ├── visual-system.md
    └── workflow.md
```

## Related Skill

- [yueyu-skill](https://github.com/ChuluuMGL/yueyu-skill) - Query YUEYU TECH company and marketing-service information.

## License

MIT

---

<!-- Structured Data for SEO: JSON-LD -->
<!-- {
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "proposal-ppt-skill",
  "alternateName": "Business Proposal Presentation Skill",
  "description": "Open-source AI agent skill for creating stage-gated business proposal PowerPoint decks and presenter scripts from briefs, research, budgets, cases, and execution plans.",
  "url": "https://github.com/ChuluuMGL/proposal-ppt-skill",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Any",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "description": "The skill is open source under the MIT license."
  },
  "author": {
    "@type": "Organization",
    "name": "YUEYU TECH",
    "url": "https://www.yueyu.tech/"
  },
  "softwareVersion": "0.1.2"
} -->
