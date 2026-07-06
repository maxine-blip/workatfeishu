# Feishu Doc Risk Review Skill

A Codex skill for people who review Feishu/Lark documents and need sharper feedback than a generic summary.

It is built for product, marketing, operations, and team leads who often read messy strategy docs, product specs, campaign plans, meeting notes, and Feishu wikis, then need to quickly answer: what is risky, what is missing, what contradicts itself, and what should be changed before the team executes.

## What it does

- Reviews Feishu documents for risks, omissions, contradictions, and weak operating details.
- Produces decision-ready findings instead of generic summaries.
- Adds replacement-ready comments when the task asks for document comments.
- Supports scoped partial rewrites without overwriting unrelated sections.
- Keeps separate review surfaces separate, such as feature updates, registration flows, and referral mechanisms.

## Best for

### Product and project owners reviewing execution docs

Use it when a product spec, wiki page, or feature update looks complete on the surface, but you need to know whether the team can actually build and operate it.

Good prompts:

- 看一下这个产品文档有没有风险，尤其是用户路径、规则口径和埋点部分
- 从负责人角度看，这个方案上线前还缺哪些关键决策
- 这个裂变机制有没有前后矛盾，哪些地方会影响开发落地

### Marketing and growth teams reviewing campaign plans

Use it when a campaign plan has many content ideas, but you need to check whether it has a clear hook, conversion path, owner, timing logic, and service handoff.

Good prompts:

- 看一下这个出分季营销方案有没有没考虑到的地方
- 这个活动方案能不能真正承接咨询线索，哪里会断
- 帮我找出这份方案里曝光、搜索、转化、服务承接之间的缺口

### Operations leads turning meeting notes into document feedback

Use it when meeting notes reveal changes that should be reflected in an existing Feishu doc, but you do not want the document rewritten blindly.

Good prompts:

- 根据这次会议纪要，帮我评论文档里需要改的地方，评论中写最终版本
- 只看第二部分和第四部分，其他先不要动
- 帮我判断哪些内容需要评论，哪些可以直接保留

### Teams that need comments instead of direct edits

Use it when you want feedback to stay visible in the document, especially for cross-functional review, PM review, or manager review.

Good prompts:

- 不要直接修改，帮我在飞书文档里评论需要调整的地方
- 评论要写清楚为什么有风险，以及建议最终改成什么
- 帮我把问题和最终版本都写在评论里，方便我后面确认

### Anyone tired of AI only summarizing the document

Use it when you want Codex to behave like a reviewer, not a note taker. The skill pushes Codex to lead with risks, contradictions, missing decisions, and concrete fixes.

## Files

- `feishu-doc-risk-review/SKILL.md`: the skill instructions
- `feishu-doc-risk-review/agents/openai.yaml`: Codex UI metadata

## Install

Copy the `feishu-doc-risk-review` folder into your Codex skills directory, then restart Codex.
