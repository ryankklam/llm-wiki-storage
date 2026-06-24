---
type: source
platform: xiaohongshu
author: 小哲讲大模型
date: 2026-06-24
url: http://xhslink.com/o/6hVsXRj9OeW
video: raw/rednote/video/2026-06-24-大模型面试精讲LoopEngineering_6hVsXRj9OeW.mp4
subtitle: raw/rednote/subtitle/2026-06-24-大模型面试精讲LoopEngineering_6hVsXRj9OeW.md
tags: [Loop Engineering, Agent Loop, 面试, 大模型, AI Agent, Prompt, Context, Harness, Claude Code, Token, Context Window, LLM]
---

# 大模型面试精讲 Loop Engineering

> 一线大厂AI工程师面试精讲Loop Engineering，深入讲解Loop的核心概念、设计原则和面试常见问题。

## 核心内容

### 背景与考察意图
- Loop Engineering 是 2026 年六月正式定名的 Agent 工程范式
- 面试官考察三件事：AI Agent 工程方法论的整体认知、Loop 内部机制的拆解能力、范式的局限和陷阱

### Loop Engineering 的核心定义
- 设计一套系统来 Prompt Agent，而不是人一条条写
- 把传统"一来一回"的传话模式升级为自动闭环：执行→观察→评估→修正
- 四代方法论层叠关系：Prompt（怎么问）→ Context（让Agent看见什么）→ Harness（把Agent放在什么环境）→ Loop（让系统自己转起来）

### Loop 的五大组件
1. **明确的目标**：Agent 自己能判断是否达成的定义（如单元测试通过、复杂度降低20%）
2. **上下文管理**：压缩、摘要和检知策略，防止撑爆 Token 上限或重复失败
3. **可调用的工具**：终端、文件系统、测试运行器，让循环基于真实反馈而非猜测
4. **产出评估**：跑测试、LLM 打分、对比 Diff，没有评估循环就失去方向
5. **停止条件**：目标达成停、最大次数停、无进展停，直接影响 Token 成本和产出质量

### Loop 与 Harness 的关系
- Harness 是舞台，Loop 是剧本
- Harness 管运行环境（工具配置、管线、日志系统）
- Loop 管自主迭代机制（目标定义、评估函数、停止条件）
- Harness 搞定能不能跑，Loop 保证跑得对不对

### 三大核心风险
1. **无限循环**：无合理停止条件 → 硬性迭代上限 + 无进展检测
2. **目标飘移**：Agent 偏离最初目标 → 每轮目标对照 + 持久化存储
3. **Context 溢出**：窗口被历史填满 → 压缩与裁剪

### 面试回答模板
Loop Engineering 是第四代 Agent 工程范式，建立在 Prompt、Context、Harness 之上。核心是设计系统来 Prompt Agent，包含五个组件和三大风险对抗手段，标志着从逐句指挥到系统设计的进化。

## 涉及概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agent Loop]] - Agent 循环机制
- [[Agentic Loop]] - Agent 自主循环
- [[Claude Code]] - 生产级 Loop 工具
- [[Token]] - Token 成本控制
- [[Context Window]] - 上下文窗口管理
- [[Guardrails]] - 停止条件与护栏
- [[Supervisor]] - 监督代理
- [[AI Agent]] - 自主执行任务的 AI 系统
- [[LLM]] - 大语言模型
