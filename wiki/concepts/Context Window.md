---
type: concept
created: 2026-06-12
updated: 2026-06-17
sources: [2026-06-12-企业AI项目rules红线, 2026-06-17-AgentSkill过多4招提升命中]
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

### Context Window 与 Skill 路由

来源：[[2026-06-17-AgentSkill过多4招提升命中]]

Skill 数量过多时，Context Window 面临严重挤占问题：

- **传统做法**：把所有 Skill 的完整 Prompt 全部塞进 Context Window，Skill 越多上下文越长
- **Progressive Disclosure（渐进式加载）**：先只加载所有 Skill 的 Name + Description（摘要级），模型判断相关后再加载完整内容
- 这样大幅减少了 Skill 对 Context Window 的占用，把空间留给真正需要的 Skill

这与 Context Window 优化的核心原则一致：**上下文不是越多越好，关键是把当前任务需要的东西留下，把过期和无关内容挡住。**

## 关联

- 相关概念：[[Token]]、[[Prompt工程]]、[[rules.md]]、[[摘要压缩]]、[[Skill]]、[[Skill路由]]、[[渐进式加载]]
- 相关策略：[[Context Window优化]]、[[Sliding Window]]

## 开放问题

- 如何在有限的 Context Window 中最大化 rules.md 的有效性？
- Progressive Disclosure 的加载策略如何与 Context Window 优先级排序结合？
