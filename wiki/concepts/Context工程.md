---
type: concept
created: 2026-05-11
updated: 2026-08-01
sources: [2026-05-11-万物都可蒸馏Skill-5min讲清机制, 2026-08-01-生产级Agent缺的不是PromptContext]
---

# Context工程

## 定义

**Context工程是大模型2.0时代的核心技术思想**，核心逻辑是**在正确的时机把正确的信息喂给大模型**。

## 与 Prompt工程的对比

| 维度 | Context工程 | Prompt工程 |
|------|-------------|------------|
| 时代 | 大模型2.0时代 | 大模型1.0时代 |
| 核心逻辑 | 在正确时机给正确信息 | 一次性告诉模型所有事 |
| 任务处理 | 拆分成多步，逐步引导 | 单次推理完成所有任务 |
| 上下文 | 渐进式披露 | 一次性全部喂入 |

## 核心灵魂

**[[渐进式上下文披露]]**：把复杂任务拆分成多步，每一步只给模型当前需要的上下文，逐步引导模型完成任务。

## 优势

1. **准确率大幅提升**：每步只处理少量上下文
2. **Token消耗反而更低**：避免无效信息干扰
3. **可单独修正**：任何一步出错都可以单独修正，不需要全部重跑

## 落地形态

**[[Skill]]** 是 Context 工程思想的标准化、可复用、可自主调用的落地形态。

## 企业级落地：Context Layer

在生产级Agent场景中，Context工程的系统化落地是 [[Context Layer]]——一个将企业知识转化为机器可用Context的持续运行基础设施：

- **核心公式**：Performance = Intelligence × Context，模型智能增长1000倍但Context几乎没动
- **系统化载体**：[[Company Brain]] 汇聚企业知识，通过MCP、SQL、Vector Retrieval等检索
- **工程化管理**：Context需要像代码一样进行版本控制、依赖管理、质量管理（[[GitHub for Context]]）
- **持续学习**：通过 [[Compounding Learning Loop]] 让Agent Trace回流修正Skills与Context

## 关键信息
- Context 工程不追求一次性告诉模型所有事（来源：[[2026-05-11-万物都可蒸馏Skill-5min讲清机制]]）
- 渐进式上下文披露是 Context 工程的核心灵魂

## 关联
- 相关概念：[[Skill]]、[[Prompt工程]]、[[渐进式上下文披露]]、[[Context Layer]]、[[Company Brain]]、[[Compounding Learning Loop]]、[[GitHub for Context]]
- 前置概念：[[Prompt]]

## 开放问题
- 如何设计最优的上下文披露策略？
- Context 工程的边界在哪里？
