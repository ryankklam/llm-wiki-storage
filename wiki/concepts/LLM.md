---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中]
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

### LLM 在 Skill 路由中的角色

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

在 Skill 路由的两阶段架构中，LLM 扮演**重排器（Reranker）**的角色：

1. **召回阶段**：由 Embedding 或关键词检索完成，轻量级、速度快
2. **重排阶段**：将召回的 Top K 候选 Skill 和用户请求一起送入 LLM，由模型做最终判断

这种分工充分利用了 LLM 的语义理解能力，同时避免了让 LLM 直接从几百个 Skill 中选择的低效做法。

## 关联

- 相关概念：[[AI Agent]]、[[Prompt工程]]、[[Context Window]]、[[Token]]、[[Skill路由]]、[[召回重排]]、[[语义匹配]]
- 实践载体：[[rules.md]]、[[CLAUDE.md]]、[[System Prompt]]

## 开放问题

- 不同 LLM 对同一规则的响应差异如何标准化？
- 在 Skill 路由中，LLM 重排的最佳输入格式是什么？
