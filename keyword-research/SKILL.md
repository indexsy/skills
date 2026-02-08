---
name: keyword-research
description: Advanced keyword research with tangential relevance discovery, search volume filtering (50+ monthly), and cannibalization detection. Use when researching keywords for SEO content strategy, finding untapped keyword opportunities, or building topic clusters. Triggers on requests like "find keywords for [topic]", "keyword research", "find tangential keywords", or "check for keyword cannibalization".
---

# Keyword Research Skill

Advanced keyword research with tangential relevance, volume filtering, and cannibalization detection.

## Overview

This skill finds keywords that are:
- **Tangentially relevant** (semantically related, not just exact matches)
- **Have search volume** (minimum 50 searches/month by default)
- **Non-cannibalizing** (unique SERP intent, not overlapping with existing targets)

## Workflow

### 1. Gather Inputs

Required:
- **Seed topic/brand** — main subject or domain
- **Target geography** (optional, default: US)

Optional:
- **Minimum volume** — default 50/month
- **Maximum difficulty** — if specified
- **Existing keywords** — to check for cannibalization

### 2. Expand Keywords

Find tangentially relevant keywords using:
- **Google Autocomplete** — related searches
- **People Also Ask** — question variations
- **Related searches** — bottom of SERP
- **Semantic variations** — topic adjacencies (e.g., for "coffee": "espresso machines", "morning routines", "caffeine alternatives")

**Tangential keyword patterns:**
- Adjacent problems (what else do they search for?)
- Upstream/downstream topics (before/after in buyer journey)
- Comparison searches (vs, alternatives, best)
- Question modifiers (how, why, what, when)

### 3. Filter by Volume

Remove keywords with < 50 monthly searches (or custom threshold).

### 4. Detect Cannibalization

For each keyword pair, check SERP overlap:

**Cannibalization Detection Logic:**
1. Get top 10 organic results for Keyword A
2. Get top 10 organic results for Keyword B
3. Calculate overlap: `(shared URLs / total unique URLs) × 100`
4. If overlap > 70%, flag as **CANNIBALIZING**
5. Group cannibalizing keywords together — user should pick ONE per group

**Example:**
- "best coffee maker" and "top rated coffee machines" → likely cannibalizing
- "best coffee maker" and "how to clean coffee maker" → NOT cannibalizing

### 5. Output Format

```
## Keyword Research Results: [Topic]

### Primary Keywords (High Priority)
| Keyword | Volume | Difficulty | Intent | Cannibalization Group |
|---------|--------|------------|--------|----------------------|
| ... | ... | ... | ... | - |

### Tangential Opportunities
| Keyword | Volume | Difficulty | Intent | Cannibalization Group |
|---------|--------|------------|--------|----------------------|
| ... | ... | ... | ... | Group A |

### Cannibalization Alerts
- **Group A**: [keyword1] vs [keyword2] — Pick one
- **Group B**: [keyword3] vs [keyword4] vs [keyword5] — Pick one

### Recommendations
1. Target [keyword] first (highest volume, non-cannibalizing)
2. Avoid [keyword2] — cannibalizes with [keyword1]
3. Consider [tangential keyword] for content expansion
```

## Tools & APIs

**For volume/difficulty data:**
- DataForSEO API (recommended)
- Ahrefs API
- SEMrush API
- Google Keyword Planner (limited)

**For cannibalization detection:**
- SerpAPI or similar for SERP fetching
- Custom overlap calculation

## Example Request

"Find tangential keywords for an organic coffee brand, minimum 100 searches/month, avoid cannibalization with existing keywords: 'best organic coffee', 'fair trade coffee beans'"

**Output would include:**
- Related: "single origin coffee", "shade grown coffee"
- Tangential: "morning energy without jitters", "sustainable farming practices"
- Cannibalization check: "best organic coffee" vs "top organic coffee" → flag as group
