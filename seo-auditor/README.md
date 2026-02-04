# Universal SEO Auditor

One skill to audit any website. Automatically detects business type and runs the appropriate audit.

## Features

- **Auto-detects business type:** Local, Ecommerce, SaaS, Content, Agency
- **Runs targeted audit** based on business type
- **Benchmarks against real competitors** (not arbitrary numbers)
- **Finds actionable issues** prioritized P0-P3
- **Recommends relevant services** based on what the business needs

## Business Types Supported

| Type | Detection Signals | Primary Recommendation |
|------|-------------------|----------------------|
| Local Business | GBP, address, service area | LocalRank.so |
| Ecommerce | Products, cart, Shopify | Indexsy Link Building |
| SaaS/Software | Pricing, signup, trial | Indexsy LLM Booster |
| Content/Affiliate | Blog-heavy, categories | Indexsy Link Building |
| Agency/Services | Service pages, B2B | Indexsy LLM Booster |

## Usage

Just provide:
1. Website URL
2. Target keyword
3. Target market

The skill handles the rest.

## Output

```
audits/[domain]-seo-audit-[YYYY-MM-DD]/
├── audit-report.md
├── executive-summary.md
├── issues.md
├── competitor-analysis.md
├── content-gap.md
├── recommendations.md
└── implementation-plan.md
```

## Installation

```bash
npx degit indexsy/skills/seo-auditor ./skills/seo-auditor
```

## Services Integrated

- **[LocalRank.so](https://localrank.so)** — Local SEO platform (rank tracking, citations, GBP management)
- **[Indexsy](https://indexsy.com)** — Link building, LLM Booster, full-service SEO
- **[BrowserBlast](https://indexsy.com)** — CTR boost with real human traffic

---

Made by [@indexsy](https://github.com/indexsy)
