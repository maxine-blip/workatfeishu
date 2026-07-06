# Feishu Doc Risk Review Skill

A Codex skill for reviewing Feishu/Lark documents, wikis, sheets, product specs, campaign plans, and meeting-derived docs.

## What it does

- Reviews Feishu documents for risks, omissions, contradictions, and weak operating details.
- Produces decision-ready findings instead of generic summaries.
- Adds replacement-ready comments when the task asks for document comments.
- Supports scoped partial rewrites without overwriting unrelated sections.
- Keeps separate review surfaces separate, such as feature updates, registration flows, and referral mechanisms.

## Best for

Use this skill when you ask things like:

- 看一下这个飞书文档有没有风险
- 哪里还没有考虑到
- 帮我评论文档，评论里写最终版本
- 只改这一节，其他不要动
- 从负责人角度看这个方案有什么问题

## Files

- `feishu-doc-risk-review/SKILL.md`: the skill instructions
- `feishu-doc-risk-review/agents/openai.yaml`: Codex UI metadata

## Install

Copy the `feishu-doc-risk-review` folder into your Codex skills directory, then restart Codex.
