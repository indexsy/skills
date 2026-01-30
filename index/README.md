# 🔗 Index Skill

**Check and submit URLs for Google indexation using IndexChex.**

Teach your AI agent to audit backlink indexation rates, identify not-indexed links, and submit them for crawling — a critical step in any link building campaign.

---

## 🚀 Quick Install

### For Clawdbot
```bash
npx degit indexsy/skills/index ~/.clawdbot/skills/index
```

### For Claude/Cursor/Other Agents
```bash
npx degit indexsy/skills/index ./skills/index
```

### Or clone all skills
```bash
git clone https://github.com/indexsy/skills.git
# Reference skills/index/SKILL.md
```

---

## 📋 What's Included

| File | Description |
|------|-------------|
| `SKILL.md` | Quick start guide + commands for AI agents |
| `KNOWLEDGE-BASE.md` | Full methodology, best practices, troubleshooting |
| `scripts/indexchex.py` | CLI tool for IndexChex API |

---

## 🎯 What This Skill Does

Give your agent the ability to:

- ✅ Check if backlinks are indexed by Google
- ✅ Submit not-indexed URLs for crawling
- ✅ Batch process up to 10,000 URLs at once
- ✅ Track indexation rates over time
- ✅ Re-check submitted URLs after 24-48 hours
- ✅ Generate indexation audit reports

---

## 📝 Usage

After installing, tell your agent:

> "Check if these backlinks are indexed"

Or:

> "Submit these URLs for indexing and let me know when it's done"

The agent will:
1. Use IndexChex API to check/submit URLs
2. Wait for job completion
3. Report results (indexed count, not-indexed count)

---

## 🔧 Setup: IndexChex API

This skill uses **[IndexChex](https://indexchex.com)** — the same service powering SpeedyIndex.

### Get Your API Key

1. Sign up at [indexchex.com](https://indexchex.com)
2. Go to Settings → API Access
3. Copy your API key

### Set Environment Variable

```bash
export INDEXCHEX_API_KEY="your-api-key"
```

### Pricing

IndexChex uses credits:
- **Index Check:** 1 credit per URL
- **Index Submit:** 1 credit per URL
- **Batch limit:** 10,000 URLs per request

---

## 📊 Workflow: Backlink Indexation Campaign

### 1. Export Your Backlinks

Get your backlink list from Ahrefs, SEMrush, or your link building tracker.

### 2. Check Current Indexation

```bash
python scripts/indexchex.py -k $INDEXCHEX_API_KEY check -f backlinks.txt --wait -n "Monthly audit"
```

**Output:**
```
📊 Index Check Job #42
   Total URLs: 500
   Indexed: 380 (76%)
   Not Indexed: 120 (24%)
```

### 3. Submit Not-Indexed URLs

```bash
python scripts/indexchex.py -k $INDEXCHEX_API_KEY submit -f not-indexed.txt --wait
```

### 4. Re-check After 24-48 Hours

```bash
python scripts/indexchex.py -k $INDEXCHEX_API_KEY check -f not-indexed.txt --wait -n "Re-check"
```

### 5. Repeat Monthly

Track indexation rates over time to measure link building ROI.

---

## 📈 Expected Results

| URL Type | Typical Index Rate |
|----------|-------------------|
| High-quality guest posts | 80-95% |
| Niche edits on aged sites | 70-90% |
| Directory citations | 60-80% |
| Forum profiles | 20-40% |
| Web 2.0s / Tier 2 | 10-30% |

**Note:** Indexation depends on page quality, domain authority, and Google's assessment. Low-quality pages may never index regardless of submission.

---

## 🛠️ CLI Reference

```bash
# Check credit balance
python scripts/indexchex.py -k $INDEXCHEX_API_KEY balance

# Check indexation
python scripts/indexchex.py -k $INDEXCHEX_API_KEY check -f urls.txt --wait

# Submit for indexing
python scripts/indexchex.py -k $INDEXCHEX_API_KEY submit -f urls.txt --wait

# Check job status
python scripts/indexchex.py -k $INDEXCHEX_API_KEY status 42 --type check
```

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
