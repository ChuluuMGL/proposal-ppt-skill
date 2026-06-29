# Runtime Compatibility

Use this file to decide whether the current agent/runtime can complete the full proposal package or must downgrade to a blueprint/script-only delivery.

## Compatibility Status

`tested` means the workflow has been exercised in that runtime or by the maintainer/user with this repository. `expected` means the skill is structurally compatible because the runtime can read local skill folders or `SKILL.md`, but full PPTX generation still depends on available presentation tooling.

| Runtime / Agent | Status | Notes |
|---|---|---|
| Claude Code | tested | User-tested with local proposal-generation flow in June 2026. PPTX output still depends on the host's available file and presentation-generation tools. |
| Codex / OpenAI coding agent | tested for repository maintenance and local PPTX demo generation | This repository was edited, validated, and pushed from Codex. Local style-demo PPTX generation was tested with the available presentation runtime, but other Codex installations may differ. |
| Generic `SKILL.md` readers | expected | Should work when the agent can read `SKILL.md` and referenced files. PPTX generation requires a separate presentation backend. |
| Cursor / Windsurf / Trae / Qoder / Antigravity / OpenClaw / Hermes | expected, not maintainer-verified | Expected to work as instruction packs when installed in a readable local skill folder. Verify invocation, file access, and PPTX tooling in the target runtime before relying on auto mode. |

Do not mark a runtime as `tested` unless someone has actually installed or loaded the skill there and run at least a guided or auto proposal workflow.

## Minimum Runtime Capabilities

Required for any mode:

- Can read `SKILL.md` and files under `references/`.
- Can access the user's brief/source files and write output files.
- Can preserve unknowns as `待确认`, `暂无公开数据`, or equivalent.

Required for full `.pptx` delivery:

- One of:
  - a native presentation/PPTX generation skill or tool,
  - `python-pptx`,
  - `pptxgenjs`,
  - an Office-compatible exporter,
  - PowerPoint/Keynote/LibreOffice automation,
  - another runtime-specific presentation backend that can create editable `.pptx` files.
- Ability to save binary `.pptx` files.
- Ability to validate at least ZIP/XML integrity, and preferably render or open the file.

Recommended for visual QA:

- PPTX-to-PNG/PDF rendering, LibreOffice, PowerPoint, Keynote, or a local preview pipeline.
- Screenshot/contact-sheet review for rhythm and layout.
- Full-size slide review for style-critical pages.

Optional:

- Image generation provider such as OpenAI image APIs, Seedream-style APIs, Flux, Midjourney, or another user-configured provider.
- HTML/SVG rendering for style assets such as ink, glass, pixel, collage, or paper texture.
- PDF extraction / image inspection tools for existing decks and source material.

## Dependency Declaration

This skill is not itself a PPTX rendering engine. It is a proposal strategy, writing, visual-system, and QA instruction pack with a fallback PPTX template.

When the user requests a finished `.pptx`, the agent must explicitly identify the available PPTX backend before building:

```markdown
PPTX backend:
Preview/render backend:
Image-generation backend:
Fallback if unavailable:
```

Do not silently claim a PPTX was produced if the runtime only produced an outline, markdown, HTML, screenshots, or a non-editable PDF.

## Fallback Modes

If full PPTX generation is unavailable, use the highest safe fallback:

| Fallback | Deliverables | When To Use |
|---|---|---|
| `blueprint-only` | brief audit, winning thesis, chapters, slide plan, proof objects, visual system, missing info | Runtime cannot create PPTX or user only wants planning. |
| `copy-and-script` | slide-by-slide copy deck plan plus presenter script `.md` | Runtime can write text files but not PPTX. |
| `template-spec` | visual system, layout recipes, palette, typography, page specs | User will build manually or in another tool. |
| `html-demo` | optional visual prototype plus `.md` script | Runtime can render HTML/SVG but cannot create editable PPTX. Clearly mark as non-PPTX prototype. |
| `repair-needed` | generated PPTX plus warning and repair notes | PPTX exists but fails compatibility checks; do not call it final. |

## Runtime QA

Before final delivery, state:

- runtime/agent used,
- PPTX backend used,
- preview/render method used,
- whether `.pptx` was opened/rendered or only structurally checked,
- any downgraded deliverables,
- unresolved environment limitations.
