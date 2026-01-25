# Smart Forking for Claude Code Sessions

**Source:** https://x.com/PerceptualPeak/status/2013844213549732057
**Author:** @PerceptualPeak (Zac)
**Date:** 2026-01-21
**Category:** Growth / AI Tools

---

## The Problem

> "Re-explaining context is where most AI productivity gains die."

Starting with a fresh context window means:
- No context = bad code
- More iteration to fix errors
- Lost knowledge from previous sessions

Too much context = drunk model, bad code, more iteration.

---

## The Solution: Smart Forking

Uses Claude's `--fork` flag to create identical duplicates of chat sessions, then intelligently matches the right session to your current task.

**Result:** One-shot 3 different minor additions to 3 different projects that would have required multiple iteration cycles with fresh context.

> "The win isn't speed, it's avoiding re-loading the whole mental model 3x."

---

## How It Works

### 1. Auto-Chunking & Embedding
- All chat history is automatically chunked & embedded
- Happens via pre-compact hook
- Lazy detection snags sessions that haven't been compacted yet

### 2. Smart Session Matching
When you run `/fork-detect`:
1. Checks session registry for non-compacted sessions
2. Chunks & embeds them if needed
3. Identifies best match using relevancy scoring

### 3. Auto-Spawning
Uses VS Code file watcher extension to:
- Auto-spawn new terminal
- Pipe in fork command with prompt string
- Session spawns, reads instructions, completes task

### Scoring Formula (Recency-Weighted)
Includes aggressive recency weighting to ensure it serves up the most recent relevant session.

---

## The Sweet Spot

> "No context = bad code. Too much context = drunk model, bad code. It's all about finding the sweet spot."

Most forked sessions are already compacted, so new sessions start at **25-35% context window**.

### Gap Detection
If session IS compacted:
1. Intelligently determines this upon spawning
2. Examines its own compacted summary
3. Identifies gaps in knowledge for the desired task
4. Dispatches two sub-agents to scour pre-compacted chat
5. Extracts missing details back to context window

---

## Advanced Use Case

> "Had similar frustrations with long running general LLM chat sessions. No way to have side-bars or challenge ideas without muddying the main topic thread. Built a chat app with branching. After exploring a side topic, inject a clean summary back into a thread, prune or reference." - @twotacos_

---

## Related Research

The concept is formalized in the RLM paper:
> "You give the LLM full context C for a query Q. LLM takes C and extracts only what's relevant to work on Q."

---

## Status

Repo coming soon (as of Jan 2026). Open source planned.

---

## Skeptical View

> "Last thing I want is to go _deeper_ into context windows. That just accelerates the point where the model becomes dumb (which is pre compaction). You want shorter conversations not longer." - @fatboygrimdark
