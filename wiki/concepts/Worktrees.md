---
type: concept
created: 2026-06-14
tags: [Worktrees, Git, 工作树, 隔离, Claude Code, Cursor, Agent]
---

# Worktrees

> Git 工作树隔离机制，让多个 Agent 同时工作而不产生文件冲突。

## 定义

Worktrees（工作树）是 Loop Engineering 中的隔离组件。只要让多个 Agent 同时干活，文件冲突就会马上出现——两个 Agent 改同一个文件。Git Worktrees 的价值就是给每个 Agent 独立的 Checkout，它们共享同一份历史，但彼此碰不到对方的工作区。

## 核心价值

- 解决机械冲突：多个 Agent 改同一文件不会互相覆盖
- 共享历史：所有 Agent 基于同一份代码库
- 独立工作区：每个 Agent 有自己的 Checkout

## 局限性

Worktrees 把文件分开，但它不会替你判断哪份改动值得合并。你能跑多少 Agent，不取决于工具，取决于你能审阅多少东西。

## 工具实现

- **Claude Code**：Agent Thread 可以同时作用在同一个 Repo 上
- **Cursor**：可以用 Git Worktree、Worktree 或者给 Sub-Agent 配 Isolation Worktree

## 相关概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agent Loop]] - Agent 循环机制
- [[Sub-Agents]] - 子代理
- [[Automations]] - 自动化触发
- [[Git]] - 版本控制工具

## 来源
- [[2026-06-14-LoopEngineering做设计循环的人]]
