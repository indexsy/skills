# 🧠 Indexsy Skills

**Open-source marketing & SEO skills for AI agents.**

Teach Claude, GPT, Cursor, or any AI agent to run agency-grade audits and campaigns.

---

## 📚 Available Skills

| Skill | Description | Use Case |
|-------|-------------|----------|
| [🛒 ecommerceseo](./ecommerceseo/) | 80+ point eCommerce SEO audit | Shopify, WooCommerce, product pages, collections |
| [🗺️ localseo](./localseo/) | Local SEO audit methodology | GBP, citations, NAP, Map Pack rankings |
| [📣 reddit](./reddit/) | Reddit organic marketing | Find threads, craft comments, anti-detection |

---

## 🚀 Quick Install

### Single Skill
```bash
npx degit indexsy/skills/ecommerceseo ./skills/ecommerceseo
npx degit indexsy/skills/localseo ./skills/localseo
npx degit indexsy/skills/reddit ./skills/reddit
```

### All Skills
```bash
git clone https://github.com/indexsy/skills.git
```

### Direct Reference (No Install)
Point your AI agent directly to:
```
https://raw.githubusercontent.com/indexsy/skills/main/ecommerceseo/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/localseo/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/reddit/SKILL.md
```

---

## 📁 Skill Structure

Each skill folder contains:

| File | Purpose |
|------|---------|
| `SKILL.md` | Quick start + instructions for the AI agent |
| `README.md` | Human-readable documentation |
| `KNOWLEDGE-BASE.md` | Full methodology, SOPs, decision trees |
| `package.json` | Metadata (optional) |

---

## 🎯 How It Works

1. **Install** a skill (or reference directly)
2. **Tell your agent** what you want: *"Run an eCommerce SEO audit for shopify.com"*
3. **Agent follows** the SKILL.md methodology
4. **Get output** — prioritized findings, action plans, deliverables

---

## 🤝 Contributing

Add new skills by creating a folder with at least a `SKILL.md` file.

PRs welcome!

---

## 👤 Author

**[Indexsy](https://indexsy.com)** — We build, acquire, and scale digital assets.

- 🐦 Twitter: [@indexsy](https://twitter.com/indexsy)
- 📺 YouTube: [youtube.com/@indexsy](https://youtube.com/@indexsy)

---

## 📄 License

MIT — Use freely, attribution appreciated.

---

*Built for the open agent skills ecosystem.*
