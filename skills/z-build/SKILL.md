---
name: z-build
description: Use when ready to implement - writing code with TDD discipline, progressive building from simple to complex, immediate feedback loops
---

# z-build — 行·火

> 「道常无为而无不为」— 火之道，不疾不徐，渐燃渐明。

## TDD 铁律（火之三相）

### 点火 RED — 先写测试
写一个会失败的测试——无火种不生焰。
- 测试描述期望行为，不是实现细节
- 运行测试，确认它**确实**失败了

### 燃烧 GREEN — 最少代码通过
写最少的代码使测试通过——火只燃其所需。
- 不写测试未要求的功能
- 不提前优化，不提前抽象

### 淬炼 REFACTOR — 清理代码
测试通过后清理——火后铸器。
- 消除重复，提取清晰命名
- 再次运行测试确认不破坏

**循环：RED → GREEN → REFACTOR → RED → …**

## 渐进式构建原则（Build-Your-Own-X）

```
第1步：最简可运行版本（骨架）
  ↓ 验证通过
第2步：添加核心功能（肌肉）
  ↓ 验证通过
第3步：处理边界情况（皮肤）
  ↓ 验证通过
第4步：优化和美化（衣服）
```

- **每步 30-90 分钟可完成**
- **每步有 git commit**（可回滚的检查点）
- **每步有可见产出**（能运行、能演示）

## 执行模式

| 模式 | 适用场景 | 工具 |
|------|---------|------|
| 本地构建 | 单文件/小改动 | 直接 Edit/Write |
| 子代理构建 | 多独立任务 | `superpowers:subagent-driven-development` |
| 计划执行 | 跨会话大任务 | `superpowers:executing-plans` |

## 编码纪律

- 写代码前确认测试策略
- 每个函数做一件事（单一职责）
- 命名即文档，复杂处加注释
- 不引入 OWASP Top 10 漏洞

## 相生流转

**火生土**：代码实现完成 → 自然流入 `z-verify`（验·土）进行全面验证。

## 相克提示

**水克火**：若调研不足（z-observe 未充分），回到探索。水灭火，方向不明时不要蛮干。

**Cross-ref:** `superpowers:test-driven-development`, `superpowers:subagent-driven-development`
