---
type: concept
created: 2026-06-12
updated: 2026-06-12
sources: [2026-06-12-企业AI项目rules红线]
---

# LLM

## 定义

**LLM（Large Language Model，大语言模型）**是 AI 编程的核心引擎。模型一代比一代聪明，但聪明不等于听话。通过 rules.md / CLAUDE.md 等规范文件，可以让 LLM 按规则稳定工作，而非自由发挥。

## 核心特征

### LLM 与规则约束
来源：[[2026-06-12-企业AI项目rules红线]]

- 模型越聪明，越需要明确边界
- 大模型的发散能力很强，不给红线会写很多额外的东西
- 规则文件让 LLM 从碰运气变成稳定可控

### 跨模型兼容性
- 立 rules.md 这套思路想通后，模型换成下一代、下下一代也成立
- 规范具有模型无关性

## 关联

- 相关概念：[[AI Agent]]、[[Prompt工程]]、[[Context Window]]、[[Token]]
- 实践载体：[[rules.md]]、[[CLAUDE.md]]、[[System Prompt]]

## 开放问题

- 不同 LLM 对同一规则的响应差异如何标准化？
