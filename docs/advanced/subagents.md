# Subagents 详解

Claude Code 的高级功能之一是能够编排多个子代理 (Subagents) 来完成复杂任务。

## 什么是 Subagents？

Subagent 是指主 Claude 实例为了解决特定子问题而调用的独立执行流。例如，当你要求 "构建一个全栈应用" 时：

1.  **Main Agent**: 规划整体架构。
2.  **Frontend Agent**: 负责 React 组件编写。
3.  **Backend Agent**: 负责 API 接口设计。
4.  **Testing Agent**: 编写并运行测试用例。

## 如何启用

通常在配置文件中开启 `experimental_subagents: true` (假设功能标志如此)。

## 实战案例

> **任务**: "分析这个 Python 项目的性能瓶颈并优化。"

Claude 可能会：
1.  启动 `Profile Agent` 运行 cProfile。
2.  读取报告，识别慢函数。
3.  启动 `Refactor Agent` 修改代码。
4.  启动 `Benchmark Agent` 验证优化效果。
