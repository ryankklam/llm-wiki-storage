---
type: concept
created: 2026-08-01
updated: 2026-08-01
sources: [2026-08-01-生产级Agent缺的不是PromptContext]
---

# GitHub for Context

## 定义

**GitHub for Context** 是将软件工程的代码管理方法论应用到企业Context管理上的理念。核心问题是："Context的GitHub长什么样？"——即如何像管理代码一样系统地管理企业的知识和上下文。

## 核心主张

企业Context需要与代码相同级别的工程化管理：

| 管理维度 | 代码管理 | Context管理 |
|----------|----------|-------------|
| 生命周期 | 版本发布、废弃流程 | Lifecycle Management |
| 协作 | Pull Request、Code Review | Collaboration机制 |
| 版本控制 | Git commit history | Versioning，变化可追踪、失败可回滚 |
| 依赖管理 | package.json、requirements.txt | Dependency Management |
| 质量保证 | CI/CD、单元测试 | Quality Management |
| 安全 | 安全扫描、权限控制 | Security & Posture Management |
| 作用域 | 全局变量 vs 局部变量 | Global Context vs Local Context |

## 角色体系

像代码仓库一样，Context管理需要明确的角色分工：

- **Approver**：审批Context变更
- **Maintainer**：维护Context质量
- **Contributor**：贡献Context内容

## 与Context Layer的关系

GitHub for Context 是 [[Context Layer]] 的设计哲学。Context Layer不仅是技术系统，更是一套管理流程——让人和AI共同维护企业知识的质量、版本和安全。

## 核心问题

- Context的profile长什么样？
- 能否有baked-in的自学习循环？
- 质量管理如何做？
- 安全态势如何管理？
- "这个东西影响所有其他东西"的依赖关系如何追踪？

## 关联

- 相关概念：[[Context Layer]]、[[Company Brain]]、[[Git]]、[[版本控制]]、[[Code Review]]
- 来源：[[2026-08-01-生产级Agent缺的不是PromptContext]]
