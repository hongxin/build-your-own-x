---
name: z-verify
description: Use when work appears complete, when debugging issues, or before claiming any success - diagnostic verification using evidence not confidence
---

# z-verify — 验·土

> 「格物致知」— 土为万物之验。不经大地承载的，皆是浮云。

## 望闻问切四诊法

### 望 Look — 观其表象
- 读错误信息全文（不要只看第一行）
- 查日志输出、控制台警告
- 看 diff：改了什么，遗漏了什么
- **工具**：`Read`, `Bash`（运行命令看输出）

### 闻 Listen — 闻其声息
- 听用户描述：关注"本来应该"和"实际发生"的差异
- 查社区讨论：相同错误是否有已知解法
- 看 CI/CD 输出：自动化工具怎么说
- **工具**：`WebSearch`, `Grep`

### 问 Ask — 问其病史
- 最近改了什么？（git log/diff）
- 环境差异？（版本、配置、OS）
- 能否稳定复现？条件是什么？
- **工具**：`Bash`（git log）, `AskUserQuestion`

### 切 Feel — 切其脉象
- 追踪数据流：输入→处理→输出每步的实际值
- 二分排查：哪一步开始出错？
- 加断点/日志：确认假设而非猜测
- **工具**：`Bash`（运行测试）, `Read`（检查状态）

## 验证铁律

<EXTREMELY-IMPORTANT>
证据先于断言，始终如此。

1. 运行命令 → 2. 阅读输出 → 3. 然后才能宣称结果

绝不说"应该可以了"——运行验证，展示证据。
</EXTREMELY-IMPORTANT>

## 验证清单

- [ ] 所有新增/修改的测试通过
- [ ] 没有引入新的 lint 警告
- [ ] 边界条件已覆盖
- [ ] 手动运行确认核心路径正常
- [ ] git diff 审查：无遗留调试代码

## 相生流转

**土生金**：验证通过 → 自然流入 `z-evolve`（化·金）进行提炼收官。

## 相克提示

**木克土**：设计约束了验证范围。不要漫无目的测试，回到设计文档确认验证边界。

**Cross-ref:** `superpowers:systematic-debugging`, `superpowers:verification-before-completion`
