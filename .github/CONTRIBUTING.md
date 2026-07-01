# Contributing to proposal-ppt-skill

This skill's value is **proposal argument logic, not decoration**. Contributions
that strengthen the winning-thesis workflow, proof objects, and honesty gates
are prioritized over pure visual polish. See the README "Design Principles".

## Ways to contribute

- **A new proposal route** — only if it has a genuinely different chapter
  structure, not a recolor of an existing route. Add it to
  `references/proposal-routes.md`.
- **A new style-template family** — must pass the three-page sample gate
  (cover / proof-mechanism / dense business) at full size before it is merged.
  See `references/style-template-strategy.md`.
- **A new QA check** — preferred over more prose rules. Add it as code to
  `scripts/audit_proposal_pptx.py` so it is objective and rerunnable.
- **Documentation fixes** — keep README, README.zh-CN.md, SKILL.md, and
  `skill.json` in sync. If you add a file, list it in the README "Included
  Files" table and the directory tree, and load it from SKILL.md if the agent
  needs it.

## Non-negotiable rules

These mirror the skill's Hard Rules. A PR that breaks them will not merge:

1. Do not invent data, cases, awards, pricing, permissions, or results.
2. Do not present AI-generated visuals as real client proof — mark them
   conceptual.
3. Do not insert the author's company information into user decks.
4. Do not claim a PPTX was delivered when only markdown/HTML/PDF exists.

## Before submitting

- Run the audit on a sample deck:
  ```bash
  python3 scripts/audit_proposal_pptx.py path/to/deck.pptx --script path/to/script.md
  ```
- Validate `skill.json` parses:
  ```bash
  python3 -m json.tool skill.json > /dev/null
  ```
- Keep the English and Chinese READMEs structurally consistent.

## Licensing

By contributing you agree your changes are released under the project's MIT
license.
