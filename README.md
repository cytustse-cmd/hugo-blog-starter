<div align="center">

**A production-ready Hugo + PaperMod blog template with Chinese-English bilingual support.**

[![Hugo](https://img.shields.io/badge/Hugo-0.139.0-blue?style=flat-square)](https://gohugo.io)
[![PaperMod](https://img.shields.io/badge/PaperMod-7.0-blue?style=flat-square)](https://github.com/adityatelange/hugo-PaperMod)
[![Deploy](https://img.shields.io/badge/Deploy-Vercel-brightgreen?style=flat-square)](https://vercel.com)

</div>

---

## Features

| Feature | Description |
|---------|-------------|
| **Hugo + PaperMod** | Fast, lightweight, and responsive design |
| **Bilingual Support** | Side-by-side Chinese and English article display |
| **Automated Deployment** | Free hosting with automatic deployment on code push |
| **Search & Archive** | Integrated search functionality and archive pages |
| **Dark Mode** | Default dark theme, no manual toggle required |
| **Bilingual Templates** | Custom layouts for Chinese-English content |

---

## Quick Start

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

## Writing Posts

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

## Configuration

### Basic Information (hugo.toml)

```toml
title = "Your Blog Title"
author = "Your Name"
baseURL = "https://your-domain.vercel.app/"
```

### Navigation Menu

Modify the `[menu]` section in `hugo.toml` to customize navigation links.

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| **config.toml conflict** | Hugo prioritizes `config.toml` over `hugo.toml`. Delete or rename it if not needed. |
| **Theme not rendering** | Run `hugo --themesDir .` or verify `theme = "PaperMod"` in hugo.toml |
| **Vercel 404** | Ensure Build Command is `hugo` and Output Directory is `public` |
| **Posts not displayed** | Set `draft: false` and verify `content/` structure |

### Use Git Submodule for Themes

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### Enable HTML in Markdown

```toml
[markup.goldmark.renderer]
  unsafe = true
```

---

## Directory Structure

```
hugo-blog-starter/
├── content/           # Content directory
│   └── posts/         # Blog posts
├── layouts/           # Custom layout templates
├── archetypes/        # Content archetypes
├── hugo.toml         # Configuration file
├── vercel.json       # Vercel configuration
└── themes/           # Theme directory (submodule)
```

---

## AI-Assisted Blog Maintenance

This template supports AI-assisted maintenance:

- AI-generated post drafts
- Grammar and style checking
- Automated summary generation

Learn more at [OpenClaw](https://github.com/openclaw/openclaw)

---

## License

[CC BY-NC 4.0](LICENSE) - Attribution + Non-Commercial
