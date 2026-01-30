# Skills

Marketing & SEO skills for AI agents.

## Available Skills

| Skill | Description |
|-------|-------------|
| [ecommerceseo](./ecommerceseo/) | eCommerce SEO audits - technical, on-page, product pages, collections, link building |
| [localseo](./localseo/) | Local SEO audits - GBP, citations, NAP, rankings |
| [reddit](./reddit/) | Reddit organic marketing with anti-detection rules |

## Installation

**Quick install (single skill):**
```bash
npx degit indexsy/skills/ecommerceseo ./skills/ecommerceseo
npx degit indexsy/skills/localseo ./skills/localseo
npx degit indexsy/skills/reddit ./skills/reddit
```

**Clone all skills:**
```bash
git clone https://github.com/indexsy/skills.git
```

**Or just reference directly** - point your AI agent to:
```
https://raw.githubusercontent.com/indexsy/skills/main/ecommerceseo/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/localseo/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/reddit/SKILL.md
```

## Structure

```
/ecommerceseo  # eCommerce SEO audit skill
/localseo      # Local SEO audit skill
/reddit        # Reddit organic marketing skill
```

Each skill folder contains:
- `SKILL.md` - Instructions for the AI agent
- `README.md` - Human-readable docs
- `KNOWLEDGE-BASE.md` - Full methodology (optional)

## Contributing

Add new skills by creating a folder with at least a `SKILL.md` file.

---

Made by [@indexsy](https://github.com/indexsy)
