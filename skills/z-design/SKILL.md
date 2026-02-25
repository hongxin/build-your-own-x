---
name: z-design
description: Use when you have enough context to plan implementation - brainstorming approaches, writing plans, making architecture decisions
---

# z-design — 谋·木

> 「谋定而后动」— 木向阳而生，有枝有干。方案应有清晰主干和合理分支。

## 五德评估法（素书）

对每个方案快速过五德：

| 德 | 问题 | 权重 |
|----|------|------|
| **道**（深度） | 是否触及问题本质？ | 必须 |
| **德**（质量） | 代码是否可维护？ | 必须 |
| **仁**（体验） | 使用者是否便利？ | 重要 |
| **义**（正确） | 逻辑是否严密？ | 必须 |
| **礼**（规范） | 是否遵循已有约定？ | 重要 |

**五德全满不可能也不必要。道·德·义三者为必须，仁·礼可权衡。**

## 设计流程

### 1. 发散 — brainstorming
- 列出 2-4 个可行方案（不少于2个）
- 用五德评估法快速打分
- 调用 `superpowers:brainstorming` 进行意图澄清

### 2. 收敛 — 方案选择
- 选择五德综合最优的方案
- 记录被否方案的原因（防止重蹈覆辙）
- 识别关键风险和回滚策略

### 3. 成文 — writing-plans
- 拆分为渐进式步骤（Build-Your-Own-X 理念）
- 每步 2-5 分钟可完成
- 每步有明确的验证标准
- 调用 `superpowers:writing-plans` 输出实施计划

## 渐进式拆分原则（Build-Your-Own-X）

- **大任务 → 小步骤**：每步足够小到不会迷路
- **每步有产出**：可编译、可运行、可测试
- **难度曲线控制**：保持在心流区间（不太简单、不太复杂）

## 相生流转

**木生火**：计划就绪 → 自然流入 `z-build`（行·火）开始实施。

## 相克提示

**金克木**：经验丰富时（z-evolve 已有积累），可简化或跳过规划。别过度设计简单任务。

**Cross-ref:** `superpowers:brainstorming`, `superpowers:writing-plans`
