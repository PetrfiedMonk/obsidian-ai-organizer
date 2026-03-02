# 🔮 Obsidian AI Organizer

> Drop your documents in. Get Obsidian-ready markdown with AI-generated tags, summaries, and metadata out.

A single-file, browser-based tool that transforms messy document collections into structured Obsidian vaults — no server, no install, no data leaving your machine (except the AI API call).

---

## ✨ Features

- **AI-powered frontmatter** — auto-generates YAML with tags, summary, keywords, and related wikilinks
- **Multi-provider** — works with Anthropic Claude (default), OpenAI GPT-4o, or Google Gemini
- **Broad format support** — TXT, MD, HTML, PDF, DOCX, CSV, JSON, YAML
- **Smart tag styles** — kebab-case, snake_case, TitleCase, or lowercase
- **Vault context** — tell the AI what your vault is about for more precise tagging
- **Concurrent processing** — batch process up to 3 files at once
- **Live preview** — inspect enhanced files before downloading
- **ZIP download** — all enhanced `.md` files packed and ready to drop into Obsidian
- **Skip logic** — optionally skip files that already have frontmatter
- **100% local** — static HTML, no backend, no tracking

---

## 🚀 Quick Start

### Option 1 — Use it instantly (GitHub Pages)

```
https://yourusername.github.io/obsidian-ai-organizer
```

No install. Just open and use.

### Option 2 — Run locally

```bash
git clone https://github.com/yourusername/obsidian-ai-organizer.git
cd obsidian-ai-organizer
open index.html   # or just double-click it
```

---

## 🔑 API Keys

You need one API key from any of these providers:

| Provider | Model | Get Key |
|---|---|---|
| **Anthropic (Claude)** ⭐ recommended | Claude Sonnet 4 | [console.anthropic.com](https://console.anthropic.com/) |
| OpenAI | GPT-4o / GPT-4o Mini | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| Google | Gemini 2.0 Flash | [aistudio.google.com](https://aistudio.google.com/) |

Your API key is used directly in the browser and **never stored or sent anywhere except the AI provider's API**.

---

## 📖 How It Works

1. **Select your AI provider** and paste your API key
2. **(Optional)** Add vault context — e.g. `"security research notes"` — so the AI tags more precisely
3. **Drop your files** into the upload zone
4. **Configure options** — choose which metadata to generate, tag style, concurrency
5. **Hit Start** — watch files process with live status updates
6. **Preview** the enhanced markdown, then **Download ZIP**
7. Unzip into your Obsidian vault's inbox folder

### Output format

Each file gets an Obsidian-compatible frontmatter block injected at the top:

```markdown
---
created: 2026-03-01
source_file: "meeting-notes.docx"
tags:
  - project-management
  - q1-planning
  - team-sync
keywords: ["OKRs", "roadmap", "sprint planning"]
summary: "Notes from Q1 planning sync covering OKR alignment, sprint prioritization, and team capacity."
related: ["[[Q1 Roadmap]]", "[[Team Capacity]]"]
---

# meeting-notes

... original content ...
```

---

## ⚙️ Processing Options

| Option | Description |
|---|---|
| Generate summary | 2-3 sentence AI summary in frontmatter |
| Extract key topics | Keywords array from main concepts |
| Generate Obsidian tags | 3-10 `#tags` in your chosen style |
| Suggest wikilinks | AI proposes `[[link]]` candidates as `related:` |
| Skip already-tagged | Skip `.md` files that already have frontmatter |
| Include created date | Adds today's date as `created:` |

---

## 📁 Project Structure

```
obsidian-ai-organizer/
├── index.html    ← the entire app (single file)
├── README.md
└── LICENSE
```

Everything lives in `index.html`. No build step. No dependencies. No node_modules.

---

## 🤝 Contributing

PRs welcome. Some ideas for improvement:

- [ ] Folder structure preservation on batch upload
- [ ] Custom frontmatter field templates
- [ ] Retry logic for rate-limited API responses
- [ ] Dark/light theme toggle
- [ ] Support for `.epub` and `.odt`
- [ ] Drag-to-reorder queue

To contribute: fork → branch → PR. Keep it single-file.

---

## 📄 License

MIT — do whatever you want with it.

---

*Built for people who think in networks, not folders.*
