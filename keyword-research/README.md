# Keyword Research

Advanced keyword research with tangential relevance discovery, search volume filtering, and cannibalization detection.

## What It Does

- **Tangential Discovery** — Finds semantically related keywords beyond exact matches
- **Volume Filtering** — Only keywords with 50+ monthly searches (configurable)
- **Cannibalization Detection** — Identifies keywords with overlapping SERP intent

## Usage

Activate the skill, then request research:

```
"Find tangential keywords for [topic], minimum 100 searches/month"

"Research keywords for organic coffee brand, avoid cannibalizing with existing: 'best organic coffee'"

"Find keyword opportunities for e-commerce site selling [product]"
```

## How It Works

### 1. Tangential Expansion
Finds keywords through:
- Google Autocomplete suggestions
- People Also Ask questions
- Related searches
- Semantic topic adjacencies

### 2. Volume Validation
Filters out keywords below your minimum threshold (default: 50/month).

### 3. Cannibalization Detection
Compares SERP results between keyword pairs:
- If top 10 results have >70% URL overlap → CANNIBALIZING
- Groups flagged keywords — you target ONE per group

## Example Output

```
## Keyword Research: Organic Coffee

### Primary Keywords
| Keyword | Volume | Difficulty | Intent |
|---------|--------|------------|--------|
| best organic coffee | 2,400 | Medium | Commercial |
| organic coffee beans | 1,800 | Low | Commercial |

### Tangential Opportunities
| Keyword | Volume | Difficulty | Cannibalization |
|---------|--------|------------|-----------------|
| morning energy without jitters | 320 | Low | - |
| sustainable coffee farming | 180 | Medium | Group A |
| eco friendly coffee brands | 150 | Low | Group A |

### Cannibalization Alerts
- **Group A**: "sustainable coffee farming" vs "eco friendly coffee brands" → Pick one

### Recommendations
1. Target "best organic coffee" first (highest volume, clear intent)
2. Create content for "morning energy without jitters" (tangential opportunity)
3. Choose ONE from Group A — recommend "eco friendly coffee brands" (lower difficulty)
```

## Data Sources

- **Volume/Difficulty**: DataForSEO, Ahrefs, SEMrush, or Google Keyword Planner
- **SERP Data**: SerpAPI or similar for cannibalization checks

## Requirements

API access recommended for:
- Keyword volume data
- SERP result fetching (for cannibalization detection)

Without APIs, skill uses search-based estimation and manual overlap analysis.