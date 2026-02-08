---
name: keyword-research
description: Advanced keyword research with tangential relevance discovery, SERP-based clustering, search volume filtering (50+ monthly), and cannibalization detection. Use when researching keywords for SEO content strategy, finding untapped keyword opportunities, building topic clusters, or detecting keyword cannibalization. Triggers on requests like "find keywords for [topic]", "keyword research", "find tangential keywords", "check for keyword cannibalization", or "cluster keywords".
---

# Keyword Research Skill

Advanced keyword research with tangential relevance, SERP clustering, volume filtering, and cannibalization detection.

## Overview

This skill finds keywords that are:
- **Tangentially relevant** (semantically related, not just exact matches)
- **Have search volume** (minimum 50 searches/month by default)
- **SERP-clustered** (grouped by actual search intent based on overlapping results)
- **Non-cannibalizing** (unique intent, not overlapping with existing targets)

## Workflow

### 1. Gather Inputs

Required:
- **Seed topic/brand** — main subject or domain
- **Target geography** (optional, default: US)

Optional:
- **Minimum volume** — default 50/month
- **Maximum difficulty** — if specified
- **Existing keywords** — to check for cannibalization
- **Primary selection method** — volume (default) or CPC (for commercial keywords)

### 2. Expand Keywords

Find tangentially relevant keywords using:

#### 2.1 Google-Based Sources
- **Autocomplete** — related searches as you type
- **People Also Ask** — question variations
- **Related searches** — bottom of SERP
- **SERP features** — featured snippets, knowledge panels

#### 2.2 Question Mining (Answer The Public style)
Generate question variations using modifiers:
- **How** — how to, how do, how can
- **What** — what is, what are, what does
- **Why** — why is, why do, why does
- **When** — when to, when is, when should
- **Where** — where to, where is, where can
- **Who** — who is, who can, who should
- **Which** — which is, which are, which should
- **Comparison** — vs, versus, or, alternative

#### 2.3 Multi-Platform Expansion
Expand beyond Google:
- **YouTube** — video-specific searches
- **Amazon** — buyer intent keywords
- **Bing** — different autocomplete suggestions
- **Reddit** — discussion-based queries

#### 2.4 Semantic Adjacencies
Find topic adjacencies (e.g., for "coffee"):
- Adjacent problems: "morning energy", "productivity tips"
- Upstream topics: "coffee bean roasting", "grinder reviews"
- Downstream topics: "coffee storage", "stain removal"
- Comparisons: "coffee vs tea", "espresso vs drip"
- Alternatives: "energy drinks", "caffeine pills"

### 3. Filter by Volume

Remove keywords with < 50 monthly searches (or custom threshold).

### 4. SERP Clustering

Group keywords by search intent using SERP overlap analysis.

#### 4.1 Clustering Algorithms

**DEFAULT Algorithm (Fast & Broad)**
- Keyword joins cluster if it shares X URLs with the **primary keyword only**
- Best for: Large datasets (100K+ keywords), content hubs
- Speed: Fastest
- Output: Broader topic clusters

**STRICT Algorithm (Tight & Precise)**
- Keyword joins cluster only if it shares X URLs with **ALL existing cluster members**
- Best for: Competitive niches, precise targeting
- Speed: Slower (2-3x)
- Output: Highly relevant clusters, but may create many single-keyword clusters due to "first-mover advantage"

**BALANCED STRICT Algorithm (Recommended)**
- Solves STRICT's "first-mover advantage" problem
- Progressive thresholds:
  - Small clusters (2-5 keywords): requires 100% match
  - Medium clusters (6-10): requires 80% match
  - Large clusters (11+): requires 60% match
- Best for: Most use cases (balanced quality and natural growth)
- Speed: Moderate (2-3x slower than DEFAULT)
- Output: Quality clusters that can grow naturally

#### 4.2 Similarity Threshold
- Range: 3-7 shared URLs in top 10 results
- Default: 4 shared URLs
- Higher number = more strict relevance
- Adjust based on desired cluster tightness

#### 4.3 Primary Keyword Selection

**Volume-Based (default):**
- Select keyword with highest search volume in cluster
- Best for: Content planning, traffic-focused strategies

