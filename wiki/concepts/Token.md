---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# Token

## 定义

**Token**是大模型处理文本的基本单位。rules.md / CLAUDE.md 的长度以 Token 计量，控制规则文件的长度是优化 Token 消耗和防止 AI 漏项的关键。

## 核心特征

### 长度与 Token 的关系
来源：[[2026-06-12-企业AI项目rules红线]]

- rules.md 建议压在 500 字以内（约 300-500 tokens）
- 复杂项目不超过 2000 字
- 过长反而会让 AI 产生额外解读和漏项

### Token 优化策略
- 精简规则表述，去除冗余
- 禁止项优先，减少允许项描述
- 使用精确术语，避免大白话

## 关联

- 相关概念：[[Context Window]]、[[Prompt工程]]、[[rules.md]]

## 开放问题

- 不同语言（中文/英文）的 Token 效率差异如何影响 rules.md 编写？
