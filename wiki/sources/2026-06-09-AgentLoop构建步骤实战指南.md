---
type: source
date: 2026-06-09
source: raw/rednote/video/2026-06-09-AgentLoop构建步骤实战指南_1CeQ447Hfxh.mp4
platform: xiaohongshu
video_id: 1CeQ447Hfxh
author: 清华鑫哥讲AI智能体
tags: [Agent Loop, Loop Engineering, Agent, LLM, Claude, Claude Code, Codex, Prompt, Tool Use, Function Calling, Skills, Supervisor, Memory, State, Context, Guardrails, Token, Orchestrator, Planner, Executor, Feedback Loop, Agentic Loop, Autonomous Agent, Multi-Agent, Single-Agent, Open Loop, Closed Loop, ReAct, Plan-and-Execute, Workflow, Chain of Thought, CoT, Reflexion, Self-Correction, Iteration, API, JSON, XML, Context Window, RAG, Knowledge Graph, CLAUDE.md, 范式转移, 编排拓扑, 流水线, 协调者-工作者模式, 并行和合, 上下文污染, 静默失败, 范围蔓延]
---

# 来源：Agent Loop构建、步骤、实战之完整指南

## 视频信息
- **作者**：清华鑫哥讲AI智能体
- **发布时间**：2026-06-09
- **视频链接**：http://xhslink.com/o/1CeQ447Hfxh
- **平台**：小红书

## 核心要点
- 校正模式：CORRECT（中文语音识别校正）
- 原始文本：353 行，中文 Whisper 转录
- 主要改进：修正大量 Whisper 识别错误、修正专有名词（Agent Loop、Loop Engineering、Agent、LLM、Claude、Claude Code、Codex、Prompt、Tool Use、Function Calling、Skills、Supervisor、Memory、State、Context、Guardrails、Token、Orchestrator、Planner、Executor、Feedback Loop、Agentic Loop、Autonomous Agent、Multi-Agent、Single-Agent、Open Loop、Closed Loop、ReAct、Plan-and-Execute、Workflow、Chain of Thought、CoT、Reflexion、Self-Correction、Iteration、API、JSON、XML、Context Window、RAG、Knowledge Graph、CLAUDE.md 等）、按内容分段添加标题层级

## 视频内容摘要

本期视频系统介绍 Agent Loop（Agent 循环）和 Loop Engineering（循环工程）这一 2026 年下半年硅谷最火的概念。Anthropic 创始人 Lior Shternberg 和 Claude Code 创始人 Boris 都公开表示应该停止写 Prompt，转向为 Agent 设计 Loops。

### 为什么是 Agent Loop —— 范式转移

Agent Loop 的爆发本质上是范式转移：原来范式是模型，现在是在循环中的人。通过 Agent Loop 的设计，把人从循环中剥离出来。一年前搞 Agent Loop 需要自己维护编排框架，现在 Claude Code、Codex 等主流产品已内置这些能力，工具不再是障碍，设计变成障碍。

### Loop 的五大构件 + Memory 层

Agent Loop 主要包括五大部分和一个 Memory 层：
1. **Agent 自动化**：Agent 自身的执行能力
2. **Tools（工具层）**：包括插件或工具层
3. **Skills（技能层）**：一组指令加上元数据，加上可选的脚本或资源。有 Skills 的 Loop 像不断积累经验的团队，每次做过的东西沉淀为 Skills，下次直接调用，缩短运行时间和次数，节省成本
4. **Supervisor（监督代理层）**：Loop 循环在无人值守时可信的重要原因。Planner 和 Checker 要分开，通过 Supervisor 来对前一个 Agent 的输出进行评分
5. **Memory（记忆层）**：一般是 Markdown 或一组 Markdown 文件，模型每轮对话都会加载

### 设计 Loop 的五步法

1. **定义停止条件**（最重要）：停止条件必须清晰、可写成代码形式，而非模糊想法。常见停止条件包括单元测试全部通过、输出结构匹配预设结构、文案评分超过阈值等
2. **构建 Context 上下文**：根据每一轮的 State 状态自动组装 Context，反映当前状态
3. **执行并捕获**：执行任务并捕获结果
4. **反馈**：将结果反馈到下一轮
5. **设置 Guardrails 护栏**：包括最大迭代次数（通常 15-50 次）、无进展检测（可能卡住）、Token 上限设置（防止成本失控）

### 6 种 Agent 编排拓扑

1. **简单流水线**：串行处理
2. **协调者-工作者模式**：上面一层协调者，下面干活的 Worker
3. **并行和合模式**：适用于处理大量文件或同时查询多个数据库，相互之间不需要信息交互
4. **带通信的并行模式**：Agent 之间可以同步信息，优化搜索路径

单 Agent 的限制包括上下文饱和、串行停顿、恢复退回等问题。

5 大失败模式：上下文污染、静默失败、范围蔓延等。

### Loop 的真实成本与 Token 优化

建立循环会消耗大量 Token，但有方法节省。6 大导致 Token 消耗增长的方式需要避开：没有终止条件（永远不会停）、没有把上一轮失败信息整合到下轮提示词（断了反馈链）等。

优化策略：协调者只路由不推理——协调者输出只是路由方向，可以非常短（如 12345 或东南西北中），所有 LLM 模型输出成本大于输入成本，省输出是四两拨千斤。

### Open Loop 与 Closed Loop

第七章讨论 Open Loop 和 Closed Loop 的区别与选择。

### Loop Engineering 的认知陷阱与未来

Loop Engineering 不是让工作变容易，而是难点上移了。原来 Prompt 工程师是协调调好的指令，现在 Loop Engineering 要求设定一个能够持续、可验证地运行来完成复杂任务的系统。需要会系统各个构件、设计系统、测试稳定性和有效性、控制成本。

### 从零开始的设计清单

五步设计清单：
1. 任务分解
2. 专家识别
3. 空间设计
4. 契约治理（写类似 CLAUDE.md 文件）
5. 运行前检查表

## 关键概念
- [[Agent Loop]]
- [[Loop Engineering]]
- [[Agentic Loop]]
- [[Supervisor]]
- [[Guardrails]]
- [[Open Loop]]
- [[Closed Loop]]

## 衍生概念
- [[Agent Loop]]
- [[Loop Engineering]]
- [[Agentic Loop]]
- [[Supervisor]]
- [[Guardrails]]
