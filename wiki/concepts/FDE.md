---
type: concept
created: 2026-05-31
updated: 2026-05-31
sources: [2026-05-31-FDE脚下的地基Ontology]
---

# FDE（Foundry Data Engine）

## 定义

**FDE（Foundry Data Engine）** 是 Palantir Foundry 平台的核心数据引擎，基于 Ontology 构建数字孪生系统。

## 核心能力

| 能力 | 说明 |
|------|------|
| Ontology 管理 | 定义实体、属性、关系 |
| 数据集成 | 多源数据统一接入 |
| 数字孪生 | 现实世界的数字映射 |
| 实时同步 | 数据变更实时反映 |

## 与 Ontology 的关系

> Ontology 是 FDE 的地基，决定了数字孪生的表达能力。

FDE 的所有数据操作都基于 Ontology 定义的对象模型：
- 数据存储 → Ontology 实体
- 数据查询 → 图遍历 + 语义推理
- 数据更新 → Ontology Action

## 关联
- 相关概念：[[Ontology]]、[[Palantir]]、[[数字孪生]]
- 相关工具：[[OSDK]]