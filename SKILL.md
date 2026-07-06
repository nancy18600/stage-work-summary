---
name: stage-work-summary
description: Create structured work summaries, probation/regularization defenses, performance review narratives, interview project stories, and project retrospectives from user notes, reports, spreadsheets, or documents. Use when the user asks to organize work experience, summarize a quarter/half-year/year, prepare a promotion or transfer defense, turn messy daily logs into a coherent narrative, or refine project experience for resume/interview use. First audit available materials, distinguish hard gaps from soft gaps, and ask for missing information before generating when gaps would materially weaken the summary. Keep the output role-agnostic unless the user explicitly provides a role.
---

# Stage Work Summary

## Core Intent

Turn scattered work records into a clear professional narrative:

Business context -> goals and metrics -> personal role -> project stories -> data evidence -> reflection -> next plan.

Do not default to any specific job family. If the user provides a role, use it; otherwise write in general business/product/project language.

## Workflow

1. Gather source material.
   - Use user-provided text first.
   - If files are provided, inspect their structure before summarizing.
   - For spreadsheets, identify sheets, date ranges, columns, metric definitions, filters, totals, top items, and obvious data-quality caveats.
   - For documents/PDFs, extract section structure, key conclusions, repeated content, unique content, and any stated recommendations.
   - Before writing, produce an internal material inventory: what sources exist, what each source can support, and what important claims remain unsupported.

2. Run a readiness gate before writing.
   - Decide whether the available material is enough to generate a useful summary.
   - Treat hard gaps as blockers unless the user explicitly asks to proceed with assumptions.
   - Treat soft gaps as caveats: proceed when the summary is still useful, but mark assumptions or suggested follow-ups.
   - If only soft gaps remain, proceed directly and note assumptions or caveats in the output.
   - If hard gaps would materially weaken the summary, ask the user for the missing items before generating.
   - After the user provides more material, inspect it and run this readiness gate again.
   - Generate only after the material is sufficient or the user explicitly asks to proceed with gaps.

   Hard gaps usually include:
   - Summary purpose: regularization defense, stage review, interview story, resume bullets, or another format.
   - Time range.
   - Some source material: notes, logs, project list, documents, metrics, or user-provided narrative.
   - User responsibilities and collaboration scope, at least at a rough level.
   - Important projects or workstreams that must be covered.

   Soft gaps usually include:
   - Business/team context.
   - Detailed collaboration map, ownership boundaries, or stakeholder names.
   - Metrics, results, or benefit logic.
   - Challenges, failures, or tradeoffs.
   - Existing source files, links, notes, or reports.
   - Desired tone, length, and output format.

   When soft gaps are missing, infer cautiously from sources and label the inference. Do not invent numbers or ownership.

3. Clarify the business.
   - Summarize what the team/business does in 1-2 concise sentences.
   - Include target users/customers/stakeholders, their current pain points, and the problem solved for users or the platform/company.
   - If this is unclear, infer cautiously from artifacts and mark assumptions.

4. Identify goals and metrics.
   - Find the team’s core goal or north-star metric.
   - Explain current status and how quarterly/yearly OKRs or workstreams support the metric.
   - When exact metrics are missing, describe the benefit logic instead of inventing numbers.

5. Define the user's role.
   - Explain the team position in the larger business.
   - State what the user owned, who they collaborated with, and where their work sat in the end-to-end workflow.
   - Distinguish direct ownership, collaboration, review/feedback, and downstream impact.

6. Build project stories.
   For each important project or requirement, use:
   - Background: what business/user/platform problem existed.
   - Expected benefit: metric impact or benefit logic.
   - Challenge: what made the work non-trivial.
   - Approach: key thinking, tradeoffs, and plan.
   - Execution: concrete actions and collaboration.
   - Result: metric movement, deliverables, adoption, or validated learning.
   - Reflection: what can be reused or improved.

