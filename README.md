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

