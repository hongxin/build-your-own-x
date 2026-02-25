---
name: z-evolve
description: Use when completing work, reviewing code quality, extracting reusable patterns, or writing skills - refinement and knowledge crystallization
---

# z-evolve — 化·金

> 「日新其德」— 金之道，百炼成钢，去粗存精。登山则情满于山。

## 三化路径

### 淬化 — Code Review
代码审查，去除杂质。
- 检查：命名清晰？职责单一？安全无漏洞？
- 关注业务逻辑正确性，而非格式琐事
- 调用 `superpowers:requesting-code-review` 进行结构化审查

### 结化 — Integration
合并收官，归于主干。
- 确认所有测试通过（z-verify 已完成）
- 清理临时代码、调试日志
- 撰写清晰的 commit message / PR description
- 调用 `superpowers:finishing-a-development-branch` 完成收官

### 升化 — Knowledge Capture
提炼经验为可复用知识。
- 发现的模式值得记录？→ 更新 memory
- 流程值得固化？→ 写新 skill
- 调用 `superpowers:writing-skills` 进行 skill 创作

## 文心雕龙写作原则（用于 skill/文档写作）

| 原则 | 含义 | 实践 |
|------|------|------|
| **风骨** | 主旨鲜明 | 每个 skill 开头一句话说清目的 |
| **通变** | 借鉴不拘泥 | 参考已有 skill 但适应新场景 |
| **练字** | 字字有用 | 无一虚设，token 效率优先 |

## 进化判断

**何时淬化：** 代码可工作但不够干净
**何时结化：** 代码干净且验证通过，准备合并
**何时升化：** 本次工作产生了可复用的洞察

**三化可并行，但至少做淬化和结化。升化视情况而定。**

## 相生流转

**金生水**：本轮完成 → 自然流入 `z-observe`（观·水），开启新一轮循环。

## 相克提示

**火克金**：理论须经实践检验。别空谈——如果总结的模式未经验证，回到 z-build 去证明。

**Cross-ref:** `superpowers:writing-skills`, `superpowers:finishing-a-development-branch`, `superpowers:requesting-code-review`
