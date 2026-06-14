---
type: concept
created: 2026-06-09
updated: 2026-06-14
tags: [Supervisor, Agent, 监督, 评审, Checker, Planner, Sub-Agents]
---

# Supervisor

> Agent Loop 中的监督代理，负责对其他 Agent 的输出进行独立评审。

## 定义

Supervisor（监督代理）是 Agent Loop 中的关键组件，负责在无人值守时确保循环的可信性。它的核心作用是将 Planner（规划者）和 Checker（检查者）分开，避免 Agent 自己评审自己时高估结果。

## 核心原理

- Agent 自审（Self-Review）时，对自己产出的结果打分会比较宽容，倾向于高估自己
- Supervisor 是另一个独立的 Agent，专门负责对前一个 Agent 的输出进行评分
- Planner 和 Checker 必须分开，通过 Supervisor 实现分离
- 写代码的人不应该默认给自己的代码盖章

## Sub-Agents 模式

在 Loop Engineering 实践中，Supervisor 通过 Sub-Agents 实现：

```
Sub-Agent A（探索问题） → Sub-Agent B（实现修复） → Sub-Agent C（验证和挑错）
```

关键不是多叫几个模型一起热闹，而是把 Maker 和 Checker 分开。Sub-Agents 很有价值，但不应该到处乱花——更适合高风险改动、共享模块、生产发布，或者明显不信任第一轮结果的时候。

## 工具支持

- **Claude Code**：Sub-Agents 可以在 Claude Agents 里用 TOML 定义角色
- **Cursor**：可以用 Claude Agents 和 Teams，给不同角色分配不同模型

## 工作模式

```
Agent A（执行） → 输出 → Supervisor（评审） → 评分/反馈 → Agent A（修正）
```

## 与对抗审查的关系

Supervisor 模式与 Anthropic 数据 Agent 架构中的"对抗审查"机制类似，都是通过独立评审来提升输出质量。

## 相关概念
- [[Agent Loop]] - Agent 循环机制
- [[Loop Engineering]] - 循环工程方法论
- [[Sub-Agents]] - 子代理
- [[对抗审查]] - 子 Agent 挑错的验证机制
- [[Self-Correction]] - 自我纠错
- [[Agent范式]] - Agent 架构范式

## 来源
- [[2026-06-09-AgentLoop构建步骤实战指南]]
- [[2026-06-14-LoopEngineering做设计循环的人]]
