---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# Context Window

## 定义

**Context Window（上下文窗口）**是 LLM 的"桌面"，会抢位置的东西包括：系统规则、当前任务、历史对话、RAG 证据、工具结果、记忆。rules.md / CLAUDE.md 的长度直接影响上下文窗口的占用。

## 核心特征

### 长度控制的重要性
来源：[[2026-06-12-企业AI项目rules红线]]

- rules.md 建议压在 500 字以内
- 超过这个字数，AI 漏掉关键项的概率明显上升
- 过长反而会让 AI 产生额外解读和漏项

### 优先级排序
来源：[[2026-05-28-如何在有限上下文窗口内放入关键内容]]

1. 系统规则（最高）
2. 当前用户请求和关键约束
3. 高相关证据（RAG 结果）
4. 最近几轮对话
5. 长期偏好摘要

## 关联

- 相关概念：[[Token]]、[[Prompt工程]]、[[rules.md]]、[[摘要压缩]]
- 相关策略：[[Context Window优化]]、[[Sliding Window]]

## 开放问题

- 如何在有限的 Context Window 中最大化 rules.md 的有效性？
