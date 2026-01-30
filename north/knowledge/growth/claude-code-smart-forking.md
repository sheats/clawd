# Smart Forking for Claude Code

**Source:** @PerceptualPeak on X (Jan 18, 2026)
**Link:** https://x.com/PerceptualPeak/status/2012741829683224584

## Concept

Use vector embeddings to find relevant past Claude Code sessions and fork from them.

## How It Works

1. Every session transcript auto-loads into a vector database via RAG
2. Invoke `/fork-detect` tool with what you want to do
3. Prompt runs through embedding model
4. Cross-references with vectorized RAG database of all previous sessions
5. Returns top 5 relevant past sessions with relevance scores
6. Pick which session to fork from
7. Get fork command to paste into new terminal

## Why It Matters

- Don't waste context from hundreds/thousands of previous sessions
- More relevant context = more effective implementation
- Seamlessly efficient feature implementation

Author offered to share implementation plan & git repo.
