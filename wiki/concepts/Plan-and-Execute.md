---
type: concept
created: 2026-05-31
tags: [Agent, AI, 规划, 执行, LLM]
---

# Plan-and-Execute

> 先规划再执行的 Agent 范式，解决 ReAct 缺乏全局视野的问题。

## 定义

Plan-and-Execute 是一种控制流程层范式，核心理念是**先规划再执行**：

1. **Plan**：模型在动手前生成完整计划
2. **Execute**：然后逐步执行计划

## 特点

### 优势
- **全局视野**：解决 ReAct 边想边做容易迷失方向的问题
- **结构清晰**：适合步骤多但结构明确的任务

### 代价
- **规划消耗推理资源**：需要额外的 LLM 调用生成计划
- **计划可能不准确**：初始规划可能需要调整

### 最佳实践
在执行中引入**重新规划机制**，当发现计划不准确时动态调整。

## 适用场景

适合**步骤多但结构清晰的任务**：
- 大型代码重构
- 复杂数据处理流水线
- 多步骤自动化流程

## 与其他范式的关系

Plan-and-Execute 属于**控制流程层**，解决 ReAct 的深层问题：
- ReAct：边想边做，适合中等复杂度
- Plan-and-Execute：先规划再执行，适合高复杂度结构化任务

可以与其他范式叠加：
- 与 Tool Use：执行阶段可以使用 Tool Use
- 与 ReAct：执行阶段可以用 ReAct 进行单步推理
- 与 Multi-Agent：Multi-Agent 中可以有 Planner 和 Executor 角色

## 相关概念
- [[Agent范式]] - Agent 架构范式总览
- [[ReAct]] - Plan-and-Execute 解决 ReAct 的弱点
- [[Multi-Agent]] - 可有 Planner/Executor 角色
- [[LLM]] - 规划需要 LLM 调用

## 来源
- [[2026-05-31-AI Agent四种范式对比]]