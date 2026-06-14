---
type: source
date: 2026-06-14
source: raw/rednote/video/2026-06-14-LoopEngineering做设计循环的人_AnDZB40fexV.mp4
platform: xiaohongshu
video_id: AnDZB40fexV
author: 思享新境
tags: [Loop Engineering, Agent Loop, Agentic Loop, AI Agent, LLM, Claude, Claude Code, Cursor, Prompt, Tool Use, Function Calling, Chain of Thought, CoT, ReAct, Plan-and-Execute, Workflow, Orchestrator, Planner, Executor, Reflexion, Self-Correction, Iteration, Feedback Loop, Autonomous Agent, Multi-Agent, Single-Agent, API, JSON, Context Window, Token, RAG, Knowledge Graph, Supervisor, Guardrails, Open Loop, Closed Loop, Pipeline, 流水线, 自动循环系统, Automations, Worktrees, Skills, Plugins, Connectors, Sub-Agents, State, MCP, Git Worktree, Triage, CI/CD, PR, Linear, GitHub Actions, Cron, Hooks, Verifier, 冷启动, 认知距离, 渐进式放弃, 验证责任]
---

# 来源：Loop Engineering：做设计循环的人

## 视频信息
- **作者**：思享新境
- **发布时间**：2026-06-14
- **视频链接**：http://xhslink.com/o/AnDZB40fexV
- **平台**：小红书

## 核心要点
- 校正模式：CORRECT（中文语音识别校正）
- 原始文本：82 行，繁体中文 Whisper 转录
- 主要改进：修正大量 Whisper 识别错误、修正专有名词（Loop Engineering、Agent Loop、Agentic Loop、AI Agent、LLM、Claude、Claude Code、Cursor、Prompt、Tool Use、Function Calling、Sub-Agents、State、Automations、Worktrees、Skills、Plugins、Connectors、MCP、Git Worktree、Triage、CI/CD、PR、Linear、GitHub Actions 等）、按内容分段添加标题层级

## 视频内容摘要

本期视频从实践角度深入讲解 Loop Engineering（循环工程），介绍如何为 Agent 设计自动循环系统。视频核心观点：顶尖程序员已经不再亲自给 AI 写提示词，而是设计"自动循环系统（Loop）"，让 AI 去指挥 AI 工作。

### 什么是 Loop Engineering

Loop Engineering 是把提示这件事本身放进工程系统里。你定义目的，AI 一轮一轮推进，直到某个可验证的条件成立。人不再站在每一轮对话的正中间，人开始站到系统设计的位置上。它改变的不是某一次输出，而是你和 Agent 协作时，谁来决定下一步。

### 从手动 Prompt 到 Agent Loop

过去两年使用 AI Agent 的方式很直接：写 Prompt、补上下文、看结果、再写下一条。Loop Engineering 换了一个姿势：构建一个小系统，它会自动发现工作、分发工作、检查结果、记录进度、决定下一步。它和 Agent Loop 很像，但位置更高一层——Agent Loop 是单个 Agent 运行的环境，Loop 则像会定时运行的 Agent Loop。

### Loop 的五个核心组件 + State

一个 Loop 需要五个组件和一个记忆系统：

1. **Automations（自动化触发）**：Loop 的心跳，让它按节奏醒来，去看 Issue、CI、最近的 Commit
2. **Worktrees（工作树隔离）**：给每个 Agent 独立的 Checkout，避免文件冲突
3. **Skills（技能沉淀）**：把项目约定、构建步骤、踩坑经验写成文件，避免每次冷启动
4. **Plugins 和 Connectors（插件与连接器）**：通过 MCP Connectors 让 Agent 接触真实工具（Issue Tracker、数据库、Slack 等）
5. **Sub-Agents（子代理）**：把 Maker 和 Checker 分开，写代码的人不给自己盖章
6. **State（状态记忆）**：可以是 Markdown、Linear Board 或 Progress Files，记住做过什么、通过什么、还剩什么

### Claude Code 与 Cursor 的实现对比

Claude Code 有 Automations Tab、内建 Worktrees、Agent Skills、MCP Plugins、Sub-Agents。Cursor 有 Agents、Queues 和 Hooks、Git Worktree、Skills、MCP Service、Agent Teams。名字不同，能力本质相同。

### Loop 的风险与挑战

三个关键问题：
1. **验证责任**：Agent 说"done"只是主张不是证明，测试/Review/上线后信号才是证据
2. **认知距离**：Loop 越快交付你没写的代码，你和系统之间的距离越大
3. **渐进式放弃**：当系统看起来能自己跑，人容易停止判断，慢慢改变工作习惯

### 核心结论

Loop Engineering 比 Prompt Engineering 更难，因为关注点移动了。你不再只是写一句提示词，而是在设计一个会持续运行、会分发工作、会记录状态、会被验证的系统。构建 Loop，但继续做工程师。

## 关键概念
- [[Loop Engineering]]
- [[Agent Loop]]
- [[Agentic Loop]]
- [[Supervisor]]
- [[Guardrails]]
- [[Open Loop]]
- [[Closed Loop]]
- [[Sub-Agents]]
- [[Automations]]
- [[Worktrees]]
- [[Skills]]
- [[State]]
- [[MCP]]
- [[Claude Code]]
- [[Cursor]]
- [[Token]]
- [[CI/CD]]

## 衍生概念
- [[Loop Engineering]]
- [[Agent Loop]]
- [[Agentic Loop]]
- [[Supervisor]]
- [[Guardrails]]
- [[Sub-Agents]]
- [[Automations]]
- [[Worktrees]]
- [[Skills]]
- [[State]]
- [[MCP]]
