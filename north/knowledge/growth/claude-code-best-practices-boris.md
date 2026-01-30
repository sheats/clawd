# Claude Code Best Practices (from Boris Cherny, Creator)

**Source:** https://x.com/startupideaspod/status/2014752657261658353
**Author:** @startupideaspod (The Startup Ideas Podcast)
**Date:** 2026-01-23
**Category:** Growth / AI Tools

---

Struggling with Claude Code? Here's what Boris Cherny, the creator of Claude Code, recommends almost every time:

## 1. Use Opus 4.5 with Thinking

- It's smarter, uses fewer tokens
- Often ends up cheaper than smaller models
- "Opus + thinking mode is a total shift. The token efficiency is real when it gets it right the first time."

## 2. Invest in Your CLAUDE.md

- Just a text file. No special format.
- **Add every mistake Claude makes so it doesn't repeat them.**
- "Being super specific helps way more than generic rules"
- Instead of "don't break existing code," write out the exact pattern that broke last time with file paths
- Basically a **bug journal** it learns from

## 3. Give Claude a Way to Verify Its Output

- Run tests
- Start a server
- Let it see the browser

> "A painter wearing a blindfold won't paint well. Neither will an LLM that can't check its own work."

## The Key Insight

**"Once the plan is good, the code is good."**

---

## Community Tips from Thread

### Prompt Template (from @rburton)
```
Let's collaborate on a feature together. I want to build .... so that a user can ... (scrum like).

Please ask me them one by one. I may want to skip some of these ideas, so ask me about each.

For each question, follow these steps:
1. Research it thoroughly before asking.
2. Explain why you're asking this question, and keep it concise.
3. Suggest multiple options (e.g., potential answers, solutions, or variations), along with your reasoning for each.
4. Indicate which option you would select and explain why.
5. Describe how your selected option would add value to the application, enhance the UI, and/or improve the UX.
```

### Additional Tips
- Adding browser access is a game changer
- Verification loops beat prompt tweaks - let agents see and test reality
- Parallelism only works with verification: "Agents don't just execute - they review each other"
- "Tightening the loop: failing tests + concrete diff constraints + small PRs"

---

**Framing:** Claude Code is less like a chatbot and more like a junior engineer with memory.
