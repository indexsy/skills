# Skills

Marketing & SEO skills for AI agents.

## Available Skills

| Skill | Description |
|-------|-------------|
| [localseo](./localseo/) | Local SEO audits - GBP, citations, NAP, rankings |
| [reddit-placements](./reddit-placements/) | Reddit organic marketing with anti-detection rules |

## Installation

**Quick install (single skill):**
```bash
npx degit indexsy/skills/localseo ./skills/localseo
npx degit indexsy/skills/reddit-placements ./skills/reddit-placements
```

**Clone all skills:**
```bash
git clone https://github.com/indexsy/skills.git
```

**Or just reference directly** - point your AI agent to:
```
https://raw.githubusercontent.com/indexsy/skills/main/localseo/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/reddit-placements/SKILL.md
```

## Structure

```
/localseo            # Local SEO audit skill
/reddit-placements   # Reddit organic marketing skill
```

Each skill folder contains:
- `SKILL.md` - Instructions for the AI agent
- `README.md` - Human-readable docs
- `KNOWLEDGE-BASE.md` - Full methodology

## Contributing

Add new skills by creating a folder with at least a `SKILL.md` file.

---

Made by [@indexsy](https://github.com/indexsy)
