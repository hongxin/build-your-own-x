# 流程图生成方案实验报告

> 实验日期：2026-03-08
> 实验目标：评估配合 Claude Code 的系统流程图生成方案

## 实验背景

为 ZPower 五行技能系统的 README 生成原理图，需要呈现五行相生（环形流转）和相克（交叉连线）两层关系——这是一个典型的"环形拓扑 + 交叉关系"图。

## 评估方案

### 方案 A：Mermaid.js（自动布局）

**工具链：** `claude-mermaid` MCP Server（已全局安装），内置 `mmdc` CLI

**流程：**
1. Claude 直接生成 `.mmd` 文件（Mermaid 语法）
2. `mmdc -i input.mmd -o output.svg/png`

**结果：**
- 五行节点被展开为纵向瀑布流（树形布局）
- 相生的"循环"语义丢失——看不出是一个环
- 相克虚线与相生实线交叉混乱
- 配色自定义（`classDef`）效果不错
- 中文渲染完整无问题

**评价：** 适合线性/树形流程，不适合环形拓扑。

### 方案 B：D2（自动布局）

**工具链：** D2 v0.7.1 单二进制，部署于 `~/.local/bin/d2`

**流程：**
1. Claude 生成 `.d2` 文件
2. `d2 --sketch --layout elk input.d2 output.png`

**结果：**
- dagre 和 elk 两个免费引擎均将五节点铺成极宽横条（24000+ px）
- sketch 模式有手绘感，视觉风格独特
- Markdown 节点内容渲染美观
- 但环形拓扑完全无法表达——和 Mermaid 一样的根本问题
- TALA 引擎（付费）可能改善，但未测试
- 中文 Markdown 有截断问题

**评价：** 层次架构图优秀，环形拓扑力不从心。

### 方案 C：Excalidraw 风格 SVG（手动坐标布局）

**工具链：** 手写 HTML+SVG → Python Playwright 截图为 PNG

**流程：**
1. Claude 生成包含 SVG 的 HTML 文件
2. 手动控制五角形顶点坐标布局
3. Playwright 截图 → PNG
4. 可选：浏览器打开 HTML 导出 SVG/PNG

**结果：**
- 五角环形布局完美呈现五行相生循环
- 相生（实线粗箭头，元素色）与相克（红色虚线穿越内部）视觉区分清晰
- 手绘滤镜（feTurbulence + feDisplacementMap）增加辨识度
- 中心区域放相克说明卡片，信息层次分明
- 中英文版本均效果良好

**评价：** 需要精确布局控制的概念图的最佳方案。

## 对比评分

| 维度 | Mermaid | D2 | Excalidraw-SVG |
|------|:-------:|:--:|:--------------:|
| 布局契合度（五行环形） | 3/10 | 2/10 | **9/10** |
| 视觉美感 | 6/10 | 7/10 | **9/10** |
| 信息完整性 | 8/10 | 6/10 | **9/10** |
| LLM 生成便利性 | **10/10** | 7/10 | 5/10 |
| 可维护性 | **9/10** | 8/10 | 4/10 |
| 嵌入便利性（GitHub） | **10/10** | 7/10 | 6/10 |

## 关键发现

### 1. 自动布局引擎的根本局限

Mermaid（dagre）和 D2（dagre/elk）的布局引擎本质是为 **DAG（有向无环图）** 设计的。遇到五行这种"五节点全连通 + 环形"结构，它们只能：
- 把环展开为链条
- 把交叉连线绕成意大利面

这不是配置问题，而是算法局限。

### 2. "概念图"vs"流程图"需要不同策略

| 图类型 | 特征 | 最佳工具 |
|--------|------|---------|
| 线性流程 | 有向无环、层次清晰 | Mermaid / D2 |
| 环形拓扑 | 节点互联、循环关系 | 手动 SVG / Excalidraw |
| 云架构 | 分层、带图标 | Diagrams (Python) |
| UML 时序图 | 严格规范 | PlantUML |

### 3. LLM + SVG 的可行性

Claude 可以直接生成包含精确坐标的 SVG 代码，质量令人惊喜：
- 五角形顶点计算准确
- 贝塞尔曲线路径自然
- 颜色搭配协调
- 多语言文本布局合理

这意味着对于非标准布局的图表，**跳过 DSL 中间层，直接生成 SVG** 可能是最优路径。

### 4. 截图工具链

Python Playwright（`playwright.sync_api`）作为截图工具非常可靠：
- macOS 上已通过 conda 安装
- 支持 headless 渲染
- `page.locator('#canvas').screenshot()` 精准截取

## 工具安装备忘

```bash
# Mermaid CLI（已随 claude-mermaid 安装）
npm install -g claude-mermaid
# 渲染命令：
/path/to/node_modules/.bin/mmdc -i input.mmd -o output.png

# D2（绿色安装）
curl -fsSL https://github.com/terrastruct/d2/releases/latest/download/d2-vX.Y.Z-macos-arm64.tar.gz -o /tmp/d2.tar.gz
tar -xzf /tmp/d2.tar.gz -C /tmp/
cp /tmp/d2-vX.Y.Z/bin/d2 ~/.local/bin/d2

# Playwright（Python，用于截图）
# 已通过 conda 环境可用
python3 -c "from playwright.sync_api import sync_playwright; print('ok')"
```

## 产出物

| 文件 | 说明 |
|------|------|
| `skills/zpower-diagram.png` | 中文五行原理图（Excalidraw 风格） |
| `skills/zpower-diagram-en.png` | 英文五行原理图（Excalidraw 风格） |
| `skills/README.md` | 中文 README，嵌入中文图 |
| `skills/README_EN.md` | 英文 README，嵌入英文图 |

---

> *再，斯可矣。* — 实验够了，该沉淀成技能了。
