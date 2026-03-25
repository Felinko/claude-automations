# Claude Automations — AI Startup Idea Finder

## Project Overview

This project uses Claude to find targeted AI startup ideas by interactively drilling from a broad niche → sub-niches → specific problems, then producing a ranked, actionable report.

## Folder Structure

```
Claude_Automations/
├── CLAUDE.md                                  ← You are here
├── skills/
│   └── startup-idea-finder/
│       ├── skill.md                           ← Invocation & interactive flow
│       └── prompt.md                          ← Step-by-step research prompt + HTML template
├── reference/
│   ├── subreddits.md                          ← Curated subreddits to search
│   └── idea-evaluation-criteria.md           ← Scoring rubric (5 dimensions, max 25)
└── outputs/                                   ← Per-run HTML reports saved here
```

## How to Use

### Local (Claude Code terminal)
```
/startup-idea-finder
```
Claude will immediately ask: **"What space do you want to explore?"**
Then drill: broad niche → sub-niche selection → deep research → ranked HTML report.

### Via Telegram
Send: `find startup ideas`
Same interactive flow — Claude replies asking for the niche, waits for your answer, proceeds.

## Interactive Flow (always followed)

```
1. Ask user for broad niche  →  wait for reply
2. Research + present 5–8 sub-niches  →  wait for user to pick one
3. Deep research on chosen sub-niche  →  collect 15–25 specific problems
4. Cluster into 8–12 targeted startup ideas
5. Score each (5 dimensions, max 25)
6. Generate HTML report  →  save to outputs/
7. Reply with summary + offer to drill deeper
```

## Output Format

**HTML files only.** Saved to `outputs/` as:
```
outputs/YYYY-MM-DD-[niche-slug]-[subniche-slug].html
```

HTML is used over markdown because:
- Human-readable in any browser without plugins
- Minimal token overhead (~30% more than markdown for equivalent content)
- Allows clean visual hierarchy (score bars, cards, color coding)
- The template in `prompt.md` is compact and reused every run

## Key Constraints

- **Always interactive** — never start researching without first asking for the niche
- **Drill to specificity** — ideas should be narrow enough to build an MVP in 6 weeks
- **AI-leverage focus** — prioritize problems where AI provides a 10x improvement, not marginal help
- **Solution gap** — deprioritize if a dominant well-funded product already exists
- **Signal over noise** — problems recurring across multiple subreddits/sources score higher

## Scoring Rubric (quick reference)

Each dimension scored 1–5. Max total: **25**.

| Dimension | What it measures |
|-----------|-----------------|
| Problem Frequency | How often this appears across sources |
| AI Leverage | Does AI provide a 10x solution? |
| Market Size | How many potential customers? |
| Solution Gap | How bad are current alternatives? |
| Monetization Clarity | Is there a clear, willing buyer? |

Full rubric: `reference/idea-evaluation-criteria.md`
