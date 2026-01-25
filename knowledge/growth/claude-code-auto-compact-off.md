# Why Turn Off Claude Code Auto-Compact

**Source:** https://x.com/dani_avila7/status/2008653214472614369
**Author:** @dani_avila7 (Daniel San)
**Date:** 2026-01-06
**Category:** Growth / AI Tools

---

## The Question

Many people ask why keep Claude Code auto-compact turned off.

## The Answer

If you configure CLAUDE.md, commands, sub-agents, and hooks properly, you almost never hit auto-compact.

**The problem:** Every time auto-compact triggered, important context was lost. After looking at how compaction actually works, it was clear that key details were being dropped.

**The solution:** Disable auto-compact and focus on better context management per session instead.

## How to Inspect Compaction

To see what happens under the hood when a compact runs:

```bash
npx claude-code-templates@latest --chats
```

This gives you:
- Full breakdown of compaction
- Per-session analytics
- Data to keep improving your workflows

---

## Key Insight

The real skill is managing context well enough that you don't need auto-compact, rather than letting the system automatically lose important details.
