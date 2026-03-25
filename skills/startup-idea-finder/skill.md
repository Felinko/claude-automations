# Skill: Startup Idea Finder

## Purpose

Interactively drill from a broad niche → scored sub-niches → specific micro-niche (with viability check) → deep problem research → ranked startup ideas. Every level is user-confirmed before proceeding.

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

This skill is **always interactive**. It never skips ahead without user input.

```
1. Ask for broad direction → wait

2. Research + score 5–8 sub-niches
   Each rated on: 🔥 Market signal · 🤖 AI leverage · 🏁 Competition level
   → wait for user to pick one

2B. Micro-niche drill
   Surface 3–5 specific customer types within the chosen sub-niche
   → wait for user to pick one

2C. Niche viability check
   Run 2 searches: competition landscape + market size
   Present: Competitive summary · Market size estimate · 🟢/🟡/🔴 verdict
   → if 🟡 Yellow or 🔴 Red, offer to pivot before going deep
   → only proceed on confirmation

3. Deep problem research on confirmed micro-niche (15–25 signals)

4. Cluster into 8–12 specific startup ideas (narrow, product-named)

5. Score each idea (5 dimensions, max 25 pts)

6. Generate HTML report → save to outputs/YYYY-MM-DD-[niche]-[subniche].html

7. Reply with 2-line #1 summary + offer to drill deeper or pivot
```

## Output Format

Always save as HTML:
```
outputs/YYYY-MM-DD-[niche-slug]-[subniche-slug].html
```

Template defined in `skills/startup-idea-finder/prompt.md`. Report includes a Niche Viability section at the top showing competition, market size, and verdict.

## Telegram Behavior

Same interactive flow — reply with each question, wait for response. At the end, send the top 5 ideas as a concise text reply and note the file path of the full HTML report.
