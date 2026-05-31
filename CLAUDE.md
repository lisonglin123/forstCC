# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Workspace Overview

这是一个以 Claude Code 配置为中心的工作空间：

- `forstCC/` — 预留给实际项目代码（当前为空）
- `ecc/` — [Everything Claude Code](https://github.com/affaan-m/everything-claude-code) 工具包的本地克隆，是 agents、skills、hooks、commands、rules 的参考实现
- `test_hello.py` — Claude Code 安装验证脚本
- `douyin_hot.txt` — 抖音热搜数据文件

工作空间本身不是 Git 仓库；`ecc/` 目录内有独立的 `.git` 仓库。

## ECC 工具包结构

ECC 提供了完整的 Claude Code 配置参考，位于 `ecc/` 下：

| 目录 | 用途 |
|------|------|
| `ecc/agents/` | 专用子 agent 定义（planner、code-reviewer、tdd-guide 等） |
| `ecc/skills/` | 工作流定义（backend-patterns、golang-patterns、tdd-workflow 等） |
| `ecc/commands/` | Slash 命令实现（`/tdd`、`/plan`、`/code-review` 等） |
| `ecc/rules/` | 静态行为准则（security、coding-style、testing 等） |
| `ecc/hooks/` | 自动化触发器配置（PreToolUse、PostToolUse、Stop） |
| `ecc/contexts/` | 动态系统提示注入上下文（dev、review、research） |
| `ecc/mcp-configs/` | MCP 服务器配置模板 |
| `ecc/scripts/` | 跨平台 Node.js 工具脚本 |
| `ecc/examples/` | CLAUDE.md 和用户配置示例 |

### ECC 测试

```bash
# 运行所有 ECC 测试
node ecc/tests/run-all.js

# 运行单个测试文件
node ecc/tests/lib/utils.test.js
node ecc/tests/lib/package-manager.test.js
```
