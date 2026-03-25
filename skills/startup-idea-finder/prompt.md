# Research Prompt: AI Startup Idea Finder

Follow every step in order. Steps 1–2 require user input before continuing.

---

## STEP 1 — Ask for the broad niche

Say exactly this (or close to it):

> **"What space do you want to explore?**
> Examples: healthcare admin, B2B SaaS tooling, creator economy, legal tech, fintech, e-commerce ops, remote work, education, construction, real estate.
> Or just describe the type of problem you're drawn to."

**Wait for the user to reply. Do not proceed until you have their answer.**

---

## STEP 2 — Research sub-niches & ask the user to pick one

Using WebSearch, find the landscape within the broad niche. Run 3–4 searches:
- "[niche] problems Reddit 2025 2026"
- "[niche] startup opportunities underserved market"
- "[niche] pain points small business OR freelancer OR founder"

From the results, identify **5–8 distinct sub-niches** — coherent problem clusters within the broad space.

Present them clearly:

> **"Here are the sub-niches I found within [niche]:**
> 1. [Sub-niche A] — e.g. "Solo practitioner billing & admin"
> 2. [Sub-niche B]
> 3. [Sub-niche C]
> ...
>
> Which one do you want to drill into? Or say 'pick the best one' and I'll choose the highest-signal sub-niche."

**Wait for the user's choice before proceeding.**

---

## STEP 3 — Deep research on the chosen sub-niche

Run **6–8 targeted searches** on the chosen sub-niche. Vary the angle:

```
site:reddit.com [sub-niche] pain points tool missing
[sub-niche] "I wish" OR "why is there no" OR "manually" automation
[sub-niche] startup ideas 2025 2026 underserved
[sub-niche] problems no good software solution
reddit [sub-niche] "takes hours" OR "so frustrated" OR "waste time"
[sub-niche] micro SaaS opportunity niche
```

For each search result, extract:
- The specific problem described (one sentence)
- Who has the problem (role / company type)
- How often it seems to occur (rare / common / ubiquitous)
- Whether AI could meaningfully solve it

Aim to collect **15–25 distinct problems**. Duplicates across sources strengthen a signal — note them.

---

## STEP 4 — Cluster into targeted ideas

Group the raw problems into **8–12 specific startup ideas**. Each idea should be:
- Narrow enough to build an MVP in 6 weeks
- Solving one clearly-articulated problem, not a vague space
- Named like a product, not a category (e.g. "AI proposal writer for UX freelancers" not "freelancer tools")

---

## STEP 5 — Score each idea

Score 1–5 on each dimension from `reference/idea-evaluation-criteria.md`:

| Dimension | Weight |
|-----------|--------|
| Problem Frequency | ×1 |
| AI Leverage Potential | ×1 |
| Market Size Signal | ×1 |
| Solution Gap | ×1 |
| Monetization Clarity | ×1 |

Max: 25. Include a one-sentence rationale per score.

---

## STEP 6 — Generate HTML report

Save the output as:
```
outputs/YYYY-MM-DD-[niche-slug]-[subniche-slug].html
```

