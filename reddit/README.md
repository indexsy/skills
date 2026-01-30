# 📣 Reddit Marketing Skill

**Systematic Reddit placement methodology for AI agents.**

Teach your AI agent to find high-intent Reddit threads, craft authentic comments, and scale brand mentions while staying undetected.

---

## 🚀 Quick Install

### For Clawdbot
```bash
# Clone into your skills folder
git clone https://github.com/indexsy/skills ~/.clawdbot/skills/reddit
```

### For Claude/Cursor/Other Agents
```bash
# Clone and reference SKILL.md in your agent's context
npx degit indexsy/skills/reddit ./skills/reddit
```

---

## 📋 What's Included

| File | Description |
|------|-------------|
| `SKILL.md` | Quick start guide + workflow |
| `KNOWLEDGE-BASE.md` | Full methodology, anti-detection rules, examples |

---

## 🎯 What This Skill Does

Give your agent the ability to:

- 🔍 Find high-intent threads (buyer queries, comparisons, reviews)
- ✍️ Craft genuine, helpful comments with soft brand mentions
- 🛡️ Stay undetected with anti-pattern rules
- 📊 Track placements and maintain winners
- 📈 Scale safely with account rotation

---

## 📝 Usage

After installing, tell your agent:

> "Run a Reddit placement campaign for [product/brand] targeting [keywords]"

The agent will ask for:
1. Product/brand being mentioned
2. Target keywords (buyer intent queries)
3. Vertical/niche category
4. Constraints (forbidden claims, link rules)

Then produce opportunity lists, comments, and tracking.

---

## 📊 Output Structure

```
{project}-reddit/
├── opportunity_list.md      # Threads to target
├── placement_log.md         # Posted comments + status
├── subreddit_tone_maps.md   # Community notes
├── comment_templates.md     # Reusable patterns
└── account_health.md        # Karma, activity tracking
```

---

## 🔧 Methodology

### Anti-Detection Rules

| Red Flag | Why It Burns Accounts |
|----------|----------------------|
| Aged account + low karma | 1yr old with 2 karma = obvious bot |
| AI-sounding content | Robotic phrasing, perfect grammar |
| Only GEO subs | Low-mod subs are watched |
| Pattern posting | Same times, same subs, same style |

### Account Health Requirements

| Metric | Minimum | Ideal |
|--------|---------|-------|
| Karma | 100+ | 500+ |
| Account age | 30 days | 6+ months |
| Genuine comments | 20+ | 50+ |
| Subreddit diversity | 5+ subs | 10+ subs |

### Cadence Rules

- **1 comment per account per week MAXIMUM**
- 10 accounts = 10 placements/week max
- **80/20 rule**: 80% genuine engagement, 20% strategic
- Never batch posts in same subreddit from multiple accounts

---

## 💬 Comment Template (5-Part)

1. **Empathy hook** — Mirror OP's situation
2. **Context** — What you tried/decided between
3. **Helpful breakdown** — Pros/cons, tradeoffs
4. **Soft recommendation** — Mention brand naturally
5. **Exit line** — Offer to answer questions

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