7. Add data-analysis evidence.
   - Show how the user used data to make decisions, diagnose success/failure, prioritize, or iterate.
   - Successful cases can be written as main achievements.
   - Failed or inconclusive cases can be prepared as interview Q&A material; do not over-feature failures in resume-style outputs unless the user asks.

8. Synthesize reusable logic.
   - Extract patterns from successful work.
   - Extract common failure causes.
   - State how the patterns guide future prioritization, iteration, and collaboration.

9. Write next steps.
   - Include personal growth plan.
   - Include business/project suggestions only when grounded in the source material.
   - Tie next steps back to the north-star metric or core goal.

## Missing-Information Questions

Ask only for high-impact gaps. Prefer one concise batch of questions over repeated interruptions.
If hard gaps and soft gaps both exist, ask hard-gap questions first and keep soft-gap questions optional.

Useful questions:

- What is the intended use of this summary, and who will read it?
- What time range should the summary cover?
- What business/team does the work support, and what is the core goal or metric?
- Which projects or workstreams must be highlighted?
- What results, metrics, or representative evidence should be included?
- What challenges, failures, or lessons learned should be mentioned?
- Do you want a long document, PPT outline, speech draft, resume bullets, or interview answers?

## Output Structure

Use the structure that fits the user’s deliverable. Prefer concise, presentation-ready writing.

### Regularization / Stage Defense

1. Personal profile
2. Business and role understanding
3. Key work results
4. Project stories and challenges
5. Data analysis and review
6. Stage summary
7. Next plan and suggestions

### PPT Outline

Use slide-level structure:

1. Title / personal profile
2. Business and team context
3. Personal scope and goals
4. Key results overview
5. Project story 1
6. Project story 2
7. Data review and reusable logic
8. Stage reflection
9. Next plan

For each slide, provide: slide title, core message, 3-5 bullets, and suggested chart/table when useful.

### Speech Draft

Write in first person, suitable for spoken delivery.

Use this flow:

Opening -> business understanding -> my role -> key work -> challenge and solution -> data/result -> reflection -> next plan -> closing.

Keep the tone natural and concise. Avoid writing slide-like dense bullets unless the user asks for speaker notes.

### Interview Project Story

Use the short format:

Project background -> personal responsibility -> key challenge -> solution -> result -> reflection.

Keep each story answerable aloud in 1-2 minutes unless the user requests long-form.

### Resume Bullet

Use action + scope + method + result:

Led/owned/collaborated on X, by doing Y, improving/achieving Z.

If exact numbers are unavailable, use a truthful qualitative result and mention the metric logic only when useful.

### Data Appendix

When source data exists, provide:

- Data scope and filters.
- Key totals and trends.
- Top items or representative cases.
- Caveats and missing data.

## Stage Summary Formula

Use `y = kx + b` when helpful:

- `y`: final goal or core metric.
- `x`: coverage scale, workload, users, projects, tests, assets, cases, or other volume driver.
- `k`: efficiency/quality/conversion rate, such as success rate, retention, conversion, adoption, ROI, cycle time, or defect rate.
- `b`: collaboration, process improvement, tooling, GTM, documentation, training, or other compounding leverage.

Adapt terms to the user's domain. Do not force the formula if it would sound unnatural.

## Evidence Rules

- Do not invent metrics.
- Label inferred metrics or assumptions clearly.
- Prefer exact counts from source files when available.
- When daily logs include repetitive process work, aggregate into monthly/quarterly totals and representative examples.
- If two documents overlap, put shared conclusions once and preserve unique content from the smaller/less comprehensive document as supporting detail.
- Keep failed experiments factual: what was tried, what signal showed failure, why it may have failed, and what changed next.

## Writing Style

- Write from the user's perspective when preparing a self-summary.
- Make business logic explicit before listing actions.
- Use clear headings and compact tables for metrics.
- Avoid empty self-praise; prove capability through context, choices, and results.
- Avoid role-specific jargon unless it appears in the user's materials.
- Keep sentences suitable for presentation or spoken defense.
