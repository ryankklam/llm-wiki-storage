---
type: concept
created: 2026-05-31
tags: [Palantir, Ontology, 开发框架, SDK]
---

# OSDK

> Ontology 定义的对象、属性、链接、动作，全都在 SDK 里自动生成类型安全的接口。

## 定义

OSDK（Ontology SDK）是 Palantir 的开发框架，让 FDE 能用已建模的 Ontology API 直接开发应用。支持 TypeScript、Python、Java。

## 核心特点

### 类型安全的接口
Ontology 里定义好的：
- 对象（Object Type）
- 属性（Property）
- 链接（Link Type）
- 动作（Action Type）

全都在 SDK 里自动生成类型安全的接口。

### 代码提示
FDE 不需要从零学习企业的数据结构和命名规则：
- 打开编辑器，所有对象都在代码提示里
- 只需要想清楚场景需要哪些对象、需要做什么操作

### 快速开发
这就是为什么 FDE 第一周就在调业务流程，而不是还在对字段名。

## 工作流程

1. Ontology 建模完成 → 对象、属性、链接、动作已定义
2. OSDK 自动生成类型安全的接口
3. FDE 在编辑器里用 Ontology API 开发
4. 极短时间内做出能用的应用

## 与传统开发的区别

| 传统开发 | OSDK 开发 |
|---------|----------|
| 从零学习数据结构和命名规则 | 所有对象在代码提示里 |
| 前三个月在对字段名 | 第一周在调业务流程 |
| 手动对接各种数据源 | Ontology 自动吸附数据 |

## 相关来源
- [[2026-05-31-FDE脚下的地基Ontology]]

## 相关概念
- [[Ontology]] - Palantir 的语义建模层
- [[FDE]] - Forward Deployed Engineer
- [[Palantir]] - 美国大数据分析公司