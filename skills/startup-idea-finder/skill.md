# Skill: Startup Idea Finder

## Purpose

Interactively drill from a broad niche → sub-niches → specific problems, then produce a ranked list of targeted AI startup ideas with strong actionability.

## Invocation

**Local (Claude Code terminal):**
```
/startup-idea-finder
```

**Via Telegram:**
```
find startup ideas
```

## Interactive Flow

This skill is **always interactive**. It never starts researching without first understanding the niche.

### Step 1 — Ask for the broad niche
Immediately upon invocation, ask:
> "What space do you want to explore? (e.g. healthcare, B2B SaaS tools, creator economy, legal tech, fintech, remote work, e-commerce)"

Wait for the user's answer before proceeding.

### Step 2 — Research & present sub-niches
Research the broad niche and surface 5–8 sub-niches. Present them to the user:
> "Here are the sub-niches I found within [niche]. Which one do you want to drill into? Or should I pick the highest-signal one and go deep?"

Wait for the user's answer.

### Step 3 — Drill into problems
Research the chosen sub-niche deeply. Find 15–25 specific problems people face within it.

### Step 4 — Score & output
Score each problem, rank, and generate the HTML report.

## Output Format

Always save output as an HTML file:
```
outputs/YYYY-MM-DD-[niche-slug]-[subniche-slug].html
```

Use the HTML template defined in `skills/startup-idea-finder/prompt.md`.

## Telegram Behavior

When triggered via Telegram, run the same interactive flow — ask the niche question as the first reply, wait for response, then proceed. At the end, send the top 5 ideas as a concise text reply and save the full HTML report to `outputs/`.
