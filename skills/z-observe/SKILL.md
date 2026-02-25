---
name: z-observe
description: Use when entering unfamiliar codebase, starting new task, or needing to build context before acting - exploration and discovery phase
---

# z-observe — 观·水

> 「知止而后有定」— 水无常形，因地制流。探索方法应适应项目地形。

## 三层探索法

### 1. 鸟瞰 — 全局结构
- `Glob` + `ls` → 目录结构、文件类型分布
- 识别：README、配置文件、入口点、测试目录
- **目标**：30秒内形成项目心智地图

### 2. 走径 — 关键路径
- `Grep` + `Read` → 核心模块、API入口、数据模型
- 追踪：import链、调用关系、配置流向
- **目标**：找到任务相关的3-5个关键文件

### 3. 潜渊 — 深度理解
- `Explore Agent` → 跨文件语义理解、架构模式识别
- 仅在前两层不足以理解时使用
- **目标**：能清晰描述组件关系和数据流

## 止观法则

**何时停止探索（止）：**
- 能用一句话描述任务边界
- 已识别要修改的文件和函数
- 已知道现有的测试覆盖情况
- 已发现可能的风险点

**探索过度的信号：**
- 已读了 >10 个与任务无关的文件
- 在"了解更多背景"中循环
- 开始关注非任务区域的代码质量

## 禹步量地（山海经）

对于大型未知项目，采用禹步法——三步定位：
1. **步一**：找到项目的"心脏"（主入口/核心模块）
2. **步二**：找到与任务相关的"经脉"（调用链）
3. **步三**：找到变更的"穴位"（具体修改点）

## 相生流转

**水生木**：探索完成后，上下文充足 → 自然流入 `z-design`（谋·木）进行规划。

## 相克提示

**土克水**：若已有充分验证数据/经验，无需再探索。证据终止探索。

**Cross-ref:** Explore agents for parallel exploration, `superpowers:brainstorming` for intent clarification.
