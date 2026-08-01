---
title: 生产级Agent 缺的不是Prompt，Context
author: Unknown
source: http://xhslink.cn/o/5oZCCwme72W
date: 2026-08-01
type: corrected-subtitle
status: corrected
duration: 329s
---

# 生产级Agent 缺的不是Prompt，Context

**来源**: [小红书](http://xhslink.cn/o/5oZCCwme72W)
**时长**: 约5分29秒

---

## 核心观点

**Performance = Intelligence × Context**

模型变得越来越聪明，但真正进入 Production 的 AI Use Case 仍然有限。问题不在于模型的认知智能（Intelligence），而在于 Agent 能否获得正确、及时、可执行的上下文（Context）。

---

## 模型智能 vs 实际效用

[00:00] Nobody has any doubt that the models are getting exponentially smarter by the day. Two years ago they couldn't pass the bar exam; today, if they were to take the bar, they'd be in the top 1% of scorers.

[00:09] On the other hand, they are not exponentially more useful by any benchmark. Only **1 out of 5** AI use cases actually make it to production. **56% of CEOs** said there is 0 financial benefit from AI today.

[00:27] So what is going on?

## Performance 的真正决定因素

[00:29] Actually, how performance is measured in the human world: **cognitive intelligence doesn't really determine real-world effectiveness**. In fact, only **10% of job performance variance** is explained by IQ.

[00:45] Think about it — would you say your smartest teammate, who scored the highest on the SATs, is also your best teammate? Or would you say no, it's the person who works the most, takes the most feedback, and learns the fastest?

[01:07] In the real world, performance is outcomes that you deliver, and **performance is a function of two things**:

- **Intelligence** — cognitive horsepower, which is a model benchmark
- **Context** — situated knowledge of your business

[01:26] And in the last decade, we have compounded on only one of those parameters. **Intelligence has 1000x'd** in the last decade; just in the last six months, we have **2x'd** on that axis.

[01:38] On the other hand, **context** — the situated knowledge of your business — that's barely moved. We've moved some data to the cloud, but that's about it. It's otherwise locked in dashboards and **Slack threads** and the head of that analyst who might be leaving next week.

## General-Purpose Agent 需要共享团队 Context

[01:56] So, started this year as general-purpose agents started to become a thing, we said: what if there was a different approach with general-purpose agents?

[02:05] Going back to the human world — well, Maya, she's not an individual star, she's part of a team. And you talk about these dream teams: Maya and someone who runs customer support, and someone who launches ads — these people work really well together.

[02:20] And often these dream teams are built on **shared context**:

- They have a **shared language**
- They have a **shared picture** of what's true today
- They have **shared playbooks**
- They have **shared norms** — who's allowed to make what decision
- They have **compounding learning loops** of what good looks like
- They have **shared memory** — "we launched this thing last quarter and it was terrible, and we're not going to make that mistake again"

[02:51] And so we said, is there a way to bring that into the way we think about AI in our companies?

## Company Brain 与 Context Layer

[02:57] The mental model we started working on was: we have these teams of humans across the board, and can these people essentially start building **domain skills**? So each of them is responsible for a certain set of skills.

[03:13] All of this goes into this common one place, which is this one **Company Brain** of sorts. I like to think of this as the **Context Layer**.

[03:20] And then this has a bunch of **retrieval mechanisms** which then talks to the general-purpose agent across the ecosystem.

## Context 应该像 Code 一样管理

[03:31] I want to start by saying: **WTF is a Context Layer?** These are the problems that a Context Layer is meant to solve.

[03:39] The question I like to ask is: **what does the GitHub for context look like?**

[03:45] Few thoughts — company context needs **lifecycle management, collaboration, and versioning**, just like code does. There's questions like: what's local context, what's global context, how do I keep this updated?

[04:02] Can context have a **profile** just like code does? Can that have a **self-learning loop** that's baked into it? What does **quality management** look like? Can you have **security and posture management** associated with that?

[04:20] I see this as having something that has built-in **versioning, quality, and dependency management**. So you should be able to say: hey, this thing impacts all these other things. This is the **Approver**, this is the **Maintainer**, these are the **Contributors**. How do you build human-plus-AI workspaces that these skills are managed via?

## Context Layer 的工作原理

[04:41] The way I think about a Context Layer is: it's a system that turns knowledge, expertise, and norms that Maya knows into a **machine-usable context** for AI systems.

[04:53] At a very high level, the way I like to think of it is:

[05:00] 1. It continually **mines context** from your business systems
[05:05] 2. It's feeding this into that one **Company Brain**
[05:09] 3. It's harnessing this in **skills and context development lifecycles** as your teams go and deploy these agents
[05:16] 4. It has a bunch of ways you can **retrieve it** — **MCP, SQL, Vector Retrieval, Hybrid Assembly**
[05:25] 5. And **pull back from traces** and build this **Compounding Learning Loop**

---

## 关键概念总结

| 概念 | 含义 |
|------|------|
| **Performance = Intelligence × Context** | Agent绩效由模型智能和业务上下文共同决定 |
| **Company Brain** | 可复用的企业级知识中枢，跨任务保持一致性 |
| **Context Layer** | 将知识/规范转化为AI可用上下文的系统层 |
| **GitHub for Context** | Context需要像代码一样进行版本管理、依赖管理、质量管理 |
| **Compounding Learning Loop** | Agent Trace回流后持续修正Skills与Context的闭环 |
| **MCP / SQL / Vector Retrieval** | Context Layer的多种检索机制 |
