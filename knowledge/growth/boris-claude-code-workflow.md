# Boris (Creator) Claude Code Workflow

**Source:** @bcherny via @aakashgupta on X (Jan 3, 2026)
**Link:** https://x.com/aakashgupta/status/2007347705945944153

## Setup

- Run 5 Claudes in parallel, numbered tabs 1-5
- System notifications when input needed
- Use **Opus 4.5 for everything** - slower but requires less steering, so faster overall

## Workflow

1. Start in **Plan mode** (shift+tab twice)
2. Iterate until good
3. Switch to auto-accept for 1-shot execution

## Organization

- **Slash commands** for "inner loop" workflows you repeat daily (lives in `.claude/commands/`)
- **Single CLAUDE.md per repo**, checked into git
- Team contributes - every mistake becomes a rule
- Tag @.claude on coworker PRs to add to CLAUDE.md as part of review

## Subagents

Use for common PR workflows:
- code-simplifier
- verify-app
- build-validator
- code-architect

## Hooks

- **PostToolUse hook** auto-formats code (handles last 10% before CI)

## Permissions

- `/permissions` to pre-allow safe bash commands
- Skip `--dangerously-skip-permissions`

## Tools via MCP

Claude uses all your tools: Slack, BigQuery, Sentry, etc.

## Verification (Key Insight)

> "Give Claude verification. Browser tests, bash commands, test suites. 2-3x quality improvement."

## Long Tasks

Options:
- Background agent verification
- Agent Stop hook
- ralph-wiggum plugin
