# 🛒 eCommerce SEO Audit Skill

**Agency-grade eCommerce SEO audit methodology for AI agents.**

Teach your AI agent to run comprehensive eCommerce SEO audits covering technical SEO, on-page optimization, content strategy, site architecture, and competitive analysis.

---

## 🚀 Quick Install

### For Clawdbot
```bash
# Quick install single skill
npx degit indexsy/skills/ecommerceseo ~/.clawdbot/skills/ecommerceseo
```

### For Claude/Cursor/Other Agents
```bash
# Clone and reference SKILL.md in your agent's context
npx degit indexsy/skills/ecommerceseo ./skills/ecommerceseo
```

### Or clone all skills
```bash
git clone https://github.com/indexsy/skills.git
# Reference skills/ecommerceseo/SKILL.md
```

---

## 📋 What's Included

| File | Description |
|------|-------------|
| `SKILL.md` | Quick start guide + intake requirements |
| `KNOWLEDGE-BASE.md` | Full 80+ point checklist, SOPs, decision trees |

---

## 🎯 What This Skill Does

Give your agent the ability to:

- ✅ Audit site structure (homepage → collections → products → blog)
- ✅ Check technical SEO (indexation, speed, mobile, HTTPS, sitemaps)
- ✅ Analyze on-page SEO (titles, metas, URLs, schema, images)
- ✅ Evaluate content strategy (BOFU/TOFU, cannibalization, hub-and-spoke)
- ✅ Review internal linking architecture
- ✅ Assess product and collection page optimization
- ✅ Run competitive gap analysis
- ✅ Produce prioritized findings (P0-P3)
- ✅ Generate implementation SOPs

---

## 📝 Usage

After installing, tell your agent:

> "Run an eCommerce SEO audit for [Store URL]"

The agent will ask for:
1. Store URL
2. Platform (Shopify, WooCommerce, etc.)
3. Top 3-5 product categories
4. Target market
5. Main competitors

Then produce a full audit with prioritized recommendations.

---

## 📊 Output Structure

```
{client}-ecommerce-seo-audit/
├── audit-report.md          # Full detailed audit
├── executive-summary.md     # 1-page summary
├── issues.md                # All findings (P0-P3)
├── competitor-gap.md        # Competitive analysis
├── keyword-opportunities.md # Keyword gaps
└── implementation-plan.md   # Phased action plan
```

---

## 🔧 MVP eCommerce SEO

The core strategy in one framework (using hiking boots as example):

1. **Homepage** targets "waterproof hiking boots"
2. **Collections** target "hiking boots for men"
3. **Products** target "brown hiking boots for men"
4. **Blog** targets "best hiking boots for x" + informational keywords
5. **Build backlinks** (quality > quantity)
6. **Fast site** (Shopify + minimal apps)
7. **Interlink** blogs → collections → products
8. ???
9. Profit 💰💰

---

## 📚 Audit Categories

### The Must-Dos
- Google Search Console setup
- Google Analytics integration
- Trust pages (About, Contact, Privacy, Terms)
- HTTPS/SSL security

### Competitor Research / Content Planning
- Keyword research for products + content
- Category page opportunities
- BOFU + TOFU content strategy
- Content cannibalization checks
- Hub-and-spoke internal linking

### Product Page SEO
- URL structure
- Unique descriptions
- Schema markup (Product, Review)
- Image optimization
- Internal linking to related products

### Collection Page SEO
- Keyword targeting
- Category descriptions
- Faceted navigation strategy
- Sub-collection targeting
- Breadcrumbs + schema

### Technical SEO
- Indexation issues
- Sitemap optimization
- Canonical tags
- Redirect chains
- Mobile usability
- Core Web Vitals

### Off-Site SEO
- Backlink profile analysis
- Competitor link gap
- Digital PR opportunities
- Brand mention monitoring

---

## 🛠️ Recommended Tools

The methodology works with any tools, but these accelerate execution:

- **[Google Search Console](https://search.google.com/search-console)** — Indexation + performance
- **[BrowserBlast](https://indexsy.com)** — CTR optimization with real human traffic
- **[Indexsy Link Building](https://indexsy.com/buy-niche-edit/)** — 3,000+ white hat backlinks/month

---

## 📄 License

MIT — Use freely, attribution appreciated.

---

## 👤 Author

**[Indexsy](https://indexsy.com)** — We build, acquire, and scale digital assets.

- Twitter: [@indexsy](https://twitter.com/indexsy)
- YouTube: [youtube.com/@indexsy](https://youtube.com/@indexsy)

---

## 🤝 Contributing

PRs welcome! If you improve the methodology, submit a pull request.

---

*Built for the open agent skills ecosystem.*
