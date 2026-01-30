# X Bookmarks Processing Strategy

*Created: 2026-01-25*

## Goal

Automatically process Peter's X bookmarks daily and organize them into a searchable knowledge base that North can reference for:
- Finding saved content on demand
- Including relevant material during brainstorming sessions
- Building a personal content library

## Workflow

1. **Daily trigger** — Cron job or heartbeat task runs once per day
2. **Fetch bookmarks** — Pull all new/unprocessed X bookmarks
3. **Extract content** — Save URL + full thread content (not just the bookmarked tweet)
4. **Categorize** — Decide where to put each bookmark based on master plan (TBD)
5. **Store** — Save to searchable files in workspace

## Storage Location

`/Users/sheats/clawd/knowledge/x-bookmarks/`

Each bookmark saved as a markdown file with:
- URL
- Author
- Date bookmarked
- Full thread content
- Category/tags
- Any notes

## Master Plan (Categories)

**Source:** `/Users/sheats/clawd/MASTER_PLAN.md`

Content gets tagged to these life areas:
- 🎯 Current Season — Quarterly priorities
- 👨‍👩‍👦‍👦 Family — Parenting, marriage, family life
- ✝️ Faith — Spiritual growth, community
- 💪 Health — Physical, mental wellness
- 💼 Business — High Cotton, ReturnZap, ventures
- 🧑‍💻 Career/Brand — Professional positioning, LinkedIn ideas
- 💰 Money — Investing, crypto, financial strategy
- 🌱 Growth — Learning, skills, interests
- 🏠 Home — Prep, DIY, hobbies
- 🔥 Freedom — Vision, milestones

## Tools Needed

- `bird` CLI skill for X/Twitter access
- Cron job for daily execution
- Memory search for retrieval

## Status

- [x] Define master plan categories (mapped to MASTER_PLAN.md)
- [x] Set up bird CLI authentication (working via browser cookies)
- [x] Create storage structure (`knowledge/` by category)
- [x] Build processing script/workflow (tested 2026-01-25)
- [x] Set up daily cron job (6 AM daily, job id: x-bookmarks-daily)

## Cron Job

**Schedule:** 0 6 * * * (6 AM daily)
**Action:** Fetch bookmarks → extract threads → save to knowledge/ → unbookmark → commit

## Notes from First Run (2026-01-25)

- Processed ~50 bookmarks
- Saved 11 valuable pieces (threads with substance)
- Skipped 39 low-value items (promos, memes, single tweets)
- Todoist bookmark processing discontinued — X bookmarks only going forward
