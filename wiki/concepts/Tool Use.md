---
type: concept
created: 2026-05-31
tags: [Agent, AI, 工具调用, Function Calling, LLM]
---

# Tool Use

> Agent 的基础能力层，决定模型能否调用外部工具。

## 定义

Tool Use 是 Agent 的基础能力层范式，核心是**模型根据上下文自主决定工具调用**：

- 要不要调工具？
- 调哪个工具？
- 传什么参数？
- 拿到结果后继续回复

## 特点

### 优势
- **延迟低**：单次调用，无多轮循环
- **架构简单**：直接调用，无复杂编排

### 代价
- **缺少全局规划**：面对多步推理，每一步独立决策，容易偏离目标
- **不适合复杂任务**：无法处理需要多步协调的场景

## 适用场景

适合**单一或简单调用**：
- 查天气
- 发邮件
- 简单数据查询
- 确定型操作

## 与其他范式的关系

Tool Use 属于**基础能力层**，是其他范式的基础：
- ReAct 的 Action 可以是 Tool Use
- Plan-and-Execute 的执行阶段可以使用 Tool Use
- Multi-Agent 中每个 Agent 可以有 Tool Use 能力

## 相关概念
- [[Agent范式]] - Agent 架构范式总览
- [[Function Calling]] - Tool Use 的具体实现方式
- [[ReAct]] - Tool Use 作为 Action
- [[LLM]] - 模型自主决定工具调用

## 来源
- [[2026-05-31-AI Agent四种范式对比]]