# proposal-ppt-skill

中文 | [English](./README.md)

面向 AI Agent 的阶段化商业提案 PPT Skill。

`proposal-ppt` 可以把客户 brief、招标文件、调研资料、品牌素材、预算、案例、排期和执行方案，转化为一套商业提案交付包：

- 可编辑 PowerPoint 文件（`.pptx`）
- 同名逐字稿文件（`.md`）
- 缺失信息与假设清单

由 **YUEYU TECH** 构建。

## 适用场景

- 商业提案 PPT
- 比稿 / 竞标 / RFP / tender proposal
- 年度运营规划
- 品牌营销 / 社媒运营 / 内容方案
- 直播、电商、活动执行方案
- AI / SaaS / 数字化咨询提案
- 招商、合作、资源整合提案
- PPT 逐页内容 + 提案逐字稿

## 工作方式

这个 Skill 采用阶段化、带确认门的工作流：

1. 启动并判断提案类型
2. 审计 brief 和资料
3. 定义赢标主张
4. 搭建章节结构和逐页蓝图
5. 撰写逐页内容
6. 生成或修改 PPTX
7. 撰写提案逐字稿
8. 执行最终 QA

默认模式是 `guided`：Agent 会先输出 brief 审计、提案逻辑、章节结构、逐页规划、proof object 和视觉方向，等待确认后再生成 PPTX 和逐字稿。

如果你明确要求“直接生成”，它会使用 `auto` 模式，并把缺失信息标注为 `待确认`。

## 包含内容

- `SKILL.md` - 核心 Skill 指令和触发元数据
- `references/` - 提案路线、页型库、视觉系统、工作流、输出规范和 QA 清单
- `assets/minimal-proposal-template.pptx` - 中性 fallback PowerPoint 模板
- `agents/openai.yaml` - Codex / OpenAI 风格 Skill 界面的元数据
- `skill.json` - 供 Skill 目录、市场和其他 Agent 读取的机器可读元数据

fallback 模板不是强制模板。它只在没有客户 VI、没有参考 PPT、也没有更明确视觉方向时使用。

## 安装方式

### Codex

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  ~/.codex/skills/proposal-ppt
```

安装后重启 Codex，让 Skill 元数据重新加载。

### Claude Code

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  .claude/skills/proposal-ppt
```

重启 Claude Code 后，可以通过提到 `proposal-ppt` 或使用你的客户端支持的 Skill 调用方式来启用。

### Cursor / Windsurf / 通用 Agent Skill 目录

把仓库克隆到你的 Agent 支持的 Skill 目录：

```bash
git clone https://github.com/ChuluuMGL/proposal-ppt-skill.git \
  .agents/skills/proposal-ppt
```

有些客户端使用 `.cursor/skills/`、`.windsurf/skills/` 或其他工作区路径。只要目录里包含本仓库文件即可。

## 推荐使用方式

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

### 直接生成 PPTX + 逐字稿

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

## 设计原则

- 从客户的业务问题出发，而不是从服务商的服务清单出发。
- 每页只表达一个判断，并且必须有一个 proof object。
- 页面标题使用结论句，而不是空泛名词。
- 把推理、讲述逻辑和口播放进逐字稿，不把长段解释塞进 PPT 页面。
- 不编造数据、案例、奖项、平台权限、报价或效果结果。
- 缺失信息标注为 `待补充`、`待确认`、`暂无公开数据` 或 `需客户确认`。

## 相关 Skill

- [yueyu-skill](https://github.com/ChuluuMGL/yueyu-skill) - 查询月瑀科技公司与营销服务信息。

## License

MIT
