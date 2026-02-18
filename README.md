# Hugo + PaperMod Bilingual Blog Template

> 📖 Also available in [简体中文](README.zh.md)

A production-ready static blog template with Chinese-English bilingual support, deployed on Vercel.

## ✨ Features

- **Hugo + PaperMod**: Fast, lightweight, and responsive design
- **Bilingual Support**: Side-by-side Chinese and English article display
- **Automated Vercel Deployment**: Free hosting with automatic deployment on code push
- **Search + Archive**: Integrated search functionality and archive pages
- **Dark Mode**: Default dark theme, no manual toggle required

---

## 🚀 Quick Start

### 1. Clone the Template

```bash
git clone https://github.com/your-username/hugo-blog-starter.git my-blog
cd my-blog
```

### 2. Install Hugo

```bash
# macOS
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

1. Push the repository to GitHub
2. Navigate to [vercel.com](https://vercel.com) and import the GitHub repository
3. Configure **Build Command**: `hugo`
4. Configure **Output Directory**: `public`
5. Click **Deploy**

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

### Basic Information (hugo.toml)

```toml
title = "Your Blog Title"
author = "Your Name"
baseURL = "https://your-domain.vercel.app/"
```

### Navigation Menu

Modify the `[menu]` section in `hugo.toml` to customize navigation links.

---

## 🛠️ Troubleshooting

### ❌ Avoid Using config.toml

Hugo prioritizes `config.toml` over `hugo.toml`. If the theme's default configuration is not required, delete or rename `config.toml` to prevent conflicts.

### ❌ Use Git Submodule for Themes

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

Direct cloning is not recommended, as it complicates update management.

### ✅ Enable HTML in Markdown

Add the following to the `[markup]` section:

```toml
[markup.goldmark.renderer]
  unsafe = true
```

### ✅ Theme Not Rendering Locally

```bash
hugo --themesDir .
```

Alternatively, verify that `theme = "PaperMod"` is correctly set in `hugo.toml`.

### ✅ Vercel Deployment Returns 404

- Ensure **Build Command** is set to `hugo` (not `hugo server`)
- Ensure **Output Directory** is set to `public`
- Verify that `vercel.json` exists in the project root

### ✅ Posts Not Displayed

- Set `draft: false` or remove the `draft` field entirely
- Verify that the `content/` directory structure is correct

---

## 📦 Directory Structure

```
hugo-blog-starter/
├── content/           # Content directory
│   └── posts/         # Blog posts
├── layouts/           # Custom layout templates (bilingual)
├── archetypes/        # Content archetypes
├── hugo.toml         # Configuration file
├── vercel.json       # Vercel configuration
└── themes/           # Theme directory (submodule)
```

---

## 🤖 AI-Assisted Blog Maintenance

This template supports AI-assisted maintenance:

- AI-generated post drafts
- Grammar and style checking
- Automated summary generation

Learn more at [OpenClaw](https://github.com/openclaw/openclaw)

---

## 📄 License

[CC BY-NC 4.0](LICENSE) - Attribution + Non-Commercial
