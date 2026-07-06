# Feishu Doc Risk Review Skill

A Codex skill for people who review Feishu/Lark documents and need sharper feedback than a generic summary.

It is built for product, marketing, operations, and team leads who often read messy strategy docs, product specs, campaign plans, meeting notes, and Feishu wikis, then need to quickly answer: what is risky, what is missing, what contradicts itself, and what should be changed before the team executes.

## What it does

- Reviews Feishu documents for risks, omissions, contradictions, and weak operating details.
- Produces decision-ready findings instead of generic summaries.
- Adds replacement-ready comments when the task asks for document comments.
- Supports scoped partial rewrites without overwriting unrelated sections.
- Keeps separate review surfaces separate, such as feature updates, registration flows, and referral mechanisms.

## Why this should be a skill

This workflow is worth turning into a skill because it is not a one-off question. It is a repeated review pattern: read the original Feishu document, identify risks and missing decisions, check contradictions across sections, and produce comments or rewrites that the team can actually use.

When you ask directly, the AI may need to relearn your working style every time. It may summarize the document, give generic suggestions, merge separate sections, or forget that you wanted comments instead of direct edits.

With this skill, Codex starts with the right defaults:

- Treat the task as a risk review, not a summary.
- Read the source material before judging.
- Check goals, user paths, rule consistency, data models, owners, SLAs, and service handoffs.
- Keep the user's original sections separate.
- Add replacement-ready comments when the user asks for comments.
- Rewrite only the named scope when the user asks for a partial edit.

In short: asking directly tells AI what to do this time. A skill teaches AI how you want this type of work done every time.

## 为什么适合做成 Skill

这个流程适合做成 Skill，是因为它不是一次性的提问，而是一套会反复使用的审查方法：先读飞书原文，再判断风险、缺口、前后矛盾，最后输出能被团队直接使用的评论或局部改写。

如果只是直接提问，AI 每次都要重新理解你的工作习惯，很容易跑偏：先总结文档、给泛泛的“建议优化”、把不同模块混在一起、忘记你只想评论而不是直接改正文，或者忘记评论里要写最终版本。

做成 Skill 后，Codex 会默认按这套方式工作：

- 把任务当成风险审查，而不是文档总结。
- 先读原文，再判断问题。
- 重点检查目标、用户路径、规则一致性、数据口径、负责人、SLA 和服务承接。
- 保留用户原来的章节拆分，不把多个问题混成一段。
- 用户说“评论”时，输出可直接替换的最终版本。
- 用户说“只改某一部分”时，只处理指定范围，不重写整篇。

简单说：直接提问，是告诉 AI 这一次要做什么；Skill，是让 AI 记住这类工作以后都应该怎么做。

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
