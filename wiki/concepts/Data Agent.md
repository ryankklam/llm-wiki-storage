---
type: concept
created: 2026-06-05
updated: 2026-06-05
sources: [2026-06-05-Anthropic数据Agent95%准确率背后②]
---

# Data Agent

## 定义

**Data Agent（数据 Agent）是利用 LLM 能力进行自助业务分析的智能系统**，能够理解自然语言问题并自动查询数据仓库生成分析结果。

## Anthropic 的 Data Agent 实践

Anthropic 内部的数据 Agent 已能实现：
- 95% 场景的自助业务分析覆盖
- 90% 的整体准确率
- 部分领域准确率接近 99%

### 核心认知

数据 Agent 的高准确率并不是因为 Claude 可以更自由地查数仓，而是系统先把正确答案空间一步步收窄：路由、执行、验证。

### 关键对比

| 配置 | 准确率 |
|------|--------|
| 无 Skills | 最高不超过 21% |
| 有 Skills | 稳定超过 95% |
| Skills + 对抗审查 | 部分领域接近 99% |

## 构建建议

### 核心规则

> 企业要做数据 Agent，不要一开始就对资料和权限。先画出你的答案路径，再让 Agent 沿这条路径工作。

### 最小可行版本

1. 少量官方数据集（Canonical Data Sets）
2. 基础语义层
3. 离线评测
4. 薄的 Knowledge Skill

先别急着造全能数据 Agent，先把最常问、最容易错、最值得治理的那几条答案路径跑通。

## 关联

- 相关概念：[[Anthropic数据Agent架构]]、[[数据Agent四层架构]]、[[语义层]]、[[Skills]]
- 相关来源：[[2026-06-05-Anthropic数据Agent95%准确率背后②]]

## 来源

- [[2026-06-05-Anthropic数据Agent95%准确率背后②]]
