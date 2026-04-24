---
title: DIKW
description: Data-Information-Knowledge-Wisdom 层级转化模型
category: concepts
tags: [DIKW, knowledge-management, data-driven]
sources: ["01_Projects/FireDispatchEngine/04_DIKW_Examples/_README.md"]
updated: 2026-04-24
summary: DIKW是Data到Information到Knowledge到Wisdom的层级转化模型，是消防调派引擎的核心知识处理范式。
provenance:
  extracted: 0.8
  inferred: 0.2
  ambiguous: 0.0
---

# DIKW

**DIKW** (Data → Information → Knowledge → Wisdom) 是信息处理的层级转化模型，是 FireDispatchEngine 调派引擎的核心知识处理范式。

## DIKW 层级

| 层级 | 输入 | 输出 | 示例（消防场景） |
|------|------|------|-----------------|
| **D** Data | 原始报警描述 | 未经处理的感知数据 | "对面楼冒烟了" |
| **I** Information | 结构化槽位信息 | 事件画像（时间、地点、类型） | 时间=19:32，地点=XX小区XX栋，类型=火灾 |
| **K** Knowledge | 规则/公式/N_total计算 | 可行动的决策依据 | N_total=8，查表得二级警 |
| **W** Wisdom | 超越规则的智慧决策 | 复杂情境的临场判断 | 历史案例类比、多部门协同 |

## 消防场景DIKW转化

在 [[FireDispatchEngine]] 中，DIKW 转化模板用于：
- 普通火灾 (`01_Ordinary_Fire_DIKW`)
- 危化火灾 (`02_Hazmat_Fire_DIKW`)
- 救援类 (`03_Rescue_DIKW`)

## DIKW 与小认知核心

DIKW 模板是小认知核心最重要的知识来源，用于：
- AI 训练样本
- 规则说明示例
- 新人培训材料

## 相关页面

- [[FireDispatchEngine]]
- [[N_total]]
- [[事件画像]]
- [[SecondBrain_Agent]] - 通用底层框架
