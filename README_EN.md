# Build Your Own X

English | **[中文](README.md)**

> "What I cannot create, I do not understand." — Richard Feynman

Inspired by [build-your-own-x](https://github.com/codecrafters-io/build-your-own-x), this is a collection of hands-on projects built from scratch — learning by building. Every project is a self-contained single-file HTML application with zero dependencies, ready to run in any browser.

**Live Demo** → [hongxin.github.io/build-your-own-x](https://hongxin.github.io/build-your-own-x/)

## Projects

| Project | Description | Key Technologies |
|---------|-------------|-----------------|
| [Tetris](projects/tetris.html) | Classic Tetris with real-time Human/AI mode switching, sound effects, particle animations, and mobile touch support | Canvas · Web Audio API · AI Evaluation · Touch Events |
| [Weather Clock](projects/braun-weather-clock.html) | Braun-inspired weather clock with real-time weather, 3-day forecast, and light/dark themes | Open-Meteo API · Geolocation · CSS Variables |
| [Raycaster Maze](projects/raycaster-maze.html) | First-person raycasting maze in the style of Wolfenstein 3D | Canvas 2D · Raycasting · DDA Algorithm |
| [Taiji Bagua](projects/taiji-bagua.html) | Interactive I Ching (Bagua) technology mapping visualization | SVG · Interactive Animation · Data-Driven |
| [Data Dashboard](projects/visualization.html) | Panoramic data dashboard of the Build-Your-Own-X ecosystem | ECharts · Dark Theme · Multi-dimensional Charts |

## Project Structure

```
build-your-own-x/
├── index.html                       # Project gallery landing page
├── projects/                        # Interactive projects
│   ├── tetris.html                  # Tetris (Human/AI dual mode)
│   ├── braun-weather-clock.html     # Braun-style weather clock
│   ├── raycaster-maze.html          # Raycasting maze
│   ├── taiji-bagua.html             # Taiji Bagua visualization
│   └── visualization.html           # ECharts data dashboard
├── skills/                          # ZPower Five Elements skill system
│   ├── README.md                    # Skill system documentation
│   ├── zpower/                      # Meta-skill: Five Elements overview
│   ├── z-observe/                   # Water · Observe: exploration & discovery
│   ├── z-design/                    # Wood · Design: planning & architecture
│   ├── z-build/                     # Fire · Build: implementation & TDD
│   ├── z-verify/                    # Earth · Verify: testing & diagnostics
│   └── z-evolve/                    # Metal · Evolve: refinement & review
├── data/                            # Shared data
│   └── skill-tree-data.json         # Structured data (Bagua + Five Virtues + Learning Paths)
└── docs/                            # Research documents
    ├── research-report.md           # Deep research report v1
    └── research-report-v2.md        # Deep research report v2
```

## ZPower Five Elements Skill System

An AI-assisted development framework designed for Claude Code, mapping the Chinese Five Elements philosophy to the software development workflow:

```
Observe(Water) → Design(Wood) → Build(Fire) → Verify(Earth) → Evolve(Metal) → cycle
```

| Element | Skill | Purpose |
|---------|-------|---------|
| Water · Observe | z-observe | Explore unfamiliar codebases, build mental models |
| Wood · Design | z-design | Brainstorm approaches, write implementation plans |
| Fire · Build | z-build | TDD-driven progressive construction |
| Earth · Verify | z-verify | Diagnose issues with evidence, not assumptions |
| Metal · Evolve | z-evolve | Code review, knowledge extraction |

See [skills/README.md](skills/README.md) for full documentation and setup instructions.

## Design Philosophy

Every project follows three principles:

- **Single File** — One HTML file contains all code; no build tools, no dependencies
- **Zero Config** — Open in a browser and it just works; no server required
- **Learn by Doing** — Each project is a practical exploration of a specific technical domain

## Research: Bagua-Mapped Technology Landscape

An in-depth analysis of the build-your-own-x repository (469K+ stars), mapping **590+ tutorials, 31 technology categories, and 37+ programming languages** to the I Ching Bagua framework.

### Bagua Mapping

| Trigram | Domain | Representative Categories | Tutorials |
|:-------:|--------|--------------------------|:---------:|
| ☰ Qian · Heaven · Creation | Rule Definition | Programming Language, Regex Engine | 50 |
| ☷ Kun · Earth · Foundation | System Basics | Operating System, Docker, Shell | 31 |
| ☵ Kan · Water · Flow | Networking | Web Server, Network Stack, Browser | 45 |
| ☲ Li · Fire · Expression | Visual Output | Game, 3D Renderer, Frontend Framework | 68 |
| ☳ Zhen · Thunder · Action | Automation | Bot, Command-Line Tool, Task Scheduler | 30 |
| ☴ Xun · Wind · Transformation | Information | Search Engine, Text Editor, Template Engine | 36 |
| ☶ Gen · Mountain · Persistence | Data Storage | Database, Blockchain, Git | 49 |
| ☱ Dui · Lake · Intelligence | Emergence | Neural Network, AI Model, Vision | 30 |

### Six Learning Paths

| Path | Direction | Progression |
|------|-----------|-------------|
| Heaven Path | Language Creator | Regex → Template → Programming Language → VM |
| Earth Path | System Architect | Memory → Shell → OS → Docker |
| Water Path | Network Engineer | Network Stack → Web Server → Browser → Distributed |
| Fire Path | Creative Full-Stack | Frontend → 3D Rendering → Game → Physics |
| Mountain Path | Data Guardian | Git → Database → Blockchain → Search Engine |
| Wisdom Path | AI Practitioner | Neural Network → Vision → AI Model → Bot |

See the full analysis in the [Deep Research Report](docs/research-report-v2.md).

## Quick Start

```bash
# Clone the repository
git clone https://github.com/hongxin/build-your-own-x.git

# Open the landing page in your browser
open build-your-own-x/index.html
```

Or visit the [live version](https://hongxin.github.io/build-your-own-x/) directly.

---

> *"Think twice, then act."* — Confucius
