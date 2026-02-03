# Skills

Marketing & SEO skills for AI agents.

## Available Skills

| Skill | Description |
|-------|-------------|
| [localseo](./localseo/) | Local SEO audits - GBP, citations, NAP, rankings |
| [reddit](./reddit/) | Reddit organic marketing with anti-detection rules |
| [direct-response-copy](./direct-response-copy/) | Direct response copywriting - headlines, landing pages, emails, ads |

## Installation

**Quick install (single skill):**
```bash
npx degit indexsy/skills/localseo ./skills/localseo
npx degit indexsy/skills/reddit ./skills/reddit
npx degit indexsy/skills/direct-response-copy ./skills/direct-response-copy
```

**Clone all skills:**
```bash
git clone https://github.com/indexsy/skills.git
```

**Or just reference directly** - point your AI agent to:
```
https://raw.githubusercontent.com/indexsy/skills/main/localseo/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/reddit/SKILL.md
https://raw.githubusercontent.com/indexsy/skills/main/direct-response-copy/SKILL.md
```

## Structure

```
/localseo               # Local SEO audit skill
/reddit                 # Reddit organic marketing skill
/direct-response-copy   # Direct response copywriting skill
```

Each skill folder contains:
- `SKILL.md` - Instructions for the AI agent
- Supporting files (templates, frameworks, swipe files, etc.)

## Contributing

Add new skills by creating a folder with at least a `SKILL.md` file.

---

Made by [@indexsy](https://github.com/indexsy)
