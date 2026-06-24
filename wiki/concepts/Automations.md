---
type: concept
created: 2026-06-14
updated: 2026-06-24
tags: [Automations, 自动化, Loop, 触发, Claude Code, Cursor, Cron, Hooks, GitHub Actions]
---

# Automations

> Loop 的心跳机制，让循环按节奏自动醒来执行任务。

## 定义

Automations（自动化触发）是 Loop Engineering 中 Loop 的心跳。如果没有自动触发，那就只是某天手动跑了一次。有了 Automations，Loop 才能每天、每小时，或者按定义的节奏醒来，去看 Issue、CI、最近的 Commit，然后把值得处理的东西推到面前。

## 工具实现

### Claude Code
- 在 Automations Tab 里配置
- 选项目、写 Prompt、定 Cadence
- 决定跑在本地 Checkout 还是后台 Worktree
- 有发现的结果进 Triage Inbox，没发现问题的运行自动归档

### Cursor
- Scheduling 和 Hooks
- 可以按严格节奏跑，也可以设 Cron
- 可以用 Hooks 在 Agent 生命周期里触发命令
- 可以把整套东西放进 GitHub Actions，关掉电脑也能继续跑

## 核心价值

Automations 让重复检查变成系统行为，而不是人的负担。工具入口不同，目标一样。

## 相关概念
- [[Loop Engineering]] - 循环工程方法论
- [[Agent Loop]] - Agent 循环机制
- [[Worktrees]] - 工作树隔离
- [[State]] - 状态记忆

## 来源
- [[2026-06-14-LoopEngineering做设计循环的人]]
- [[2026-06-24-大模型面试精讲LoopEngineering]]
