---
type: concept
created: 2026-05-31
tags: [Agent, AI, 多智能体, 协作, AutoGen, CrewAI]
---

# Multi-Agent

> 多智能体范式，通过角色分离应对超复杂任务。

## 定义

Multi-Agent 是一种组织架构层范式，核心理念是**把复杂任务拆给多个专门 Agent**：

- 每个 Agent 有自己的角色、工具和知识范围
- 通过消息或共享状态协作

## 特点

### 优势
- **职责分离**：每个 Agent 只需关注自己的范围
- **Context Window 优化**：每个 Agent 的上下文窗口只需关注自己的范围
- **专业化**：每个 Agent 可以有专门的工具和知识

### 代价
- **编排复杂**：需要设计 Agent 间的协作机制
- **排查难度高**：需同时追踪多 Agent 状态
- **延迟累积**：多 Agent 协作增加通信开销

## 主流框架

| 框架 | 特点 |
|------|------|
| AutoGen | Microsoft 开源，支持多 Agent 对话和协作 |
| CrewAI | 角色扮演式协作，定义 Agent 角色、任务、工具 |

## 适用场景

适合**角色边界清晰的协作场景**：
- 软件工程的多角色配合（开发、测试、运维）
- 内容编审发布流程（写作、审核、发布）
- 复杂业务流程自动化

## 与其他范式的关系

Multi-Agent 属于**组织架构层**，可以与其他范式叠加：
- 单个 Agent 可以用 Tool Use、ReAct、Plan-and-Execute
- Multi-Agent 解决的是 Agent 间的协作问题

### 典型架构
- **Orchestrator**：协调多个 Agent 的中央控制器
- **Planner**：负责规划任务分配
- **Executor**：负责执行具体任务

## Multi-Agent 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

在 Multi-Agent 架构中，Skill 路由问题可以通过**分层路由**来缓解：

- **Orchestrator（协调器）**先判断任务类型，将请求路由到对应的 Sub-Agent 或 Skill 组
- 每个 Sub-Agent 只管理自己领域内的少量 Skill，避免了全局平铺的问题
- 这与 Skill Tree 的分层思想一致：大类 → 子类 → 具体 Skill

大型 AI Agent 系统通常采用这种分层路由而非一次性全量匹配。

## 相关概念
- [[Agent范式]] - Agent 架构范式总览
- [[AutoGen]] - Microsoft 多 Agent 框架
- [[CrewAI]] - 角色扮演式多 Agent 框架
- [[Context Window]] - 每个 Agent 只需关注自己的范围
- [[Skill路由]] - Agent Skill 选择机制
- [[分层路由]] - 分层缩小搜索空间

## 来源
- [[2026-05-31-AI Agent四种范式对比]]
- [[2026-06-17-AgentSkill过多4招提升命中]]