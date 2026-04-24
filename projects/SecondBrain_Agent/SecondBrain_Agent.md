---
title: SecondBrain_Agent
description: 个人/团队Agent系统 - 小认知核心+外部记忆+智能路由
category: projects
tags: [agent, memory, routing, fine-tune, SecondBrain]
sources: ["01_Projects/SecondBrain_Agent/index.md"]
updated: 2026-04-24
summary: 将第二大脑升级为具备小认知核心、外部记忆、智能路由的个人/团队Agent系统，实现知识自动转化与高效应用。
provenance:
  extracted: 0.8
  inferred: 0.2
  ambiguous: 0.0
---

# SecondBrain_Agent

**项目目标**：将第二大脑升级为具备「小认知核心 + 外部记忆 + 智能路由」的个人/团队 Agent 系统，实现知识自动转化与高效应用。

## 核心架构

```
用户输入 → 小认知核心 → 外部记忆检索 → 智能路由 → 输出/行动
                     ↑
                  反馈学习
```

## 主要模块

| 模块 | 说明 |
|------|------|
| 状态机设计 | 知识工作流自动化 |
| Agent路由逻辑 | 智能分发与调度 |
| 小认知核心fine-tune | 轻量模型优化 |
| 外部记忆 | 向量检索标签 + 知识图谱索引 |

## 与FireDispatchEngine的关系

作为通用底层框架，先在消防场景（[[FireDispatchEngine]]）验证，再泛化。

## 负责人

yong | 最后更新：2026-04-24
