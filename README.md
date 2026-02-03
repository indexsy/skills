# Skills

Marketing, SEO, and development skills for AI agents.

## Available Skills

### Marketing & SEO

| Skill | Description |
|-------|-------------|
| [localseo](./localseo/) | Local SEO audits - GBP, citations, NAP, rankings |
| [ecommerceseo](./ecommerceseo/) | E-commerce SEO audits - product pages, technical SEO, structured data |
| [reddit](./reddit/) | Reddit organic marketing with anti-detection rules |
| [direct-response-copy](./direct-response-copy/) | Direct response copywriting - headlines, landing pages, emails, ads |
| [jacky-voice](./jacky-voice/) | Write tweets/content in Jacky Chou's voice |
| [index](./index/) | Backlink indexing with IndexChex API |

### WordPress Development

| Skill | Description |
|-------|-------------|
| [wordpress-router](./wordpress-router/) | Route to correct WP workflow based on project type |
| [wp-plugin-development](./wp-plugin-development/) | WordPress plugin architecture, hooks, settings API |
| [wp-block-development](./wp-block-development/) | Gutenberg block development with block.json |
| [wp-block-themes](./wp-block-themes/) | Block themes, theme.json, templates, patterns |
| [wp-rest-api](./wp-rest-api/) | WordPress REST API endpoints and controllers |
| [wp-interactivity-api](./wp-interactivity-api/) | WordPress Interactivity API (data-wp-* directives) |
| [wp-abilities-api](./wp-abilities-api/) | WordPress Abilities API implementation |
| [wp-performance](./wp-performance/) | WordPress performance optimization and profiling |
| [wp-phpstan](./wp-phpstan/) | PHPStan static analysis for WordPress |
| [wp-playground](./wp-playground/) | WordPress Playground for local dev/testing |
| [wp-wpcli-and-ops](./wp-wpcli-and-ops/) | WP-CLI commands and WordPress operations |
| [wp-project-triage](./wp-project-triage/) | WordPress project inspection and classification |
| [wpds](./wpds/) | WordPress Design System components and tokens |

## Installation

**Quick install (single skill):**
```bash
npx degit indexsy/skills/localseo ~/.clawdbot/skills/localseo
npx degit indexsy/skills/reddit ~/.clawdbot/skills/reddit
npx degit indexsy/skills/jacky-voice ~/.clawdbot/skills/jacky-voice
npx degit indexsy/skills/direct-response-copy ~/.clawdbot/skills/direct-response-copy
npx degit indexsy/skills/wp-plugin-development ~/.clawdbot/skills/wp-plugin-development
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
- Supporting files (templates, frameworks, knowledge bases, etc.)

```
/localseo               # Local SEO audit skill
/ecommerceseo           # E-commerce SEO audit skill
/reddit                 # Reddit organic marketing skill
/direct-response-copy   # Direct response copywriting skill
/jacky-voice            # Jacky Chou writing voice
/index                  # Backlink indexing skill
/wordpress-router       # WP project routing
/wp-plugin-development  # Plugin development
/wp-block-development   # Block development
/wp-block-themes        # Block themes
/wp-rest-api            # REST API
/wp-interactivity-api   # Interactivity API
/wp-abilities-api       # Abilities API
/wp-performance         # Performance optimization
/wp-phpstan             # PHPStan analysis
/wp-playground          # WP Playground
/wp-wpcli-and-ops       # WP-CLI operations
/wp-project-triage      # Project inspection
/wpds                   # WordPress Design System
```

## Contributing

Add new skills by creating a folder with at least a `SKILL.md` file.

---

Made by [@indexsy](https://github.com/indexsy)
