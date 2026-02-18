# Hugo + PaperMod 双语博客模板

一个开箱即用的静态博客模板，支持中英双语，部署到 Vercel。

## ✨ 特性

- **Hugo + PaperMod**：快速、简洁、响应式
- **双语支持**：中英文章并排显示
- **Vercel 一键部署**：免费托管，自动更新
- **Search + Archive**：内置搜索和归档页面
- **暗黑主题**：默认暗黑，无需切换

---

## 🚀 快速开始

### 1. 克隆模板

```bash
git clone https://github.com/你的用户名/hugo-blog-starter.git my-blog
cd my-blog
```

### 2. 安装 Hugo

```bash
# Mac
brew install hugo

# Linux
sudo apt install hugo
```

### 3. 本地预览

```bash
hugo server
# 访问 http://localhost:1313
```

### 4. 部署到 Vercel

1. 把仓库推到 GitHub
2. 去 [vercel.com](https://vercel.com) 导入 GitHub 仓库
3. **Build Command**: `hugo`
4. **Output Directory**: `public`
5. Deploy!

---

## 📝 写文章

```bash
hugo new posts/你的文章标题.md
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

## ⚙️ 配置修改

### 基本信息 (hugo.toml)

```toml
title = "你的博客标题"
author = "你的名字"
baseURL = "https://你的域名.vercel.app/"
```

### 菜单配置

在 `hugo.toml` 中修改 `[menu]` 部分。

---

## 🛠️ 常见问题 (血泪教训)

### ❌ 不要用 config.toml

Hugo 会优先读取 `config.toml`，会覆盖 `hugo.toml`！
如果不用主题自带配置，直接删掉或改名。

### ❌ themes 要用 submodule

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

不要直接 clone，否则更新麻烦。

### ✅ Markdown 里用 HTML

需要在 `[markup]` 开启：

```toml
[markup.goldmark.renderer]
  unsafe = true
```

### ✅ 本地调试主题不生效？

```bash
hugo --themesDir .
```

或者检查 `hugo.toml` 里的 `theme = "PaperMod"` 是否正确。

### ✅ Vercel 部署404？

- 检查 Build Command 是 `hugo`（不是 `hugo server`）
- Output Directory 是 `public`
- 确认 `vercel.json` 存在

### ✅ 文章没显示？

- `draft: false` 或者删掉 draft 字段
- `content/` 目录结构要正确

---

## 📦 目录结构

```
hugo-blog-starter/
├── content/           # 文章目录
│   └── posts/         # 博客文章
├── layouts/           # 自定义模板 (双语)
├── archetypes/        # 文章模板
├── hugo.toml         # 配置文件
├── vercel.json       # Vercel 配置
└── themes/           # 主题 (submodule)
```

---

## 🤖 用 AI 维护博客

这个模板可以用 AI 辅助维护：
- AI 帮你写文章草稿
- AI 检查语法
- AI 生成摘要

详见 [OpenClaw](https://github.com/openclaw/openclaw)

---

## 📄 许可证

[CC BY-NC 4.0](LICENSE) - 署名 + 非商用

---

## 🤖 用 AI 维护博客
