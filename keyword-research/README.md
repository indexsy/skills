# Keyword Research

Advanced keyword research with tangential relevance discovery, SERP-based clustering, search volume filtering, and cannibalization detection.

## What It Does

- **Tangential Discovery** — Finds semantically related keywords beyond exact matches
- **Question Mining** — Answer The Public-style question keyword expansion
- **Multi-Platform** — Expands beyond Google (YouTube, Amazon, Bing)
- **SERP Clustering** — Groups keywords by actual search intent using 3 algorithms
- **Volume Filtering** — Only keywords with 50+ monthly searches (configurable)
- **Cannibalization Detection** — Identifies keywords with overlapping SERP intent

## Usage

Activate the skill, then request research:

```
"Find tangential keywords for organic coffee, minimum 100 searches/month"

"Research keywords for e-commerce, use BALANCED STRICT clustering"

"Cluster keywords by SERP overlap, CPC-based primary selection"

"Check cannibalization between: 'best coffee maker' and 'top coffee machines'"
```

## Clustering Algorithms

### DEFAULT (Fast & Broad)
- Keyword joins cluster if it shares X URLs with **primary keyword only**
- Best for: Large datasets (100K+ keywords)
- Speed: Fastest

### STRICT (Tight & Precise)
- Keyword must share X URLs with **ALL cluster members**
- Best for: Competitive niches
- Speed: 2-3x slower
- May create many single-keyword clusters

### BALANCED STRICT (Recommended)
- Progressive thresholds:
  - 2-5 keywords: 100% match required
  - 6-10 keywords: 80% match
  - 11+ keywords: 60% match
- Best for: Most use cases
- Speed: Moderate

## Primary Keyword Selection

**Volume-Based (default):**
- Select highest search volume in cluster
- Best for: Traffic-focused strategies

**CPC-Based:**
- Select highest cost-per-click in cluster
- Best for: Commercial keywords, e-commerce, PPC planning

## Cannibalization Detection

Compares SERP results between keyword pairs:
- Get top 10 results for each keyword
- Calculate URL overlap percentage
- If overlap > 70%, flag as **CANNIBALIZING**
- Group flagged keywords — target ONE per group

## Example Output

```
## Keyword Research: Organic Coffee

### Summary
- Total keywords: 1,247
- Clusters formed: 34
- Cannibalization alerts: 3

### Top Clusters

#### Cluster 1: best organic coffee beans (Volume: 2,400)
| Keyword | Volume | Difficulty | CPC | Intent |
|---------|--------|------------|-----|--------|
| best organic coffee beans | 2,400 | Medium | $2.50 | Commercial |
| organic coffee beans | 1,800 | Low | $1.80 | Commercial |
| top rated organic coffee | 890 | Low | $1.20 | Commercial |

**Action:** Target all with ONE page

### Cannibalization Alerts
- **Group A**: "organic coffee" vs "organic coffee beans" — 82% overlap — Pick one

### Question Opportunities
| Keyword | Volume | Difficulty | Source |
|---------|--------|------------|--------|
| how to brew organic coffee | 320 | Low | People Also Ask |
| is organic coffee worth it | 180 | Low | People Also Ask |
```

## Data Sources

- **Volume/Difficulty/CPC**: DataForSEO, Ahrefs, SEMrush
- **SERP Data**: DataForSEO SERP API (~$0.60/1000 keywords), SerpAPI
- **Multi-Platform**: YouTube API, Amazon autocomplete, Bing API

## Configuration Options

| Option | Default | Description |
|--------|---------|-------------|
| Algorithm | BALANCED STRICT | DEFAULT, STRICT, or BALANCED STRICT |
| Similarity Threshold | 4 URLs | 3-7 shared URLs required |
| Min Volume | 50/month | Filter threshold |
| Primary Method | Volume | Volume or CPC |
| SERP Data Age | 7 days | Reuse saved data |

## Requirements

API access recommended:
- DataForSEO (volume, CPC, SERP data)
- Proxies (for large-scale scraping)

Without APIs: Uses search-based estimation and manual analysis (slower, less accurate).
