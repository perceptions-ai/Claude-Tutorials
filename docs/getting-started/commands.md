# 常用命令

掌握 Claude Code 的核心命令，提升编码效率。

## 基础交互

| 命令 | 描述 | 示例 |
| :--- | :--- | :--- |
| `claude ask` | 提问一般性编程问题 | `claude ask "如何在 Python 中解析 JSON?"` |
| `claude explain` | 解释选定或指定文件的代码逻辑 | `claude explain ./src/main.py` |
| `claude fix` | 尝试修复代码中的错误或 lint 问题 | `claude fix ./app.js` |

## 项目管理

*   `claude init`: 在当前目录初始化 Claude 配置。
*   `claude analyze`: 分析整个项目的结构和依赖。

## 进阶指令

!!! tip "自然语言指令"
    Claude Code 的强大之处在于理解自然语言。你通常不需要记住复杂的参数，只需清晰描述意图。

    > "帮我重构这个函数，使其更加模块化，并添加 TypeScript 类型定义。"
