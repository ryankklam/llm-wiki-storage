---
type: overview
created: 2026-05-10
updated: 2026-05-25
---

# 知识库概览

> 本 Wiki 由 LLM 自动维护。

## 当前状态
- 来源数量：3
- 总页面数：28
- 最近更新：2026-05-25

## 核心发现
<!-- 随着知识积累，这里将总结最重要的发现 -->

### Prompt工程最佳实践（Anthropic 官方）

#### 结构化 Prompt
- 使用 XML tags 分离角色、指南、政策、语气等
- 经验法则：如果你无法区分，模型也无法区分

#### 评估驱动开发
- 控制用例：验证基本功能
- 边缘用例：防止问题再次出现
- 能力边界用例：确保正确升级或拒绝

#### 关键教训
- **指令不增加能力**：需要计算时给工具
- **说明权衡的两面**：不只说成本，也要说收益
- **模型可能扣留信息**：过度优化可能导致信息扣留

#### Agent 构建策略
- 简单任务：小模型 + 好 Prompt
- 复杂推理：大模型 + Extended Thinking
- 高可靠性：生成-评估-修复循环

### Agent分类体系
Agent按产出类型可分为两大类：
1. **Coding Agent**（Claude Code、Codex、OpenCode）：产出代码，预装完整工具链
2. **日常任务Agent**（Pi Agent）：产出结果，极简底座 + Skill按需扩展

### Pi Agent的核心优势
- System Prompt不到1500 tokens（Claude Code约20000 tokens）
- 三大优势：快、省（token消耗约1%）、聪明（注意力集中）
- 核心公式：Agent + Skill = 最基本的框架

### Skill生态
- Skill是给Agent的说明书/操作手册
- 按需安装，支持global和project两种模式
- 覆盖搜索、文件读取、语音合成、图片生成、视频制作等场景
