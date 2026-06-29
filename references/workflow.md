# Guided Workflow and Stage Gates

Use this file when the task needs a structured, engineering-like proposal creation process. The default mode is guided: confirm the blueprint before building the PPTX unless the user asks for direct generation.

## Stage 0: Start and Route

Determine these routing choices before writing slide content.

### Work Mode

- `guided`: first produce blueprint, then wait for user confirmation before building files.
- `auto`: produce the full PPTX and script in one pass with assumptions marked.
- `edit`: modify an existing PPTX and keep the source deck's visual rules unless asked to restyle.
- `audit`: review a proposal deck and return issues/recommendations only.

Default: `guided`.

### Proposal Route

Choose one primary route from `proposal-routes.md`:

- `brand-social-content`
- `annual-operation-retainer`
- `project-execution-live-ecommerce`
- `consulting-digital-ai-saas`
- `partnership-sponsorship`

If unsure, infer from the brief and state the assumption.

### Depth

- `light`: 10-15 slides, suitable for early discussion or small proposal.
- `standard`: 18-30 slides, suitable for normal client proposal or comparison.
- `deep`: 30-60 slides, suitable for annual plan, formal tender, or complex execution.

Default: `standard`.

### Visual Source

Priority order:

1. Existing PPTX being edited
2. User-provided client template or reference deck
3. Client VI / logo / brand colors
4. Explicit user visual direction
5. Public template family from `style-template-strategy.md` plus palette/font/asset plan
6. `assets/minimal-proposal-template.pptx` fallback

When a strong style is requested and no approved reference deck exists, the visual source is not considered approved until the three-page style sample gate in `style-systems.md` passes.

### Required Deliverables

Default deliverables:

- editable `.pptx`
- presenter script `.md`
- missing-information section inside the `.md`

Optional deliverables:

- outline-only blueprint
- page-by-page copy deck plan
- budget table appendix
- speaker notes embedded in PPTX
- bilingual version

## Stage 0 Output

If the user has not already specified routing, output a compact startup summary:

```markdown
## 启动判断

- 工作模式：
- 提案类型：
- 页数深度：
- 视觉来源：
- 必须包含：
- 当前缺失但可先推进：
```

Ask at most three questions, only when the answer materially changes scope, budget, visual system, or proposal route. Otherwise proceed with assumptions.

Suggested questions:

1. 这次是正式比稿/竞标，还是内部预沟通？
2. 是否有客户 VI、logo 或参考 PPT？
3. 需要包含报价/团队/案例/逐字稿中的哪些？

## Stage 1: Brief Intake Check

Read the actual input files or pasted brief. Produce a brief audit before strategy.

Required output:

```markdown
## Brief 审计

| 类别 | 已确认信息 | 缺失/待确认 | 对提案的影响 |
|---|---|---|---|
| 客户目标 |  |  |  |
| 评审/决策标准 |  |  |  |
| 服务范围 |  |  |  |
| 周期/排期 |  |  |  |
| 预算/报价口径 |  |  |  |
| KPI/验收 |  |  |  |
| 案例/资质 |  |  |  |
| 风险边界 |  |  |  |
```

Gate: do not invent missing fields. In guided mode, continue to Stage 2 using clearly marked assumptions unless the missing field blocks structure.

## Stage 2: Proposal Blueprint

Create the commercial logic before slide copy.

Required output:

```markdown
## 提案蓝图

### 1. 赢标主张

### 2. 客户最关心的判断标准

### 3. 章节结构

| 章节 | 章节目标 | 客户应记住什么 |
|---|---|---|

### 4. 逐页规划

| 页码 | 页面标题 | 页面目的 | Proof object | 视觉形式 | 信息状态 |
|---|---|---|---|---|---|

### 5. 视觉系统建议

若使用强风格路线，必须包含：

- 模板家族：
- 商业适配理由：
- Style DNA：
- 字体方案：
- 资产计划：
- 组件变形：
- 需要先测试的 3 页样张：
- 不适合该风格承载的页面：

### 6. 页面节奏图

| 页码 | 密度 | 页型 | 节奏作用 |
|---|---|---|---|

### 7. 视觉资产计划

| 页码 | 资产类型 | 用途 | 来源 | 状态 |
|---|---|---|---|---|

### 8. 需要确认的问题
```

