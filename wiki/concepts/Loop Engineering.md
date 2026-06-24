---
type: concept
created: 2026-06-09
updated: 2026-06-24
tags: [Loop Engineering, Agent, 工程, 设计, 范式转移, 自动循环系统]
---

# Loop Engineering

> 为 Agent 设计循环系统的工程方法论，是 Prompt 工程的进阶形态。

## 定义

Loop Engineering（循环工程）是指为 Agent 设计、构建和维护循环系统的工程实践。它代表从 Prompt 工程到系统工程的范式转移——不再只是写好提示词，而是设计一个能够持续、可验证地运行来完成复杂任务的系统。

## 核心认知

Loop Engineering 不是让工作变容易，而是难点上移了：
- 原来 Prompt 工程师：协调调好的指令
- 现在 Loop Engineering：设定一个系统能够持续、可验证地运行来完成复杂任务

Loop Engineering 比 Prompt Engineering 更难，因为关注点移动了。你不再只是写一句提示词，而是在设计一个会持续运行、会分发工作、会记录状态、会被验证的系统。

## 能力要求

Loop Engineering 要求工程师具备以下能力：
1. **系统设计**：熟悉系统各个构件，能够设计整体架构
2. **稳定性测试**：测试系统的稳定性和有效性
3. **成本控制**：在稳定有效运行的基础上控制成本
4. **生产环境适配**：确保系统能够在生产环境中使用

## Loop 的五个核心组件 + State

一个 Loop 大概需要五个组件和一个记忆系统：

| 组件 | 核心职责 |
|------|----------|
| Automations（自动化触发） | Loop 的心跳，按节奏醒来，去看 Issue、CI、Commit |
| Worktrees（工作树隔离） | 给每个 Agent 独立的 Checkout，避免文件冲突 |
| Skills（技能沉淀） | 把项目约定、构建步骤、踩坑经验写成文件，避免冷启动 |
| Plugins 和 Connectors | 通过 MCP Connectors 让 Agent 接触真实工具 |
| Sub-Agents（子代理） | 把 Maker 和 Checker 分开，写代码的人不给自己盖章 |
| State（状态记忆） | Markdown、Linear Board 或 Progress Files，记住进度 |

## 工具实现

Claude Code 和 Cursor 都已内置这些能力：
- **Claude Code**：Automations Tab、内建 Worktrees、Agent Skills、MCP Plugins、Sub-Agents
- **Cursor**：Agents、Queues 和 Hooks、Git Worktree、Skills、MCP Service、Agent Teams

名字不同，能力本质相同。重点不是按下某个按钮，重点是设计一个换了工具也还能跑的工作回路。

## Loop 的风险与挑战

1. **验证责任**：Agent 说"done"只是主张不是证明，测试/Review/上线后信号才是证据
2. **认知距离**：Loop 越快交付你没写的代码，你和系统之间的距离越大
3. **渐进式放弃**：当系统看起来能自己跑，人容易停止判断，慢慢改变工作习惯

## 四代方法论层叠关系

Loop Engineering 是第四代 Agent 工程范式，建立在 Prompt、Context、Harness 三代工程之上。四者不是替代关系，而是层叠关系：

| 范式 | 核心问题 | 比喻 |
|------|----------|------|
| Prompt | 你怎么问 | 提问方式 |
| Context | 你让 Agent 看见什么 | 信息供给 |
| Harness | 你把 Agent 放在什么环境 | 运行环境 |
| Loop | 让这套系统自己转起来 | 自动闭环 |

Loop 在最上层调度一切，标志着人在 AI 工作流中从逐句指挥进化为系统设计。

## Loop 的五大组件（面试视角）

从面试精讲角度，Loop 包含五个核心组件：

| 组件 | 核心职责 | 面试关键点 |
|------|----------|------------|
| 明确的目标 | Agent 自己能判断是否达成 | 不是模糊的"帮我优化代码"，而是可验证的定义 |
| 上下文管理 | 压缩、摘要、检知策略 | 防止撑爆 Token 上限或重复失败 |
| 可调用的工具 | 终端、文件系统、测试运行器 | 循环质量取决于反馈的真实性 |
| 产出评估 | 跑测试、LLM 打分、对比 Diff | 没有评估循环就失去方向 |
| 停止条件 | 目标达成停、最大次数停、无进展停 | 直接影响 Token 成本和产出质量 |

## Loop 与 Harness 的关系

- **Harness 是舞台，Loop 是剧本**
- Harness 管运行环境：工具配置、管线、日志系统
- Loop 管自主迭代机制：目标定义、评估函数、停止条件
- Harness 搞定能不能跑，Loop 保证跑得对不对，以及跑到什么时候停

## 三大核心风险与对抗手段

| 风险 | 描述 | 对抗手段 |
|------|------|----------|
| 无限循环 | 无合理停止条件，消耗大量 Token 无产出 | 硬性迭代上限 + 无进展检测 |
| 目标飘移 | Agent 偏离最初目标，做看似相关但不解决问题的事 | 每轮目标对照 + 持久化存储 |
| Context 溢出 | 长期运行中窗口被历史填满 | 压缩与裁剪（完成部分凝练为记录，失败尝试标记为已排除） |

## 从零开始的设计清单

1. **任务分解**：将复杂任务拆解为可执行的子任务
2. **专家识别**：确定每个子任务需要的专家角色
3. **空间设计**：设计 Agent 之间的协作空间
4. **契约治理**：写类似 CLAUDE.md 文件，定义规则和约束
5. **运行前检查**：按照检查表逐项验证

## 与 Prompt 工程的区别

| 维度 | Prompt 工程 | Loop Engineering |
|------|------------|-----------------|
| 核心产出 | 提示词 | 循环系统 |
| 关注点 | 单次交互质量 | 系统持续运行 |
| 验证方式 | 人工评估 | 自动化验证 |
| 成本控制 | 单次 Token 消耗 | 循环累计 Token 消耗 |
| 复杂度 | 低 | 高 |

## 相关概念
- [[Agent Loop]] - Agent 循环机制
- [[Agentic Loop]] - Agent 循环的另一种表述
- [[Guardrails]] - 循环护栏机制
- [[Supervisor]] - 监督代理层
- [[Sub-Agents]] - 子代理，Maker 和 Checker 分离
- [[Automations]] - 自动化触发机制
- [[Worktrees]] - 工作树隔离
- [[Skills]] - 技能沉淀
- [[State]] - 状态记忆
- [[Agent范式]] - Agent 架构范式

## 来源
- [[2026-06-09-AgentLoop构建步骤实战指南]]
- [[2026-06-14-LoopEngineering做设计循环的人]]
- [[2026-06-24-大模型面试精讲LoopEngineering]]
