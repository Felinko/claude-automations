# Skill: Startup Idea Finder

## Purpose

Research the internet for signals of unmet needs and pain points, then surface a ranked list of startup ideas with strong AI-leverage potential.

## Invocation

**Local (Claude Code terminal):**
```
/startup-idea-finder
/startup-idea-finder healthcare AI
/startup-idea-finder B2B SaaS tools
```

**Via Telegram:**
```
find startup ideas
find startup ideas about [topic]
```

## Inputs

| Input | Required | Description |
|-------|----------|-------------|
| `topic` | Optional | Narrow the search to a specific domain (e.g., "legal tech", "remote work tools") |
| `subreddits` | Optional | Override the default subreddit list from `reference/subreddits.md` |

If no topic is provided, run a broad search across all subreddits in `reference/subreddits.md`.

## Outputs

1. **Ranked markdown table** — saved to `outputs/YYYY-MM-DD-[topic-slug].md`
2. **Telegram reply** — top 10 ideas sent inline if triggered via Telegram

## Behavior

When this skill is invoked, execute the full prompt in `skills/startup-idea-finder/prompt.md`.

When triggered via **Telegram**:
- Run the full research workflow
- Reply to the Telegram chat with a concise top-10 list (use the `reply` MCP tool)
- Save the full report to `outputs/`

## Example Output Format

```markdown
## Startup Ideas — [Date] — [Topic]

| Rank | Niche | Core Problem | AI Leverage | Score |
|------|-------|-------------|-------------|-------|
| 1 | Legal contract review for freelancers | No affordable tool for non-lawyers to review contracts | AI can flag risky clauses instantly | 23/25 |
| 2 | ... | ... | ... | ... |
```
