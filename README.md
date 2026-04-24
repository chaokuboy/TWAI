# TWAI - TeleWave.ai 知识库

**telewave.ai** 的个人/团队知识管理系统，基于 Obsidian + 第二大脑方法论构建。

---

## 核心架构

```
用户输入 → 小认知核心 → 外部记忆检索 → 智能路由 → 输出/行动
                     ↑
                  反馈学习
```

## 核心方法论

- **[[DIKW]]** - Data → Information → Knowledge → Wisdom 层级转化模型
- **[[PARA_System]]** - Projects/Areas/Resources/Archives 知识分类法
- **[[MOC]]** - Maps of Content 内容地图导航

---

## 目录结构

### 01_Projects - 当前项目

有明确目标、正在进行的工作：

| 项目 | 说明 |
|------|------|
| **FireDispatchEngine** | 智能消防调派引擎 - 基于DIKW架构的119报警全闭环系统 |
| **SecondBrain_Agent** | 个人/团队Agent系统 - 小认知核心+外部记忆+智能路由 |

### 02_Areas - 长期领域

需持续投入精力维护的能力范围：

| 领域 | 说明 |
|------|------|
| **KnowledgeManagement** | 第二大脑方法论、DIKW、PARA、状态机 |
| **Emergency_Response** | 消防、应急、救援领域专业知识 |

### 03_Resources - 参考资源

可复用、基础性、长期有效的知识和模板：

| 资源 | 说明 |
|------|------|
| **Firefighting_Knowledge** | 消防专业知识、火灾预测模型、子场景分类 |
| **Templates** | DIKW模板、调派JSON模板、状态机模板 |

### 04_Archives - 归档

已完成或废弃的内容，保留参考价值。

### 05_ExternalMemory_Index - 外部记忆索引

整个第二大脑的「可检索外部记忆」核心：

- `FireDispatch_Tags/` - 消防调派专用向量标签
- `DIKW_Tags/` - DIKW层级标签体系
- `KnowledgeGraph/` - 实体-关系图谱
- `VectorTags/` - 通用向量检索标签

### 99_MOC - 内容地图导航

核心模块的总导航页：

- `FireDispatch_MOC` - 消防调派引擎总导航
- `DIKW_MOC` - 知识管理方法论总导航
- `Agent_Dispatch_MOC` - Agent调度总导航

---

## 核心概念

- **[[小认知核心]]** - 轻量级认知处理单元，负责接收报警信息、提取关键槽位
- **[[外部记忆]]** - 向量检索 + 知识图谱索引的混合记忆系统
- **[[N_total]]** - 战术力量需求总量计算公式
- **[[警情定级]]** - 基于N_total的1-5级分类体系
- **[[火灾子场景]]** - 覆盖95%+火警的10大分类

---

## 快速导航

- [[FireDispatch_MOC]] - 消防调派引擎完整导航
- [[DIKW_MOC]] - 知识管理方法论导航
- [[火灾子场景分类]] - 10大火灾场景速查

---

## 版本信息

- **最后更新**：2026-04-24
- **Obsidian Vault**
- **托管**：GitHub (Obsidian Git 插件)