Use this HTML template exactly (replace all `{{placeholders}}`):

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>{{Niche}} — {{Sub-niche}} — {{Date}}</title>
  <style>
    *{box-sizing:border-box;margin:0;padding:0}
    body{font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif;background:#0f0f13;color:#e2e2e8;line-height:1.7;padding:40px 20px 80px}
    .container{max-width:900px;margin:0 auto}
    header{border-bottom:1px solid #2a2a36;padding-bottom:28px;margin-bottom:40px}
    h1{font-size:1.8rem;font-weight:700;color:#fff}
    h1 span{color:#7c6cf8}
    .meta{display:flex;gap:20px;margin-top:14px;flex-wrap:wrap}
    .chip{background:#1a1a24;border:1px solid #2a2a36;border-radius:20px;padding:4px 12px;font-size:0.75rem;color:#aaa}
    h2{font-size:1.1rem;font-weight:600;color:#fff;margin:44px 0 16px;padding-bottom:8px;border-bottom:1px solid #1e1e2a}
    table{width:100%;border-collapse:collapse;font-size:0.85rem}
    th{text-align:left;padding:10px 12px;font-size:0.68rem;text-transform:uppercase;letter-spacing:1px;color:#555;background:#1a1a24}
    td{padding:12px;border-bottom:1px solid #1a1a24;vertical-align:top}
    tr:hover td{background:#13131c}
    .rank{color:#555;font-weight:700;text-align:center;width:36px}
    .idea-name{font-weight:600;color:#c4b5fd}
    .problem{color:#aaa}
    .ai{color:#86efac}
    .score{font-weight:700;text-align:center;white-space:nowrap}
    .hi{color:#a78bfa}.mid{color:#7dd3fc}.lo{color:#6b7280}
    .bar{display:inline-block;width:40px;height:3px;background:#1e1e2a;border-radius:2px;margin-left:6px;vertical-align:middle}
    .bar-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,#7c6cf8,#a78bfa)}
    .card{background:#13131c;border:1px solid #1e1e2a;border-radius:10px;padding:24px 28px;margin-bottom:20px}
    .card-header{display:flex;align-items:center;gap:12px;margin-bottom:20px}
    .badge{width:32px;height:32px;border-radius:50%;background:linear-gradient(135deg,#7c6cf8,#a78bfa);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:0.85rem;color:#fff;flex-shrink:0}
    .card-title{font-size:1rem;font-weight:700;color:#fff}
    .card-score{margin-left:auto;font-weight:700;color:#a78bfa}
    .section-label{font-size:0.68rem;text-transform:uppercase;letter-spacing:1px;color:#7c6cf8;margin-bottom:4px;margin-top:14px}
    .card p{color:#bbb;font-size:0.875rem}
    .sources a{color:#7c6cf8;text-decoration:none;font-size:0.85rem;display:block;margin-top:8px}
    .sources a:hover{text-decoration:underline}
  </style>
</head>
<body>
<div class="container">
  <header>
    <h1>{{Niche}} — <span>{{Sub-niche}}</span></h1>
    <div class="meta">
      <span class="chip">{{Date}}</span>
      <span class="chip">{{N}} ideas ranked</span>
      <span class="chip">{{signal_count}} signals collected</span>
    </div>
  </header>

  <h2>Ranked Ideas</h2>
  <table>
    <thead>
      <tr><th>#</th><th>Idea</th><th>Core Problem</th><th>AI Angle</th><th>Score</th></tr>
    </thead>
    <tbody>
      <!-- For each idea: -->
      <tr>
        <td class="rank">{{rank}}</td>
        <td><span class="idea-name">{{idea_name}}</span></td>
        <td class="problem">{{core_problem}}</td>
        <td class="ai">{{ai_angle}}</td>
        <td class="score {{hi|mid|lo}}">{{score}}/25<span class="bar"><span class="bar-fill" style="width:{{pct}}%"></span></span></td>
      </tr>
    </tbody>
  </table>

  <h2>Top 3 Deep Dives</h2>

  <!-- Repeat for top 3: -->
  <div class="card">
    <div class="card-header">
      <div class="badge">{{rank}}</div>
      <div class="card-title">{{idea_name}}</div>
      <div class="card-score">{{score}}/25</div>
    </div>
    <div class="section-label">Why the problem is real</div>
    <p>{{why_real}}</p>
    <div class="section-label">Who the customer is</div>
    <p>{{customer}}</p>
    <div class="section-label">How AI makes it 10x better</div>
    <p>{{ai_leverage}}</p>
    <div class="section-label">What a v1 looks like</div>
    <p>{{v1}}</p>
    <div class="section-label">Scoring breakdown</div>
    <p>Frequency {{f}}/5 · AI leverage {{a}}/5 · Market {{m}}/5 · Solution gap {{g}}/5 · Monetization {{mo}}/5</p>
  </div>

  <h2>Sources</h2>
  <div class="sources">
    <!-- list source links -->
  </div>
</div>
</body>
</html>
```

---

## STEP 7 — Final reply

After saving the file, tell the user:
- The file path where the report was saved
- A 3-line summary of the #1 idea
- Offer to drill deeper into any single idea or pivot to a different sub-niche
