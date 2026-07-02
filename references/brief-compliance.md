# Brief Compliance Matrix

> The most engineerable score lever in a bid: **responsiveness / compliance**. In formal procurement (RFP / tender / 招标) it is typically **30–50% of the scored weight**, and it is fully deterministic — unlike creativity, price, or relationships. This gate makes the agent maximize that score by decomposing the brief into scored requirements and proving every one is covered before delivery.

Use this gate whenever the proposal responds to a brief, tender, RFP, or any document that states requirements or evaluation criteria. For a fully open creative pitch with no stated criteria, use the **open-brief fallback** at the end.

## What it produces

A **Brief Compliance Matrix**: a table mapping every brief requirement to the slide(s) and proof object that address it, plus a gap/orphan check. It is a **required deliverable appendix** — showing it to the client is itself a "rigor" score point.

## Stage A — Brief Decomposition

Read the real brief/tender. Extract every requirement and evaluation criterion into a numbered list. For each, capture:

- **#** — stable id (`R1`, `R2`, …).
- **Requirement** — the brief's actual wording, condensed to one line.
- **Type** — 范围(scope) / 标准(criteria) / KPI / 预算(budget) / 格式(format: page count, language, deliverables) / 合规(compliance: qualifications, legal) / 时间(timeline).
- **Weight** — the brief's stated weight/points if any; else blank.
- **Source** — where in the brief (section / page) so it is auditable.

Rules:

- Extract the brief's **own** criteria, not generic categories. If the brief lists a scoring rubric, use it verbatim.
- One requirement per row; split compound requirements (`X 且 Y` → two rows).
- If a requirement is ambiguous or unverifiable, mark it `待确认` and keep going — do not invent an interpretation.

## Stage B — Coverage Matrix

Map each requirement to the slide(s) and proof object that address it:

| # | Brief 要求 / 评分项 | 类型 | 权重 | 对应页 | Proof object | 状态 |
|---|---|---|---|---|---|---|
| R1 | 覆盖一线 3 城试点 | 范围 | 15% | P06 | 试点动销数据 | ✅ 已覆盖 |
| R2 | 提供 ROI 模型 | 标准 | 10% | — | — | ⚠️ 缺口 |
| R3 | 风险与应对方案 | 合规 | 8% | P14 | 风险矩阵 | ✅ 已覆盖 |
| R4 | 全中文、≤30 页 | 格式 | — | 全册 | — | ✅ 已覆盖 |

Status values:

- `✅ 已覆盖` — mapped to a slide **and** has a proof object.
- `◐ 部分` — mapped but the proof is weak; strengthen before delivery.
- `⚠️ 缺口` — no slide addresses it. **Blocks delivery** unless explicitly deferred.
- `❓ 待确认` — ambiguous; needs client clarification (state the question).

## Stage C — Compliance Gate (before delivery)

Run before claiming the deck is done:

1. **No gaps** — every `⚠️ 缺口` must be resolved (add a slide + proof) or explicitly marked `待客户确认` with a reason. A **weighted** requirement left uncovered blocks delivery.
2. **No orphans** — every slide should map to ≥1 `R`. A slide mapping to no requirement is a **自嗨页** (self-indulgent page): cut it, merge it, or rework it to answer a real brief requirement.
3. **Weight check** — if the brief states weights, report covered-weight %; target **100% of weighted items** before delivery, and state any uncovered weight explicitly.
4. **Deliver the matrix** — as a client-facing appendix (last section of the presenter script, or a dedicated compliance slide if the user wants it in the deck).

## Hard rules

- Do not deliver a brief/tender response without a Brief Compliance Matrix.
- Do not leave a **weighted** brief requirement uncovered; if genuinely unanswerable, mark it `待客户确认` with a reason — never silently skip.
- Do not keep slides that map to no brief requirement.
- Do not invent brief requirements that are not in the source.

## Open-brief fallback

When there is no formal brief (open creative pitch), still produce a matrix: infer 3–7 decision criteria from the client goal and mark them as **assumptions** (`待确认`). This keeps the same discipline and lets the user confirm the criteria they are actually being scored against — which is often the single most useful question to ask before writing.
