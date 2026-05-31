# forstCC

> Claude Code 自动化开发工作空间

## 项目简介

forstCC 是一个以 **Claude Code** 为核心的 AI 辅助开发工作空间。项目集成了完整的 [Everything Claude Code (ECC)](https://github.com/affaan-m/everything-claude-code) 工具包，提供开箱即用的 AI 编程代理、Slash 命令、安全审查、自动化测试等能力。

## 目录结构

```
forstCC/
├── CLAUDE.md              # Claude Code 项目指令（AI 行为规则）
├── forstCC/               # 📦 项目源代码（业务代码放这里）
├── ecc/                   # 🧰 ECC 工具包（代理/命令/技能/规范）
├── test_hello.py          # 🧪 安装验证脚本
├── douyin_hot.txt         # 📊 数据采集样本
├── 项目目录说明.md        # 📖 完整目录索引与分类说明
└── README.md              # 📖 本文件
```

> 详细目录结构请查看 **[项目目录说明.md](./项目目录说明.md)**

## 快速开始

```bash
# 验证 Claude Code 安装
python test_hello.py

# 运行 ECC 测试套件
node ecc/tests/run-all.js
```

## ECC 工具包能力

| 模块 | 数量 | 说明 |
|------|------|------|
| Agents | 12 | 专用子代理（planner/code-reviewer/tdd-guide 等） |
| Commands | 19 | Slash 命令（`/tdd` `/plan` `/code-review` 等） |
| Skills | 15 | 技能工作流（语言模式/安全审查/TDD 等） |
| Rules | 8 | 行为准则（编码/测试/安全/Git 等） |
| Scripts | 9 | 自动化工具脚本 |
| Tests | 4 | 测试套件 |

## 技术栈

- **AI 辅助**：Claude Code（Anthropic Claude 4.X 系列）
- **配置参考**：Everything Claude Code (ECC)
- **语言**：Python（验证脚本）、JavaScript/Node.js（ECC 工具脚本）
