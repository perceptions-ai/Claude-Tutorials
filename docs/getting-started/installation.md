# 安装步骤

本指南将帮助您在不同操作系统上安装 Claude Code。

## 系统要求

在开始之前，请确保您的系统满足以下要求：

*   **操作系统**:
    *   Windows 10/11 (推荐 WSL2)
    *   macOS 10.14+
    *   Linux (Ubuntu 18.04+, Debian, 等)
*   **环境**: Node.js 18+ (部分插件可能需要), Python 3.8+ (如果使用 Python 相关工具)

## 安装流程

### 1. 申请访问权限

Claude Code 目前可能处于预览或特定访问阶段。请前往 [Anthropic 官网](https://www.anthropic.com/) 查看最新的访问获取方式。

### 2. 下载与安装

!!! note "注意事项"
    具体的安装包形式可能随版本更新而变化（CLI 工具、VS Code 插件或独立应用）。以下以通用 CLI 为例。

```bash
# 如果是通过 npm 分发的 CLI 工具
npm install -g @anthropic/claude-code
```

### 3. 验证安装

安装完成后，在终端运行以下命令验证：

```bash
claude --version
```

如果看到版本号输出，说明安装成功。

## 下一步

安装完成后，请继续进行 [环境配置](configuration.md) 以获得最佳体验。
