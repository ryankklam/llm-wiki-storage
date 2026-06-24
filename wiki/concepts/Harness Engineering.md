---
type: concept
created: 2026-06-24
tags: [Harness Engineering, Agent, 运行环境, 工具配置, 管线, 日志系统, Loop Engineering]
---

# Harness Engineering

> 为 Agent 提供运行环境的工程实践，是 Loop Engineering 的基础设施层。

## 定义

Harness Engineering（环境工程）是指为 Agent 构建运行环境的工程实践，涵盖工具配置、管线（Pipeline）和日志系统。它是 Loop Engineering 的基础——没有 Harness 提供的运行环境，Loop 就无法执行。

## 核心职责

- **工具配置**：为 Agent 配置可调用的工具（终端、文件系统、测试运行器等）
- **管线管理**：定义数据和工作流的流转路径
- **日志系统**：记录 Agent 的运行状态和输出

## 与 Loop Engineering 的关系

- **Harness 是舞台，Loop 是剧本**
- Harness 管运行环境，Loop 管自主迭代机制
- Harness 搞定能不能跑，Loop 保证跑得对不对，以及跑到什么时候停
- Loop 建立在 Harness 之上，两者不可分割

## 四代方法论中的位置

| 范式 | 层级 | 核心问题 |
|------|------|----------|
| Prompt | 第一层 | 你怎么问 |
| Context | 第二层 | 你让 Agent 看见什么 |
| Harness | 第三层 | 你把 Agent 放在什么环境 |
| Loop | 第四层 | 让这套系统自己转起来 |

## 相关概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agent Loop]] - Agent 循环机制
- [[Context工程]] - 上下文工程
- [[Prompt Engineering]] - 提示工程
- [[Tool Use]] - 工具调用能力

## 来源
- [[2026-06-24-大模型面试精讲LoopEngineering]]
