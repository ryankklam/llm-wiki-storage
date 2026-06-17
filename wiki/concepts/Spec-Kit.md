---
type: concept
created: 2026-06-17
updated: 2026-06-17
sources: [2026-06-17-AI编程交付企业级项目SpecKit]
---

# Spec-Kit

## 定义

**Spec-Kit** 是 Anthropic 官方开源的 Spec 驱动开发框架，专门配 Claude Code、Cursor、Copilot 等 AI 编程工具使用。相较于轻量框架 OpenSpec，Spec-Kit 具有更广泛的应用场景、可插拔架构和社区生态。

## 核心特征

### 与 OpenSpec 的对比

| 维度 | OpenSpec | Spec-Kit |
|------|----------|----------|
| 定位 | 轻量入门框架 | 企业级完整框架 |
| 命令数 | 3 条核心命令 | 5 条核心 + 9 条全命令 |
| Greenfield | 困难，无引导式提问 | Constitution 立宪法，从零构建体系 |
| 主动追问 | 无 Clarify 机制 | Clarify 主动提问，发现盲点 |
| 校验 | 依赖人工经验 | Verify 内置一致性校验 |
| 门控 | 无 Gate 机制 | 每步 Gate 门控，人工确认后推进 |
| 扩展性 | 固定功能 | Extension 插件市场 + Preset 主题替换 |
| 上手难度 | 低 | 中等 |

### 五条核心命令（最小闭环）

1. **立宪法（Constitution）**：给项目放一份 CLAUDE.md / rules.md，定义项目规则
2. **说需求（Spec）**：把需求写成 AI 能读懂的格式
3. **出方案（Plan）**：AI 拿着规则和需求出技术方案
4. **拆任务（Tasks）**：把方案拆成可单独验收的任务
5. **生成（Execute）**：AI 按任务清单写代码

### 两道可选关卡

- **Clarify（主动追问）**：AI 主动提问，发现需求中的盲点和冲突
- **Verify（一致性检查）**：内置校验，检查生成代码与 Spec 是否一致

### 五大组件系统

1. **CLI 主体**：面向用户的唯一入口，总调度
2. **AI Agent 注册中心**：集成 Claude Code、Cursor 等主流 AI 编程工具
3. **扩展系统（Extension）**：插件市场，做加法，新增能力
4. **预设系统（Preset）**：主题包，做替换，覆盖默认输出规范
5. **工作流引擎（Workflow）**：内置标准流程（0.6.1 版本引入）

## 关键信息

- Spec-Kit 的核心理念：让 AI 停下来等你点头，比让 AI 跑得快更重要（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）
- 大道至简：9 个命令中 5 条核心命令就够跑通一个项目（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）
- Claude Code 本身是黑盒，Spec-Kit 通过文档驱动让人类掌控整个开发进度（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）
- 方法通用：工具换成 Cursor、Claude Code、Codex 都成立，模型换下一代也成立（来源：[[2026-06-17-AI编程交付企业级项目SpecKit]]）

## 关联

- 相关概念：[[OpenSpec]]、[[Constitution]]、[[Clarify]]、[[Verify]]、[[Gate]]、[[Extension]]、[[Preset]]、[[Workflow]]
- 相关工具：[[Claude Code]]、[[Cursor]]、[[Claude]]、[[Anthropic]]
- 相关概念：[[rules.md]]、[[CLAUDE.md]]、[[AI项目规范]]、[[企业级AI项目]]
- 对比概念：[[OpenSpec]]（轻量）vs Spec-Kit（企业级）

## 开放问题

- Spec-Kit 的 Extension 生态何时成熟？
- Preset 系统能否标准化为跨团队共享的模板？
- Spec-Kit 与 CI/CD 流程如何深度集成？
