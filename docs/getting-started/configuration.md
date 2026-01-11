# 环境配置

配置您的开发环境以适配 Claude Code。

## 认证设置

首次使用通常需要登录或提供 API Key。

```bash
claude login
# 或者设置环境变量
export ANTHROPIC_API_KEY="sk-..."
```

## 配置文件

您可以创建 `.clauderc` 或类似配置文件来定制行为（具体文件名视版本而定）。

```json
{
  "theme": "dark",
  "language": "zh-CN",
  "editor": "vscode"
}
```

## VS Code 集成

如果您使用 Visual Studio Code，建议安装官方或推荐的扩展插件，以便在这款最流行的编辑器中直接调用 Claude Code 的能力。

1. 打开 VS Code 扩展市场。
2. 搜索 "Claude"。
3. 安装官方插件。

## Shell 集成

为了在终端中更方便地使用，可以将自动补全脚本添加到您的 shell 配置中 (`.bashrc` 或 `.zshrc`).

```bash
# 示例（假设支持 completion 命令）
source <(claude completion zsh)
```
