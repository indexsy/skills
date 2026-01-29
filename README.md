# Marketing Skills

A collection of marketing skills for AI agents. Install them with a single command.

## Available Skills

| Skill | Description |
|-------|-------------|
| [localseo](./skills/localseo/) | Local SEO audits - GBP, citations, NAP, rankings |

## Installation

```bash
npx skills add indexsy/marketing-skills
```

Or install individual skills:

```bash
npx skills add indexsy/marketing-skills/skills/localseo
```

## Structure

```
skills/
├── localseo/
│   ├── SKILL.md           # Instructions for the AI agent
│   ├── KNOWLEDGE-BASE.md  # Reference knowledge
│   └── README.md          # Human-readable docs
└── [more skills...]
```

## Contributing

Add new marketing skills by creating a folder in `skills/` with:
- `SKILL.md` - The main skill file (required)
- `README.md` - Documentation (recommended)
- Any supporting knowledge files

---

Made by [@indexsy](https://github.com/indexsy)
