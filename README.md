# Build Your Own X：造物即修行

> "What I cannot create, I do not understand." — Richard Feynman

对 GitHub 上 **469K+ stars** 的 [build-your-own-x](https://github.com/codecrafters-io/build-your-own-x) 仓库进行深度研究，以《周易》八卦映射技术版图，用五德体系解析 **590+ 篇教程、31 个技术类别、37+ 种编程语言** 构成的造物生态。

## 项目结构

```
├── index.html                       # 项目画廊着陆页
├── projects/
│   ├── braun-weather-clock.html     # 伯朗风格天气时钟
│   ├── raycaster-maze.html          # 光线投射迷宫
│   ├── taiji-bagua.html             # 太极八卦交互可视化
│   └── visualization.html           # ECharts 数据大屏
├── data/
│   └── skill-tree-data.json         # 结构化数据（八卦 + 五德 + 学习路径）
└── docs/
    ├── research-report.md           # 深度研究报告 v1
    └── research-report-v2.md        # 深度研究报告 v2
```

## 核心框架

### 八卦映射 — 万物归于八象

将 31 个技术类别按本质属性映射到八卦体系：

| 卦象 | 领域 | 代表类别 | 教程数 |
|:---:|------|---------|:-----:|
| ☰ 乾·天·创生 | 规则定义 | Programming Language, Regex Engine | 50 |
| ☷ 坤·地·承载 | 系统基础 | Operating System, Docker, Shell | 31 |
| ☵ 坎·水·流通 | 网络连接 | Web Server, Network Stack, Browser | 45 |
| ☲ 离·火·显现 | 可见表达 | Game, 3D Renderer, Frontend Framework | 68 |
| ☳ 震·雷·驱动 | 自动行动 | Bot, Command-Line Tool, Task Scheduler | 30 |
| ☴ 巽·风·渗透 | 信息转化 | Search Engine, Text Editor, Template Engine | 36 |
| ☶ 艮·山·守护 | 数据持久 | Database, Blockchain, Git | 49 |
| ☱ 兑·泽·汇智 | 智慧涌现 | Neural Network, AI Model, Vision | 30 |

### 五德评分

每个八卦分组按**道/德/仁/义/礼**五个维度评分（10 分制），衡量技术深度、抽象层级、社区活跃度等特征。

### 六条修炼路径

| 路径 | 方向 | 进阶顺序 |
|------|------|---------|
| 天路 | 语言创造者 | Regex → Template → Programming Language → VM |
| 地路 | 系统架构师 | Memory → Shell → OS → Docker |
| 水路 | 网络工程师 | Network Stack → Web Server → Browser → Distributed |
| 火路 | 创意全栈 | Frontend → 3D Rendering → Game → Physics |
| 山路 | 数据守护者 | Git → Database → Blockchain → Search Engine |
| 智路 | AI 实践者 | Neural Network → Vision → AI Model → Bot |

## 数据洞察

**语言三极**：Python (88) + JavaScript (77) 构成应用阳极，C (67) + C++ (54) 构成系统阴极，Go (36) + Rust (26) 代表现代中极。

**幂律分布**：头部 5 类占总量 22%，Programming Language (41篇) 和 Game (34篇) 分别代表 "理解力的极限测试" 与 "创造力的终极表达"。

**趋势信号**：Rust 在系统编程和 WebAssembly 领域持续增长，Zig 作为新挑战者进入视野。

## 快速开始

打开 `index.html` 即可浏览所有项目。在线访问：[GitHub Pages](https://hongxin.github.io/build-your-own-x/)

## 方法论

- **数据来源**：`codecrafters-io/build-your-own-x` README.md（2026-02-25 获取）
- **映射原则**：基于技术类别的核心属性（底层/应用、静态/动态、面向机器/面向用户）归类，非机械对应
- **评分标准**：10 分制主观评分，基于领域教程的整体特征和技术要求

---

> *"再，斯可矣。"* — 思考够了，就去造吧。
