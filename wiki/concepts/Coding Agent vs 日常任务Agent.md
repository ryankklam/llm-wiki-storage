---
type: concept
created: 2026-05-25
updated: 2026-05-25
sources: [2026-05-25-Pi Agent比Codex更适合普通人的AI工具, 2026-05-10-skill实战- 从0到1写一个你自己的skill]
---

# Coding Agent vs 日常任务Agent

## 定义
Agent按产出类型可分为两大类：
1. **Coding Agent**：产出是代码，目标是帮助开发者写项目
2. **日常任务Agent**：产出是结果（文件、网页、音频、视频等），代码只是中间手段

## 关键信息
- **Coding Agent代表**：Claude Code、Codex、OpenCode
  - 预装完整的写代码流程：代码审核、测试、Git操作、代码规范
  - 开箱即用，适合开发者
  - System Prompt较长（Claude Code约20000 tokens）
- **日常任务Agent代表**：Pi Agent
  - 底座极简（4个工具：读文件、写文件、改文件、跑命令）
  - 通过Skill按需扩展能力
  - System Prompt极短（不到1500 tokens）
  - 适合非开发者的日常办公需求

## 核心区别
| 维度 | Coding Agent | 日常任务Agent |
|------|-------------|--------------|
| 产出 | 代码 | 结果（文件/网页/音频/视频） |
| 设计思路 | 预制好的完整工具链 | 极简底座 + 按需安装Skill |
| 适用人群 | 开发者 | 所有人 |
| 代表产品 | Claude Code, Codex, OpenCode | Pi Agent |
| 解决的问题 | 开发效率 | 工作流效率 |

## 关联
- 相关概念：[[Pi Agent]]、[[Skill]]、[[Claude Code]]
- 相关来源：[[2026-05-25-Pi Agent比Codex更适合普通人的AI工具]]

## 开放问题
- 未来是否会出现更多类型的Agent分类？
- 两类Agent的边界是否会模糊？
