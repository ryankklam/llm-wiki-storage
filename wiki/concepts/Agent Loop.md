---
type: concept
created: 2026-06-09
updated: 2026-06-24
tags: [Agent, Loop, 循环, Feedback Loop, Iteration, Self-Correction, 自动循环系统]
---

# Agent Loop

> Agent 的核心运行机制，通过循环迭代实现自主完成任务。

## 定义

Agent Loop（Agent 循环）是指 Agent 在执行任务时，通过反复迭代"感知-推理-行动-反馈"的过程，逐步逼近目标并完成任务的工作模式。它是 Agent 自主性的核心体现。

## 核心构成

Agent Loop 主要包括五大部分和一个 Memory 层：

1. **Agent 自动化**：Agent 自身的执行能力
2. **Tools（工具层）**：Agent 调用外部工具的能力
3. **Skills（技能层）**：一组指令加上元数据，加上可选的脚本或资源，沉淀经验供后续复用
4. **Supervisor（监督代理层）**：在无人值守时确保可信性的关键组件
5. **Memory（记忆层）**：Markdown 文件，每轮对话都会加载

## Loop 的五个核心组件（实践视角）

从 Loop Engineering 的实践角度看，一个 Agent Loop 包含：

| 组件 | 核心职责 |
|------|----------|
| Automations | Loop 的心跳，让它按节奏醒来 |
| Worktrees | 给每个 Agent 独立的 Checkout，避免文件冲突 |
| Skills | 把项目约定写成文件，避免每次冷启动 |
| Plugins 和 Connectors | 通过 MCP 让 Agent 接触真实工具 |
| Sub-Agents | Maker 和 Checker 分开，写代码的不给自己盖章 |
| State | 记住做过什么、通过什么、还剩什么 |

## Loop 的五大组件（面试视角）

从面试精讲角度，Agent Loop 包含五个核心组件：

| 组件 | 核心职责 |
|------|----------|
| 明确的目标 | Agent 自己能判断是否达成的定义，如单元测试通过、复杂度降低20% |
| 上下文管理 | 压缩、摘要、检知策略，防止撑爆 Token 上限或重复失败 |
| 可调用的工具 | 终端、文件系统、测试运行器，循环质量取决于反馈的真实性 |
| 产出评估 | 跑测试、LLM 打分、对比 Diff，没有评估循环就失去方向 |
| 停止条件 | 目标达成停、最大次数停、无进展停，直接影响 Token 成本和产出质量 |

## 三大核心风险

1. **无限循环**：无合理停止条件 → 硬性迭代上限 + 无进展检测
2. **目标飘移**：Agent 偏离最初目标 → 每轮目标对照 + 持久化存储
3. **Context 溢出**：窗口被历史填满 → 压缩与裁剪

## 设计五步法

1. **定义停止条件**：必须清晰、可写成代码形式（如单元测试通过、输出结构匹配、评分超过阈值）
2. **构建 Context 上下文**：根据每轮 State 状态自动组装
3. **执行并捕获**：执行任务并捕获结果
4. **反馈**：将结果反馈到下一轮
5. **设置 Guardrails 护栏**：最大迭代次数（15-50次）、无进展检测、Token 上限

## 为什么现在爆发

- 一年前需要自己维护编排框架，现在 Claude Code、Cursor 等主流产品已内置
- 工具不再是障碍，设计变成障碍
- Anthropic 创始人 Lior Shternberg 和 Claude Code 创始人 Boris 都公开倡导
- 顶尖程序员已经不再亲自给 AI 写提示词，而是设计自动循环系统

## 与 Prompt 工程的关系

Agent Loop 代表从 Prompt 工程到 Loop Engineering 的范式转移。原来重点是写好提示词，现在重点是设计循环系统。

## 相关概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agentic Loop]] - Agent 循环的另一种表述
- [[Supervisor]] - 监督代理层
- [[Guardrails]] - 循环护栏机制
- [[Open Loop]] - 开放循环
- [[Closed Loop]] - 闭环
- [[Sub-Agents]] - 子代理
- [[Automations]] - 自动化触发
- [[Worktrees]] - 工作树隔离
- [[Skills]] - 技能沉淀
- [[State]] - 状态记忆
- [[Agent范式]] - Agent 架构范式

## 来源
- [[2026-06-09-AgentLoop构建步骤实战指南]]
- [[2026-06-14-LoopEngineering做设计循环的人]]
- [[2026-06-24-大模型面试精讲LoopEngineering]]
