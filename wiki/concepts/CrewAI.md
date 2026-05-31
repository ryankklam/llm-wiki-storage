---
type: concept
created: 2026-05-31
tags: [Agent, AI, 框架, Multi-Agent, 角色扮演]
---

# CrewAI

> 角色扮演式多 Agent 协作框架。

## 定义

CrewAI 是一个多 Agent 框架，核心理念是**角色扮演式协作**：

- 定义 Agent 角色（如研究员、分析师、写手）
- 定义任务（每个 Agent 负责什么）
- 定义工具（每个 Agent 用什么工具）

## 特点

- **角色定义清晰**：每个 Agent 有明确的角色和职责
- **任务分配明确**：任务按角色分配
- **工具绑定灵活**：每个 Agent 可以有专门的工具集
- **协作编排**：支持顺序、并行、层级等协作模式

## 与其他范式的关系

CrewAI 是 Multi-Agent 范式的典型实现：
- 适合角色边界清晰的协作场景
- 如软件工程的多角色配合、内容编审发布流程

## 相关概念
- [[Multi-Agent]] - CrewAI 实现的范式
- [[Agent范式]] - Agent 架构范式总览
- [[AutoGen]] - 另一个多 Agent 框架

## 来源
- [[2026-05-31-AI Agent四种范式对比]]