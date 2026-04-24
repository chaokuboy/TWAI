---
title: Workflow_StateMachine
description: 知识工作流状态机
category: concepts
tags: [workflow, state-machine, knowledge-management]
sources: ["02_Areas/KnowledgeManagement/Workflow_StateMachine.md"]
updated: 2026-04-24
summary: 知识工作流状态机定义知识从捕获到归档的完整生命周期。
provenance:
  extracted: 0.8
  inferred: 0.2
  ambiguous: 0.0
---

# Workflow_StateMachine

**知识工作流状态机**定义知识从捕获到归档的完整生命周期。

## 状态流转

```
Capture → Process → Organize → Review → Output → Archive
```

## 各状态说明

| 状态 | 说明 | 产出 |
|------|------|------|
| **Capture** | 接收原始输入（报警、文档、想法） | 原始Data |
| **Process** | 清洗、结构化、质量评分 | 干净Data |
| **Organize** | 按PARA分类，关联现有知识 | 信息卡片 |
| **Review** | 复盘、更新、补充链接 | 更新内容 |
| **Output** | 生成调派令/文档/报告 | 可执行产出 |
| **Archive** | 归档或转入外部记忆 | 归档存储 |

## DIKW中的位置

在 [[DIKW_Framework]] 的8步闭环中，Workflow_StateMachine 对应：
- Capture → CleanData → RetrieveMemory → ReasonPlan → DecisionPoint → **Synthesize** → Express → UpdateMemory

## 相关页面

- [[PARA_System]]
- [[DIKW_Framework]]
- [[SecondBrain_Agent]]
