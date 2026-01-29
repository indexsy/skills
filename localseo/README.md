# 🗺️ Local SEO Audit Skill

**Agency-grade local SEO audit methodology for AI agents.**

Teach your AI agent to run comprehensive local SEO audits covering Google Business Profile, citations, NAP consistency, reviews, and competitive analysis.

---

## 🚀 Quick Install

### For Clawdbot
```bash
# Clone into your skills folder
git clone https://github.com/indexsy/local-seo-skill ~/.clawdbot/skills/local-seo-audit
```

### For Claude/Cursor/Other Agents
```bash
# Clone and reference SKILL.md in your agent's context
git clone https://github.com/indexsy/local-seo-skill
```

---

## 📋 What's Included

| File | Description |
|------|-------------|
| `SKILL.md` | Quick start guide + intake requirements |
| `KNOWLEDGE-BASE.md` | Full methodology, SOPs, decision trees |

---

## 🎯 What This Skill Does

Give your agent the ability to:

- ✅ Audit NAP (Name/Address/Phone) consistency across web
- ✅ Analyze Google Business Profile completeness
- ✅ Check citation coverage (Yelp, Facebook, Apple, Bing, etc.)
- ✅ Evaluate review velocity and reputation
- ✅ Run competitive gap analysis
- ✅ Produce prioritized findings (P0-P3)
- ✅ Generate implementation SOPs

---

## 📝 Usage

After installing, tell your agent:

> "Run a local SEO audit for [Business Name]"

The agent will ask for:
1. Business name
2. Address
3. Phone number
4. Website URL
5. Top 3-5 services
6. Target city/area

Then produce a full audit with prioritized recommendations.

---

## 📊 Output Structure

```
{client}-local-seo-audit/
├── audit-report.md          # Full detailed audit
├── executive-summary.md     # 1-page summary
├── issues.md                # All findings (P0-P3)
├── competitor-gap.md        # Competitive analysis
└── implementation-plan.md   # Phased action plan
```

---

## 🔧 Methodology

Based on the **3 Forces of Local SEO**:

1. **Relevance** — How well the business matches the query
2. **Distance** — Proximity to searcher
3. **Prominence** — Authority and trust signals

### Priority Order

1. Identity + Trust Foundations (NAP, citations)
2. Google Business Profile optimization
3. Local website reinforcement
4. Reviews + reputation system
5. Authority signals (mentions, links)
6. Competitive gap closure

---

## 🛠️ Recommended Tools

The methodology works with any tools, but these accelerate execution:

- **[LocalRank.so](https://localrank.so)** — Citations, LLM citations, rank tracking grids
- **Google Search Console** — Organic visibility
- **Schema validators** — Structured data checks

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
