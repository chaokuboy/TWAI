---
title: N_total
description: 战术力量需求总量计算公式
category: concepts
tags: [N_total, dispatch-scale, calculation-model]
sources: ["01_Projects/FireDispatchEngine/01_Requirements/01_Dispatch_Scale_Calculation_Model.md"]
updated: 2026-04-24
summary: N_total是调派规模计算的核心公式，计算警情所需的最小作战单元数量（以"车"为单位），用于确定出动等级和车辆编成。
provenance:
  extracted: 0.9
  inferred: 0.1
  ambiguous: 0.0
---

# N_total

**N_total** 是 [[FireDispatchEngine]] 调派规模计算的核心公式，代表一次警情所需的**最小作战单元数量**（以"车"为单位）。

## 完整公式

$$N_{\text{total}} = N_{\text{base}} + \alpha_{\text{sub}} + \beta_{\text{struct}} + G_{\text{special}} + M_{\text{support}} + \Delta_{\text{confidence}} + \Delta_{\text{scene}}$$

## 分项说明

| 分项 | 含义 | 计算依据 | 权重 |
|------|------|----------|------|
| **N_base** | 基础力量 | 子场景卡片默认值 | 基础 |
| **α_sub** | 物质修正 | 能量物质类型 + 荷载 | 最高 |
| **β_struct** | 结构修正 | 建筑高度 + 结构类型 | 高 |
| **G_special** | 特种模块 | 特殊画像触发 | 中 |
| **M_support** | 保障模块 | 发展阶段 + 预计作战时长 | 低 |
| **Δ_confidence** | 置信度修正 | 核心槽位平均置信度（<75%时触发） | 动态 |
| **Δ_scene** | 子场景专用修正 | 10大子场景预设 | 动态 |

## N_total 与警情等级映射

| N_total 范围 | 警情等级 | 典型场景 |
|---|---|---|
| 1~4 车 | 一级 | 普通住宅火灾 |
| 5~8 车 | 二级 | 地下车库初期 |
| 9~12 车 | 三级 | 高层85m火灾 |
| 13~18 车 | 四级 | 化工园区火灾 |
| 19车及以上 | 五级 | 大面积灾害 |

## 10大子场景参考值

| 子场景 | N_base | N_total范围 | 映射等级 |
|--------|--------|-------------|----------|
| 普通住宅火灾 | 2 | 2-4 | 一级 |
| 高层住宅火灾 | 4 | 8-12 | 三级 |
| 地下车库火灾 | 3 | 7-10 | 二~三级 |
| 化工/危化品园区 | 5 | 13-20 | 四级 |
| 锂电池火灾 | 4 | 10-15 | 三~四级 |

## 计算流程

```
接警 → 事件画像 → 匹配场景卡片 → N_base → α_sub → β_struct → G_special → M_support → Δ_confidence → Δ_scene → N_total → 查表定级
```

## 相关页面

- [[FireDispatchEngine]]
- [[DIKW]]
- [[事件画像]]
- [[警情定级]]
- [[约束校验]]
