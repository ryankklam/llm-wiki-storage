---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# XML

## 定义

**XML（Extensible Markup Language）**是结构化数据标记语言。在 AI 编程中，Anthropic 推荐使用 XML Tags 来结构化 Prompt，分离角色、指南、政策、语气等内容。

## 核心特征

### XML Tags 在 Prompt 工程中的应用
来源：[[2026-05-25-Anthropic内部Prompt写法]]

- 使用 XML tags 分离角色、指南、政策、语气等
- 经验法则：如果你无法区分，模型也无法区分
- 是 Anthropic 官方推荐的结构化 Prompt 方式

## 关联

- 相关概念：[[JSON]]、[[Markdown]]、[[Prompt工程]]、[[Anthropic Prompt技巧]]

## 开放问题

- XML Tags 与其他结构化方式（如 JSON、YAML）在 Prompt 工程中的优劣对比？
