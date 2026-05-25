---
type: concept
created: 2026-05-10
updated: 2026-05-25
sources: [2026-05-10-skill实战- 从0到1写一个你自己的skill, 2026-05-25-Pi Agent比Codex更适合普通人的AI工具]
---

# Skill

## 定义
Skill 是一份给Agent的说明书/操作手册。Agent读完之后就知道怎么来具体地干活了。Skill的本质是一个文件夹，核心是 skill.md 这个文档。

## 关键信息

### 基本结构
```
my-skill/
├── skill.md           Skill的大脑（元数据 + 操作指南）
├── scripts/           需要执行的脚本（可选）
└── reference/         模板文件、配置示例等参考材料（可选）
```

### Skill的两部分
- **上面是元数据**：告诉AI"我是谁，我能干什么"
- **下面是操作指南**：告诉AI"我具体应该怎么干"

### 安装方式
- **global**：所有项目都可以使用的Skill
- **project**：仅当前项目可用的Skill

### 常用Skill分类
| 类别 | 推荐Skill | 说明 |
|------|----------|------|
| 搜索 | Tavily Search | 免费1000次/月，注册简单，适合新手 |
| 搜索 | Brave Search | 搜索结果更好，需绑定信用卡 |
| 文件读取 | PDF Skill | OpenAI发布，支持文字版和扫描版PDF |
| 文件读取 | Word/PPT/Excel Skill | 处理Office文档 |
| 语音合成 | TTS Skill | 无需账号，直接安装使用 |
| 图片生成 | GPT-4o Skill | 调用GPT-4o生成图片 |
| 视频制作 | HyperFrames | 生成带动画的HTML网页，可渲染为视频 |

### 核心公式
**Agent + Skill = 最基本的框架**

这是对普通人来说现在最基本的框架，最本质的逻辑。

### 设计理念
- 底座保持极简，能力按需安装
- 装一个Skill，Agent就多一项能力
- 每个人手中的Agent最后长得都不太一样

## 关联
- 相关概念：[[Pi Agent]]、[[Coding Agent vs 日常任务Agent]]、[[Skill Store]]、[[Skill Creator]]、[[按需加载]]
- 相关实体：Claude Code
- 相关来源：[[2026-05-10-skill实战- 从0到1写一个你自己的skill]]、[[2026-05-25-Pi Agent比Codex更适合普通人的AI工具]]

## 开放问题
- Skill生态的标准化程度如何？
- 不同Agent之间的Skill能否互通？
