---
title: AlarmEvent
description: 警情事件 - 记录一次警情全生命周期
category: entities
tags: [alarm-event, incident, domain-entity]
sources: ["01_Projects/FireDispatchEngine/05_DataModel/01_Core_Entities_And_Domain_Model.md"]
updated: 2026-04-24
summary: AlarmEvent是消防调派系统的核心聚合根，记录一次警情的全生命周期数据。
provenance:
  extracted: 0.9
  inferred: 0.1
  ambiguous: 0.0
---

# AlarmEvent（警情事件）

**AlarmEvent** 是 [[FireDispatchEngine]] 调派系统的**核心聚合根**，记录一次警情全生命周期。

## 职责

- 包含 [[事件画像]]（EventPortrait）
- 关联 [[DispatchPlan]]（出动方案）
- 贯穿接警→定级→调派→战评全流程

## 相关实体

| 实体 | 关系 |
|------|------|
| EventPortrait | 包含 |
| AlarmLevel | 关联 |
| DispatchPlan | 包含 |
| AuditLog | 关联 |

## 相关页面

- [[FireDispatchEngine]]
- [[事件画像]]
- [[DispatchPlan]]
