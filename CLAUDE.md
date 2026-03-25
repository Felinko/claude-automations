# Claude Automations — AI Startup Idea Finder

## Project Overview

This project uses Claude to find AI startup ideas by scanning the internet (Reddit and beyond) for signals — pain points, unsolved problems, and underserved niches — then producing a ranked, actionable list of opportunities with strong AI-leverage potential.

## Folder Structure

```
Claude_Automations/
├── CLAUDE.md                          ← You are here
├── skills/
│   └── startup-idea-finder/
│       ├── skill.md                   ← How to invoke the skill
│       └── prompt.md                  ← The research & analysis prompt
├── reference/
│   ├── subreddits.md                  ← Curated subreddits to search
│   └── idea-evaluation-criteria.md   ← Scoring rubric
└── outputs/                           ← Per-run results saved here
```

## How to Use

### Local (Claude Code terminal)
Run the skill directly:
```
/startup-idea-finder
/startup-idea-finder [optional: topic focus, e.g. "healthcare AI"]
```

### Via Telegram
Send a message to the bot:
```
find startup ideas
find startup ideas about [topic]
```
Claude will reply with the top 10 ideas inline and save the full report to `outputs/`.

## Output Convention

Every run saves a file to `outputs/` named:
```
outputs/YYYY-MM-DD-[topic-slug].md
```

The output contains a ranked markdown table:

| Rank | Niche | Core Problem | AI Leverage | Score |
|------|-------|-------------|-------------|-------|
| 1    | ...   | ...         | ...         | 23/25 |

## Key Constraints

- **Focus on AI-leverageable problems** — prioritize problems where AI provides a 10x better solution, not just a marginal improvement.
- **Prefer underserved niches** — if there's already a dominant, well-funded product solving the problem, deprioritize it.
- **Signal over noise** — a problem mentioned repeatedly across multiple subreddits and time periods is stronger than a single viral post.
- **Monetization clarity** — flag ideas with clear B2B or subscription revenue potential higher.

## Workflow Summary

```
Search Reddit → Extract pain signals → Cluster into niches → Score → Rank → Output
```

See `skills/startup-idea-finder/prompt.md` for the full step-by-step research prompt.
