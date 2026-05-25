# HTML 转设计规范

将 HTML 原型转换为设计规范和重构就绪的产品智能，供 AI 编码代理使用。

## 概述

此技能将来自 Lovable、v0、Bolt 等工具的交互式网页原型或 HTML 设计稿转换为设计规范和重构就绪的产品智能。它探索原型、去重 UI 状态、捕获证据，并生成既保留交互流程又保留视觉样式的输出，以便进行重构。

## 功能特性

- **全面分析**：探索 HTML 原型并捕获 UI 状态
- **结构化输出**：生成 pages.json、flows.json、graph.json、style.json
- **视觉文档**：捕获不同视口的截图
- **设计规范**：创建详细的规范和重构提示
- **工作流自动化**：创建分析目录结构的脚本

## 输出结构

每次分析运行都会创建一个包含以下内容的目录：
- `pages.json` - 页面/状态清单
- `flows.json` - 用户流程和交互转换
- `graph.json` - 包含节点和边的 UI 状态图
- `style.json` - 设计令牌和组件样式
- `screenshots/` - 不同状态和视口的视觉证据
- `prompts/` - AI 重构提示
- `specs/` - 详细的设计规范

## 使用方法

此技能设计用于 AI 编码代理。主要工作流程记录在 `SKILL.md` 中。

### 快速开始

1. 使用 `scripts/create_run_dir.py` 脚本创建分析目录：
   ```bash
   python scripts/create_run_dir.py /path/to/project --name "my-prototype" --target "http://localhost:3000"
   ```

2. 按照 `SKILL.md` 中的工作流程分析原型

3. 生成用于重构的结构化输出

## 参考文档

- `SKILL.md` - 完整的技能文档和工作流程
- `references/output-schemas.md` - 输出文件的 JSON 模式定义
- `agents/openai.yaml` - 代理接口配置

## 许可证

此技能移植自原始 [技能仓库](https://github.com/opoojkk/skills)。