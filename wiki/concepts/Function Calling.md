---
type: concept
created: 2026-05-31
tags: [Agent, AI, 工具调用, LLM, API]
---

# Function Calling

> LLM 调用外部函数/API 的能力，Tool Use 的具体实现方式。

## 定义

Function Calling 是 Tool Use 的具体实现方式，让 LLM 能够：
- 理解可用的函数/API
- 决定何时调用哪个函数
- 生成正确的调用参数
- 处理函数返回结果

## 特点

- **结构化输出**：函数调用参数是结构化的 JSON
- **双向交互**：LLM 可以调用函数，函数结果返回给 LLM
- **可扩展**：可以定义任意数量的函数

## 与其他范式的关系

Function Calling 是 Tool Use 的实现方式：
- Tool Use：范式概念（要不要调工具）
- Function Calling：技术实现（怎么调）

可以与其他范式叠加：
- ReAct 的 Action 可以是 Function Calling
- Plan-and-Execute 的执行阶段可以用 Function Calling
- Multi-Agent 中每个 Agent 可以有 Function Calling 能力

## 相关概念
- [[Tool Use]] - Function Calling 实现的范式
- [[Agent范式]] - Agent 架构范式总览
- [[ReAct]] - ReAct 的 Action 可以是 Function Calling
- [[LLM]] - LLM 的函数调用能力

## 来源
- [[2026-05-31-AI Agent四种范式对比]]