# Build Your Own X：造物即修行

**[English](README_EN.md)** | 中文

> "What I cannot create, I do not understand." — Richard Feynman

受 [build-your-own-x](https://github.com/codecrafters-io/build-your-own-x) 启发，从零开始亲手构建各种有趣的小项目——用造物理解原理。每个项目都是独立的单文件 HTML 应用，零依赖，浏览器直接打开即可运行。

**在线体验** → [hongxin.github.io/build-your-own-x](https://hongxin.github.io/build-your-own-x/)

## 项目展示

| 项目 | 简介 | 关键技术 |
|------|------|---------|
| [Tetris](projects/tetris.html) | 网页版俄罗斯方块，支持人类/AI 实时切换，音效粒子特效，触屏适配 | Canvas · Web Audio API · AI 评估算法 · Touch Events |
| [Weather Clock](projects/braun-weather-clock.html) | 伯朗(Braun)设计风格的天气时钟，实时天气 + 三日预报，明暗双主题 | Open-Meteo API · Geolocation · CSS Variables |
| [Raycaster Maze](projects/raycaster-maze.html) | 第一人称视角光线投射迷宫，Wolfenstein 3D 风格实时渲染 | Canvas 2D · Raycasting · DDA 算法 |
| [Taiji Bagua](projects/taiji-bagua.html) | 太极八卦技术映射交互可视化，五德雷达图 | SVG · 交互动画 · 数据驱动 |
| [Data Dashboard](projects/visualization.html) | Build-Your-Own-X 生态全景数据大屏 | ECharts · 暗色主题 · 多维图表 |

## 项目结构

```
build-your-own-x/
├── index.html                       # 项目画廊着陆页
├── projects/                        # 交互式项目
│   ├── tetris.html                  # 俄罗斯方块（人类/AI 双模式）
│   ├── braun-weather-clock.html     # 伯朗风格天气时钟
│   ├── raycaster-maze.html          # 光线投射迷宫
│   ├── taiji-bagua.html             # 太极八卦交互可视化
│   └── visualization.html           # ECharts 数据大屏
├── skills/                          # ZPower 五行技能系统
│   ├── README.md                    # 技能系统文档
│   ├── zpower/                      # 元技能：五行总纲
│   ├── z-observe/                   # 水·观：探索与发现
│   ├── z-design/                    # 木·谋：规划与设计
│   ├── z-build/                     # 火·行：构建与实现
│   ├── z-verify/                    # 土·验：验证与诊断
│   └── z-evolve/                    # 金·化：进化与收官
├── data/                            # 共享数据
│   └── skill-tree-data.json         # 结构化数据（八卦 + 五德 + 学习路径）
└── docs/                            # 研究文档
    ├── research-report.md           # 深度研究报告 v1
    └── research-report-v2.md        # 深度研究报告 v2
```

## ZPower 五行技能系统

一套为 Claude Code 设计的 AI 辅助开发框架，将五行哲学映射到软件开发工作流：

```
观(水) → 谋(木) → 行(火) → 验(土) → 化(金) → 循环
```

| 五行 | 技能 | 用于 |
|------|------|------|
| 水·观 | z-observe | 探索未知代码，建立全局认知 |
| 木·谋 | z-design | 头脑风暴，设计方案 |
| 火·行 | z-build | TDD 驱动，渐进式构建 |
| 土·验 | z-verify | 望闻问切，证据先于断言 |
| 金·化 | z-evolve | 代码审查，知识萃取 |

详细文档和安装说明见 [skills/README.md](skills/README.md)。

## 设计理念

每个项目遵循三个原则：

- **单文件完整** — 一个 HTML 文件包含全部代码，无需构建工具、无需安装依赖
- **零配置运行** — 浏览器打开即用，不依赖服务端
- **学以致用** — 每个项目都是对某个技术领域的实践探索

## 研究：八卦映射技术版图

对 build-your-own-x 仓库（469K+ stars）进行深度分析，以《周易》八卦映射 **590+ 篇教程、31 个技术类别、37+ 种编程语言** 的造物生态。

### 八卦映射

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

### 六条修炼路径

| 路径 | 方向 | 进阶顺序 |
|------|------|---------|
| 天路 | 语言创造者 | Regex → Template → Programming Language → VM |
| 地路 | 系统架构师 | Memory → Shell → OS → Docker |
| 水路 | 网络工程师 | Network Stack → Web Server → Browser → Distributed |
| 火路 | 创意全栈 | Frontend → 3D Rendering → Game → Physics |
| 山路 | 数据守护者 | Git → Database → Blockchain → Search Engine |
| 智路 | AI 实践者 | Neural Network → Vision → AI Model → Bot |

完整分析见 [深度研究报告](docs/research-report-v2.md)。

## 快速开始

```bash
# 克隆仓库
git clone https://github.com/hongxin/build-your-own-x.git

# 用浏览器打开着陆页
open build-your-own-x/index.html
```

或直接访问 [在线版本](https://hongxin.github.io/build-your-own-x/)。

---

> *"再，斯可矣。"* — 思考够了，就去造吧。
