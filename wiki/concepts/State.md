---
type: concept
created: 2026-06-14
tags: [State, 状态记忆, Loop, Agent, Markdown, Linear, Progress Files]
---

# State

> Loop 的状态记忆系统，让循环能跨轮次保持连续性。

## 定义

State（状态记忆）是 Loop Engineering 中的记忆组件。没有 Automations，Loop 不会醒；没有 State，Loop 会失忆；没有 Verifier，Loop 会自信地错。State 让 Loop 不是每轮都从零推倒，而是接着上一轮继续跑。

## 存储形式

State 可以是多种形式：
- Markdown 文件
- Linear Board
- Agent 的 MB（Memory Board）
- Progress Files

## 核心价值

State File 记住做过什么、通过什么、还剩什么。这样明天早上 Loop 不是重来一遍，而是接着昨天继续跑。状态先落地，工作再分发——否则只是在并行制造更多需要合并的改动。

## 与 Skills 的配合

Skills 把项目约定写成文件避免冷启动，State 把运行进度写成文件避免失忆。两者配合让 Loop 具备真正的持续运行能力。

## 相关概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agent Loop]] - Agent 循环机制
- [[Skills]] - 技能沉淀
- [[Automations]] - 自动化触发
- [[Guardrails]] - 循环护栏机制

## 来源
- [[2026-06-14-LoopEngineering做设计循环的人]]
