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

## 🚀 部署到 Cloudflare Pages (推荐)

由于网络原因，推荐部署到 Cloudflare Pages。

### 1. 准备工作

确保仓库中包含 `requirements.txt`。

### 2. 在 Cloudflare 上创建项目

1.  登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)。
2.  进入 **Compute (Workers & Pages)** -> **Overview**。
3.  点击 **Create Application** -> **Pages** -> **Connect to Git**。
4.  选择您的仓库 (`claude-code-tutorials`)。

### 3. 构建配置 (关键！)

在配置页面填写以下信息：

*   **Framework preset**: 选 `None` 或 `MkDocs` (如果有)
*   **Build command**: `pip install -r requirements.txt && mkdocs build`
*   **Build output directory**: `site`

**⚠️ 重要步骤：设置 Python 版本**

Cloudflare 默认 Python 版本较旧，会导致构建失败。请务必在 **Environment variables** 部分添加：

*   **Variable name**: `PYTHON_VERSION`
*   **Value**: `3.8` (或更高，如 3.11)

### 4. 部署与完成

点击 **Save and Deploy**。构建完成后，您将获得一个 `*.pages.dev` 的域名。

> **提示**: 部署成功后，请记得修改 `mkdocs.yml` 中的 `site_url` 为您的 Cloudflare 域名，以确保搜索和站点地图功能正常。

## 📝 贡献

欢迎提交 PR 补充更多的 Claude Code 使用技巧！
