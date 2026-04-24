---
title: VehicleType
description: 消防车辆类型字典 - 水罐、举高、抢险、防化等
category: entities
tags: [vehicle-type, fire-vehicle, resource]
sources: ["01_Projects/FireDispatchEngine/05_DataModel/07_Vehicle_And_Resource_Model.md"]
updated: 2026-04-24
summary: VehicleType是消防车辆类型字典实体，定义水罐、举高、抢险、防化等各类消防车辆。
provenance:
  extracted: 0.8
  inferred: 0.2
  ambiguous: 0.0
---

# VehicleType（车辆类型）

**VehicleType** 是消防车辆类型字典实体，定义各类消防车辆。

## 常见车辆类型

| 类型 | 用途 | 典型场景 |
|------|------|----------|
| 水罐消防车 | 主战供水 | 普通火灾 |
| 举高消防车 | 高空作业 | 高层火灾 |
| 抢险救援车 | 破拆、救人 | 交通事故、救援 |
| 防化消防车 | 化学泄漏 | 危化品事故 |
| 泡沫消防车 | 油类火灾 | 化工火灾 |
| 云计算消防车 | 通信指挥 | 大型灾害 |

## 相关页面

- [[FireDispatchEngine]]
- [[DispatchPlan]]
- [[约束校验]]
