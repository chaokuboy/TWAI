---
title: FireDispatchEngine
description: 智能消防调派引擎 - 基于DIKW架构的数据驱动闭环系统
category: projects
tags: [fire-dispatch, dispatch-engine, DIKW, multi-agent, N_total]
sources: ["01_Projects/FireDispatchEngine/index.md"]
updated: 2026-04-24
summary: 消防调派引擎是接处警7.0系统的核心指挥大脑，实现"事件画像→N_total计算→自动定级→编成生成→约束校验→人工确认"的全流程数据驱动闭环。
provenance:
  extracted: 0.7
  inferred: 0.2
  ambiguous: 0.1
---

# FireDispatchEngine

**消防智能调派引擎**是接处警7.0系统的核心指挥大脑，基于「干净数据 + 小认知核心 + 外部记忆」架构，实现从119报警到精准调派、实时指挥、事后学习的全闭环。

## 核心定位

传统模式：先定级后派车（经验驱动）→ **新模式**：事件画像 → N_total → 自动定级 → 编成生成 → 约束校验 → 定级反向验证 → 人工确认（数据驱动）

## 核心原则

| 原则 | 说明 |
|------|------|
| 数据驱动 | 所有决策基于事件画像 + 10大子场景 |
| 闭环治理 | 正向计算 + 定级反向验证 + 战评反馈 |
| 人工最终负责 | 系统主导计算，关键节点强制人工确认 |
| 可配置可扩展 | 规则、系数、子场景均支持后台热更新 |

## 核心公式

**N_total** = N_base + α_sub + β_struct + G_special + M_support + Δ_confidence + Δ_scene

N_total代表战术力量需求总量，用于确定出动等级和车辆编成。

## 架构流程

```
接警 → 画像生成 → N_total计算 → 定级映射 → 反向验证 → 出动方案 → 战评
```

## 五大核心目标

1. **精准匹配战术需求** - N_total准确率 ≥ 95%
2. **实战可行性保障** - 实际到场率 ≥ 95%（三层约束校验）
3. **数据定力闭环** - 定级反向验证通过率 ≥ 98%
4. **责任清晰可追溯** - 人工确认节点覆盖率 100%
5. **高效资源利用** - 资源利用率85-95%，冗余<15%

## 目录结构

- [[01_Requirements]] - 需求、子场景画像、计算模型、业务规则
- [[02_Scenarios]] - 全链路场景模拟与典型案例
- [[03_SystemDesign]] - 多智能体架构、状态机、数据流
- [[04_DIKW_Examples]] - 普通/危化/救援类 DIKW 转化模板
- [[05_DataModel]] - 核心实体、ER图、数据库结构
- [[06_DispatchEngine]] - 调派引擎核心逻辑（定级、路由、约束）
- [[07_TimeAxis_Roadmap]] - 时间轴与开发路线图
- [[08_Simulation_Data]] - 模拟、审计、责任机制
- [[09_Appendix]] - 公式、参考、附录

## 相关项目

- [[SecondBrain_Agent]] - 通用底层框架，本项目的验证实例

## 负责人

yong | 最后更新：2026-04-24 | 版本：v1.0
