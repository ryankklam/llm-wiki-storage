---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中]
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

### Token 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

Skill 数量过多时，Token 消耗成为关键问题：

- **全量加载**：100个Skill × 每个Skill 500 tokens = 50,000 tokens，远超大多数模型的Context Window
- **Progressive Disclosure**：先只加载Name + Description（约50 tokens/Skill），100个Skill仅需5,000 tokens
- **召回重排**：召回Top 10后，只需加载10个Skill的完整内容，Token消耗大幅降低

**Token优化关键策略**：协调者只路由不推理——在分层路由中，上层路由器的输出只是路由方向（如选择哪个大类），可以非常短。所有LLM模型输出成本大于输入成本，省输出是四两拨千斤。

## 关联

- 相关概念：[[Context Window]]、[[Prompt工程]]、[[rules.md]]、[[Skill路由]]、[[渐进式加载]]、[[召回重排]]

## 开放问题

- 不同语言（中文/英文）的 Token 效率差异如何影响 rules.md 编写？
- Skill Description 的最佳长度（tokens）是多少？
