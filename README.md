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

## 🛠 本地开发与预览

如果您需要修改内容并查看效果，可以在本地运行预览服务器。

### 1. 安装依赖

建议在虚拟环境中安装依赖：

```bash
# 创建虚拟环境 (可选，但在 Linux/Mac 上推荐)
python3 -m venv .venv
source .venv/bin/activate  # Windows 用户使用: .venv\Scripts\activate

# 安装依赖
pip install -r requirements.txt
```

### 2. 启动预览

```bash
mkdocs serve
```

运行后，在浏览器访问 http://127.0.0.1:8000 即可实时预览修改效果。

## 🚀 部署到 Netlify

本项目已配置 `netlify.toml`，支持一键部署到 Netlify。

### 1. 推送到 GitHub

首先，将代码推送到您的 GitHub 仓库：

```bash
# 如果是新仓库
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```

### 2. 在 Netlify 上创建站点

1.  登录 [Netlify](https://www.netlify.com/)。
2.  点击 **"Add new site"** -> **"Import from an existing project"**。
3.  选择 **GitHub** 并授权。
4.  选择您的仓库（例如 `claude-code-tutorials`）。

### 3. 自动配置与部署

由于项目中已包含 `netlify.toml`，Netlify 会自动识别构建设置：
*   **Build command**: `pip install -r requirements.txt && mkdocs build`
*   **Publish directory**: `site`

直接点击 **"Deploy site"** 即可。以后每次推送到 GitHub，Netlify 都会自动重新构建并更新网站。

## 📝 贡献

欢迎提交 PR 补充更多的 Claude Code 使用技巧！
