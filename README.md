# Claude Code Tutorials Website

这是一个基于 [MkDocs](https://www.mkdocs.org/) 和 [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 构建的静态文档网站项目，用于分享 **Claude Code** 的使用教程及经验。

项目结构参考了 [ctok.ai](https://ctok.ai/) 的内容组织。

## 📁 目录结构

```
.
├── docs/                   # 文档源文件 (Markdown)
│   ├── getting-started/    # 快速开始
│   ├── practices/          # 最佳实践
│   ├── advanced/           # 高级教程
│   ├── community.md        # 社区资源
│   └── index.md            # 首页
├── mkdocs.yml              # 网站配置文件
├── .gitignore              # Git 忽略配置
└── README.md               # 本说明文件
```

## 🛠 如何运行

要在本地预览此网站，您需要安装 Python 环境。

### 1. 安装依赖

建议在虚拟环境中安装依赖：

```bash
# 创建虚拟环境 (可选，但在 Linux/Mac 上推荐)
python3 -m venv .venv
source .venv/bin/activate  # Windows 用户使用: .venv\Scripts\activate

# 安装 MkDocs 和 Material 主题
pip install mkdocs-material
```

### 2. 启动本地服务器

```bash
mkdocs serve
```

运行后，在浏览器访问 http://127.0.0.1:8000 即可预览网站。

### 3. 构建静态文件

如果您需要部署到服务器（如 GitHub Pages 或 Nginx）：

```bash
mkdocs build
```

构建生成的 HTML 文件将位于 `site/` 目录下。

## 🚀 部署到 GitHub Pages

1.  在 GitHub 上创建一个新仓库（例如 `claude-code-tutorials`）。
2.  将本地内容推送到仓库：

    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/<your-username>/<repo-name>.git
    git push -u origin main
    ```

3.  启用 GitHub Actions 自动部署：
    *   在仓库中创建 `.github/workflows/ci.yml` (参考 MkDocs 官方文档)
    *   或者直接使用 `gh-deploy` 命令（需在本地配置好权限）：
        ```bash
        mkdocs gh-deploy
        ```

## 📝 贡献

欢迎提交 PR 补充更多的 Claude Code 使用技巧！
