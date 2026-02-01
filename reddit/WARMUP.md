# Reddit Account Warmup

> Warmup workflow for Reddit accounts using auto-commenter framework.
> Each account has unique persona. Run daily via cron or "Warm up Reddit accounts".

---

## Trigger Commands

- "Warm up Reddit accounts"
- "Run Reddit warmup"
- "Fill warmup quota"

---

## Pre-Start Check

```
1. Read memory/reddit-accounts.md for account list
2. Check tracking/reddit/YYYY-MM-DD.md for today's activity
3. Calculate remaining quota per account:
   - Week 1-2: Browse only + reply to own viral post comments
   - Week 3+: Max 2 comments/day in home sub only
   - Week 5+: Can expand to r/all browsing
```

---

## Warmup Phases (Per Account)

| Phase | Duration | Activity |
|-------|----------|----------|
| 1 | Week 1 | Reply to comments on own viral post ONLY |
| 2 | Weeks 1-2 | Browse home sub 5-30 min/day, max 1 comment/week |
| 3 | Week 3-4 | Home sub only, max 2 comments/day |
| 4 | Week 5+ | Expand to r/all, general engagement |

---

## Batch Workflow

```
[Start]
    ↓
[1] Load account list from memory/reddit-accounts.md
    ↓
[2] For each account with remaining quota:
    ↓
    [2-1] Start MoreLogin profile (API: POST /api/env/start)
    [2-2] Connect browser to debug port
    [2-3] Load account persona from personas/[account].md
    [2-4] Check warmup phase (based on warmup start date)
    [2-5] Execute phase-appropriate activity:
          - Phase 1: Check viral post for new comments, reply if any
          - Phase 2-3: Browse home sub, find post, write comment
          - Phase 4: Browse r/all, engage naturally
    [2-6] Update tracking/reddit/YYYY-MM-DD.md
    [2-7] Close MoreLogin profile
    [2-8] Wait 2-5 minutes before next account
    ↓
[3] Generate completion report
    ↓
[End]
```

---

## Comment Writing Rules

### STRICT RULES (All Accounts)
- ❌ **NO EM DASHES (—)** - Never use em dashes, use commas or periods instead
- ❌ No AI-sounding phrases ("I'd be happy to", "Great question!")
- ❌ No marketing language
- ❌ No links unless absolutely natural
- ✅ Match the persona's unique voice (see personas/)
- ✅ Include typos/casual language occasionally
- ✅ Keep it short (1-3 sentences usually)
- ✅ Sound like a real person

### Per-Account Persona
Each account has unique writing style in `personas/[account].md`:
- Vocabulary preferences
- Sentence structure patterns
- Emoji usage (or not)
- Casual vs formal tone
- Interests reflected in comments

---

## Single Comment Workflow (Within Batch)

### Step 1: Navigate to Target
```
Phase 1-3: browser_navigate("reddit.com/r/{home_sub}/new/")
Phase 4: browser_navigate("reddit.com/r/all/rising/")
```

### Step 2: Find Suitable Post
```
Criteria:
- Has < 50 comments (not oversaturated)
- Posted within last 24 hours
- Topic matches account interests (from persona)
- NOT already commented on today (check tracking)
```

### Step 3: Analyze Post
```
- Read post content fully
- Understand what OP wants
- Check existing comments for tone
- Decide if comment adds value
```

### Step 4: Write Comment (Using Persona)
```
1. Load personas/[account].md
2. Draft comment matching persona voice
3. Verify NO em dashes
4. Keep authentic and short
```

### Step 5: Post & Track
```
1. Click comment box, type, submit
2. Copy comment permalink
3. Update tracking/reddit/YYYY-MM-DD.md
```

---

## Tracking File Format

`tracking/reddit/YYYY-MM-DD.md`:

```markdown
# Reddit Warmup - YYYY-MM-DD

## Summary
| Account | Phase | Home Sub | Comments | Browse Time |
|---------|-------|----------|----------|-------------|
| Laura-Cockerha | 1 | r/MVAgusta | 0 | 12 min |
| Michele-Speer | 1 | r/sunflowers | 1 | 8 min |

## Activity Log

### [HH:MM] Laura-Cockerha
- **Action**: Browsed r/MVAgusta
- **Duration**: 12 minutes
- **Posts viewed**: 5
- **Comments**: 0

### [HH:MM] Michele-Speer
- **Action**: Commented on r/sunflowers
- **Post**: [Title](URL)
- **Comment**: "love the colors on this one"
- **Permalink**: [link]
```

---

## Error Handling

| Error | Response |
|-------|----------|
| MoreLogin profile won't start | Skip account, note in log |
| Reddit rate limit | Wait 10 min, retry once |
| Account suspended | STOP, alert Jacky immediately |
| Proxy blocked | Skip account, note for proxy rotation |
| No suitable posts | Browse only, skip commenting |

---

## Completion Report

```
---
## Warmup Completion - YYYY-MM-DD

**Accounts processed**: 8/10
**Total browse time**: 47 minutes
**Comments posted**: 3

### Per Account
| Account | Status | Activity |
|---------|--------|----------|
| Laura-Cockerha | ✅ | Browsed 12 min |
| Michele-Speer | ✅ | Commented 1x |
| Matilda-Seth | ⏸️ | Skipped (LOW TRUST) |

### Issues
- LoreneK_Walker: Still needs viral post
---
```

---

## Files Reference

| File | Purpose |
|------|---------|
| `personas/[account].md` | Unique writing style per account |
| `tracking/reddit/YYYY-MM-DD.md` | Daily activity log |
| `memory/reddit-accounts.md` | Account list + status |
| `memory/reddit-warmup-sop.md` | Warmup phases detail |
