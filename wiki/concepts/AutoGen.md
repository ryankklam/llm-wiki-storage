---
type: concept
created: 2026-05-31
tags: [Agent, AI, 框架, Multi-Agent, Microsoft]
---

# AutoGen

> Microsoft 开源的多 Agent 协作框架。

## 定义

AutoGen 是 Microsoft 开源的多 Agent 框架，支持多个 Agent 之间的对话和协作。

## 特点

- **多 Agent 对话**：支持 Agent 间的自动对话
- **可定制 Agent**：每个 Agent 可以有不同的角色、工具和能力
- **人机协作**：支持人类介入 Agent 对话
- **范式叠加**：单个 Agent 可以同时用 ReAct、Function Calling，整体又是 Multi-Agent 架构

## 与其他范式的关系

AutoGen 是 Multi-Agent 范式的典型实现：
- 单个 Agent 可以用 ReAct、Function Calling
- 整体是 Multi-Agent 架构
- 四层范式可以叠加而非互斥

## 相关概念
- [[Multi-Agent]] - AutoGen 实现的范式
- [[Agent范式]] - Agent 架构范式总览
- [[CrewAI]] - 另一个多 Agent 框架
- [[ReAct]] - AutoGen 中的 Agent 可以用 ReAct

## 来源
- [[2026-05-31-AI Agent四种范式对比]]