---
type: source
date: 2026-05-25
source: raw/rednote/video/2026-05-25-Anthropic内部Prompt写法_419zuSb3IEc.mp4
platform: xiaohongshu
video_id: 419zuSb3IEc
author: Margot Van Laar (Anthropic)
tags: [Prompt, Prompt工程, Anthropic, Claude, XML tags, Evaluations, Chain of Thought, Agent, System Prompt, Stop Sequence, Tool Use]
---

# 来源：Anthropic内部Prompt写法，33分钟精华总结

## 视频信息
- **作者**：Margot Van Laar (Anthropic Applied AI Engineer)
- **发布时间**：2026-05-25
- **视频链接**：http://xhslink.com/o/419zuSb3IEc
- **平台**：小红书

## 核心要点
- 校正模式：TRANSLATE（英文翻译中文）
- 原始文本：234 行，英文演讲转录
- 主要改进：翻译为中文、修正专有名词（Anthropic、Prompt、Claude、System Prompt、XML tags、Chain of Thought、CoT、few-shot、zero-shot、context window、temperature、top_p、tokens等）、按内容分段添加标题层级

## 视频内容摘要

这是 Anthropic 应用 AI 工程师 Margot Van Laar 在 Code with Claude 会议上的演讲，系统讲解了 Prompt 编写的最佳实践。

### 两个核心场景

1. **维护现有 Prompt**：已有 Prompt 在生产环境中运行，迁移到新模型或架构变更后出现问题
2. **从零构建 Agent**：需要从头开始编写 Prompt

### Prompt 维护最佳实践

#### 评估套件设计
- **控制用例（Control Case）**：应该总是通过的用例，明确无误
- **边缘用例（Edge Cases）**：之前看到模型失败的用例
- **能力边界用例**：测试模型是否知道何时转交人工或拒绝回答

#### Prompt 清理与优化
1. **添加结构**：使用 XML tags 分离角色、指南、政策、语气等
2. **创建输出契约**：定义清晰的输出格式，使用 Stop Sequence
3. **清理遗留补丁**：删除针对旧模型的冗余指令

#### 针对性解决失败模式
- **热点数据问题**：模型过度遵循"永远不要给错误信息"指令，导致扣留信息
- **按比例计算问题**：指令不增加能力，需要给模型工具
- **账单错误升级问题**：说明权衡的两面，不只说成本也要说收益

### Agent 构建策略

通过员工排班表示例，比较了多种方法：
1. **Sonnet 4.6 + 简单 Prompt**：所有用例失败
2. **Opus 4.7 + 简单 Prompt**：违规减少但仍失败
3. **Opus 4.7 + Extended Thinking**：可靠但 tokens 和延迟高
4. **Sonnet 4.6 + 优化 Prompt**：部分通过，但输出限制问题
5. **生成-评估-修复循环**：最佳方案，tokens 少、延迟低

### 核心教训

- **指令不增加能力**：需要计算时给工具，而不是告诉它"正确计算"
- **说明权衡的两面**：不只说成本，也要说收益
- **版本控制**：追踪防御性更改的原因
- **模型可能扣留信息**：不只是幻觉，过度优化也可能导致信息扣留
- **经验法则**：如果你在阅读 Prompt 时无法区分指南、政策和数据，模型很可能也无法区分

## 关键概念
- [[Prompt]]
- [[Prompt工程]]
- [[Anthropic Prompt技巧]]
- [[System Prompt]]
- [[Chain of Thought]]
- [[XML Tags]]
- [[Evaluations]]
- [[生成-评估-修复循环]]

## 衍生概念
- [[Anthropic Prompt技巧]]
- [[XML Tags]]
- [[Evaluations]]
- [[输出契约]]
- [[生成-评估-修复循环]]
