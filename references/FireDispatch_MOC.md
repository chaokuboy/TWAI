---
title: FireDispatch_MOC
description: 消防调派引擎知识总导航
category: references
tags: [MOC, fire-dispatch, navigation, index]
sources: ["99_MOC/FireDispatch_MOC_v2026-04.md"]
updated: 2026-04-24
summary: FireDispatch_MOC是消防调派引擎的总导航页，串联01-09所有模块的核心知识。
provenance:
  extracted: 0.9
  inferred: 0.1
  ambiguous: 0.0
---

# FireDispatch_MOC

**FireDispatch_MOC** 是 [[FireDispatchEngine]] 消防调派引擎的**总导航页**，串联01-09所有模块。

## 快速入口

- [[01_Requirements]] —— 需求与规则
- [[04_DIKW_Examples]] —— DIKW示例
- [[06_DispatchEngine]] —— 调派引擎核心
- [[07_TimeAxis_Roadmap]] —— 开发路线图

## 核心概念

- [[小认知核心]] —— 接收报警，提取槽位
- [[外部记忆]] —— 向量检索+知识图谱
- [[DIKW]] —— Data→Information→Knowledge→Wisdom
- [[N_total]] —— 战术力量需求公式

## 三大场景

| 场景 | N_total范围 | 特点 |
|------|-------------|------|
| 普通火灾 | 4-8 | 常规编成，快速响应 |
| 危化火灾 | 10-20 | 特殊装备，防毒防爆 |
| 救援类 | 6-12 | 救援装备，分层梯次 |

## 状态机总览

```
接警登记 → 事件画像 → N_total计算 → 约束校验 → 调派方案 → 出动反馈
```

**目标**：首波力量 ≤ 8分钟到场

## 相关MOC

- [[DIKW_MOC]]
- [[Agent_Dispatch_MOC]]
