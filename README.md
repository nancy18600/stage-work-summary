# Stage Work Summary

`stage-work-summary` is a role-agnostic skill for turning scattered work records into structured stage summaries, regularization defenses, performance review narratives, interview project stories, resume bullets, PPT outlines, and speech drafts.

## What It Does

This skill helps organize notes, daily logs, project lists, spreadsheets, reports, and PDFs into a professional narrative:

Business context -> goals and metrics -> personal role -> project stories -> data evidence -> reflection -> next plan.

It first checks whether the available material is sufficient. If key information is missing, it distinguishes hard gaps from soft gaps:

- Hard gaps block generation unless the user explicitly asks to proceed with assumptions.
- Soft gaps can be handled with caveats, assumptions, or follow-up suggestions.

## Simple Usage

Use:

```text
Use $stage-work-summary to organize my work records into a structured stage summary.
```

Or in Chinese:

```text
用 $stage-work-summary 帮我整理一份阶段性工作总结。
```

## Best Inputs

Provide as many of these as possible:

- Purpose: regularization defense, stage review, interview story, resume bullet, PPT outline, or speech draft.
- Time range.
- Work records: daily logs, weekly reports, project documents, metrics, spreadsheets, or notes.
- Responsibilities: what you owned, supported, reviewed, or collaborated on.
- Important projects or workstreams.
- Results, metrics, benefit logic, or representative evidence.
- Challenges, failures, tradeoffs, and lessons learned.
- Desired tone, length, and output format.

## Outputs Supported

- Regularization or stage defense document.
- PPT outline.
- Speech draft.
- Interview project story.
- Resume bullet.
- Data appendix.

## Included Files

- `SKILL.md`: the skill definition and workflow.
- `agents/openai.yaml`: UI metadata.
- `stage_work_summary_prompt.md`: prompt version of the skill.
- `阶段工作总结提示词版.pdf`: PDF prompt manual.

## 中文说明

`stage-work-summary` 是一个用来整理阶段性工作总结的 Skill。它适合把零散的日报、周报、项目文档、数据表、复盘材料和个人想法，整理成一份能用于转正答辩、阶段复盘、述职汇报、面试项目讲述、简历经历或 PPT 大纲的成体系内容。

简单说，它会帮你把“我做了很多事，但不知道怎么讲清楚”变成“我负责什么、为什么做、怎么做、结果如何、有什么沉淀、下一步怎么走”。

### 它会怎么工作

它不会一上来就硬写总结，而是先检查资料够不够：

- 硬缺口：没有这些信息就很容易写偏，比如时间范围、总结用途、核心工作内容、关键结果等。遇到硬缺口时，会先向你确认，除非你明确说可以先按假设生成。
- 软缺口：有了会更好，但没有也能继续，比如更细的量化收益、协作方反馈、失败案例细节等。遇到软缺口时，会在文中标注假设或给出后续补充建议。

然后它会把内容整理成一条清楚的叙事链路：

业务背景 -> 目标和指标 -> 个人角色 -> 重点项目 -> 数据结果 -> 挑战复盘 -> 个人成长 -> 下一步规划。

### 适合什么时候用

- 要写转正答辩或阶段性工作总结。
- 要整理半年/季度/实习期工作成果。
- 要把项目经历改成面试回答。
- 要把零散工作记录提炼成简历 bullet。
- 要生成 PPT 大纲或答辩讲稿。
- 手里有很多日报、表格、文档，但不知道怎么组织成一份完整材料。

### 怎么使用

最简单的说法：

```text
用 $stage-work-summary 帮我整理一份阶段性工作总结。
```

更完整的说法：

```text
用 $stage-work-summary 根据我提供的日报、数据表和项目文档，整理一份 2026 上半年工作总结，输出为转正答辩风格，包含业务理解、个人职责、重点项目、数据结果、挑战复盘、个人成长和下一步规划。
```

如果想生成 PPT 大纲：

```text
用 $stage-work-summary 帮我生成阶段性工作总结的 PPT 大纲，每页写标题、核心内容和讲述重点。
```

如果想生成讲稿：

```text
用 $stage-work-summary 帮我把这份总结改成 5 分钟答辩讲稿，语气自然一点，适合对评委口头讲。
```

### 最好提供哪些资料

资料越完整，输出越贴近真实工作：

- 总结用途：转正、述职、阶段复盘、面试、简历、PPT 或讲稿。
- 时间范围：例如 2026 上半年、某个季度、实习期。
- 工作记录：日报、周报、需求文档、复盘文档、项目清单。
- 数据材料：消耗、ROI、DAU、留存、点击率、转化率、产出数量等。
- 业务背景：团队做什么、面向什么用户、解决什么问题。
- 个人职责：你负责什么、参与什么、推动什么、协作什么。
- 重点项目：每个项目的背景、目标、动作、难点、结果。
- 复盘材料：成功经验、失败原因、数据分析过程、后续优化方向。
- 输出要求：字数、语气、格式、是否要 PPT 大纲或讲稿。

### 输出会长什么样

它可以输出：

- 阶段性工作总结正文。
- 转正答辩材料。
- PPT 结构大纲。
- 答辩/汇报讲稿。
- 面试项目故事。
- 简历项目经历。
- 数据分析与复盘附录。

### 文件说明

- `SKILL.md`：Skill 的正式工作流程。
- `agents/openai.yaml`：Skill 的展示与配置元信息。
- `stage_work_summary_prompt.md`：可以直接复制使用的提示词版本。
- `阶段工作总结提示词版.pdf`：PDF 版提示词说明书。