Gate: in guided mode, stop here and ask the user to confirm the blueprint before building PPTX. If a rich style is requested, no client VI exists, or a reusable public template is being created, use `style-template-strategy.md` and create/specify the three-page sample gate before scaling to the full deck. In auto mode, proceed, but still apply the Style DNA Contract and record visual assumptions in the script.

For strong visual routes, the preferred sample set is exactly:

1. cover / big-idea page,
2. proof / mechanism page,
3. dense business page.

Use these samples to decide whether the style can be used across the deck or only on expressive pages.

## Stage 3: Slide Copy Draft

Write slide-level copy from the approved blueprint.

For each slide, draft:

- final slide title
- subtitle or lead sentence
- body bullets / table text / diagram labels
- proof object content
- source or assumption note
- script intent

Quality gate:

- One slide = one judgment.
- Slide title is a conclusion sentence.
- Every slide has a visible proof object.
- No slide depends on long oral explanation to make sense.

## Stage 4: PPT Build

Build or edit the PPTX after the copy draft is stable.

Use the active presentation tooling and its QA rules. For new PowerPoint decks, produce editable objects rather than screenshots where possible.

Build order:

1. Create or inherit visual system.
2. Select a named palette from `palette-library.md` when no client VI exists.
3. If no client VI exists or a rich style is requested, select a public template family from `style-template-strategy.md` or document the explicit custom route.
4. Run the Style DNA Contract; define commercial fit, layout grammar, assets, typography, component transformations, density rhythm, business-clean pages, and anti-examples before drawing.
5. Select fonts and fallbacks from `font-system.md`.
6. Create or generate required assets using `asset-pipeline.md`; keep key business text editable.
7. For a new style/template route, build or specify three full-size samples first: cover/big-idea, strategy/mechanism, and proof-dense.
8. Create master chrome: margins, title zone, page numbers, footer/source style.
9. Build slides by page type and density class from `layout-rhythm.md`.
10. Insert proof objects: tables, matrices, timelines, screenshots, diagrams, sample pages.
11. Render full-size previews and a contact sheet.
12. Fix overlap, clipping, wrapping, alignment, density, over-clustered content, dead empty zones, weak style recognition, identical component grammar across styles, and low-taste primitive-shape placeholders.
13. Run PPTX compatibility QA from `quality-check.md`; if the file is structurally valid but PowerPoint cannot open it, rewrite it through an Office-compatible exporter and deliver the repaired copy.

Gate: do not deliver before rendering/inspection. Mention if visual QA could not be fully performed.

## Stage 5: Presenter Script

Write the `.md` script after slide order is final.

Each slide needs:

- page objective
- why this slide appears here
- suggested exact talk track
- transition sentence
- confirmation notes for assumptions, figures, and claims

The script should make the presenter's reasoning explicit, while the slide remains concise.

## Stage 6: Final QA and Handoff

Run `quality-check.md` before final response.

Final response must include:

- PPTX path
- script MD path
- mode used: guided / auto / edit / audit
- template or visual source used
- QA performed
- unresolved assumptions

## Recommended User Prompts

### Guided Test

```text
用 $proposal-ppt 根据下面 brief 做一份商业提案。

先不要生成 PPTX。请先输出：
1. Brief 审计
2. 赢标主张
3. 章节结构
4. 逐页标题、页面目的、proof object
5. 视觉系统建议
6. 需要我确认的问题

brief:
...
```

### Direct Generation

```text
用 $proposal-ppt 直接根据下面 brief 产出一个可编辑 PPTX 和同名逐字稿 MD。

要求：
- 自动判断提案类型和页数
- 缺失信息标注为待确认
- 不编造数据、案例、报价和效果
- 没有客户 VI 时使用 fallback 商务模板
- 输出到当前项目 outputs 文件夹

brief:
...
```

### Existing Deck Revision

```text
用 $proposal-ppt 修改这个已有提案 PPTX。

目标：
- 保留原视觉风格
- 优化赢标主张和章节逻辑
- 每页改成结论句标题
- 补 proof object 建议
- 同步输出逐字稿 MD

文件：
...
```
