# Output Contract

When the task is to create a commercial proposal, deliver a PPTX and a presenter script Markdown file.

## File Naming

Use clear names:

- `<client-or-project>-proposal.pptx`
- `<client-or-project>-proposal-script.md`

If the user specifies a folder, use it. Otherwise create an `outputs/` folder under the active workspace or another project-appropriate output directory.

## Deck Content Contract

The deck must include, unless the user asks for a different format:

1. Winning thesis
2. Chapter structure
3. Brief translation or client problem restatement
4. Decision standards
5. Evidence/insight pages
6. Core strategy
7. Solution modules
8. Execution cadence
9. Team and collaboration
10. KPI/measurement
11. Budget/commercial boundaries when relevant
12. Risk control
13. Proof/case/evidence pages
14. Closing recommendation and next steps

For lightweight proposals, combine items, but do not omit the commercial logic.

## Presenter Script Markdown

Use this structure:

```markdown
# <Proposal Title> 逐字稿

## 1. 提案总逻辑

- 赢标主张：
- 客户核心问题：
- 我们的判断：
- 讲述顺序：
- 需要客户确认的信息：

## 2. 章节讲述节奏

| 章节 | 目标 | 客户应记住什么 |
|---|---|---|

## 3. 逐页逐字稿

### Slide 01｜<slide title>

**页面目的：**

**这一页为什么放在这里：**

**建议逐字稿：**
<speaker script in natural spoken Chinese>

**转场：**

**待确认/备注：**
```

Do not include hidden reasoning or private chain-of-thought. It is acceptable and required to include presentation rationale, business logic, source notes, and assumptions.

## Missing Information List

If inputs are incomplete, include a section in the script:

```markdown
## 4. 需要客户补充的信息

| 信息 | 用途 | 当前处理 |
|---|---|---|
```

Use this list instead of stopping unless the missing item prevents even a rough proposal from being drafted.

## User-Facing Summary

After finishing, report:

- PPTX path
- script MD path
- whether the deck used client VI, a reference deck, or the minimal fallback template
- tests/QA performed
- unresolved assumptions
