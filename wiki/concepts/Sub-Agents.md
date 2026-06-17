---
type: concept
created: 2026-06-14
tags: [Sub-Agents, Agent, 子代理, Maker, Checker, Supervisor, Claude Code, Cursor]
---

# Sub-Agents

> Loop 中的子代理，将 Maker 和 Checker 角色分离，实现独立评审。

## 定义

Sub-Agents（子代理）是 Loop Engineering 中的关键组件，指在一个主循环中运行的多个专门化 Agent。它的核心价值不是多叫几个模型一起热闹，而是把 Maker（实现者）和 Checker（检查者）分开。

## 核心原理

- 一个 Agent 负责探索问题
- 一个 Agent 负责实现修复
- 另一个 Agent 负责验证和挑错
- 写代码的人不应该默认给自己的代码盖章

## 成本判断

Sub-Agents 很有价值，但不应该到处乱花。它更适合：
- 高风险改动
- 共享模块
- 生产发布
- 明显不信任第一轮结果的场景

## 工具支持

- **Claude Code**：Sub-Agents 可以在 Claude Agents 里用 TOML 定义角色
- **Cursor**：可以用 Claude Agents 和 Teams，给不同角色分配不同模型

## Sub-Agents 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

在 Skill 数量庞大的系统中，Sub-Agents 可以承担**分层路由**中的子域路由角色：

- 每个 Sub-Agent 只负责特定领域的 Skill 子集
- 避免了单个 Agent 需要处理上百个 Skill 的全局路由问题
- Orchestrator 先路由到 Sub-Agent，Sub-Agent 再在局部范围内选择具体 Skill

这与 Skill Tree 的分层思想一致：Orchestrator 对应第一层大类判断，Sub-Agent 对应第二层子类和具体 Skill 选择。

## 相关概念
- [[Supervisor]] - 监督代理
- [[Loop Engineering]] - 循环工程方法论
- [[Agent Loop]] - Agent 循环机制
- [[Guardrails]] - 循环护栏机制
- [[Skill路由]] - Agent Skill 选择机制
- [[分层路由]] - 分层缩小搜索空间

## 来源
- [[2026-06-14-LoopEngineering做设计循环的人]]
- [[2026-06-17-AgentSkill过多4招提升命中]]
