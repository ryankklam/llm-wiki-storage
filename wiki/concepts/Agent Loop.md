---
type: concept
created: 2026-06-09
tags: [Agent, Loop, 循环, Feedback Loop, Iteration, Self-Correction]
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

## 设计五步法

1. **定义停止条件**：必须清晰、可写成代码形式（如单元测试通过、输出结构匹配、评分超过阈值）
2. **构建 Context 上下文**：根据每轮 State 状态自动组装
3. **执行并捕获**：执行任务并捕获结果
4. **反馈**：将结果反馈到下一轮
5. **设置 Guardrails 护栏**：最大迭代次数（15-50次）、无进展检测、Token 上限

## 为什么现在爆发

- 一年前需要自己维护编排框架，现在 Claude Code、Codex 等主流产品已内置
- 工具不再是障碍，设计变成障碍
- Anthropic 创始人 Lior Shternberg 和 Claude Code 创始人 Boris 都公开倡导

## 与 Prompt 工程的关系

Agent Loop 代表从 Prompt 工程到 Loop Engineering 的范式转移。原来重点是写好提示词，现在重点是设计循环系统。

## 相关概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agentic Loop]] - Agent 循环的另一种表述
- [[Supervisor]] - 监督代理层
- [[Guardrails]] - 循环护栏机制
- [[Open Loop]] - 开放循环
- [[Closed Loop]] - 闭环
- [[Agent范式]] - Agent 架构范式
- [[Skills]] - 技能沉淀机制

## 来源
- [[2026-06-09-AgentLoop构建步骤实战指南]]