**CPC-Based (for commercial keywords):**
- Select keyword with highest cost-per-click in cluster
- Best for: E-commerce, transactional intent, PPC planning

### 5. Cannibalization Detection

Check if new keywords cannibalize with existing targets:

**Logic:**
1. Get top 10 organic results for existing keyword
2. Get top 10 organic results for new keyword
3. Calculate overlap: `(shared URLs / total unique URLs) × 100`
4. If overlap > 70%, flag as **CANNIBALIZING**
5. User should target ONE per cannibalization group

**Example:**
- "best coffee maker" vs "top rated coffee machines" → likely cannibalizing
- "best coffee maker" vs "how to clean coffee maker" → NOT cannibalizing

### 6. Re-Clustering

When adding new keywords to existing research:
- Use saved SERP data (configurable age: 1-30 days)
- Distribute new keywords into existing clusters
- Mark new additions with "New" badge
- Track which run added each keyword ("Run #")
- Avoids rebuilding all clusters from scratch

### 7. Output Format

```
## Keyword Research Results: [Topic]

### Summary
- Total keywords analyzed: X
- Clusters formed: Y
- Cannibalization alerts: Z

### Top Clusters (by volume)

#### Cluster 1: [Primary Keyword] (Volume: X)
| Keyword | Volume | Difficulty | CPC | Intent |
|---------|--------|------------|-----|--------|
| primary keyword | 2,400 | Medium | $2.50 | Commercial |
| related kw 1 | 1,200 | Low | $1.80 | Commercial |
| related kw 2 | 890 | Low | $1.20 | Informational |

**Recommended action:** Target all with ONE comprehensive page

---

#### Cluster 2: [Primary Keyword] (Volume: X)
...

### Cannibalization Alerts
- **Group A**: [keyword1] vs [keyword2] — 85% overlap — Pick one
- **Group B**: [keyword3] vs [keyword4] vs [keyword5] — 72% overlap — Pick one

### Tangential Opportunities (Low Competition)
| Keyword | Volume | Difficulty | Source |
|---------|--------|------------|--------|
| question-based kw | 320 | Low | People Also Ask |
| comparison kw | 180 | Low | Semantic |

### Recommendations
1. Target Cluster 1 first (highest volume, commercial intent)
2. Avoid Group A keywords — cannibalizing with existing content
3. Create FAQ content for question-based opportunities
```

## Tools & APIs

**For keyword expansion:**
- DataForSEO API (recommended for volume/difficulty/CPC)
- Ahrefs API
- SEMrush API
- Google Keyword Planner (limited)

**For SERP scraping:**
- DataForSEO SERP API (recommended, ~$0.60 per 1000 keywords)
- SerpAPI
- Proxies + custom scraper (for large volumes)

**For multi-platform:**
- YouTube API (for video keywords)
- Amazon autocomplete scraper
- Bing API

## Best Practices

### When to Use Each Algorithm

| Algorithm | Use When | Dataset Size |
|-----------|----------|--------------|
| DEFAULT | Need broad topics, have 100K+ keywords | 50K-200K |
| STRICT | Competitive niche, need precision | 5K-20K |
| BALANCED STRICT | Most cases (recommended) | 10K-100K |

### When to Use CPC-Based Primary Selection

Use CPC instead of volume when:
- Keywords are transactional/commercial
- You're planning PPC campaigns
- Revenue per visitor matters more than volume
- E-commerce or lead gen focus

### Similarity Threshold Guidelines

| Threshold | Result | Use Case |
|-----------|--------|----------|
| 3 URLs | Loose clusters | Maximum coverage |
| 4 URLs | Balanced | Default choice |
| 5-6 URLs | Tight clusters | High relevance |
| 7 URLs | Very strict | Minimal cannibalization |

## Example Request

"Find tangential keywords for an organic coffee brand, minimum 100 searches/month, use BALANCED STRICT clustering, CPC-based primary selection, check cannibalization with existing keywords: 'best organic coffee', 'fair trade coffee beans'"

**Output includes:**
- Clusters formed by SERP overlap
- Primary keywords selected by CPC
- Cannibalization groups with existing keywords
- Question-based opportunities from People Also Ask
- Multi-platform suggestions (Amazon, YouTube)
