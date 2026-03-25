# Research Prompt: AI Startup Idea Finder

Follow these steps in order. Do not skip steps.

---

## Step 1: Load Context

- Read `reference/subreddits.md` for the target subreddit list.
- Read `reference/idea-evaluation-criteria.md` for the scoring rubric.
- Note any topic focus provided by the user (default: broad search).

---

## Step 2: Search for Pain-Point Signals

Use WebSearch to find Reddit posts expressing frustration, unmet needs, or missing tools. Run **at least 8 searches** using the patterns below. Vary the subreddits and topics.

**Search query templates (use site:reddit.com):**

```
site:reddit.com/r/[subreddit] "I wish there was" AI tool
site:reddit.com/r/[subreddit] "why is there no" software
site:reddit.com/r/[subreddit] "I can't find anything that" automates
site:reddit.com/r/[subreddit] "so frustrated" tool doesn't exist
site:reddit.com/r/[subreddit] "does anyone know a tool" that can
site:reddit.com/r/[subreddit] "I would pay for" app
site:reddit.com/r/[subreddit] "manually doing" takes hours
site:reddit.com/r/[subreddit] "there has to be a better way"
```

If a topic focus was given, incorporate it into the search queries.

For each search, extract:
- The core problem described
- The subreddit it came from
- Approximate recency (recent posts score higher)
- Any upvote/engagement signal mentioned

---

## Step 3: Extract & Log Raw Signals

Create a raw list of 20–40 distinct problems found. For each:
- One-sentence problem description
- Source subreddit(s)
- Whether AI could meaningfully solve it (yes/no/partial)

---

## Step 4: Cluster into Niches

Group the raw signals into 10–15 thematic niches. A niche is a coherent problem space, not just a single complaint. Examples:
- "Freelancer contract management"
- "AI-assisted content repurposing for solo creators"
- "Automated bookkeeping for non-accountants"

---

## Step 5: Score Each Niche

Score each niche using `reference/idea-evaluation-criteria.md`. Each criterion is 1–5. Max score: 25.

Calculate a total score and brief rationale for each.

---

## Step 6: Rank & Output

Produce the final ranked table. Include the top 15 niches.

```markdown
## AI Startup Ideas — [YYYY-MM-DD] — [Topic or "General"]

| Rank | Niche | Core Problem | AI Leverage | Score |
|------|-------|-------------|-------------|-------|
| 1    | ...   | ...         | ...         | X/25  |
```

After the table, include a **Top 3 Deep Dives** section with 2–3 paragraphs each on the highest-scoring ideas: why the problem is real, who the customer is, how AI makes it 10x better, and what a v1 product might look like.

---

## Step 7: Save Output

Save the full report to:
```
outputs/YYYY-MM-DD-[topic-slug].md
```

If triggered via Telegram, also reply to the chat with the top 10 rows of the table plus a one-line summary of the #1 idea.
