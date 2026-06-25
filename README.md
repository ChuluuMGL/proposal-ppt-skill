# proposal-ppt-skill

Stage-gated business proposal presentation skill for AI agents.

`proposal-ppt` turns client briefs, tender files, research, brand materials, budgets, cases, and execution plans into a commercial proposal package:

- editable PowerPoint deck (`.pptx`)
- same-name presenter script (`.md`)
- missing-information and assumption list

Built by **YUEYU TECH**.

## What It Helps With

- 商业提案 PPT
- 比稿 / 竞标 / RFP / tender proposal
- 年度运营规划
- 品牌营销 / 社媒运营 / 内容方案
- 直播、电商、活动执行方案
- AI / SaaS / 数字化咨询提案
- 招商、合作、资源整合提案
- PPT 逐页内容 + 逐字稿

## How It Works

The skill uses a guided, stage-gated workflow:

1. Start and route the proposal
2. Audit the brief and source materials
3. Define the winning thesis
4. Build the chapter and page blueprint
5. Draft slide-level copy
6. Build or edit the PPTX
7. Write the presenter script
8. Run final QA

Default mode is `guided`: the agent first outputs the brief audit, proposal logic, chapter structure, page plan, proof objects, and visual direction for confirmation. If you ask it to proceed directly, it uses `auto` mode and marks missing information as `待确认`.

## Included Assets

- `SKILL.md` - core instructions and trigger metadata
- `references/` - proposal routes, page types, visual system, workflow, output contract, and QA checklist
- `assets/minimal-proposal-template.pptx` - neutral fallback PowerPoint template
- `agents/openai.yaml` - UI metadata for Codex/OpenAI-style skill surfaces
- `skill.json` - machine-readable metadata for skill directories and marketplaces

The fallback template is not forced. It is used only when there is no client VI, no reference deck, and no stronger visual direction.

## Installation

### Codex

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  ~/.codex/skills/proposal-ppt
```

Restart Codex after installation so the skill metadata is reloaded.

### Claude Code

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  .claude/skills/proposal-ppt
```

Restart Claude Code, then invoke the skill by mentioning `proposal-ppt` or using the relevant skill command surface supported by your client.

### Cursor / Windsurf / Generic Agent Skill Directory

Clone the repository into the skill directory supported by your agent:

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  .agents/skills/proposal-ppt
```

Some clients use `.cursor/skills/`, `.windsurf/skills/`, or other workspace-specific paths. The required folder contents are the same.

## Recommended Prompts

### Guided Blueprint First

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

### Direct PPTX + Script

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

## Design Principles

- Start from the client's business problem, not the vendor's service list.
- Every slide should have one judgment and one proof object.
- Use conclusion-style slide titles.
- Put reasoning and oral explanation into the presenter script, not dense slide text.
- Do not invent data, cases, awards, platform permissions, pricing, or performance results.
- Mark missing information as `待补充`, `待确认`, `暂无公开数据`, or `需客户确认`.

## Related Skill

- [yueyu-skill](https://github.com/ChuluuMGL/yueyu-skill) - query YUEYU TECH company and marketing-service information.

## License

MIT
