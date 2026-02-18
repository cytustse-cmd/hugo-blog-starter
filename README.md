# Hugo + PaperMod Bilingual Blog Template

> 📖 Also available in [简体中文](README.zh.md)

A ready-to-use static blog template with Chinese-English bilingual support, deployed on Vercel.

## ✨ Features

- **Hugo + PaperMod**: Fast, clean, responsive
- **Bilingual Support**: Chinese and English articles displayed side by side
- **One-Click Vercel Deploy**: Free hosting, auto-deploy on push
- **Search + Archive**: Built-in search and archive pages
- **Dark Mode**: Default dark, no toggle needed

---

## 🚀 Quick Start

### 1. Clone the Template

```bash
git clone https://github.com/your-username/hugo-blog-starter.git my-blog
cd my-blog
```

### 2. Install Hugo

```bash
# Mac
brew install hugo

# Linux
sudo apt install hugo
```

### 3. Local Preview

```bash
hugo server
# Visit http://localhost:1313
```

### 4. Deploy to Vercel

1. Push repo to GitHub
2. Go to [vercel.com](https://vercel.com) → Import GitHub repo
3. **Build Command**: `hugo`
4. **Output Directory**: `public`
5. Deploy!

---

## 📝 Writing Posts

```bash
hugo new posts/your-post-title.md
```

Post template:

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

## ⚙️ Configuration

### Basic Info (hugo.toml)

```toml
title = "Your Blog Title"
author = "Your Name"
baseURL = "https://your-domain.vercel.app/"
```

### Menu

Modify `[menu]` section in `hugo.toml`.

---

## 🛠️ Common Issues (Lessons Learned)

### ❌ Don't Use config.toml

Hugo prioritizes `config.toml` over `hugo.toml`! 
If you don't need theme's default config, delete or rename it.

### ❌ Use Submodule for Themes

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

Don't clone directly, otherwise updates are painful.

### ✅ Enable HTML in Markdown

Add to `[markup]`:

```toml
[markup.goldmark.renderer]
  unsafe = true
```

### ✅ Theme Not Working Locally?

```bash
hugo --themesDir .
```

Or check `theme = "PaperMod"` in `hugo.toml`.

### ✅ Vercel 404 Error?

- Build Command: `hugo` (not `hugo server`)
- Output Directory: `public`
- Make sure `vercel.json` exists

### ✅ Posts Not Showing?

- Set `draft: false` or remove draft field
- Check `content/` directory structure

---

## 📦 Directory Structure

```
hugo-blog-starter/
├── content/           # Posts directory
│   └── posts/         # Blog posts
├── layouts/           # Custom templates (bilingual)
├── archetypes/        # Post templates
├── hugo.toml         # Config file
├── vercel.json       # Vercel config
└── themes/           # Theme (submodule)
```

---

## 🤖 Maintain with AI

This template can be maintained with AI assistance:
- AI drafts posts
- AI checks grammar
- AI generates summaries

See [OpenClaw](https://github.com/openclaw/openclaw)

---

## 📄 License

[CC BY-NC 4.0](LICENSE) - Attribution + Non-Commercial
