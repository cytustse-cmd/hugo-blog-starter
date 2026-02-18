<div align="center">

<img width="1500" height="400" alt="Hugo 博客模板" src="https://images.unsplash.com/photo-1499750310107-5fef28a66643?w=1500&h=400&fit=crop" />

<br/>
<br/>

**一个开箱即用的 Hugo + PaperMod 双语博客模板，支持中英双语。**

[![Hugo](https://img.shields.io/badge/Hugo-0.139.0-blue?style=flat-square)](https://gohugo.io)
[![PaperMod](https://img.shields.io/badge/PaperMod-7.0-blue?style=flat-square)](https://github.com/adityatelange/hugo-PaperMod)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue?style=flat-square)](LICENSE)
[![Deploy](https://img.shields.io/badge/Deploy-Vercel-brightgreen?style=flat-square)](https://vercel.com)

</div>

---

## ✨ 特性

| 特性 | 说明 |
|------|------|
| **Hugo + PaperMod** | 轻量、简洁、响应式设计 |
| **双语支持** | 中英文文章并排显示 |
| **自动化部署** | 免费托管，代码推送后自动部署 |
| **搜索与归档** | 内置搜索功能及归档页面 |
| **暗黑主题** | 默认暗黑模式，无需手动切换 |
| **双语模板** | 自定义中英双语文章布局 |

---

## 🚀 快速开始

### 1. 克隆模板

```bash
git clone https://github.com/your-username/hugo-blog-starter.git my-blog
cd my-blog
```

### 2. 安装 Hugo

```bash
# macOS
brew install hugo

# Linux
sudo apt install hugo
```

### 3. 本地预览

```bash
hugo server
# 访问 http://localhost:1313
```

### 4. 部署至 Vercel

1. 将仓库推送至 GitHub
2. 访问 [vercel.com](https://vercel.com) 并导入 GitHub 仓库
3. 配置 **Build Command**：`hugo`
4. 配置 **Output Directory**：`public`
5. 点击 **Deploy** 开始部署

---

## 📝 撰写文章

```bash
hugo new posts/your-post-title.md
```

文章模板：

```markdown
---
title: "标题"
date: 2026-02-18
draft: false
---

## English Title

Your English content here...

---

## 中文标题

你的中文内容...
```

---

## ⚙️ 配置说明

### 基本信息 (hugo.toml)

```toml
title = "您的博客标题"
author = "您的名字"
baseURL = "https://your-domain.vercel.app/"
```

### 导航菜单

修改 `hugo.toml` 文件中的 `[menu]` 部分以自定义导航链接。

---

## 🛠️ 常见问题排查

| 问题 | 解决方案 |
|------|----------|
| **config.toml 冲突** | Hugo 优先读取 `config.toml`，如无需用请删除或重命名 |
| **主题渲染异常** | 运行 `hugo --themesDir .` 或检查 `hugo.toml` 中的 `theme` 配置 |
| **Vercel 404** | 确认 Build Command 为 `hugo`，Output Directory 为 `public` |
| **文章无法显示** | 设置 `draft: false`，检查 `content/` 目录结构 |

### 使用 Git Submodule 管理主题

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### 启用 Markdown 内嵌 HTML

```toml
[markup.goldmark.renderer]
  unsafe = true
```

---

## 📦 目录结构

```
hugo-blog-starter/
├── content/           # 内容目录
│   └── posts/         # 博客文章
├── layouts/           # 自定义模板
├── archetypes/        # 内容模板
├── hugo.toml         # 配置文件
├── vercel.json       # Vercel 配置
└── themes/           # 主题目录（submodule）
```

---

## 🤖 AI 辅助博客维护

本模板支持 AI 辅助维护：

- AI 生成文章草稿
- 语法与风格检查
- 自动化摘要生成

详见 [OpenClaw](https://github.com/openclaw/openclaw)

---

## 📄 许可证

[CC BY-NC 4.0](LICENSE) - 署名 + 非商业性使用
