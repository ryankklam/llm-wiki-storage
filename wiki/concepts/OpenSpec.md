---
type: concept
created: 2026-06-17
updated: 2026-06-17
sources: [2026-06-17-AI编程交付企业级项目SpecKit]
---

# OpenSpec

## 定义

**OpenSpec** 是一个轻量级的 Spec 驱动开发框架，适合新手入门。通过三条核心命令（Propose、Apply、Tasks）即可完成一个子功能模块的闭环开发。

## 核心特征

### 三条核心命令

1. **Exploring**：通过对话探索技术方案和功能需求
2. **Propose**：将需求落成本地 Markdown 文档（设计文档、Spec 文档、Tasks.md 任务清单）
3. **Apply**：根据 Propose 阶段生成的文档，逐个完成代码执行
4. **归档**：完成模块后进行文档归档

### 适用场景

- 新手入门，不太了解 Spec 驱动规范
- 从 1 到 N 的已有项目迭代（Brownfield）
- 快速完成小功能点或大项目体系的闭环

### 三大缺陷

来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]

1. **Greenfield 困难**：从零到一搭建项目没有引导式提问，Exploring 阶段没有提问式的引导，适合有技术理解的人
2. **无 Clarify 机制**：不会主动追问缺什么信息，如果需求不明确或技术框架不理解，返工概率很高
3. **Verify 依赖人工**：校验依赖人工经验，如果校验维度没有很好定义，依然检查不出问题

### 与 Spec-Kit 的对比

| 维度 | OpenSpec | Spec-Kit |
|------|----------|----------|
| 定位 | 轻量入门 | 企业级完整 |
| 命令数 | 3 条核心 | 5 条核心 + 9 条全命令 |
| Greenfield | 困难 | Constitution 立宪法 |
| 主动追问 | 无 | Clarify |
| 校验 | 依赖人工 | Verify 内置 |
| 门控 | 无 | Gate 门控 |
| 扩展 | 固定功能 | Extension + Preset |

## 关键信息

- OpenSpec 优势明显（轻量、上手快），劣势也比较明显（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）
- OpenSpec 更适合从 1 到 N 进行开发，不太适合从零进行开发（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）

## 关联

- 相关概念：[[Spec-Kit]]、[[Constitution]]、[[Clarify]]、[[Verify]]、[[Propose]]、[[Apply]]
- 对比概念：[[Spec-Kit]]（企业级）vs OpenSpec（轻量级）
- 相关工具：[[Claude Code]]、[[Cursor]]

## 开放问题

- OpenSpec 是否会演进出 Clarify 和 Verify 机制？
- OpenSpec 和 Spec-Kit 能否结合使用？
