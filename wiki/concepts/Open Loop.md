---
type: concept
created: 2026-06-09
updated: 2026-06-14
tags: [Open Loop, Closed Loop, Agent, 循环, 反馈, 认知距离]
---

# Open Loop

> 开放循环，循环的输出不直接反馈回输入的 Agent 运行模式。

## 定义

Open Loop（开放循环）是指 Agent 的循环运行中，输出不直接反馈回输入的模式。与 Closed Loop（闭环）相对，Open Loop 中缺乏自动反馈机制，通常需要人工介入来评估结果并决定下一步。

## 与 Closed Loop 的区别

| 维度 | Open Loop | Closed Loop |
|------|-----------|-------------|
| 反馈机制 | 无自动反馈 | 自动反馈回输入 |
| 人工介入 | 需要人工评估 | 无人值守运行 |
| 适用场景 | 简单任务、需要人工判断 | 可自动化验证的任务 |
| 可信性 | 依赖人工评审 | 依赖自动验证 |

## 认知距离问题

Loop 越快交付你没写的代码，你和系统之间的距离就越大。在 Open Loop 模式下，人工介入可以缓解这个问题，但也意味着工程师需要更频繁地审查系统输出。

## 适用场景

- 任务结果难以自动评估
- 需要人工判断和决策
- 简单的单步任务
- 安全性要求高的场景

## 相关概念
- [[Closed Loop]] - 闭环模式
- [[Agent Loop]] - Agent 循环机制
- [[Feedback Loop]] - 反馈循环
- [[Agentic Loop]] - Agent 循环

## 来源
- [[2026-06-09-AgentLoop构建步骤实战指南]]
- [[2026-06-14-LoopEngineering做设计循环的人]]
