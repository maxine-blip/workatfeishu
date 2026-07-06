---
name: feishu-doc-risk-review
description: Use when reviewing Feishu/Lark docs, wikis, sheets, product specs, campaign plans, meeting-derived docs, or cloud-document sections for risks, omissions, contradictions, weak operating details, comments, replacement-ready feedback, or scoped partial rewrites.
---

# Feishu Doc Risk Review

## Overview

Use this skill to turn Feishu document review into a decision-ready critique or a controlled edit pass. The default output is not a recap: it should surface risks, missing decisions, contradictions, and concrete fixes.

## Modes

Infer the mode from the user's wording:

| User asks for | Mode | Output |
| --- | --- | --- |
| "看一下有没有风险", "哪里不完善", "未考虑到什么" | Risk review | Findings grouped by the user's sections or by severity |
| "进行评论", "评论里写最终版本", "不要直接修改" | Comment pass | Block-anchored comments with replacement-ready wording |
| "只改这一段", "局部改写", "只调整某几节" | Scoped rewrite | Only the named scope changes; leave the rest alone |
| "帮我放进文档", "直接更新飞书" | Edit pass | Update the document, then verify the targeted content |

If the request mixes modes, do the safer narrower action first: comment before direct edits, scoped rewrite before full rewrite.

## Source Handling

Read the original material before judging. For Feishu docs, use the relevant installed Lark/Feishu skills and tools to fetch document content, outline, block IDs, comments, or sheet metadata. If the document is a wiki wrapper, inspect or resolve the underlying doc type when needed.

Preserve these constraints:

- Respect explicit exclusion zones such as "先不看第七部分".
- Keep user-provided section splits separate, such as "功能更新 / 未登录入口 / 裂变机制".
- Use the user's role framing. If they say "我是负责人角度", write from the manager or owner perspective.
- Do not overwrite a whole document when the user named specific sections.
- If live document access fails, separate access/tooling blockers from the actual review logic and explain what could not be verified.

## Risk Review Checklist

Use the checklist selectively; do not dump it as a template.

- Goal: Is the objective measurable, time-bound, and tied to the real business moment?
- User path: Is there one clear next action, intake route, or conversion handoff?
- Operating scaffolding: Are owners, deadlines, SLAs, priority rules, and fallback states defined?
- Rule consistency: Do diagrams, body text, tables, prompts, profile pages, and FAQs agree?
- Data model: Are required fields, events, metrics, attribution, and calculation rules defined?
- Scope control: Is the first release or campaign trying to carry too many P0 items?
- Edge states: Are empty, loading, duplicate, expired, capped, suspicious, failed, and manual-compensation states covered where relevant?
- Trust and compliance: Are claims, score interpretation, incentives, privacy, and user-facing promises safe enough?
- Content/operation fit: Does the plan have a hook, distribution path, search/keyword capture, and service承接 instead of only content ideas?
- Evidence: Does the plan rely on assumptions that need source material, meeting notes, data, or date-sensitive verification?

## Output Contract

Lead with the judgment. Prefer concise, actionable findings over praise or background.

For risk reviews:

1. State the overall verdict in 1-2 sentences.
2. List findings in the same sections the user used, unless severity ordering is clearly better.
3. For each finding, include: problem, why it matters, suggested fix.
4. Call out hard contradictions explicitly with the conflicting values or wording.
5. End with the few decisions that must be settled before execution.

For comment passes:

1. Find the smallest relevant block or section.
2. Write comments that are ready to paste into the document.
3. Include the final replacement wording inside the comment when the user asks for "最终版本".
4. Do not modify document content unless the user also asks for direct changes.
5. After adding comments, verify that comments landed or report the exact limitation.

For scoped rewrites:

1. Restate the allowed scope briefly.
2. Rewrite only that scope.
3. Preserve the document's existing structure unless the structure is the problem.
4. Verify the changed section by targeted readback when possible.

## Comment Style

Use comments as decision support, not vague suggestions.

Good comment shape:

```text
这里建议补充[具体缺口]，否则[具体风险]。建议最终版本改为：
[可直接替换的文本]
```

When a comment is about a rule conflict, include the conflicting locations or values:

```text
这里和前文规则不一致：此处写[值A]，但流程图/表格写[值B]。建议先统一为一个口径，再进入开发或对外说明。
```

## Feishu-Specific Tactics

- Fetch outline or sheet/workbook metadata first when the doc is long or split across tabs.
- Prefer block-level reads and updates for partial work.
- For wiki docs, comments may fail on the wiki layer; try the underlying docx token or text block when available.
- Whiteboard, Mermaid, image, or embedded blocks may not support direct comments; comment on the nearest explanatory text block instead.
- After edits, verify by outline, keyword, or targeted section readback rather than rereading everything.

## Common Failures

| Failure | Correction |
| --- | --- |
| The answer summarizes the document | Convert to risks, missing decisions, and fixes |
| The review merges separate surfaces | Keep the user's section names separate |
| The edit replaces too much | Narrow to the named block or section |
| The comment says "建议优化" | Name the exact replacement or decision needed |
| The plan seems complete because it is long | Check conversion path, owner/SLA, data plumbing, and fallback states |
| One section looks coherent | Cross-check diagrams, body text, tables, prompts, and user-facing pages |
