---
type: concept
created: 2026-05-25
updated: 2026-05-25
sources: [2026-05-25-Pi Agent比Codex更适合普通人的AI工具]
---

# Pi Agent

## 定义
Pi Agent 是一个面向日常任务的AI Agent，与Claude Code、Codex、OpenCode等Coding Agent不同，它的产出不是代码，而是直接交付结果（文件、网页、音频、视频等）。它采用极简主义设计理念，底座只保留4个最基本的工具：读文件、写文件、改文件和跑命令。

## 关键信息
- **设计理念**：极简底座 + Skill按需安装，每个人搭建的Pi Agent都不同
- **官网口号**："There are many agents in the world. This one is yours."（世界上有很多Agent，但这个是你自己的）
- **System Prompt**：不到1500 tokens，比Claude Code（约20000 tokens）少十几倍
- **三大优势**：
  1. **快**：上下文短，模型计算快，输出快
  2. **省**：token消耗约为Claude Code的1%甚至更少
  3. **聪明**：没有冗长的编程提示词抢注意力，在日常任务中表现更好
- **Open Router排名**：每天token消耗量排第6，但每次对话消耗仅为其他Agent的几分之一
- **OpenCode数据**：约5%的生产流量跑在Pi Agent上
- **运行环境**：默认命令行界面，可通过PieWeb包装为网页应用
- **基础依赖**：Node.js

## Skill生态
通过安装不同的Skill，Pi Agent可以获得以下能力：
- **搜索**：Tavily Search、Brave Search
- **文件读取**：PDF、Word、PPT、Excel
- **语音合成**：TTS
- **图片生成**：GPT-4o
- **视频制作**：HyperFrames（先生成带动画的HTML网页，再渲染为视频）

## 关联
- 相关概念：[[Skill]]、[[Coding Agent vs 日常任务Agent]]、[[PieWeb]]
- 相关实体：Claude Code、Codex、OpenCode
- 相关来源：[[2026-05-25-Pi Agent比Codex更适合普通人的AI工具]]

## 开放问题
- Pi Agent在复杂多步骤任务中的可靠性如何？
- Skill生态的第三方贡献情况如何？
