---
type: concept
created: 2026-05-31
tags: [Agent, AI, 架构, 范式]
---

# Agent范式

> AI Agent 的架构范式，定义 Agent 的组织方式和决策流程。

## 定义

Agent 范式是指 AI Agent 的架构模式，决定 Agent 如何组织、推理、行动和协作。四种范式并非同层级对比对象，而是分属不同维度：

| 范式 | 层级 | 核心问题 |
|------|------|----------|
| Tool Use | 基础能力层 | 模型能否调用外部工具？ |
| ReAct | 推理框架层 | 推理和行动如何交替？ |
| Plan-and-Execute | 控制流程层 | 先规划还是边想边做？ |
| Multi-Agent | 组织架构层 | 多个 Agent 怎么协作？ |

## 关键认知

四种范式**可以叠加而非互斥**：
- AutoGen 里的一个 Agent 可以同时用 ReAct、Function Calling
- 整体又是 Multi-Agent 架构

选型不是四选一，而是根据场景在每一层做组合决策。

## 技术选型框架

### 第一看任务复杂度
- 单步或少量调用 → Tool Use
- 多步推理 + 可解释性 → ReAct
- 步骤多且结构化高 → Plan-and-Execute
- 角色天然分离或单 Agent 上下文装不下 → Multi-Agent

### 第二看延迟敏感度
- 实时交互 → Tool Use 或最简 ReAct
- 后台批处理 → Plan-and-Execute 或 Multi-Agent

### 第三看可观测性需求
- ReAct 的循环是天然审计追踪
- Multi-Agent 需同时追踪多 Agent 状态，排查难度最高

## 核心原则

技术选型的核心不是找最好的范式，而是**用最少的复杂度解决当前问题**。范式越高级，系统复杂度越高，复杂度本身就是成本。

## 相关概念
- [[ReAct]] - 推理框架层范式
- [[Plan-and-Execute]] - 控制流程层范式
- [[Multi-Agent]] - 组织架构层范式
- [[Tool Use]] - 基础能力层范式
- [[Context Window]] - 上下文窗口限制

## 来源
- [[2026-05-31-AI Agent四种范式对比]]