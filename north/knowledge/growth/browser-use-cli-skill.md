# Browser Use CLI + Skill for Claude Code

**Source:** https://x.com/gregpr07/status/2014258487828807950
**Author:** @gregpr07 (Gregor Zunic)
**Date:** 2026-01-22
**Category:** Growth / AI Tools
**GitHub:** https://github.com/browser-use/browser-use

---

## What It Does

Give your Claude Code/Codex agent a browser. Perfect for local dev.

**Example prompt:**
> "go to localhost:3000, tell me what's wrong with the UI and keep improving it until it looks pretty"

It just works.

---

## Modes

- ✅ **Headless** (fast)
- ✅ **Your real Chrome** (with logins)
- ✅ **Cloud browsers** (proxies + anti-detection)

---

## Installation

2-line skill install. 100% OSS.

**Requirements:** Python and pip3 (note: not disclosed but required for WSL/NodeJS users)

---

## Key Differentiator vs Agent-Browser

| Feature | Browser Use | Agent-Browser |
|---------|-------------|---------------|
| Connection | Pure CDP (Chrome DevTools Protocol) | Playwright-based |
| Dependencies | Minimal (pure Python) | More dependencies |
| Element Detection | Proprietary optimized extraction layer | Accessibility tree |

> "Agent-browser is literally playwright, but with much nicer dev focused interface on top. I tried to combine the DX simplicity of agent-browser, while keeping dependencies super low." - @gregpr07

---

## Why It Matters

> "Giving the coding agent a real browser is where the 'it works on my machine' loop finally closes. Once it can see the UI, you can move from code guesses to evidence. The win is fewer back-and-forth cycles, not prettier prompts." - @BrandGrowthOS

---

## CLI vs MCP

> "I prefer CLI because it doesn't pollute the context with MCP tools!" - @gregpr07

---

## Additional Notes

- Works with devcontainers in headless mode
- Remote browser requires API key (for mass scraping use cases)
- Results have been "great so far" per early users
