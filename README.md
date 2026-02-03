# Skills

Marketing & SEO skills for AI agents.

## Available Skills

| Skill | Description |
|-------|-------------|
| [localseo](./localseo/) | Local SEO audits - GBP, citations, NAP, rankings |
| [ecommerceseo](./ecommerceseo/) | E-commerce SEO audits - product pages, technical SEO, structured data |
| [reddit](./reddit/) | Reddit organic marketing with anti-detection rules |
| [direct-response-copy](./direct-response-copy/) | Direct response copywriting - headlines, landing pages, emails, ads |
| [index](./index/) | Backlink indexing with IndexChex API |

## Installation

**Quick install (single skill):**
```bash
npx degit indexsy/skills/localseo ~/.clawdbot/skills/localseo
npx degit indexsy/skills/ecommerceseo ~/.clawdbot/skills/ecommerceseo
npx degit indexsy/skills/reddit ~/.clawdbot/skills/reddit
npx degit indexsy/skills/direct-response-copy ~/.clawdbot/skills/direct-response-copy
npx degit indexsy/skills/index ~/.clawdbot/skills/index
```

**Clone all skills:**
```bash
git clone https://github.com/indexsy/skills.git
```

**Or reference directly** - point your AI agent to:
```
https://raw.githubusercontent.com/indexsy/skills/main/[skill-name]/SKILL.md
```

## Structure

Each skill folder contains:
- `SKILL.md` - Instructions for the AI agent
- `README.md` - Installation and usage
- Supporting files (templates, frameworks, knowledge bases, etc.)

```
/localseo               # Local SEO audit skill
/ecommerceseo           # E-commerce SEO audit skill
/reddit                 # Reddit organic marketing skill
/direct-response-copy   # Direct response copywriting skill
/index                  # Backlink indexing skill
```

## Contributing

Add new skills by creating a folder with at least `SKILL.md` and `README.md`.

---

Made by [@indexsy](https://github.com/indexsy)
