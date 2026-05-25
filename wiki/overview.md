---
type: overview
created: 2026-05-10
updated: 2026-05-25
---

# 知识库概览

> 本 Wiki 由 LLM 自动维护。

## 当前状态
- 来源数量：2
- 总页面数：22
- 最近更新：2026-05-25

## 核心发现
<!-- 随着知识积累，这里将总结最重要的发现 -->

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
