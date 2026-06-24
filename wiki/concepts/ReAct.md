---
type: concept
created: 2026-05-31
tags: [Agent, AI, 推理, ReAct, LLM]
---

# ReAct

> Reasoning + Acting，推理与行动交织的 Agent 范式。

## 定义

ReAct 是一种推理框架层范式，核心是**推理和行动交织进行**。格式是 Thought-Action-Observation 三段循环：

1. **Thought**：先思考下一步做什么
2. **Action**：执行动作
3. **Observation**：拿到观察结果再继续思考

## 特点

### 优势
- **可解释性强**：打开日志能看到每一步的决策路径
- **适合审计追踪**：循环结构天然记录推理过程

### 代价
- **延迟高**：每多轮循环就多一次 LLM 调用
- **缺乏全局视野**：边想边做，面对长任务容易迷失方向

## 适用场景

适合**中等复杂度且对可观测性要求高的任务**：
- 客服工单处理
- 数据分析任务
- 需要审计追踪的场景

## 与其他范式的关系

ReAct 属于**推理框架层**，可以与其他范式叠加：
- 与 Tool Use：ReAct 的 Action 可以是 Tool Use
- 与 Plan-and-Execute：Plan-and-Execute 解决 ReAct 缺乏全局视野的问题
- 与 Multi-Agent：Multi-Agent 中的单个 Agent 可以用 ReAct

## 相关概念
- [[Agent范式]] - Agent 架构范式总览
- [[Plan-and-Execute]] - 解决 ReAct 缺乏全局视野
- [[Tool Use]] - ReAct 的 Action 可以是 Tool Use
- [[LLM]] - 每轮循环需要 LLM 调用
- [[Context Window]] - 上下文窗口限制

## 来源
- [[2026-05-31-AI Agent四种范式对比]]