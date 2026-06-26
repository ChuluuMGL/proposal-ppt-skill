# proposal-ppt-skill

> **面向 AI Agent 的商业提案 PPT Skill**
> 一个开源 Skill，用于把客户 brief、调研资料、预算、案例、排期和执行计划，转化为阶段化商业提案 PPT、可编辑 PowerPoint 文件和提案逐字稿。

中文 | [English](./README.md)

[![Skill](https://img.shields.io/badge/AI%20Skill-proposal--ppt-0E5E43)](./SKILL.md)
[![Version](https://img.shields.io/badge/version-0.1.1-green)](./skill.json)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](./LICENSE)
[![Template](https://img.shields.io/badge/template-PPTX-blue)](./assets/minimal-proposal-template.pptx)
[![Workflow](https://img.shields.io/badge/workflow-stage--gated-purple)](./references/workflow.md)

---

## 这个 Skill 能做什么

`proposal-ppt` 可以把杂乱的提案输入，整理成一套商业提案交付包：

| 输出 | 内容 |
|---|---|
| 可编辑 `.pptx` | 一份有完整叙事、逐页 proof object、视觉系统和 QA 标准的商业提案 PPT。 |
| 逐字稿 `.md` | 提案总逻辑、章节讲述节奏、逐页话术、转场句和待确认信息。 |
| 缺失信息清单 | 明确列出不能编造、需要客户补充或进一步确认的信息。 |

它的目标不是“把 PPT 做漂亮”，而是帮助客户判断：为什么这份方案值得被选择。

---

## 适用场景

| 场景 | 典型需求 |
|---|---|
| 商业提案 PPT | “根据这个客户 brief 做一份提案 PPT。” |
| 比稿 / 竞标 / RFP / 招标提案 | “把招标文件整理成 pitch deck 和逐字稿。” |
| 年度运营规划 | “做一份年度社媒/内容/账号运营方案。” |
| 品牌营销 / 社媒内容方案 | “做品牌 campaign、社媒运营或内容机制提案。” |
| 直播、电商、活动执行方案 | “做包含预算、SOP、风险、KPI 的项目执行提案。” |
| AI / SaaS / 数字化咨询 | “做包含路线图、架构图、价值模型的解决方案 PPT。” |
| 招商、合作、资源整合提案 | “做资源包、权益包、合作模式和激活场景提案。” |
| 已有 PPT 优化 | “优化现有 PPT 的逻辑、标题、proof object 和逐字稿。” |

---

## 工作流程

这个 Skill 采用专业提案生产中常见的阶段化工作流：

| 阶段 | 检查门 | 产物 |
|---|---|---|
| 0. 启动与路由 | 判断工作模式、提案类型、页数深度、视觉来源和交付物。 | 启动判断 |
| 1. Brief 审计 | 区分已确认事实和缺失信息。 | Brief 审计 |
| 2. 提案蓝图 | 建立赢标主张、章节结构、逐页规划和 proof object。 | 待确认蓝图 |
| 3. 逐页文案 | 撰写页面标题、正文、图表/矩阵/样稿说明。 | 逐页内容草稿 |
| 4. PPT 绘制 | 生成或修改 PowerPoint 文件。 | 可编辑 `.pptx` |
| 5. 逐字稿 | 撰写提案逻辑和逐页讲述话术。 | `.md` 逐字稿 |
| 6. 最终 QA | 检查逻辑、证据、视觉、预算、KPI 和风险。 | 可交付文件包 |

默认模式是 `guided`：Agent 会先输出提案蓝图，等待确认后再生成 PPTX。  
如果你要求“直接生成”，它会进入 `auto` 模式，并把缺失信息标注为“待确认”。

---

## 工作模式

| 模式 | 适用情况 | 行为 |
|---|---|---|
| `guided` | 需要先确认策略和结构。 | 先输出审计和蓝图，确认后再做 PPTX。 |
| `auto` | 需要快速得到完整初稿。 | 直接生成 PPTX 和逐字稿，假设项明确标注。 |
| `edit` | 已有 PPTX 需要优化。 | 保留原视觉系统，除非你要求重新设计。 |
| `audit` | 只需要审阅或诊断。 | 输出问题、风险和修改建议，不生成新 PPT。 |

---

## 提案路线

这个 Skill 不会把所有提案塞进同一套模板，而是根据 brief 选择主路线：

| 路线 | 适合项目 |
|---|---|
| 品牌、社媒与内容营销 | 品牌 campaign、社媒运营、创意概念、内容机制。 |
| 年度运营与代运营服务 | 常态化运营、账号管理、B2B 内容资产、客户经营。 |
| 项目执行、直播电商与活动 | 直播、电商、活动执行、重制作项目、复杂交付。 |
| 咨询、数字化、AI、SaaS | 转型咨询、AI 工具、SaaS 平台、工作流自动化。 |
| 招商、赞助与资源整合 | 赞助、渠道合作、联合营销、权益包和资源包。 |

完整路由逻辑见 [`references/proposal-routes.md`](./references/proposal-routes.md)。

---

## 包含文件

| 文件 / 目录 | 用途 |
|---|---|
| [`SKILL.md`](./SKILL.md) | Skill 核心元数据和主指令。 |
| [`references/workflow.md`](./references/workflow.md) | 阶段化工作流、检查门和推荐提示词。 |
| [`references/proposal-routes.md`](./references/proposal-routes.md) | 提案类型路由和章节结构。 |
| [`references/page-types.md`](./references/page-types.md) | 页型库和 proof object 标准。 |
| [`references/visual-system.md`](./references/visual-system.md) | 视觉方向、字体、版式、图表和截图规范。 |
| [`references/output-contract.md`](./references/output-contract.md) | PPTX 和逐字稿的输出格式要求。 |
| [`references/quality-check.md`](./references/quality-check.md) | 交付前 QA 清单和常见失败模式。 |
| [`assets/minimal-proposal-template.pptx`](./assets/minimal-proposal-template.pptx) | 中性 fallback PowerPoint 模板。 |
| [`agents/openai.yaml`](./agents/openai.yaml) | Codex / OpenAI 风格 Skill 界面元数据。 |
| [`skill.json`](./skill.json) | 供 Skill 目录、市场和其他 Agent 读取的机器可读元数据。 |

fallback 模板只在没有客户 VI、没有参考 PPT、也没有明确视觉方向时使用，不会强制套用。

---

## 安装

### 让 AI Agent 帮你安装

你可以直接对支持代码操作的 AI Agent 说：

> 帮我安装 proposal-ppt skill，仓库地址：https://github.com/ChuluuMGL/proposal-ppt-skill

### 手动安装

| Agent / IDE | 建议 Skill 目录 |
|---|---|
| Codex | `~/.codex/skills/proposal-ppt/` |
| Claude Code | `.claude/skills/proposal-ppt/` |
| Cursor | `.cursor/skills/proposal-ppt/` |
| Qoder | `.qoder/skills/proposal-ppt/` |
| Trae | `.trae/skills/proposal-ppt/` |
| Windsurf | `.windsurf/skills/proposal-ppt/` |
| 通用 Agent | `.agents/skills/proposal-ppt/` |

示例：

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  ~/.codex/skills/proposal-ppt
```

安装后重启你的 Agent，让 Skill 元数据重新加载。

---

## 推荐提示词

### 先生成蓝图，再确认

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

### 直接生成 PPTX 和逐字稿

```text
用 $proposal-ppt 直接根据下面 brief 产出：
1. 可编辑 PowerPoint 文件
2. 同名 Markdown 逐字稿

要求：
- 自动判断提案类型和页数
- 缺失信息标注为待确认
- 不编造数据、案例、报价和效果
- 没有客户 VI 时使用 fallback 商务模板
- 输出到当前项目 outputs 文件夹

brief:
...
```

### 修改已有提案 PPT

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

---

## 设计原则

- 从客户的业务问题出发，而不是从服务商的服务清单出发。
- 每页只表达一个判断，并且必须有一个 proof object。
- 页面标题使用结论句，而不是空泛名词。
- 把推理、讲述逻辑和口播放进逐字稿，不把长段解释塞进 PPT 页面。
- 不编造数据、案例、奖项、平台权限、报价或效果结果。
- 明确标注未知信息，而不是隐藏或脑补。
- 预算、KPI、负责人、验收标准和风险边界必须可见。

---

## 常见问答

**Q：这是 PowerPoint 模板，还是 AI Skill？**  
A：这是 AI Skill。内置 PPTX 只是中性 fallback 模板，核心价值是提案工作流、页型规划、proof object 逻辑和逐字稿结构。

**Q：它会自动生成 PPTX 吗？**  
A：可以，但需要在支持创建或编辑 PowerPoint 的 Agent 环境中使用。Codex 环境下通常会结合本地 presentation 工具生成可编辑 PPTX。

**Q：需要 MCP 服务器吗？**  
A：不需要。这是本地 Skill 包，不是 MCP Server。

**Q：能使用客户已有 PPT 模板吗？**  
A：可以。用户提供的模板、已有 PPTX 或客户 VI 优先级高于 fallback 模板。

**Q：会不会编造市场数据或案例效果？**  
A：不会。Skill 明确要求未知数据标注为待补充或待确认。

**Q：其他 Agent 可以用吗？**  
A：可以，只要对应 Agent 支持 Skill 文件夹，或能读取 `SKILL.md` 风格的 Skill 包。不同客户端安装路径不同。

---

## 技术规格

| 项目 | 说明 |
|---|---|
| Skill 名称 | `proposal-ppt` |
| 仓库 | `ChuluuMGL/proposal-ppt-skill` |
| 形态 | 本地 Skill 文件夹，包含 `SKILL.md`、references、assets 和 metadata |
| 主要输出 | `.pptx` + `.md` |
| 内置资产 | 中性 fallback PowerPoint 模板 |
| License | MIT |
| 作者 | YUEYU TECH |

## 目录结构

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
    ├── proposal-routes.md
    ├── quality-check.md
    ├── visual-system.md
    └── workflow.md
```

## 相关 Skill

- [yueyu-skill](https://github.com/ChuluuMGL/yueyu-skill) - 查询月瑀科技公司与营销服务信息。

## License

MIT

---

<!-- Structured Data for SEO: JSON-LD -->
<!-- {
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "proposal-ppt-skill",
  "alternateName": "商业提案 PPT Skill",
  "description": "开源 AI Agent Skill，用于根据 brief、调研、预算、案例和执行计划生成阶段化商业提案 PowerPoint 文件与逐字稿。",
  "url": "https://github.com/ChuluuMGL/proposal-ppt-skill",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Any",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "CNY",
    "description": "Skill 开源免费，MIT 协议"
  },
  "author": {
    "@type": "Organization",
    "name": "YUEYU TECH",
    "url": "https://www.yueyu.tech/"
  },
  "softwareVersion": "0.1.1"
} -->
